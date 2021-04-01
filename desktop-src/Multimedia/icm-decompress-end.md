---
title: Mensagem de ICM_DECOMPRESS_END (VFW. h)
description: A \_ mensagem de término de DEScompactação ICM \_ Notifica um driver de descompactação de vídeo para encerrar a descompactação e liberar recursos alocados para descompactação. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS_END
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645017"
---
# <a name="icm_decompress_end-message"></a>\_Mensagem de final de DEScompactação ICM \_

A mensagem de **\_ \_ término de descompactação ICM** notifica um driver de descompactação de vídeo para encerrar a descompactação e liberar recursos alocados para descompactação. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O driver deve liberar todos os recursos alocados para a mensagem de [**\_ \_ início de descompactação do ICM**](icm-decompress-begin.md) .

[**ICM \_ Descompactar \_ início**](icm-decompress-begin.md) e **\_ descompactação \_ de ICM** não aninhe. Se o driver receber **a \_ descompactação ICM \_ começar** antes que a descompactação seja interrompida com o **\_ \_ ponto de descompactação ICM**, ela deverá reiniciar a descompactação com novos parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





