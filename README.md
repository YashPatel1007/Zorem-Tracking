# Integration Guide

## Step 1: Download and Set Up the SDK
1. Download the SDK Zip File from our [official website](link_to_sdk).
2. Unzip the downloaded file and copy the contents into your plugin's main folder.
3. Rename the copied folder to "zorem-tracking".
4. This SDK will provide the necessary functionality for integrating with our services.

## Step 2: Initialize Plugin Instance
Within your plugin's codebase, choose a unique function name that will allow easy access to your plugin's instance.

## Step 3: Configure Admin Menu
Choose how your plugin's main settings page should be accessible:
- **Top-Level Menu:**
  - Select "A custom top-level admin menu."
  - Specify a unique menu slug (e.g., "my-plugin-settings").
- **Sub Menu:**
  - Choose a suitable parent menu (settings, tools, users, plugins, appearance, media, posts, comments, or dashboard).
  - Define a submenu slug (e.g., "my-plugin-settings").
- **No Settings Page:**
  - Choose this option if your plugin doesn't require a settings page.

## Step 4: Configure Admin Menu
Copy the provided code and paste it at the top of your main plugin's PHP file, right after the plugin's header comment.

## Step 5: Add the Snippet Code
Copy the provided code and paste it right after the plugin's header comment in your main plugin's PHP file.

```php
require_once $this->get_plugin_path() . '/zorem-tracking/zorem-tracking.php';
$this->tracker = WC_Trackers::get_instance();
$this->tracker->set_tracker_data( array(
    'custom_key' => '544641515656',
    'user_id' => '10',
    'slug' => 'woocommerce-advanced-shipment-tracking'
) );
