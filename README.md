# Confirmation Link

CSS-only mechanism to require a confirmation before allowing an action.

**N.B. :** current template is a `Django` template.
# Preview

![default](confirm-link-01-default.png "Default") ← default
![clicked](confirm-link-02-clicked.png "Clicked") ← clicked
![require-corfirmation](confirm-link-03-require-corfirmation.png "Require-corfirmation") ← require corfirmation

# Usage

## Django
```python
{% url 'core:remove_measure' measure.id as action_url %}
{% trans 'supprimer' as delete %}
{% include 'components/widgets/_confirm-link.html' with item=measure url=action_url action=delete %}
```