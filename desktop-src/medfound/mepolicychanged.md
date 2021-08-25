---
description: Gerado por um componente de pipeline quando a política de saída para o fluxo é mudada. Esse evento se aplica somente ao conteúdo protegido.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Evento MEPolicyChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac87d3dae63b20d19c91f0fdef5471060753152901d9096b1be315cd76e9974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957406"
---
# <a name="mepolicychanged-event"></a>Evento MEPolicyChanged

Gerado por um componente de pipeline quando a política de saída para o fluxo é mudada. Esse evento se aplica somente ao conteúdo protegido.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype                | Descrição                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Ponteiro para a interface [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) da nova política para o fluxo.<br/> <br/> |



## <a name="remarks"></a>Comentários

Todas as saídas confiáveis devem manipular esse evento. Media Foundation transformação (MFTs) recebem esse evento por meio do método [**IMFTransform::P rocessEvent.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) Os sinks de mídia recebem esse evento [**por meio do método IMFStreamSink::P marker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)

A saída confiável deve aplicar a nova política ou retornar o código de erro MF \_ E \_ POLICY SEM \_ SUPORTE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                                              |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




