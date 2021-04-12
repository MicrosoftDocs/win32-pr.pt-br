---
title: Mensagem de EM_SETPASSWORDCHAR (WinUser. h)
description: Define ou remove o caractere de senha para um controle de edição. Quando um caractere de senha é definido, esse caractere é exibido no lugar dos caracteres digitados pelo usuário. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- Controles de EM_SETPASSWORDCHAR de mensagens do Windows
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
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455019"
---
# <a name="em_setpasswordchar-message"></a>\_Mensagem em SETpasswordchar

Define ou remove o caractere de senha para um controle de edição. Quando um caractere de senha é definido, esse caractere é exibido no lugar dos caracteres digitados pelo usuário. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O caractere a ser exibido no lugar dos caracteres digitados pelo usuário. Se esse parâmetro for zero, o controle removerá o caractere da senha atual e exibirá os caracteres digitados pelo usuário.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Quando um controle de edição recebe a mensagem em **\_ SetPasswordChar** , o controle redesenha todos os caracteres visíveis usando o caractere especificado pelo parâmetro *wParam* . Se *wParam* for zero, o controle redesenhará todos os caracteres visíveis usando os caracteres digitados pelo usuário.

Se um controle de edição for criado com o estilo de [**\_ senha es**](edit-control-styles.md) , o caractere de senha padrão será definido como um asterisco ( \* ). Se um controle de edição for criado sem o estilo de **\_ senha es** , não haverá nenhum caractere de senha. O estilo **es \_ password** será removido se uma mensagem em **\_ SetPasswordChar** for enviada com o parâmetro *wParam* definido como zero.

**Controles de edição:** Os controles de edição de várias linhas não dão suporte ao estilo de senha ou às mensagens.

**Edição avançada:** Com suporte no Microsoft rich edit 2,0 e posterior. Os controles de linha única e de edição de várias linhas dão suporte ao estilo e às mensagens da senha. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETpasswordchar**](em-getpasswordchar.md)
</dt> </dl>

 

 





