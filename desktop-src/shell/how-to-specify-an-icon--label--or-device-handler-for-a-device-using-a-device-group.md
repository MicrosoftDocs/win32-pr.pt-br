---
description: Os grupos de dispositivos permitem a especificação dos ícones, do rótulo ou das propriedades DeviceHandlers para qualquer dispositivo que declare a si mesmo parte desse grupo.
ms.assetid: 84433068-A869-479D-8ADA-E8221B38CCAE
title: Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando um grupo de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e534aa6fa1bc7dbfe1bae3a2825a14f18096176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921669"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a>Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando um grupo de dispositivos

Os grupos de dispositivos permitem a especificação dos ícones, do rótulo ou das propriedades DeviceHandlers para qualquer dispositivo que declare a si mesmo parte desse grupo. Se o grupo de dispositivos não for um grupo de dispositivos fornecido pelo sistema, uma chave que define o grupo de dispositivos será adicionada sob a chave **AutoplayHandlers** \\ **DeviceGroups** . Você não precisa definir todas as três propriedades para cada grupo; Você pode definir apenas as propriedades que deseja personalizar. No entanto, dispositivos e manipuladores de dispositivo devem sempre ter ícones e rótulos associados para atender aos requisitos mínimos de usabilidade.

## <a name="instructions"></a>Instruções


O exemplo a seguir usa um sistema com várias unidades zip anexadas. Sem especificar os ícones, rótulo e valores de DeviceHandlers para cada unidade individualmente, você cria um grupo de dispositivos chamado ZipDrive e define esses valores dentro dele. Cada unidade Zip é então declarada como um membro do grupo ZipDrive.

Primeiro, defina o grupo de dispositivos adicionando a seguinte chave *ZipDrive* e seus valores.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceGroups
                        ZipDrive
                           Icons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-103
                           NoMediaIcons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-104
                           Label [REG_SZ] = My Custom Device Label
                           DeviceHandlers [REG_SZ] = MyDeviceHandler
```

Cada dispositivo de unidade Zip é declarado como parte do grupo ZipDrive, herdando as propriedades desse grupo. Na chave **Deviceparameters** da instância do dispositivo, adicione um valor chamado filetype como tipo **reg \_ sz**. A entrada de dados para esse valor é o nome do grupo de dispositivos.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceGroup [REG_SZ] = ZipDrive
```

Você também pode adicionar propriedades de dispositivo personalizadas que não sejam ícones, rótulo e DeviceHandlers sob a chave do grupo de dispositivos e, em seguida, aplicá-las a todos os dispositivos que pertencem a esse grupo de dispositivos.

> [!Note]  
> As propriedades definidas no nível da instância do dispositivo têm precedência sobre as propriedades definidas no nível do grupo de dispositivos, que, por sua vez, têm precedência sobre as propriedades definidas no nível de classe do dispositivo.

 

 

 



