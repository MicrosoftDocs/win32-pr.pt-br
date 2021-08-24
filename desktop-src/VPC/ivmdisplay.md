---
title: Interface IVMDisplay (VPCCOMInterfaces.h)
description: Controla as configurações de exibição de uma máquina virtual. A interface IVMDisplay para uma máquina virtual pode ser recuperada usando a propriedade IVMVirtualMachine Display.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- COMPUTADOR Virtual da interface IVMDisplay
- COMPUTADOR Virtual da interface IVMDisplay, descrito
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6239747477cdddf0ecbcf3acac90e33e61c0f5f4c9dd327b80eb6a33cb113c32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654136"
---
# <a name="ivmdisplay-interface"></a>Interface IVMDisplay

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla as configurações de exibição de uma máquina virtual. A **interface IVMDisplay** para uma máquina virtual pode ser recuperada usando a [**propriedade IVMVirtualMachine::D isplay.**](ivmvirtualmachine-display.md)

## <a name="members"></a>Membros

A **interface IVMDisplay** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDisplay** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **interface IVMDisplay** tem esses métodos.



| Método                                                       | Descrição                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) | Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.<br/> |
| [**SetDimensions**](ivmdisplay-setdimensions.md)            | Define a altura e a largura da exibição da máquina virtual, em pixels.<br/>                       |



 

### <a name="properties"></a>Propriedades

A **interface IVMDisplay** tem essas propriedades.



| Propriedade                                             | Tipo de acesso          | Descrição                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**Canresize**](ivmdisplay-canresize.md)<br/> | Somente leitura<br/> | Indica se o Convidado permite alterações de resolução.<br/>                             |
| [**Altura**](ivmdisplay-height.md)<br/>       | Somente leitura<br/> | A altura da exibição da máquina virtual, em pixels.<br/>                            |
| [**Thumbnail**](ivmdisplay-thumbnail.md)<br/> | Somente leitura<br/> | Uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.<br/> |
| [**VideoMode**](ivmdisplay-videomode.md)<br/> | Somente leitura<br/> | O modo de vídeo atual (Texto, VGA, SVGA e assim por diante).<br/>                               |
| [**Largura**](ivmdisplay-width.md)<br/>         | Somente leitura<br/> | A largura da exibição da máquina virtual, em pixels.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDisplay é definido como \_ 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



 

