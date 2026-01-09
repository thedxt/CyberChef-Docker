![CyberChef](https://github.com/user-attachments/assets/1c6b870c-53f4-453a-9c51-d65664d81d0e)

# CyberChef Docker
This is a Docker compose setup for CyberChef with the option to use a Cloudflare tunnel.
The Docker compose files use the official [CyberChef image](https://github.com/gchq/CyberChef) and the official [Cloudflare tunnel image](https://github.com/cloudflare/cloudflared) (if you use the Cloudflare tunnel version).

There are two Docker compose files.
- `docker-compose-cf.yml` is CyberChef using a Cloudflare tunnel to enable external access.
- `docker-compose-no-cf.yml` is CyberChef locally with no Cloudflare tunnel.

Use a `.env` file to define your variables.

### .env Variables
 - `CONTAINER_NAME` the name of your CyberChef stack.
   - The one with `_app` appended to it is the CyberChef application image.
   - The one with `_cf` appended to it is the Cloudflare tunnel image (if you choose to use one) for the CyberChef application.
 - `APP_PORT` is the port that the CyberChef application will run on locally. This will also be the port you need to use in your Cloudflare tunnel, if you choose to use one.
 - `CF_TUNNEL` the Base64 of the Cloudflare tunnel for CyberChef.

More detailed documentation.
