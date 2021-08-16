---
title: EM_GETPASSWORDCHAR mensagem (Winuser.h)
description: Obtém o caractere de senha que um controle de edição exibe quando o usuário ins apresenta texto. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- EM_GETPASSWORDCHAR controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c4e7ac576f18d0ab28fcf8c2288d2bee7966866a71180a81c34896c2396f56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831199"
---
# <a name="em_getpasswordchar-message"></a>Mensagem \_ EM GETPASSWORDCHAR

Obtém o caractere de senha que um controle de edição exibe quando o usuário ins apresenta texto. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

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

## <a name="return-value"></a>Valor retornado

O valor de retorno especifica o caractere a ser exibido no lugar de quaisquer caracteres digitados pelo usuário. Se o valor de retorno for **NULL,** não haverá nenhum caractere de senha e o controle exibirá os caracteres digitados pelo usuário.

## <a name="remarks"></a>Comentários

Se um controle de edição for criado com o estilo [**SENHA do \_ ES,**](edit-control-styles.md) o caractere de senha padrão será definido como um asterisco ( \* ). Se um controle de edição for criado sem o estilo **SENHA do \_ ES,** não haverá nenhum caractere de senha. Para alterar o caractere de senha, envie a [**mensagem EM \_ SETPASSWORDCHAR.**](em-setpasswordchar.md)

**Editar controles:** Controles de edição multilinha não são suportados pelo estilo de senha ou mensagens.

**Edição rica:** Com suporte no Microsoft Rich Edit 2.0 e posterior. Os controles de edição de linha única e multilinha suportam o estilo de senha e as mensagens. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md)
</dt> </dl>

 

 





