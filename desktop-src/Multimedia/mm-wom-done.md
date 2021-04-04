---
title: Mensagem de MM_WOM_DONE (mmsystem. h)
description: A \_ mensagem mm wom \_ concluído é enviada para uma janela quando o buffer de saída fornecido está sendo retornado para o aplicativo. Os buffers são retornados para o aplicativo quando eles são reproduzidos ou como resultado de uma chamada para a função waveOutReset.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- Multimídia do Windows de mensagem MM_WOM_DONE
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645253"
---
# <a name="mm_wom_done-message"></a>MM \_ wom de \_ mensagens concluídas

A mensagem **mm \_ wom \_ concluído** é enviada para uma janela quando o buffer de saída fornecido está sendo retornado para o aplicativo. Os buffers são retornados para o aplicativo quando eles são reproduzidos ou como resultado de uma chamada para a função [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Identificador para o dispositivo de saída de wave-áudio que reproduziu o buffer.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Ponteiro para uma estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) identificando o buffer.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

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

 

