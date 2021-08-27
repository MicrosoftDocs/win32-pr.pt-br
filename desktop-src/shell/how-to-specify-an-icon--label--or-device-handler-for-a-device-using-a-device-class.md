---
description: As classes de dispositivo permitem a especificação das propriedades Icons, Label e DeviceHandlers para qualquer dispositivo dessa classe.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando uma classe de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ef06228d9b533f2793384c0053017f06aca72d05bd64c5333aa2aadca48dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111766"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a>Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando uma classe de dispositivo

As classes de dispositivo permitem a especificação das propriedades Icons, Label e DeviceHandlers para qualquer dispositivo dessa classe. Isso é semelhante ao uso de grupos de dispositivos, mas as classes de dispositivo e suas associações são determinadas pelo hardware em vez de serem criadas ou atribuídas. Cada nome de chave de classe, que é Plug and Play GUID da interface do dispositivo, é encontrado na **chave DeviceClasses.** Na chave de classe individual, atribua os valores para Icons, Label e DeviceHandlers.

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

Você também pode adicionar propriedades de dispositivo personalizadas na chave de classe do dispositivo. As propriedades personalizadas do dispositivo se aplicam a todos os dispositivos nessa classe. Os dispositivos e manipuladores de dispositivos sempre devem ter ícones e rótulos associados para atender aos requisitos mínimos de usabilidade.

> [!Note]  
> As propriedades definidas no nível da instância do dispositivo têm precedência sobre as propriedades definidas no nível do grupo de dispositivos, que, por sua vez, têm precedência sobre as propriedades definidas no nível de classe do dispositivo.

 

 

 



