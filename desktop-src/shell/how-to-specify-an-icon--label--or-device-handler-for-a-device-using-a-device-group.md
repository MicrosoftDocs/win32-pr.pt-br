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
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a><span data-ttu-id="00dd4-103">Como especificar um ícone, rótulo ou manipulador de dispositivo para um dispositivo usando um grupo de dispositivos</span><span class="sxs-lookup"><span data-stu-id="00dd4-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>

<span data-ttu-id="00dd4-104">Os grupos de dispositivos permitem a especificação dos ícones, do rótulo ou das propriedades DeviceHandlers para qualquer dispositivo que declare a si mesmo parte desse grupo.</span><span class="sxs-lookup"><span data-stu-id="00dd4-104">Device groups allow the specification of the Icons, Label, or DeviceHandlers properties for any device that declares itself part of that group.</span></span> <span data-ttu-id="00dd4-105">Se o grupo de dispositivos não for um grupo de dispositivos fornecido pelo sistema, uma chave que define o grupo de dispositivos será adicionada sob a chave **AutoplayHandlers** \\ **DeviceGroups** .</span><span class="sxs-lookup"><span data-stu-id="00dd4-105">If the device group is not a system-provided device group, a key that defines the device group will be added under the **AutoplayHandlers**\\**DeviceGroups** key.</span></span> <span data-ttu-id="00dd4-106">Você não precisa definir todas as três propriedades para cada grupo; Você pode definir apenas as propriedades que deseja personalizar.</span><span class="sxs-lookup"><span data-stu-id="00dd4-106">You do not need to set all three properties for each group; you can set only those properties that you want to customize.</span></span> <span data-ttu-id="00dd4-107">No entanto, dispositivos e manipuladores de dispositivo devem sempre ter ícones e rótulos associados para atender aos requisitos mínimos de usabilidade.</span><span class="sxs-lookup"><span data-stu-id="00dd4-107">However, devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

## <a name="instructions"></a><span data-ttu-id="00dd4-108">Instruções</span><span class="sxs-lookup"><span data-stu-id="00dd4-108">Instructions</span></span>


<span data-ttu-id="00dd4-109">O exemplo a seguir usa um sistema com várias unidades zip anexadas.</span><span class="sxs-lookup"><span data-stu-id="00dd4-109">The following example uses a system with several attached Zip drives.</span></span> <span data-ttu-id="00dd4-110">Sem especificar os ícones, rótulo e valores de DeviceHandlers para cada unidade individualmente, você cria um grupo de dispositivos chamado ZipDrive e define esses valores dentro dele.</span><span class="sxs-lookup"><span data-stu-id="00dd4-110">Without specifying the Icons, Label, and DeviceHandlers values for each drive individually, you create a device group called ZipDrive and define those values within it.</span></span> <span data-ttu-id="00dd4-111">Cada unidade Zip é então declarada como um membro do grupo ZipDrive.</span><span class="sxs-lookup"><span data-stu-id="00dd4-111">Each Zip drive is then declared a member of the ZipDrive group.</span></span>

<span data-ttu-id="00dd4-112">Primeiro, defina o grupo de dispositivos adicionando a seguinte chave *ZipDrive* e seus valores.</span><span class="sxs-lookup"><span data-stu-id="00dd4-112">First, define the device group by adding the following *ZipDrive* key and its values.</span></span>

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

<span data-ttu-id="00dd4-113">Cada dispositivo de unidade Zip é declarado como parte do grupo ZipDrive, herdando as propriedades desse grupo.</span><span class="sxs-lookup"><span data-stu-id="00dd4-113">Each Zip drive device is then declared as part of the ZipDrive group, inheriting the properties of that group.</span></span> <span data-ttu-id="00dd4-114">Na chave **Deviceparameters** da instância do dispositivo, adicione um valor chamado filetype como tipo **reg \_ sz**.</span><span class="sxs-lookup"><span data-stu-id="00dd4-114">Under the **DeviceParameters** key of the device instance, add a value named DeviceGroup as type **REG\_SZ**.</span></span> <span data-ttu-id="00dd4-115">A entrada de dados para esse valor é o nome do grupo de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="00dd4-115">The data entry for this value is the name of the device group.</span></span>

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

<span data-ttu-id="00dd4-116">Você também pode adicionar propriedades de dispositivo personalizadas que não sejam ícones, rótulo e DeviceHandlers sob a chave do grupo de dispositivos e, em seguida, aplicá-las a todos os dispositivos que pertencem a esse grupo de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="00dd4-116">You can also add custom device properties other than Icons, Label, and DeviceHandlers under the device group's key and then apply them to all devices that belong to that device group.</span></span>

> [!Note]  
> <span data-ttu-id="00dd4-117">As propriedades definidas no nível da instância do dispositivo têm precedência sobre as propriedades definidas no nível do grupo de dispositivos, que, por sua vez, têm precedência sobre as propriedades definidas no nível de classe do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="00dd4-117">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 



