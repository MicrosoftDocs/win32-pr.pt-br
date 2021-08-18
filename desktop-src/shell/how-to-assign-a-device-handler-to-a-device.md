---
description: Ilustra o processo para adicionar um manipulador de dispositivos a um dispositivo.
title: Como atribuir um manipulador de dispositivos a um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de091a7206e8fe2d9ea2781e2c5b3475cb71446bae2effa9e017795ced8b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092970"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a>Como atribuir um manipulador de dispositivos a um dispositivo

Ilustra o processo para adicionar um manipulador de dispositivos a um dispositivo.

## <a name="instructions"></a>Instruções


Para atribuir um manipulador de dispositivos a um dispositivo, na sub-chave **Parâmetros** do Dispositivo da instância do dispositivo, adicione um valor do tipo **REG \_ SZ** chamado **DeviceHandlers**. A entrada de dados para esse valor é o nome do manipulador de dispositivo.

A seguir está um exemplo de entrada para um dispositivo Vid \_ 059&Pid \_ 0031 fictício.

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

Os manipuladores de dispositivos também podem ser atribuídos usando [configurações de grupo de dispositivos](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) [ou classe de](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) dispositivo.

 

 



