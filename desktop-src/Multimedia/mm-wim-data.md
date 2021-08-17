---
title: Mensagem de MM_WIM_DATA (mmsystem. h)
description: A \_ mensagem de \_ dados wim mm é enviada para uma janela quando a onda de dados de áudio está presente no buffer de entrada e o buffer está sendo retornado para o aplicativo. A mensagem pode ser enviada quando o buffer está cheio ou depois que a função waveInReset é chamada.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- mensagem de MM_WIM_DATA Windows multimídia
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b209e59032c0da4c875a316008c889cf064ae7d8bc48f5c621125a06582673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065466"
---
# <a name="mm_wim_data-message"></a>MM \_ \_ mensagem de dados wim

A mensagem de **\_ \_ dados wim mm** é enviada para uma janela quando a onda de dados de áudio está presente no buffer de entrada e o buffer está sendo retornado para o aplicativo. A mensagem pode ser enviada quando o buffer está cheio ou depois que a função [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) é chamada.


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

Identificador para o dispositivo de entrada de wave-áudio que recebeu os dados.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Ponteiro para uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica o buffer que contém os dados.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

O buffer retornado pode não estar cheio. Use o membro **dwBytesRecorded** da estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) especificada por *lParam* para determinar o número de bytes gravados no buffer retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Áudio de onda](waveform-audio.md)
</dt> <dt>

[Mensagens de formato de onda](waveform-messages.md)
</dt> </dl>

 

