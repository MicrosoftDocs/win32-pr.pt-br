---
title: Mensagem de ICM_DRAW_SETTIME (VFW. h)
description: O ICM \_ desenha \_ setTime fornece informações de sincronização para um driver de renderização que manipula a temporização de quadros de desenho.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_SETTIME
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824324"
---
# <a name="icm_draw_settime-message"></a>\_ \_ Mensagem setTime do ICM Draw

O **ICM \_ desenha \_ setTime** fornece informações de sincronização para um driver de renderização que manipula a temporização de quadros de desenho. As informações de sincronização são o número de exemplo do quadro a ser desenhado. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) .


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*
</dt> <dd>

Número de exemplo do quadro a ser renderizado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Normalmente, o driver compara o valor especificado com o número de quadro associado à hora de seu relógio interno e tenta sincronizar os dois se a diferença for significativa.

Use essa mensagem quando o hardware executar sua própria descompactação assíncrona, tempo e desenho, e o hardware depender de um sinal de sincronização externo (o hardware não está sendo usado como o mestre de sincronização).

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

 

 





