---
title: Mensagem de MCIWNDM_GETERROR (VFW. h)
description: A \_ mensagem GETerror MCIWNDM recupera o último erro MCI encontrado. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetError.
ms.assetid: f110a9b3-5b05-4bf0-85d1-b49ce7396222
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETERROR
topic_type:
- apiref
api_name:
- MCIWNDM_GETERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2977bb079351824b48da21f4ba3cc2dc5afe7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824219"
---
# <a name="mciwndm_geterror-message"></a>\_Mensagem GETerror MCIWNDM

A **mensagem \_ GetError MCIWNDM** recupera o último erro MCI encontrado. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .


```C++
MCIWNDM_GETERROR 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamanho, em bytes, do buffer de erro.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Ponteiro para um buffer definido pelo aplicativo usado para retornar a cadeia de caracteres de erro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o valor de erro de inteiro se for bem-sucedido.

## <a name="remarks"></a>Comentários

Se *LP* for um ponteiro válido, uma cadeia de caracteres terminada em nulo correspondente ao erro será retornada em seu buffer. Se a cadeia de caracteres de erro for maior do que o buffer, MCIWnd o truncará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
</dt> </dl>

 

 





