# TrackTrendy Analytics

TrackTrendy Analytics is a lightweight, privacy-friendly alternative to Google Analytics. This is a white-labeled version of [Plausible Analytics](https://github.com/plausible/analytics).

## Attribution

This software is based on Plausible Analytics, which is licensed under AGPL-3.0. All modifications for TrackTrendy branding maintain this license.

## Deployment

TrackTrendy Analytics can be deployed using Docker:

```bash
# Clone the repository
git clone https://github.com/yourusername/tracktrendy-analytics.git
cd tracktrendy-analytics

# Generate a secret key
openssl rand -base64 64 | tr -d '\n' > .env
echo "SECRET_KEY_BASE=$(cat .env)" > .env

# Start the services
docker-compose up -d
