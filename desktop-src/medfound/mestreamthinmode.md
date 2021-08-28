---
description: Gerado por um fluxo de mídia quando ele inicia ou interrompe a finamento do fluxo. Para obter informações sobre a fina, consulte sobre o controle de taxa.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Evento MEStreamThinMode (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13a9cc5b625a8b366bece1debc2017fce51e35d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479512"
---
# <a name="mestreamthinmode-event"></a>Evento MEStreamThinMode

Gerado por um fluxo de mídia quando ele inicia ou interrompe a finamento do fluxo. Para obter informações sobre a *fina*, consulte [sobre o controle de taxa](about-rate-control.md).

Esse evento pode ser enviado em resposta ao método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) ou ao método [**IMFQualityAdvise:: setdropmode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.




| VARTYPE | Descrição | 
|---------|-------------|
| VT_BOOL<br /> | Indica se a fina foi iniciada ou interrompida.<br /><ul><li>VARIANT_TRUE: amostras entregues depois que esse evento é finado.</li><li>VARIANT_FALSE: exemplos entregues após esse evento não são Finados.</li></ul><br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




