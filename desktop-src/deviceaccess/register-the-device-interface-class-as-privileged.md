---
title: Registrar a interface do dispositivo como restrita a aplicativos privilegiados
description: Este tópico mostra como adicionar a propriedade Restricted que indica que somente aplicativos privilegiados podem acessar uma classe de interface do dispositivo.
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 62bca034a2edab9b31267f14672b4821ca6569dead0fd645d98c52c234c24cb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029046"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a>Registrar a interface do dispositivo como restrita a aplicativos privilegiados

Os aplicativos têm acesso negado à funcionalidade personalizada do driver, a menos que tenham permissões concedidas por meio de metadados de dispositivo assinado. Este tópico mostra como adicionar a **propriedade Restricted** que indica que somente aplicativos privilegiados podem acessar uma classe de interface do dispositivo. Drivers de dispositivo personalizados devem ter essa propriedade.

## <a name="instructions"></a>Instruções

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a>Definindo a propriedade Restricted em um arquivo INF (informações)

Na seção `InterfaceInstall32` , o GUID da classe de interface do dispositivo é registrado.

As linhas sob a **diretiva AddProperty configuram** as propriedades da classe de dispositivo. A segunda linha define uma propriedade personalizada em uma categoria de propriedade personalizada. O GUID da categoria de propriedade é **14c83a99-0b3f-44b7-be4c-a178d3990564** e o identificador de propriedade **é 2**. O valor `Flags` de entrada opcional não está presente e o tipo é **17** (**DEVPROP_TYPE_BOOLEAN**). O valor da propriedade é **1**.

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

## <a name="remarks"></a>Comentários

Em vez da **diretiva AddInterface,** o driver também pode chamar a rotina [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) para registrar a classe de interface do dispositivo.

Você também pode definir a propriedade de interface restrita chamando a [**rotina IoSetDeviceInterfacePropertyData.**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata)

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de acesso de driver personalizado,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)aplicativos de dispositivo [UWP para dispositivos internos,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Centro de Desenvolvimento de Hardware](/windows-hardware/drivers/)
