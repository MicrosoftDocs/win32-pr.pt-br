---
title: Mensagem de EM_SETHANDLE (WinUser. h)
description: Define o identificador da memória que será usada por um controle de edição de várias linhas.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- Controles de EM_SETHANDLE de mensagens do Windows
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
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086187"
---
# <a name="em_sethandle-message"></a>\_Mensagem em SEThandle

Define o identificador da memória que será usada por um controle de edição de várias linhas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o buffer de memória que o controle de edição usa para armazenar o texto atualmente exibido em vez de alocar sua própria memória. Se necessário, o controle realoca essa memória.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Antes que um aplicativo defina um novo identificador de memória, ele deve enviar uma mensagem em em [**\_ GetHandle**](em-gethandle.md) para recuperar o identificador do buffer de memória atual e liberar essa memória.

Um controle de edição realoca automaticamente o buffer determinado sempre que ele precisa de espaço adicional para o texto, ou remove texto suficiente para que o espaço adicional não seja mais necessário.

O envio de uma mensagem em **\_ onhandle** limpa o buffer de desfazer (em [**\_ cancelamento**](em-canundo.md) retorna zero) e o sinalizador de modificação interna (em [**\_ GetModify**](em-getmodify.md) retorna zero). A janela de controle de edição é redesenhada.

**Edição avançada:** Não há suporte para a mensagem em **\_ SetHandle** . Os controles de edição avançados não armazenam texto como uma matriz simples de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ CANcelamento**](em-canundo.md)
</dt> <dt>

[**em \_ GEThandle**](em-gethandle.md)
</dt> <dt>

[**em \_ GETmodify**](em-getmodify.md)
</dt> </dl>

 

 





