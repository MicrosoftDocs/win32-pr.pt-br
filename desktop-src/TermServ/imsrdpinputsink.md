---
title: Interface IMsRdpInputSink
description: Área de trabalho remota de entrada.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- Interface IMsRdpInputSink Serviços de Área de Trabalho Remota
- Interface IMsRdpInputSink Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2167106577a005f6e4ba13ee77edcdbc77302efad9de00395fc7360ade4c5720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058835"
---
# <a name="imsrdpinputsink-interface"></a>Interface IMsRdpInputSink

Área de trabalho remota de entrada.

## <a name="members"></a>Membros

A interface **IMsRdpInputSink** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpInputSink** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMsRdpInputSink** tem esses métodos.



| Método                                                               | Descrição                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| [**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))               | Adiciona entrada de toque.<br/>         |
| [**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))           | Inicie o quadro de toque.<br/>        |
| [**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))               | Quadro de toque final.<br/>          |
| [**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))       | Envia evento de teclado.<br/>     |
| [**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85)) | Envia o evento do botão do mouse.<br/> |
| [**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))     | Envia o evento de movimentação do mouse.<br/>   |
| [**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))   | Envia o evento de roda do mouse.<br/>  |
| [**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))               | Envia evento de sincronização.<br/>         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpInputSink é definido como 4606850E-76A7-4E28-A47E-C7174F619351<br/>     |



 

