---
title: Mensagem de ICM_DECOMPRESS_END (VFW. h)
description: o ICM \_ descompactar \_ mensagem de término notifica um driver de descompactação de vídeo para encerrar a descompactação e liberar recursos alocados para descompactação. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- mensagem de ICM_DECOMPRESS_END Windows multimídia
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
ms.openlocfilehash: a0c877afac3db0e4cf4d7c476ca3806d2acd15bdf72764549b2958490574a4f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691156"
---
# <a name="icm_decompress_end-message"></a>ICM \_ Descompactar \_ mensagem de término

o **ICM \_ descompactar \_** mensagem de término notifica um driver de descompactação de vídeo para encerrar a descompactação e liberar recursos alocados para descompactação. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

o driver deve liberar todos os recursos alocados para a [**ICM \_ descompactar \_**](icm-decompress-begin.md) a mensagem de início.

[**ICM \_ descompactar \_ início**](icm-decompress-begin.md) e **ICM \_ descompactar \_ fim** não aninhar. se o driver receber **ICM \_ descompactar \_ começar** antes que a descompactação seja interrompida com **ICM \_ \_ término da descompactação**, ela deverá reiniciar a descompactação com novos parâmetros.

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

 

 





