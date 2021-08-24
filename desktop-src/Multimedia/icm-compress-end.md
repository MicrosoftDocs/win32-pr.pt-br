---
title: Mensagem de ICM_COMPRESS_END (VFW. h)
description: a \_ mensagem de fim de compactação ICM \_ notifica um driver de compactação de vídeo para encerrar a compactação e liberar recursos alocados para compactação. Você pode enviar essa mensagem explicitamente ou usando a macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- mensagem de ICM_COMPRESS_END Windows multimídia
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
ms.openlocfilehash: 9c320190da37d286db1c20329a849ea09ac6d915087e9d3bdbb2333d31cec3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785036"
---
# <a name="icm_compress_end-message"></a>ICM \_ COMPACTar \_ mensagem de término

a mensagem de **\_ \_ fim de compactação ICM** notifica um driver de compactação de vídeo para encerrar a compactação e liberar recursos alocados para compactação. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

VCM salva as configurações da mensagem de [**\_ \_ início ICM compactar**](icm-compress-begin.md) mais recente. **ICM \_ compactar \_ início** e **ICM \_ compactar \_ fim** não aninhar. se o seu driver receber **ICM \_ compactar \_ começar** antes que a compactação seja interrompida com **ICM \_ \_ extremidade de compactação**, ela deverá reiniciar a compactação com novos parâmetros.

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

 

 





