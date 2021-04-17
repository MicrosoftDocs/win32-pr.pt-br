---
description: Para enumerar os dispositivos de bateria em um computador local, use a função SetupDiGetClassDevs.
ms.assetid: 17e3c779-91ba-4901-9435-b73dedbf0b89
title: Enumerando dispositivos de bateria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d610feda8fd312bbefe2742da50d82a664a8ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769296"
---
# <a name="enumerating-battery-devices"></a>Enumerando dispositivos de bateria

Para enumerar os dispositivos de bateria em um computador local, use a função [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) . O parâmetro *ClassGuid* é um ponteiro para **a \_ \_ bateria GUID DEVCLASS** (definida em BatClass. h). Para enumerar todas as baterias, defina o parâmetro *Enumerator* como **nulo** e defina o parâmetro *flags* como **DIGCF \_ presente** \| **DIGCF \_ INTERFACEDEVICE**. Para obter os nomes dos dispositivos de bateria, use as funções [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces) e [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx) nos dados retornados. Para abrir um identificador de arquivo para cada um dos dispositivos de bateria, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) com esses nomes.

O exemplo de C++ a seguir mostra como enumerar dispositivos de bateria em um computador local.


```C++
DWORD GetBatteryState()
 {
#define GBS_HASBATTERY 0x1
#define GBS_ONBATTERY  0x2
  // Returned value includes GBS_HASBATTERY if the system has a 
  // non-UPS battery, and GBS_ONBATTERY if the system is running on 
  // a battery.
  //
  // dwResult & GBS_ONBATTERY means we have not yet found AC power.
  // dwResult & GBS_HASBATTERY means we have found a non-UPS battery.

  DWORD dwResult = GBS_ONBATTERY;

  // IOCTL_BATTERY_QUERY_INFORMATION,
  // enumerate the batteries and ask each one for information.

  HDEVINFO hdev =
            SetupDiGetClassDevs(&GUID_DEVCLASS_BATTERY, 
                                0, 
                                0, 
                                DIGCF_PRESENT | DIGCF_DEVICEINTERFACE);
  if (INVALID_HANDLE_VALUE != hdev)
   {
    // Limit search to 100 batteries max
    for (int idev = 0; idev < 100; idev++)
     {
      SP_DEVICE_INTERFACE_DATA did = {0};
      did.cbSize = sizeof(did);

      if (SetupDiEnumDeviceInterfaces(hdev,
                                      0,
                                      &GUID_DEVCLASS_BATTERY,
                                      idev,
                                      &did))
       {
        DWORD cbRequired = 0;

        SetupDiGetDeviceInterfaceDetail(hdev,
                                        &did,
                                        0,
                                        0,
                                        &cbRequired,
                                        0);
        if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
         {
          PSP_DEVICE_INTERFACE_DETAIL_DATA pdidd =
            (PSP_DEVICE_INTERFACE_DETAIL_DATA)LocalAlloc(LPTR,
                                                         cbRequired);
          if (pdidd)
           {
            pdidd->cbSize = sizeof(*pdidd);
            if (SetupDiGetDeviceInterfaceDetail(hdev,
                                                &did,
                                                pdidd,
                                                cbRequired,
                                                &cbRequired,
                                                0))
             {
              // Enumerated a battery.  Ask it for information.
              HANDLE hBattery = 
                      CreateFile(pdidd->DevicePath,
                                 GENERIC_READ | GENERIC_WRITE,
                                 FILE_SHARE_READ | FILE_SHARE_WRITE,
                                 NULL,
                                 OPEN_EXISTING,
                                 FILE_ATTRIBUTE_NORMAL,
                                 NULL);
              if (INVALID_HANDLE_VALUE != hBattery)
               {
                // Ask the battery for its tag.
                BATTERY_QUERY_INFORMATION bqi = {0};

                DWORD dwWait = 0;
                DWORD dwOut;

                if (DeviceIoControl(hBattery,
                                    IOCTL_BATTERY_QUERY_TAG,
                                    &dwWait,
                                    sizeof(dwWait),
                                    &bqi.BatteryTag,
                                    sizeof(bqi.BatteryTag),
                                    &dwOut,
                                    NULL)
                    && bqi.BatteryTag)
                 {
                  // With the tag, you can query the battery info.
                  BATTERY_INFORMATION bi = {0};
                  bqi.InformationLevel = BatteryInformation;

                  if (DeviceIoControl(hBattery,
                                      IOCTL_BATTERY_QUERY_INFORMATION,
                                      &bqi,
                                      sizeof(bqi),
                                      &bi,
                                      sizeof(bi),
                                      &dwOut,
                                      NULL))
                   {
                    // Only non-UPS system batteries count
                    if (bi.Capabilities & BATTERY_SYSTEM_BATTERY)
                     {
                      if (!(bi.Capabilities & BATTERY_IS_SHORT_TERM))
                       {
                        dwResult |= GBS_HASBATTERY;
                       }

                      // Query the battery status.
                      BATTERY_WAIT_STATUS bws = {0};
                      bws.BatteryTag = bqi.BatteryTag;

                      BATTERY_STATUS bs;
                      if (DeviceIoControl(hBattery,
                                          IOCTL_BATTERY_QUERY_STATUS,
                                          &bws,
                                          sizeof(bws),
                                          &bs,
                                          sizeof(bs),
                                          &dwOut,
                                          NULL))
                       {
                        if (bs.PowerState & BATTERY_POWER_ON_LINE)
                         {
                          dwResult &= ~GBS_ONBATTERY;
                         }
                       }
                     }
                   }
                 }
                CloseHandle(hBattery);
               }
             }
            LocalFree(pdidd);
           }
         }
       }
        else  if (ERROR_NO_MORE_ITEMS == GetLastError())
         {
          break;  // Enumeration failed - perhaps we're out of items
         }
     }
    SetupDiDestroyDeviceInfoList(hdev);
   }

  //  Final cleanup:  If we didn't find a battery, then presume that we
  //  are on AC power.

  if (!(dwResult & GBS_HASBATTERY))
    dwResult &= ~GBS_ONBATTERY;

  return dwResult;
 }
```



Para enumerar os dispositivos de bateria conectados a um computador remoto, use a classe WMI de [**\_ bateria do Win32**](/windows/desktop/CIMWin32Prov/win32-battery) em um script ou aplicativo de cliente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx)
</dt> <dt>

[**\_marca de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**\_informações de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_status de \_ consulta da bateria do IOCTL \_**](ioctl-battery-query-status.md)
</dt> </dl>

 

 
