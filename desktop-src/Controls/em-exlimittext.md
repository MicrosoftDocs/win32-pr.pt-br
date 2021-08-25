---
title: EM_EXLIMITTEXT mensagem (Richedit.h)
description: Define um limite superior para a quantidade de texto que o usuário pode digitar ou colar em um controle de edição rico.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- EM_EXLIMITTEXT controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f9879323f3feade3ece536cd130b274b423c98aebedd6b6f5ef1497d995d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915676"
---
# <a name="em_exlimittext-message"></a>Mensagem EM \_ EXLIMITTEXT

Define um limite superior para a quantidade de texto que o usuário pode digitar ou colar em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica a quantidade máxima de texto que pode ser inserida. Se esse parâmetro for zero, o máximo padrão será usado, que é de 64 mil caracteres. Um objeto COM conta como um único caractere.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

O limite de texto definido pela mensagem **EM \_ EXLIMITTEXT** não limita a quantidade de texto que você pode transmitir para um controle de edição rico usando a mensagem [**EM \_ STREAMIN**](em-streamin.md) com *lParam definido* como SF \_ TEXT. No entanto, ele limita a quantidade de texto que você pode transmitir para um controle de edição rico usando a mensagem **EM \_ STREAMIN** com *lParam definido* como SF \_ RTF.

Antes **de EM \_ EXLIMITTEXT** ser chamado, o limite padrão para a quantidade de texto que um usuário pode inserir é de 32.767 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ STREAMIN**](em-streamin.md)
</dt> </dl>

 

 





