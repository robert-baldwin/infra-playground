FROM ruby:3

WORKDIR /app

ADD Gemfile* /app/

ENV BUNDLE_GEMFILE=/app/Gemfile
ENV BUNDLE_JOBS=2
ENV BUNDLE_PATH=/app/bundle

RUN bundle install

ADD . /app
