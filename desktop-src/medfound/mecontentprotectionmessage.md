---
description: Gerado por um componente de pipeline quando a configuração muda para um dos esquemas de proteção de saída. Esse evento se aplica somente ao conteúdo protegido.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Evento MEContentProtectionMessage (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0316767025fe4446909146b92cfcea8abcc3e0511990c19485a50c94dbc3fa59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013826"
---
# <a name="mecontentprotectionmessage-event"></a>Evento MEContentProtectionMessage

Gerado por um componente de pipeline quando a configuração muda para um dos esquemas de proteção de saída. Esse evento se aplica somente ao conteúdo protegido.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ VAZIO<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Todas as saídas confiáveis devem manipular esse evento. Media Foundation transformação (MFTs) recebem esse evento por meio do método [**IMFTransform::P rocessEvent.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) Os sinks de mídia recebem esse evento [**por meio do método IMFStreamSink::P marker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)

A saída confiável deve aplicar as alterações de política ou retornar o código de erro MF \_ E \_ POLICY SEM \_ SUPORTE.

Os dados e atributos do evento dependem do sistema de proteção de conteúdo em uso.

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

 

 




