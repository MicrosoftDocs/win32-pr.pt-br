---
title: Mensagem de EM_SETUIANAME (RichEdit. h)
description: Define o nome de um controle de edição rico para a automação da interface do usuário (UIA).
ms.assetid: 60506FEE-9708-4668-8846-42B0B696DD9A
keywords:
- Controles de EM_SETUIANAME de mensagens do Windows
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
ms.openlocfilehash: b0102b792a9eccfc6116acc3a534b00fb64b7ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918615"
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

## <a name="return-value"></a>Retornar valor

TRUE se o nome de UIA for definido com êxito; caso contrário, FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





