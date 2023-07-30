# caching-nginx
# Nginx Cache Server Repository

Welcome to the Nginx Cache Server Repository! This repository serves as a default Nginx server and cache server. It enables caching of responses to improve performance and reduce server load. 

## Cache Purge

To clear the cache for a specific image, you can make a "purge" request. By sending a "purge" request for a particular image, the cache server will remove the cached copy of that image, allowing the server to fetch a fresh copy from the backend.

Please note that purging the cache is an important operation and should be done with caution. Make sure to specify the correct image URL in your "purge" request to avoid unintended cache clearances.

## Usage

1. Clone this repository to your local environment:

   ```
   git clone https://github.com/your-username/nginx-cache-server.git
   cd nginx-cache-server
   ```

2. Install and configure Nginx on your system if not already done.

3. Start the Nginx server with cache enabled:

   ```
   nginx -p . -c nginx.conf
   ```

4. Access your Nginx server using the appropriate URL and port number.

## Purging the Cache

To purge the cache for a specific image, you can send an HTTP "PURGE" request to the Nginx cache server with the URL of the image you want to clear from the cache.

Example "purge" request using `curl`:

```
curl -X PURGE http://your-server-url.com/path/to/image.jpg
```

Make sure to replace `http://your-server-url.com/path/to/image.jpg` with the actual URL of the image you want to purge from the cache.

## Contributing

If you encounter any issues or would like to contribute to this project, feel free to create a pull request or open an issue in this repository.

Thank you for using the Nginx Cache Server! Happy caching!
