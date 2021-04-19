---
description: Gerado por um fluxo de mídia quando ele inicia ou interrompe a finamento do fluxo. Para obter informações sobre a fina, consulte sobre o controle de taxa.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Evento MEStreamThinMode (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793289"
---
# <a name="mestreamthinmode-event"></a>Evento MEStreamThinMode

Gerado por um fluxo de mídia quando ele inicia ou interrompe a finamento do fluxo. Para obter informações sobre a *fina*, consulte [sobre o controle de taxa](about-rate-control.md).

Esse evento pode ser enviado em resposta ao método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) ou ao método [**IMFQualityAdvise:: setdropmode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>VARTYPE</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>VT_BOOL<br/></td>
<td>Indica se a fina foi iniciada ou interrompida.<br/>
<ul>
<li>VARIANT_TRUE: amostras entregues depois que esse evento é finado.</li>
<li>VARIANT_FALSE: exemplos entregues após esse evento não são Finados.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




