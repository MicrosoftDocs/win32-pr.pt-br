---
description: Enviado por um MFT (Asynchronous Media Foundation Transformation) quando novos dados de saída estão disponíveis no MFT.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Evento METransformHaveOutput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787015"
---
# <a name="metransformhaveoutput-event"></a>Evento METransformHaveOutput

Enviado por um MFT (Asynchronous Media Foundation Transformation) quando novos dados de saída estão disponíveis no MFT.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição               |
|----------------------|---------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> |



## <a name="attributes"></a>Atributos

Nenhum atributo definido para este evento.

## <a name="remarks"></a>Comentários

MFTs assíncronas envie esse evento por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . O MFTs síncrono nunca envia este evento.

Quando o cliente do MFT receber esse evento, ele deverá chamar [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obter a saída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[MFTs assíncrona](asynchronous-mfts.md)
</dt> </dl>

 

 




