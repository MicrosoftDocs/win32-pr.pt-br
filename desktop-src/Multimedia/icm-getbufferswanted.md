---
title: Mensagem de ICM_GETBUFFERSWANTED (VFW. h)
description: a \_ mensagem ICM GETBUFFERSWANTED consulta um driver para o número de buffers a serem alocados. Você pode enviar essa mensagem explicitamente ou usando a macro ICGetBuffersWanted.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- mensagem de ICM_GETBUFFERSWANTED Windows multimídia
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bd5fae6e9f008649366cf922ef117f5b6f7560a7764c4f8d81552a255de48a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495866"
---
# <a name="icm_getbufferswanted-message"></a>ICM \_ Mensagem GETBUFFERSWANTED

a mensagem **ICM \_ GETBUFFERSWANTED** consulta um driver para o número de buffers a serem alocados. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) .


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*
</dt> <dd>

Endereço para conter o número de amostras que o driver precisa para renderizar os dados com eficiência.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna ICERR \_ OK se o êxito ou o ICERR \_ não tiver suporte de outra forma.

## <a name="remarks"></a>Comentários

Essa mensagem é usada por drivers que usam o hardware para renderizar dados e para garantir um intervalo de tempo mínimo causado pela espera pela chegada de buffers. Por exemplo, se um driver controla uma placa de descompactação de vídeo que pode conter 10 quadros de vídeo, ele poderia retornar 10 para esta mensagem. Isso instrui os aplicativos a tentar manter 10 quadros à frente do quadro que ele precisa atualmente.

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

 

 





