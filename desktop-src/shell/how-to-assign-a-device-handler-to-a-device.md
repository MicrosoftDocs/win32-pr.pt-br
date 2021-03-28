---
description: Ilustra o processo para adicionar um manipulador de dispositivo a um dispositivo.
title: Como atribuir um manipulador de dispositivo a um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16db6a39406e3d8ba7cd8b497e12883685b80d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967916"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a><span data-ttu-id="e3b40-103">Como atribuir um manipulador de dispositivo a um dispositivo</span><span class="sxs-lookup"><span data-stu-id="e3b40-103">How to Assign a Device Handler to a Device</span></span>

<span data-ttu-id="e3b40-104">Ilustra o processo para adicionar um manipulador de dispositivo a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3b40-104">Illustrates the process for adding a device handler to a device.</span></span>

## <a name="instructions"></a><span data-ttu-id="e3b40-105">Instruções</span><span class="sxs-lookup"><span data-stu-id="e3b40-105">Instructions</span></span>


<span data-ttu-id="e3b40-106">Para atribuir um manipulador de dispositivo a um dispositivo, na subchave de **parâmetros** do dispositivo da instância do dispositivo, adicione um valor do tipo **reg \_ sz** chamado **DeviceHandlers**.</span><span class="sxs-lookup"><span data-stu-id="e3b40-106">To assign a device handler to a device, under the **Device Parameters** subkey of the device instance, add a value of type **REG\_SZ** named **DeviceHandlers**.</span></span> <span data-ttu-id="e3b40-107">A entrada de dados para esse valor é o nome do manipulador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3b40-107">The data entry for this value is the name of the device handler.</span></span>

<span data-ttu-id="e3b40-108">Veja a seguir um exemplo de entrada para um \_ dispositivo 0031 Pid&059 de identificação fictícia \_ .</span><span class="sxs-lookup"><span data-stu-id="e3b40-108">The following is an example entry for a fictitious Vid\_059&Pid\_0031 device.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceHandlers = MyDeviceHandler
```

<span data-ttu-id="e3b40-109">Os manipuladores de dispositivos também podem ser atribuídos usando configurações de [classe de dispositivo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) ou [grupo de dispositivos](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) .</span><span class="sxs-lookup"><span data-stu-id="e3b40-109">Device handlers can also be assigned by using [device group](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) or [device class](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) settings.</span></span>

 

 



