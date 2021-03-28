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
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a><span data-ttu-id="69623-103">Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando uma classe de dispositivo</span><span class="sxs-lookup"><span data-stu-id="69623-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>

<span data-ttu-id="69623-104">As classes de dispositivo permitem a especificação dos ícones, do rótulo e das propriedades DeviceHandlers para qualquer dispositivo dessa classe.</span><span class="sxs-lookup"><span data-stu-id="69623-104">Device classes allow the specification of the Icons, Label, and DeviceHandlers properties for any device of that class.</span></span> <span data-ttu-id="69623-105">Isso é semelhante ao uso de grupos de dispositivos, mas as classes de dispositivo e suas associações são determinadas pelo hardware em vez de serem criadas ou atribuídas.</span><span class="sxs-lookup"><span data-stu-id="69623-105">This is similar to the use of device groups, but device classes and their memberships are determined by the hardware rather than being created or assigned.</span></span> <span data-ttu-id="69623-106">Cada nome de chave de classe, que é a Plug and Play GUID de interface de dispositivo, é encontrado na chave **DeviceClasses** .</span><span class="sxs-lookup"><span data-stu-id="69623-106">Each class key name, which is the Plug and Play device interface GUID, is found under the **DeviceClasses** key.</span></span> <span data-ttu-id="69623-107">Na chave de classe individual, atribua os valores para ícones, rótulo e DeviceHandlers.</span><span class="sxs-lookup"><span data-stu-id="69623-107">Under the individual class key, assign the values for Icons, Label, and DeviceHandlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="69623-108">Instruções</span><span class="sxs-lookup"><span data-stu-id="69623-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="69623-109">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="69623-109">Step 1:</span></span>

<span data-ttu-id="69623-110">O exemplo a seguir mostra os valores de chave de classe e DeviceHandlers para a interface de volume.</span><span class="sxs-lookup"><span data-stu-id="69623-110">The following example shows the class key and DeviceHandlers values for the volume interface.</span></span>

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

<span data-ttu-id="69623-111">Você também pode adicionar propriedades de dispositivo personalizadas na chave de classe do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69623-111">You can also add custom device properties under the device class key.</span></span> <span data-ttu-id="69623-112">As propriedades de dispositivo personalizadas, em seguida, se aplicam a todos os dispositivos nessa classe.</span><span class="sxs-lookup"><span data-stu-id="69623-112">The custom device properties then apply to all devices in that class.</span></span> <span data-ttu-id="69623-113">Os dispositivos e manipuladores de dispositivos sempre devem ter ícones e rótulos associados para atender aos requisitos mínimos de usabilidade.</span><span class="sxs-lookup"><span data-stu-id="69623-113">Devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

> [!Note]  
> <span data-ttu-id="69623-114">As propriedades definidas no nível da instância do dispositivo têm precedência sobre as propriedades definidas no nível do grupo de dispositivos, que, por sua vez, têm precedência sobre as propriedades definidas no nível de classe do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="69623-114">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 



