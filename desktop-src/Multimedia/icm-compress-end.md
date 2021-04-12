---
title: Mensagem de ICM_COMPRESS_END (VFW. h)
description: A \_ mensagem de final de compactação ICM \_ Notifica um driver de compactação de vídeo para encerrar a compactação e liberar recursos alocados para compactação. Você pode enviar essa mensagem explicitamente ou usando a macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_END
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454910"
---
# <a name="icm_compress_end-message"></a>\_Mensagem de final de compactação ICM \_

A mensagem de **\_ \_ final de compactação ICM** notifica um driver de compactação de vídeo para encerrar a compactação e liberar recursos alocados para compactação. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

VCM salva as configurações da mensagem de [**\_ \_ início de compactação ICM**](icm-compress-begin.md) mais recente. **ICM \_ COMPACTar \_ begin** e **ICM \_ compactar \_ fim** não aninhar. Se o driver receber **a \_ compactação de ICM, \_ comece** antes que a compactação seja interrompida com a **\_ \_ extremidade de compactação ICM**, ela deverá reiniciar a compactação com novos parâmetros

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

 

 





