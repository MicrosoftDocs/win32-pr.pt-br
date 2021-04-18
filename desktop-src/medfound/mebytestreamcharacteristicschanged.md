---
description: Enviado por um fluxo de bytes quando as características do fluxo de bytes forem alteradas.
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: Evento MEByteStreamCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762216"
---
# <a name="mebytestreamcharacteristicschanged-event"></a>Evento MEByteStreamCharacteristicsChanged

Enviado por um fluxo de bytes quando as características do fluxo de bytes forem alteradas.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE               | Descrição                           |
|-----------------------|---------------------------------------|
| VT \_ vazio <br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento indica que uma ou mais das seguintes características foram alteradas:

-   Sinalizadores de capacidade ([**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))
-   Sinalizador de fim de fluxo ([**IMFByteStream:: IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))
-   Comprimento ([**IMFByteStream:: GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))

Nem todas as implementações de [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) dão suporte a esse evento. Para receber o evento, consulte o objeto byte-Stream para a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




