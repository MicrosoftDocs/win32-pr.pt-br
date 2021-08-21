---
title: Mensagem de EM_SETUIANAME (RichEdit. h)
description: Define o nome de um controle de edição rico para a automação da interface do usuário (UIA).
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- controles de Windows de mensagem de EM_SETUIANAME
topic_type:
- apiref
api_name:
- EM_SETUIANAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603d59b7bf246ee8ed7987d42399281ac1b0520ef27e206f2f8eeddf8f363d87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412321"
---
# <a name="em_setuianame-message"></a>\_Mensagem em SETUIANAME

Define o nome de um controle de edição rico para a automação da interface do usuário (UIA).


```C++
#define EM_SETUIANAME       (WM_USER + 320)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres de nome terminada em nulo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

TRUE se o nome de UIA for definido com êxito; caso contrário, FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





