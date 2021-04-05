---
title: Mensagem de EM_SETMODIFY (WinUser. h)
description: Define ou limpa o sinalizador de modificação para um controle de edição. O sinalizador de modificação indica se o texto dentro do controle de edição foi modificado. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Controles de EM_SETMODIFY de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824526"
---
# <a name="em_setmodify-message"></a>\_Mensagem em SETmodify

Define ou limpa o sinalizador de modificação para um controle de edição. O sinalizador de modificação indica se o texto dentro do controle de edição foi modificado. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O novo valor para o sinalizador de modificação. Um valor **true** indica que o texto foi modificado e um valor **false** indica que ele não foi modificado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

O sistema limpa automaticamente o sinalizador de modificação para zero quando o controle é criado. Se o usuário alterar o texto do controle, o sistema definirá o sinalizador como diferente de zero. Você pode enviar a mensagem em [**\_ GetModify**](em-getmodify.md) para o controle de edição para recuperar o estado atual do sinalizador.

**Edição avançada 1,0:** Os objetos criados sem o sinalizador de **\_ dinâmica REO** bloquearão suas extensões quando o sinalizador de modificação for definido como **false**.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

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

[**em \_ GETmodify**](em-getmodify.md)
</dt> <dt>

[**Reobjeto**](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





