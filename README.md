# IoT-substation-monitoring
# IoT Substation Monitoring System

MAX_VOLTAGE = 250
MAX_CURRENT = 100
MAX_TEMPERATURE = 80

print("==============================")
print("   IoT SUBSTATION MONITORING")
print("==============================")

voltage = float(input("Enter transformer voltage (V): "))
current = float(input("Enter transformer current (A): "))
temperature = float(input("Enter transformer temperature (°C): "))

fault = False

print("\n--- Monitoring Data ---")
print("Voltage    :", voltage, "V")
print("Current    :", current, "A")
print("Temperature:", temperature, "°C")

# Voltage monitoring
if voltage > MAX_VOLTAGE:
    print("⚠️ Over-voltage detected!")
    fault = True

# Current monitoring
if current > MAX_CURRENT:
    print("⚠️ Overcurrent detected!")
    fault = True

# Temperature monitoring
if temperature > MAX_TEMPERATURE:
    print("⚠️ High temperature detected!")
    fault = True

# Final status
if fault:
    print("\n🔴 SUBSTATION ALERT")
    print("⚠️ Fault condition detected")
    print("📡 IoT Alert Sent")
else:
    print("\n🟢 SUBSTATION STATUS: NORMAL")
    print("✅ All parameters are within limits")
    print("📡 Data sent to monitoring system")
