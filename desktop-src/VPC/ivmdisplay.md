---
title: Interface IVMDisplay (VPCCOMInterfaces. h)
description: Controla as configurações de exibição de uma máquina virtual. A interface IVMDisplay para uma máquina virtual pode ser recuperada usando a propriedade de exibição IVMVirtualMachine.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Virtual PC de interface IVMDisplay
- Virtual PC de interface IVMDisplay, descrito
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
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918828"
---
# <a name="ivmdisplay-interface"></a>Interface IVMDisplay

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla as configurações de exibição de uma máquina virtual. A interface **IVMDisplay** para uma máquina virtual pode ser recuperada usando a propriedade [**IVMVirtualMachine::D isplay**](ivmvirtualmachine-display.md) .

## <a name="members"></a>Membros

A interface **IVMDisplay** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDisplay** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMDisplay** tem esses métodos.



| Método                                                       | Descrição                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) | Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.<br/> |
| [**Setdimensions**](ivmdisplay-setdimensions.md)            | Define a altura e a largura da exibição da máquina virtual, em pixels.<br/>                       |



 

### <a name="properties"></a>Propriedades

A interface **IVMDisplay** tem essas propriedades.



| Propriedade                                             | Tipo de acesso          | Descrição                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**Redimensionar**](ivmdisplay-canresize.md)<br/> | Somente leitura<br/> | Indica se o convidado permite alterações de resolução.<br/>                             |
| [**Altura**](ivmdisplay-height.md)<br/>       | Somente leitura<br/> | A altura da exibição da máquina virtual, em pixels.<br/>                            |
| [**Thumbnail**](ivmdisplay-thumbnail.md)<br/> | Somente leitura<br/> | Uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.<br/> |
| [**Videomode**](ivmdisplay-videomode.md)<br/> | Somente leitura<br/> | O modo de vídeo atual (texto, VGA, SVGA e assim por diante).<br/>                               |
| [**Largura**](ivmdisplay-width.md)<br/>         | Somente leitura<br/> | A largura da exibição da máquina virtual, em pixels.<br/>                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



 

