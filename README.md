# [`sensirion` module](https://github.com/viam-modules/sensirion)

This [sensirion module](https://app.viam.com/module/viam/sensirion) implements a sensirion [sht3xd](https://cdn-shop.adafruit.com/product-files/2857/Sensirion_Humidity_SHT3x_Datasheet_digital-767294.pdf) sensor for temperature and humidity using the [`rdk:component:sensor` API](https://docs.viam.com/appendix/apis/components/sensor/).

> [!NOTE]
> Before configuring your sensor, you must [create a machine](https://docs.viam.com/cloud/machines/#add-a-new-machine).

Navigate to the [**CONFIGURE** tab](https://docs.viam.com/configure/) of your [machine](https://docs.viam.com/fleet/machines/) in the [Viam app](https://app.viam.com/).
[Add sensor / viam:sensirion:sht3xd to your machine](https://docs.viam.com/configure/#components).

## Configure your sht3xd sensor

Copy and paste the following attributes into your JSON configuration:

```json
{
  "i2c_bus": "0",
}
```

### Attributes

The following attributes are available for `viam:sensirion:sht3xd` sensors:

| Attribute | Type | Required? | Description |
| --------- | ---- | --------- | ----------- |
| `i2c_bus` | string | **Required** | The index of the I2C bus on the board that the sensor is wired to. |
| `i2c_address` | string | Optional | The [I2C device address](https://learn.adafruit.com/i2c-addresses/overview) of the sensor. <br> Default: `0x44` |

### Example configuration
```json
  {
    "i2c_bus": "<your-i2c-bus-index-on-board>",
    "i2c_address": "<your-i2c-address>"    
  }
```

### Next Steps
- To test your sensor, expand the **TEST** section of its configuration pane or go to the [**CONTROL** tab](https://docs.viam.com/fleet/control/).
- To write code against your sensor, use one of the [available SDKs](https://docs.viam.com/sdks/).
- To view examples using a sensor component, explore [these tutorials](https://docs.viam.com/tutorials/).
