---
description: Ocorreu um erro não fatal durante o streaming.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Evento MENonFatalError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296573"
---
# <a name="menonfatalerror-event"></a>Evento MENonFatalError

Ocorreu um erro não fatal durante o streaming. Qualquer componente Media Foundation pode enviar esse evento a qualquer momento.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE            | Descrição                                                        |
|--------------------|--------------------------------------------------------------------|
| \_UI4 VT<br/> | Valor **HRESULT** que descreve o erro.<br/> <br/> |



## <a name="attributes"></a>Atributos

Nenhum atributo definido para este evento.

## <a name="remarks"></a>Comentários

Esse evento sinaliza um erro inesperado, mas recuperável durante o streaming. Por exemplo, uma fonte de mídia poderá enviar esse evento se ele descartar um pacote.

Não envie esse evento para sinalizar que um método assíncrono falhou. Se um método assíncrono falhar, o código de erro será retornado no evento normal para esse método.

Se ocorrer um erro de streaming não recuperável, envie o evento [MEError](meerror.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




