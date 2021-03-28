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
# <a name="how-to-assign-a-device-handler-to-a-device"></a>Como atribuir um manipulador de dispositivo a um dispositivo

Ilustra o processo para adicionar um manipulador de dispositivo a um dispositivo.

## <a name="instructions"></a>Instruções


Para atribuir um manipulador de dispositivo a um dispositivo, na subchave de **parâmetros** do dispositivo da instância do dispositivo, adicione um valor do tipo **reg \_ sz** chamado **DeviceHandlers**. A entrada de dados para esse valor é o nome do manipulador do dispositivo.

Veja a seguir um exemplo de entrada para um \_ dispositivo 0031 Pid&059 de identificação fictícia \_ .

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

Os manipuladores de dispositivos também podem ser atribuídos usando configurações de [classe de dispositivo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) ou [grupo de dispositivos](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) .

 

 



