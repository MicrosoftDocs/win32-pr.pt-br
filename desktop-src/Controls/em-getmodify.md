---
title: Mensagem de EM_GETMODIFY (WinUser. h)
description: Obtém o estado de um sinalizador de modificação do controle de edição. O sinalizador indica se o conteúdo do controle de edição foi modificado. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- Controles de EM_GETMODIFY de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824224"
---
# <a name="em_getmodify-message"></a>Em \_ getmodificar mensagem

Obtém o estado de um sinalizador de modificação do controle de edição. O sinalizador indica se o conteúdo do controle de edição foi modificado. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o conteúdo do controle de edição tiver sido modificado, o valor de retorno será diferente de zero; caso contrário, será zero.

## <a name="remarks"></a>Comentários

O sistema limpa automaticamente o sinalizador de modificação para zero quando o controle é criado. Se o usuário alterar o texto do controle, o sistema definirá o sinalizador como diferente de zero. Você pode enviar a [**mensagem \_ eme**](em-setmodify.md) para o controle de edição para definir ou limpar o sinalizador.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETmodify**](em-setmodify.md)
</dt> </dl>

 

 





