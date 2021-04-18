---
title: Mensagem de ICM_DRAW_GETTIME (VFW. h)
description: A \_ mensagem ICM Draw \_ getTime solicita um driver de renderização que controla o tempo dos quadros de desenho para retornar o valor atual de seu relógio interno. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawGetTime.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_GETTIME
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754330"
---
# <a name="icm_draw_gettime-message"></a>\_ \_ Mensagem getTime do ICM Draw

A mensagem **ICM \_ draw \_ getTime** solicita um driver de renderização que controla o tempo dos quadros de desenho para retornar o valor atual de seu relógio interno. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*
</dt> <dd>

Endereço para conter a hora atual. O valor de retorno deve ser especificado em exemplos.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Em geral, essa mensagem é suportada por hardware que executa sua própria descompactação assíncrona, tempo e desenho. A mensagem também pode ser enviada se o hardware estiver sendo usado como o mestre de sincronização.

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

 

 





