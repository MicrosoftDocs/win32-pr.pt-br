---
title: EM_SETPASSWORDCHAR mensagem (Winuser.h)
description: Define ou remove o caractere de senha de um controle de edição. Quando um caractere de senha é definido, esse caractere é exibido no lugar dos caracteres digitados pelo usuário. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- EM_SETPASSWORDCHAR controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56cdfbc108ad5bc1b3e2e11b72937a92da473bcbfa01e974056743ed2e6fde1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412311"
---
# <a name="em_setpasswordchar-message"></a>Mensagem EM \_ SETPASSWORDCHAR

Define ou remove o caractere de senha de um controle de edição. Quando um caractere de senha é definido, esse caractere é exibido no lugar dos caracteres digitados pelo usuário. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O caractere a ser exibido no lugar dos caracteres digitados pelo usuário. Se esse parâmetro for zero, o controle removerá o caractere de senha atual e exibirá os caracteres digitados pelo usuário.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Quando um controle de edição recebe a mensagem **EM \_ SETPASSWORDCHAR,** o controle redesenha todos os caracteres visíveis usando o caractere especificado pelo *parâmetro wParam.* Se *wParam* for zero, o controle redesenhará todos os caracteres visíveis usando os caracteres digitados pelo usuário.

Se um controle de edição for criado com o estilo [**SENHA do \_ ES,**](edit-control-styles.md) o caractere de senha padrão será definido como um asterisco ( \* ). Se um controle de edição for criado sem o estilo **SENHA do \_ ES,** não haverá nenhum caractere de senha. O **estilo SENHA \_ do ES** será removido se uma **mensagem EM \_ SETPASSWORDCHAR** for enviada com o *parâmetro wParam* definido como zero.

**Editar controles:** Controles de edição multilinha não são suportados pelo estilo de senha ou mensagens.

**Edição rica:** Com suporte no Microsoft Rich Edit 2.0 e posterior. Os controles de edição de linha única e multilinha suportam o estilo de senha e as mensagens. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ GETPASSWORDCHAR**](em-getpasswordchar.md)
</dt> </dl>

 

 





