---
title: EM_GETLINECOUNT mensagem (Winuser.h)
description: Obtém o número de linhas em um controle de edição multilinha. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETLINECOUNT controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44487084da8df8edd463fc0683c9d27fcba19a2993465e5493edfd8bb7c3c6b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006679"
---
# <a name="em_getlinecount-message-winuserh"></a>EM_GETLINECOUNT mensagem (Winuser.h)

Obtém o número de linhas em um controle de edição multilinha. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

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

O valor de retorno é um inteiro que especifica o número total de linhas de texto no controle de edição multilinha ou controle de edição rich. Se o controle não tiver texto, o valor de retorno será 1. O valor de retorno nunca será menor que 1.

## <a name="remarks"></a>Comentários

A **mensagem EM \_ GETLINECOUNT** recupera o número total de linhas de texto, não apenas o número de linhas que estão visíveis no momento.

Se o recurso Wordwrap estiver habilitado, o número de linhas poderá mudar quando as dimensões da janela de edição mudarem.

**Edição rica:** Com suporte no Microsoft Rich Edit 1.0 e posterior. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

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

[**EM \_ GETLINE**](em-getline.md)
</dt> <dt>

[**EM \_ LINELENGTH**](em-linelength.md)
</dt> <dt>

[**Editar \_ GetLineCount**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





