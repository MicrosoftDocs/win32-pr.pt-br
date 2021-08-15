---
title: ICM_DECOMPRESS_END mensagem (Vfw.h)
description: A ICM DECOMPRESS END notifica um driver de descompactação de vídeo para encerrar a descompactação e liberar recursos alocados para \_ \_ descompactação. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END mensagem Windows Multimídia
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
# <a name="icm_decompress_end-message"></a>\_ICM Mensagem DECOMPRESS \_ END

A **ICM \_ DECOMPRESS \_ END** notifica um driver de descompactação de vídeo para encerrar a descompactação e liberar recursos alocados para descompactação. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressEnd.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou se um erro for o contrário.

## <a name="remarks"></a>Comentários

O driver deve liberar todos os recursos alocados para a [**ICM \_ DECOMPRESS \_ BEGIN.**](icm-decompress-begin.md)

[**ICM \_ DECOMPRESS \_ BEGIN**](icm-decompress-begin.md) e **ICM \_ DECOMPRESS \_ END não** aninham. Se o driver receber ICM **\_ DECOMPRESS \_ BEGIN** antes que a descompactação seja interrompida com **ICM \_ DECOMPRESS \_ END**, ele deverá reiniciar a descompactação com novos parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Compactação de Vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





