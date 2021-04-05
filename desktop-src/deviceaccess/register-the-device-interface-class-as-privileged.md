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
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a>Registrar a interface do dispositivo como restrita a aplicativos com privilégios

Os aplicativos têm acesso negado à funcionalidade de driver personalizada, a menos que recebam permissões por meio de metadados de dispositivo assinados. Este tópico mostra como adicionar a propriedade **Restricted** que indica que somente aplicativos privilegiados podem acessar uma classe de interface de dispositivo. Os drivers de dispositivo personalizados devem ter essa propriedade.

## <a name="instructions"></a>Instruções

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a>Definindo a propriedade restrita em um arquivo de informações (INF)

Na `InterfaceInstall32` seção, o GUID da classe de interface do dispositivo é registrado.

As linhas na diretiva **AddProperty** definem as propriedades da classe de dispositivo. A segunda linha define uma propriedade personalizada em uma categoria de propriedade personalizada. O GUID de categoria de propriedade é **14c83a99-0b3f-44b7-be4c-a178d3990564** e o identificador de propriedade é **2**. O `Flags` valor de entrada opcional não está presente e o tipo é **17** (**DEVPROP_TYPE_BOOLEAN**). O valor da propriedade é **1**.

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

Em vez da diretiva **AddInterface** , o driver também pode chamar a rotina [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) para registrar a classe da interface do dispositivo.

Você também pode definir a propriedade de interface restrita chamando a rotina [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) .

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de acesso de driver personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [centro de desenvolvimento de hardware](/windows-hardware/drivers/)
