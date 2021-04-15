---
description: Use os elementos de programação de energia do dispositivo para gerenciar a maneira como os dispositivos são executados enquanto o sistema está em estado de suspensão.
ms.assetid: 44479f5d-2e92-4802-a633-3e0bb7d61e94
title: Usando a API de energia do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cabd7a54efc0979360a863dc9c0cf16d69d8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505876"
---
# <a name="using-the-device-power-api"></a><span data-ttu-id="87ad6-103">Usando a API de energia do dispositivo</span><span class="sxs-lookup"><span data-stu-id="87ad6-103">Using the Device Power API</span></span>

<span data-ttu-id="87ad6-104">Use os elementos de programação de energia do dispositivo para gerenciar a maneira como os dispositivos são executados enquanto o sistema está em estado de suspensão.</span><span class="sxs-lookup"><span data-stu-id="87ad6-104">Use the Device Power programming elements to manage the way devices perform while the system is in a sleep state.</span></span>

## <a name="opening-and-closing-the-device-list"></a><span data-ttu-id="87ad6-105">Abrindo e fechando a lista de dispositivos</span><span class="sxs-lookup"><span data-stu-id="87ad6-105">Opening and closing the device list</span></span>

<span data-ttu-id="87ad6-106">Abrir e fechar a lista de dispositivos é um processo dispendioso em termos de tempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="87ad6-106">Opening and closing the device list is a costly process in terms of CPU time.</span></span> <span data-ttu-id="87ad6-107">As funções [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) e [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) que fazem isso só serão necessárias se o aplicativo precisar consultar a lista de dispositivos várias vezes.</span><span class="sxs-lookup"><span data-stu-id="87ad6-107">The [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions that do this are only necessary if the application needs to query the device list multiple times.</span></span>

<span data-ttu-id="87ad6-108">Se [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) for chamado, [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) deverá ser chamado quando as consultas de lista de dispositivos forem concluídas.</span><span class="sxs-lookup"><span data-stu-id="87ad6-108">If [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) is called, [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) must be called when device-list queries are complete.</span></span> <span data-ttu-id="87ad6-109">[**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) e [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) não fecharão a lista de dispositivos se ela tiver sido explicitamente aberta pelo **DevicePowerOpen**.</span><span class="sxs-lookup"><span data-stu-id="87ad6-109">[**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) will not close the device list if it has been explicitly opened by **DevicePowerOpen**.</span></span>

## <a name="enumerating-devices"></a><span data-ttu-id="87ad6-110">Enumerando dispositivos</span><span class="sxs-lookup"><span data-stu-id="87ad6-110">Enumerating devices</span></span>

<span data-ttu-id="87ad6-111">A função [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) detecta se a lista de dispositivos está aberta e, se não estiver, abre.</span><span class="sxs-lookup"><span data-stu-id="87ad6-111">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="87ad6-112">**DevicePowerEnumDevices** enumera os dispositivos com base nos critérios de pesquisa especificados.</span><span class="sxs-lookup"><span data-stu-id="87ad6-112">**DevicePowerEnumDevices** enumerates the devices based on the specified search criteria.</span></span> <span data-ttu-id="87ad6-113">Se a lista de dispositivos foi aberta pela função, ela é fechada antes que a função seja retornada.</span><span class="sxs-lookup"><span data-stu-id="87ad6-113">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="enabling-and-disabling-a-device-from-waking-the-system"></a><span data-ttu-id="87ad6-114">Habilitando e desabilitando um dispositivo de ativar o sistema</span><span class="sxs-lookup"><span data-stu-id="87ad6-114">Enabling and disabling a device from waking the system</span></span>

<span data-ttu-id="87ad6-115">A função [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) , semelhante a [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), detecta se a lista de dispositivos está aberta e, caso contrário, a abre.</span><span class="sxs-lookup"><span data-stu-id="87ad6-115">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function, similar to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices), detects whether the device list is open, and if not, opens it.</span></span> <span data-ttu-id="87ad6-116">**DevicePowerSetDeviceState** define os critérios especificados para o dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="87ad6-116">**DevicePowerSetDeviceState** then sets the specified criteria for the specified device.</span></span> <span data-ttu-id="87ad6-117">Se a lista de dispositivos foi aberta pela função, ela é fechada antes que a função seja retornada.</span><span class="sxs-lookup"><span data-stu-id="87ad6-117">If the device list was opened by the function, it is closed before the function returns.</span></span>

## <a name="example-code"></a><span data-ttu-id="87ad6-118">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="87ad6-118">Example Code</span></span>

<span data-ttu-id="87ad6-119">O exemplo a seguir demonstra o uso da API de energia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87ad6-119">The following example demonstrates the use of the Device Power API.</span></span>


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



<span data-ttu-id="87ad6-120">Neste exemplo, a lista de dispositivos é aberta uma vez e fechada uma vez.</span><span class="sxs-lookup"><span data-stu-id="87ad6-120">In this example the device list is opened once, and closed once.</span></span> <span data-ttu-id="87ad6-121">Se as funções [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) e [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) não forem chamadas, a lista de dispositivos teria sido aberta e fechada por cada chamada para [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) e [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate).</span><span class="sxs-lookup"><span data-stu-id="87ad6-121">If the [**DevicePowerOpen**](/windows/desktop/api/PowrProf/nf-powrprof-devicepoweropen) and [**DevicePowerClose**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerclose) functions were not called, the device list would have been opened and closed by each call to [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) and [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate).</span></span> <span data-ttu-id="87ad6-122">Usando **DevicePowerOpen** e **DevicePowerClose** , salvamos abrindo a lista de dispositivos duas vezes desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="87ad6-122">By using **DevicePowerOpen** and **DevicePowerClose** we saved opening the device list two unnecessary times.</span></span>

 

 



