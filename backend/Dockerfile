FROM ruby:3.2

ARG RUBYGEMS_VERSION=3.4.6
ARG RUBY_VERSION=ruby:3.2

RUN mkdir /api

WORKDIR /api

COPY Gemfile /api/Gemfile

COPY Gemfile.lock /api/Gemfile.lock

RUN gem update --system ${RUBYGEMS_VERSION} && \
    bundle install

COPY . /api

COPY entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]

CMD ["rails", "server", "-b", "0.0.0.0"]