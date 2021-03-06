# Authy
[![Build status](https://badge.buildkite.com/a4d73c8458b58f04fdb5af7e7179d242b872aef8f61577415f.svg)](https://buildkite.com/365-assistance-pty-ltd/authy)

Elixir library access to the Authy API, based loosely on the [ruby gem](https://github.com/authy/authy-ruby).

## Features

- [x] Phone Verification

## Installation

1. Add authy to your list of dependencies in `mix.exs`:

  ```
  def deps do
    [{:authy, github: "365assistance/authy"}]
  end
  ```

2. Ensure authy is started before your application:

  ```
  def application do
    [applications: [:authy]]
  end
  ```

3. Configure your api key and defaults for the various APIs

  ```
  config :authy,
    api_key: System.get_env("AUTHY_API_KEY")
    phone_verification: [
      via: "sms",
      country_code: "61",
      locale: "en-AU",
      custom_message: "Verification code, yo!"]
  ```
