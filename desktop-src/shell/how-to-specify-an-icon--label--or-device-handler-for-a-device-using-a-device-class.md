---
description: As classes de dispositivo permitem a especificação dos ícones, do rótulo e das propriedades DeviceHandlers para qualquer dispositivo dessa classe.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando uma classe de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81ee6fa469a6bec13abbc1d8a088f5fb334ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988976"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a>Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando uma classe de dispositivo

As classes de dispositivo permitem a especificação dos ícones, do rótulo e das propriedades DeviceHandlers para qualquer dispositivo dessa classe. Isso é semelhante ao uso de grupos de dispositivos, mas as classes de dispositivo e suas associações são determinadas pelo hardware em vez de serem criadas ou atribuídas. Cada nome de chave de classe, que é a Plug and Play GUID de interface de dispositivo, é encontrado na chave **DeviceClasses** . Na chave de classe individual, atribua os valores para ícones, rótulo e DeviceHandlers.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

O exemplo a seguir mostra os valores de chave de classe e DeviceHandlers para a interface de volume.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceClasses
                        {53f5630d-b6bf-11d0-94f2-00a0c91efb8b}
                           DeviceHandlers [REG_SZ] = GenericVolumeHandler
```

Você também pode adicionar propriedades de dispositivo personalizadas na chave de classe do dispositivo. As propriedades de dispositivo personalizadas, em seguida, se aplicam a todos os dispositivos nessa classe. Os dispositivos e manipuladores de dispositivos sempre devem ter ícones e rótulos associados para atender aos requisitos mínimos de usabilidade.

> [!Note]  
> As propriedades definidas no nível da instância do dispositivo têm precedência sobre as propriedades definidas no nível do grupo de dispositivos, que, por sua vez, têm precedência sobre as propriedades definidas no nível de classe do dispositivo.

 

 

 



