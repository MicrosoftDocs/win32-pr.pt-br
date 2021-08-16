---
title: EM_SETHANDLE mensagem (Winuser.h)
description: Define o handle da memória que será usada por um controle de edição multilinha.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- EM_SETHANDLE controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3ece3eb9c385b5f4d468a7dd2f08ff3335a4314b4c90569cdba453c4815728f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412587"
---
# <a name="em_sethandle-message"></a>Mensagem EM \_ SETHANDLE

Define o handle da memória que será usada por um controle de edição multilinha.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para o buffer de memória que o controle de edição usa para armazenar o texto exibido no momento em vez de alocar sua própria memória. Se necessário, o controle relocará essa memória.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Antes de um aplicativo define um novo alça de memória, ele deve enviar uma mensagem [**EM \_ GETHANDLE**](em-gethandle.md) para recuperar o handle do buffer de memória atual e deve liberar essa memória.

Um controle de edição relocará automaticamente o buffer determinado sempre que precisar de espaço adicional para o texto ou remover texto suficiente para que o espaço adicional não seja mais necessário.

Enviar uma **mensagem EM \_ SETHANDLE** limpa o buffer de desfazer ([**EM \_ CANUNDO**](em-canundo.md) retorna zero) e o sinalizador de modificação interno ([**EM \_ GETMODIFY retorna**](em-getmodify.md) zero). A janela de controle de edição é redesenhada.

**Edição rica:** Não há suporte para a mensagem **EM \_ SETHANDLE.** Controles de edição rich não armazenam texto como uma matriz simples de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**EM \_ GETHANDLE**](em-gethandle.md)
</dt> <dt>

[**EM \_ GETMODIFY**](em-getmodify.md)
</dt> </dl>

 

 





