FROM ruby:alpine

# The following is typically supplied by the DEV Team
# Install curl for testing purposes (NOT in production)
RUN apk add build-base && gem install sinatra && gem install thin && apk add curl

# Copy the source frin the git repo into the image
COPY . .

# Meta Data for the container
ENTRYPOINT ["ruby"]
CMD ["hasher.rb"]
EXPOSE 8080
