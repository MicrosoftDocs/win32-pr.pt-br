---
title: Registrar a interface do dispositivo como restrita a aplicativos com privilégios
description: Este tópico mostra como adicionar a propriedade Restricted que indica que somente aplicativos privilegiados podem acessar uma classe de interface de dispositivo.
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: e23f8b7f2cc1884e2f878739f56507e79eb1bb69
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008562"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a><span data-ttu-id="ea9c6-103">Registrar a interface do dispositivo como restrita a aplicativos com privilégios</span><span class="sxs-lookup"><span data-stu-id="ea9c6-103">Register the device interface as restricted to privileged apps</span></span>

<span data-ttu-id="ea9c6-104">Os aplicativos têm acesso negado à funcionalidade de driver personalizada, a menos que recebam permissões por meio de metadados de dispositivo assinados.</span><span class="sxs-lookup"><span data-stu-id="ea9c6-104">Applications are denied access to custom driver functionality, unless they're granted permissions through signed device metadata.</span></span> <span data-ttu-id="ea9c6-105">Este tópico mostra como adicionar a propriedade **Restricted** que indica que somente aplicativos privilegiados podem acessar uma classe de interface de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea9c6-105">This topic shows how to add the **Restricted** property that indicates that only privileged apps can access a device interface class.</span></span> <span data-ttu-id="ea9c6-106">Os drivers de dispositivo personalizados devem ter essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="ea9c6-106">Custom device drivers must have this property.</span></span>

## <a name="instructions"></a><span data-ttu-id="ea9c6-107">Instruções</span><span class="sxs-lookup"><span data-stu-id="ea9c6-107">Instructions</span></span>

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a><span data-ttu-id="ea9c6-108">Definindo a propriedade restrita em um arquivo de informações (INF)</span><span class="sxs-lookup"><span data-stu-id="ea9c6-108">Setting the Restricted property in an information (INF) file</span></span>

<span data-ttu-id="ea9c6-109">Na `InterfaceInstall32` seção, o GUID da classe de interface do dispositivo é registrado.</span><span class="sxs-lookup"><span data-stu-id="ea9c6-109">In the `InterfaceInstall32` section, the GUID of the device interface class is registered.</span></span>

<span data-ttu-id="ea9c6-110">As linhas na diretiva **AddProperty** definem as propriedades da classe de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea9c6-110">The lines under the **AddProperty** directive set the device class properties.</span></span> <span data-ttu-id="ea9c6-111">A segunda linha define uma propriedade personalizada em uma categoria de propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="ea9c6-111">The second line sets a custom property in a custom property category.</span></span> <span data-ttu-id="ea9c6-112">O GUID de categoria de propriedade é **14c83a99-0b3f-44b7-be4c-a178d3990564** e o identificador de propriedade é **2**.</span><span class="sxs-lookup"><span data-stu-id="ea9c6-112">The property-category GUID is **14c83a99-0b3f-44b7-be4c-a178d3990564**, and the property identifier is **2**.</span></span> <span data-ttu-id="ea9c6-113">O `Flags` valor de entrada opcional não está presente e o tipo é **17** (**DEVPROP_TYPE_BOOLEAN**).</span><span class="sxs-lookup"><span data-stu-id="ea9c6-113">The optional `Flags` entry value is not present, and the type is **17** (**DEVPROP_TYPE_BOOLEAN**).</span></span> <span data-ttu-id="ea9c6-114">O valor da propriedade é **1**.</span><span class="sxs-lookup"><span data-stu-id="ea9c6-114">The value of the property is **1**.</span></span>

```Text
; Below, {11111111-0000-1111-0000-111111111111} is the GUID of the
; new device interface class in an AddInterface directive



; -- Interface installation
[InterfaceInstall32]
{11111111-0000-1111-0000-111111111111}=NewInterfaceInstall

[NewInterfaceInstall]
AddProperty=PrivilegedProperties

[PrivilegedProperties]
; DEVPKey_DeviceInterfaceClass_Restricted
{14c83a99-0b3f-44b7-be4c-a178d3990564}, 2, 17,,1 ; -- non-zero indicates privileged
```

## <a name="remarks"></a><span data-ttu-id="ea9c6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea9c6-115">Remarks</span></span>

<span data-ttu-id="ea9c6-116">Em vez da diretiva **AddInterface** , o driver também pode chamar a rotina [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) para registrar a classe da interface do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea9c6-116">Instead of the **AddInterface** directive, the driver can also call the [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine to register the device interface class.</span></span>

<span data-ttu-id="ea9c6-117">Você também pode definir a propriedade de interface restrita chamando a rotina [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) .</span><span class="sxs-lookup"><span data-stu-id="ea9c6-117">You can also set the restricted interface property by calling the [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea9c6-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea9c6-118">Related topics</span></span>

<span data-ttu-id="ea9c6-119">[Exemplo de acesso de driver personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [centro de desenvolvimento de hardware](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="ea9c6-119">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
