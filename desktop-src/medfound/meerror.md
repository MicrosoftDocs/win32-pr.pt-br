---
description: 'Sinaliza um erro sério. Qualquer componente Media Foundation pode enviar esse evento a qualquer momento. Chame IMFMediaEvent:: GetStatus para obter o código de erro da operação que falhou.'
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Evento MEError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd012bf7fbb7f21f37201a67f5c203f5981be6aa16795e2a3c37d16ea268f67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941466"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




