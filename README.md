# Confirmation Link

CSS-only mechanism to require a confirmation before allowing an action.

Currently only available as a `Django` template.

## Requirements

* (optional) [Bootstrap](http://getbootstrap.com/) `≥3` ;

## Preview

![default](preview/confirm-link-01-default.png "Default") ← default
![clicked](preview/confirm-link-02-clicked.png "Clicked") ← clicked
![require-corfirmation](preview/confirm-link-03-require-corfirmation.png "Require-corfirmation") ← require corfirmation

## Usage

1. Import the `SCSS` in your main stylesheet: 

        @import "confirm-link";

2. add the `HTML` code from [./_confirm-link.html](./_confirm-link.html) to your form ;

    ```python
    {% url 'core:remove_measure' measure.id as action_url %}
    {% trans 'supprimer' as delete %}
    {% include 'components/widgets/_confirm-link.html' with item=measure url=action_url action=delete %}
    ```