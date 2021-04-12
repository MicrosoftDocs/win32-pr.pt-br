---
title: Mensagem de ICM_DRAW_QUERY (VFW. h)
description: A \_ mensagem de consulta de desenho ICM \_ consulta um driver de renderização para determinar se ele pode renderizar dados em um formato específico. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawQuery.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_QUERY
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455326"
---
# <a name="icm_draw_query-message"></a>Mensagem de consulta de \_ desenho ICM \_

A mensagem de **\_ \_ consulta de desenho ICM** consulta um driver de renderização para determinar se ele pode renderizar dados em um formato específico. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se o driver puder renderizar dados no formato especificado ou ICERR \_ BADFORMAT de outra forma.

## <a name="remarks"></a>Comentários

Essa mensagem é diferente da mensagem [**ICM \_ draw \_ begin**](icm-draw-begin.md) , pois consulta o driver em um sentido geral. **ICM \_ O DRAW \_ begin** determina se o driver pode desenhar os dados usando o formato especificado sob condições específicas, como esticar a imagem.

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

 

