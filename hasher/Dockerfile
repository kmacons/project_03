FROM ruby:alpine
RUN apk add --update build-base curl
RUN gem install sinatra
RUN gem install thin
ADD hasher.rb /
ADD entry-point.sh /bin/
ENTRYPOINT ["entry-point.sh"]
CMD ["ruby", "hasher.rb"]
EXPOSE 80
