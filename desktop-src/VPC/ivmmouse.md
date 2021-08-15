---
title: Interface IVMMouse (VPCCOMInterfaces.h)
description: Controla o dispositivo do mouse em uma VM.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- COMPUTADOR Virtual da interface IVMMouse
- INTERFACE IVMMouse pc virtual , descrito
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912365065b639f3c970390746c8e23ae1fc33648ecdf14278365290c503da26d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998846"
---
# <a name="ivmmouse-interface"></a>Interface IVMMouse

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla o dispositivo do mouse em uma VM (máquina virtual). O **IVMMouse** para uma máquina virtual pode ser recuperado usando a [**propriedade IVMVirtualMachine::Mouse.**](ivmvirtualmachine-mouse.md) As coordenadas para o dispositivo mouse podem ser representadas em coordenadas absolutas ou em coordenadas delta. Use a [**propriedade UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) para distinguir entre os dois métodos de representação de coordenadas. Observe que a recuperação da posição atual do cursor e o uso de coordenadas absolutas só serão suportados se o sistema operacional convidado tiver os componentes de integração instalados.

## <a name="members"></a>Membros

A **interface IVMMouse** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMMouse** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **interface IVMMouse** tem esses métodos.



| Método                                  | Descrição                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [**Clicar**](ivmmouse-click.md)         | Simula um clique de botão do mouse.<br/>                                         |
| [**GetButton**](ivmmouse-getbutton.md) | Recupera o estado atual (para cima ou para baixo) do botão do mouse especificado.<br/> |
| [**SetButton**](ivmmouse-setbutton.md) | Define o estado atual (para cima ou para baixo) do botão do mouse especificado.<br/>      |



 

### <a name="properties"></a>Propriedades

A **interface IVMMouse** tem essas propriedades.



| Propriedade                                                                         | Tipo de acesso           | Descrição                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [**HorizontalPosition**](ivmmouse-horizontalposition.md)<br/>             | Leitura/gravação<br/> | A coordenada X absoluta do mouse.<br/>                                         |
| [**ScrollWheelPosition**](ivmmouse-scrollwheelposition.md)<br/>           | Somente gravação<br/> | A coordenada z do mouse (somente relativa).<br/>                                  |
| [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md)<br/> | Leitura/gravação<br/> | Indica se as coordenadas do mouse representam coordenadas absolutas ou relativas.<br/> |
| [**VerticalPosition**](ivmmouse-verticalposition.md)<br/>                 | Leitura/gravação<br/> | A coordenada Y absoluta do mouse.<br/>                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMmouse é definido como \_ ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



 

