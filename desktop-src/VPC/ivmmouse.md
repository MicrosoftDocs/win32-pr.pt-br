---
title: Interface IVMMouse (VPCCOMInterfaces. h)
description: Controla o dispositivo de mouse em uma VM.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- Virtual PC de interface IVMMouse
- Virtual PC de interface IVMMouse, descrito
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
ms.openlocfilehash: 7041b8a28b924ffedc8ff23edd2b04afdaa78be2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824696"
---
# <a name="ivmmouse-interface"></a>Interface IVMMouse

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Controla o dispositivo de mouse em uma máquina virtual (VM). O **IVMMouse** para uma máquina virtual pode ser recuperado usando a propriedade [**IVMVirtualMachine:: mouse**](ivmvirtualmachine-mouse.md) . As coordenadas para o dispositivo de mouse podem ser representadas em coordenadas absolutas ou em coordenadas Delta. Use a propriedade [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) para distinguir entre os dois métodos de representação de coordenadas. Observe que a recuperação da posição atual do cursor e o uso de coordenadas absolutas só têm suporte se o sistema operacional convidado tiver os componentes de integração instalados.

## <a name="members"></a>Membros

A interface **IVMMouse** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMMouse** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMMouse** tem esses métodos.



| Método                                  | Descrição                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [**Clicar**](ivmmouse-click.md)         | Simula um clique no botão do mouse.<br/>                                         |
| [**Getbutton**](ivmmouse-getbutton.md) | Recupera o estado atual (para cima ou para baixo) do botão do mouse especificado.<br/> |
| [**SetButton**](ivmmouse-setbutton.md) | Define o estado atual (para cima ou para baixo) do botão do mouse especificado.<br/>      |



 

### <a name="properties"></a>Propriedades

A interface **IVMMouse** tem essas propriedades.



| Propriedade                                                                         | Tipo de acesso           | Descrição                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [**HorizontalPosition**](ivmmouse-horizontalposition.md)<br/>             | Leitura/gravação<br/> | A coordenada x absoluta do mouse.<br/>                                         |
| [**ScrollWheelPosition**](ivmmouse-scrollwheelposition.md)<br/>           | Somente gravação<br/> | A coordenada z do mouse (somente relativo).<br/>                                  |
| [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md)<br/> | Leitura/gravação<br/> | Indica se as coordenadas do mouse representam coordenadas absolutas ou relativas.<br/> |
| [**VerticalPosition**](ivmmouse-verticalposition.md)<br/>                 | Leitura/gravação<br/> | A coordenada y absoluta do mouse.<br/>                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse é definido como ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



 

