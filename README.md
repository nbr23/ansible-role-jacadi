# ansible-role-jacadi

ansible role for [jacadi](https://github.com/nbr23/jacadi)

Usage:

```yaml
- hosts: raspberrypi
  roles:
    - role: ansible-role-jacadi
      jacadi_audiodev: "plughw:1,0"
      jacadi_extra_routes_path: /opt/jacadi/extra_routes.json
      jacadi_extra_audio_path: /opt/jacadi/extra_audio
```

Variables:

| Variable | Default | Description |
|----------|---------|-------------|
| `jacadi_image` | `nbr23/jacadi:full` | Container image |
| `jacadi_port` | `8080` | Host port |
| `jacadi_user` | `1000` | Container user ID |
| `jacadi_audio_group` | `29` | Audio group ID |
| `jacadi_audiodev` | `plughw:1,0` | ALSA device |
| `jacadi_extra_routes_path` | | Path to extra_routes.json on host |
| `jacadi_extra_audio_path` | | Path to extra audio directory on host |
| `jacadi_restart_policy` | `unless-stopped` | Container restart policy |
| `jacadi_env` | `{}` | Extra container environment variables, e.g. `TTS_PROVIDER`, `TTS_API_KEY` |

Requires the `community.docker` collection.
