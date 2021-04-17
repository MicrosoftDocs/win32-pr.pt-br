---
description: 'Sinaliza um erro sério. Qualquer componente Media Foundation pode enviar esse evento a qualquer momento. Chame IMFMediaEvent:: GetStatus para obter o código de erro da operação que falhou.'
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Evento MEError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb557dffb2c73a63031a193c331edabe470db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763795"
---
# <a name="meerror-event"></a>Evento MEError

Sinaliza um erro sério. Qualquer componente Media Foundation pode enviar esse evento a qualquer momento. Chame [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) para obter o código de erro da operação que falhou.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento deve ser usado somente para erros inesperados. Não envie esse evento para sinalizar que um método assíncrono falhou. Se um método assíncrono falhar, o código de erro será retornado no evento normal para esse método.

Se ocorrer um erro recuperável durante o streaming, envie o evento [MENonFatalError](menonfatalerror.md) .

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

 

 




