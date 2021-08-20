---
title: Mensagem de ICM_DRAW_GETTIME (VFW. h)
description: a ICM \_ \_ mensagem gettime de desenho solicita um driver de renderização que controla o tempo de quadros de desenho para retornar o valor atual de seu relógio interno. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawGetTime.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- mensagem de ICM_DRAW_GETTIME Windows multimídia
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
ms.openlocfilehash: 2ecf151b0c22b4de96421b4c11239ce147a21b6d60808b1d84506f3bad699954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987366"
---
# <a name="icm_draw_gettime-message"></a>ICM \_ DESENHAR \_ mensagem GETtime

a **ICM \_ mensagem \_ gettime de desenho** solicita um driver de renderização que controla o tempo de quadros de desenho para retornar o valor atual de seu relógio interno. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .


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

 

 





