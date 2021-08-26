---
description: Use os elementos de programação de Energia do Dispositivo para gerenciar o desempenho dos dispositivos enquanto o sistema está em um estado de sleep.
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: Usando a API de Energia do Dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aff8239c1cd0ffc8d5e8abaf0133a9ca42bb3a01a5b6fc2acef7850929a8484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032766"
---
# <a name="using-the-device-power-api"></a>Usando a API de Energia do Dispositivo

Use os elementos de programação de Energia do Dispositivo para gerenciar o desempenho dos dispositivos enquanto o sistema está em um estado de sleep.

## <a name="opening-and-closing-the-device-list"></a>Abrindo e fechando a lista de dispositivos

Abrir e fechar a lista de dispositivos é um processo caro em termos de tempo de CPU. As [**funções DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) e [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) que fazem isso só serão necessárias se o aplicativo precisar consultar a lista de dispositivos várias vezes.

Se [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) for chamado, [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) deverá ser chamado quando as consultas da lista de dispositivos são concluídas. [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) e [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) não fecharão a lista de dispositivos se ela tiver sido aberta explicitamente por **DevicePowerOpen**.

## <a name="enumerating-devices"></a>Enumerando dispositivos

A [**função DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) detecta se a lista de dispositivos está aberta e, caso não seja, a abre. **DevicePowerEnumDevices** enumera os dispositivos com base nos critérios de pesquisa especificados. Se a lista de dispositivos tiver sido aberta pela função, ela será fechada antes que a função retorne.

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a>Habilitando e desabilitando um dispositivo de ativar o sistema

A [**função DevicePowerSetDeviceState,**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) semelhante a [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), detecta se a lista de dispositivos está aberta e, caso não seja, a abre. **DevicePowerSetDeviceState** define os critérios especificados para o dispositivo especificado. Se a lista de dispositivos tiver sido aberta pela função, ela será fechada antes que a função retorne.

## <a name="example-code"></a>Código de exemplo

O exemplo a seguir demonstra o uso da API de Energia do Dispositivo.


```C++
#define _WIN32_WINNT 0x0600
#include <Windows.h>
#include <PowrProf.h>
#include <stdio.h>
#include <tchar.h>

#pragma comment(lib, "PowrProf.lib")

int __cdecl main()
{
 // Define and initialize our return variables.
 LPWSTR  pRetBuf = NULL;
 ULONG bufSize = MAX_PATH * sizeof(WCHAR);
 ULONG uIndex = 0;
 BOOLEAN bRet = FALSE;

 // Open the device list, querying all devices
 if (!DevicePowerOpen(0)) 
  {
   printf("ERROR: The device database failed to initialize.\n");
   return FALSE;
  }

 // Enumerate the device list, searching for devices that support 
 // waking from either the S1 or S2 sleep state and are currently 
 // present in the system, and not devices that have drivers 
 // installed but are not currently attached to the system, such as 
 // in a laptop docking station.

 pRetBuf = (LPWSTR)LocalAlloc(LPTR, bufSize);

 while (NULL != pRetBuf && 
        0 != (bRet = DevicePowerEnumDevices(uIndex,
           DEVICEPOWER_FILTER_DEVICES_PRESENT,
           PDCAP_WAKE_FROM_S1_SUPPORTED|PDCAP_WAKE_FROM_S2_SUPPORTED,
           (PBYTE)pRetBuf,
           &bufSize)))
  {
   printf("Device name: %S\n", pRetBuf);

   // For the devices we found that have support for waking from 
   // S1 and S2 sleep states, disable them from waking the system.
   bRet = (0 != DevicePowerSetDeviceState((LPCWSTR)pRetBuf, 
                                  DEVICEPOWER_CLEAR_WAKEENABLED, 
                                  NULL));

   if (0 != bRet) 
    {
     printf("Warning: Failed to set device state.\n");
    }
   uIndex++;
  }

 // Close the device list.
 DevicePowerClose();
 if (pRetBuf!= NULL) LocalFree(pRetBuf);
 pRetBuf = NULL;

 return TRUE;
}
```



Neste exemplo, a lista de dispositivos é aberta uma vez e fechada uma vez. Se as funções [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) e [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) não fossem chamadas, a lista de dispositivos teria sido aberta e fechada por cada chamada para [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) e [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate). Usando **DevicePowerOpen e** **DevicePowerClose** salvamos abrindo a lista de dispositivos duas vezes desnecessárias.

 

 



