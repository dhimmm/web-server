# Use the official OpenResty image as the base
FROM openresty/openresty:latest

# Create cache directory
RUN mkdir -p /var/cache/nginx

# Set permissions for the cache directory
RUN chown -R www-data:www-data /var/cache/nginx \
    && chmod -R 755 /var/cache/nginx

# Copy the Nginx configuration file
COPY nginx.conf /etc/nginx/nginx.conf

# Start OpenResty (Nginx)
CMD ["openresty", "-g", "daemon off;"]
