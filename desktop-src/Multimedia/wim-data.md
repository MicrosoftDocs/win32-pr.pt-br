---
title: WIM_DATA mensagem (Mmsystem.h)
description: A mensagem WIM DATA é enviada para a função de retorno de chamada de entrada waveform-audio determinada quando os dados waveform-audio estão presentes no buffer de entrada e o buffer está sendo retornado \_ para o aplicativo.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- WIM_DATA mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956dacefa507c2c92f05afdd39bc9c803c630421c81620e0320f3b06648b13b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940744"
---
# <a name="wim_data-message"></a>Mensagem WIM \_ DATA

A **mensagem WIM \_ DATA** é enviada para a função de retorno de chamada de entrada waveform-audio determinada quando os dados waveform-audio estão presentes no buffer de entrada e o buffer está sendo retornado para o aplicativo. A mensagem pode ser enviada quando o buffer estiver cheio ou depois que a [**função waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) for chamada.


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*Dwparam1*
</dt> <dd>

Ponteiro para uma [**estrutura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica o buffer que contém os dados.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*Dwparam2*
</dt> <dd>

Reservado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

O buffer retornado pode não estar cheio. Use o **membro dwBytesRecorded** da estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) especificada por *lpwvhdr* para determinar o número de bytes gravados no buffer retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Waveform Audio](waveform-audio.md)
</dt> <dt>

[Mensagens de forma de onda](waveform-messages.md)
</dt> </dl>

 

