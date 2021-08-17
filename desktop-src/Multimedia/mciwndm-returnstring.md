---
title: MCIWNDM_RETURNSTRING mensagem (Vfw.h)
description: A mensagem RETURNSTRING MCIWNDM recupera a resposta ao comando de cadeia de \_ caracteres MCI mais recente enviado a um dispositivo MCI.
ms.assetid: 36a5222c-a63c-4b8c-ad0c-a00477e95b96
keywords:
- MCIWNDM_RETURNSTRING mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_RETURNSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ea9624c70245c67f0f6a78af68bf291ae3ce60ba65ae2cd273008bbc914ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137653"
---
# <a name="mciwndm_returnstring-message"></a>Mensagem RETURNSTRING MCIWNDM \_

A **mensagem \_ RETURNSTRING MCIWNDM** recupera a resposta ao comando de cadeia de caracteres MCI mais recente enviado a um dispositivo MCI. As informações na resposta são fornecidas como uma cadeia de caracteres terminada em nulo. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndReturnString.**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)


```C++
MCIWNDM_RETURNSTRING 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Tamanho, em bytes, do buffer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Ponteiro para um buffer definido pelo aplicativo para conter a cadeia de caracteres terminada em nulo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro correspondente à cadeia de caracteres MCI.

## <a name="remarks"></a>Comentários

Se a cadeia de caracteres terminada em nulo for maior que o buffer, a cadeia de caracteres será truncada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
</dt> </dl>

 

 





