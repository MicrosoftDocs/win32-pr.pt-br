---
title: TVM_GETISEARCHSTRING mensagem (Commctrl.h)
description: Recupera a cadeia de caracteres de pesquisa incremental para um controle de exibição de árvore.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- TVM_GETISEARCHSTRING controles Windows mensagem
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79838b2b0d2f109216caf970d33d51b4a3c1369da7b1fc47f5a53e45c3ee82fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060236"
---
# <a name="tvm_getisearchstring-message"></a>Mensagem TVM \_ GETISEARCHSTRING

Recupera a cadeia de caracteres de pesquisa incremental para um controle de exibição de árvore. O controle de exibição de árvore usa a cadeia de caracteres de pesquisa incremental para selecionar um item com base em caracteres digitados pelo usuário. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetISearchString de TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para o buffer que recebe a cadeia de caracteres de pesquisa incremental.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o número de caracteres na cadeia de caracteres de pesquisa incremental.

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do programa. Você deve alocar um buffer grande o suficiente para manter a cadeia de caracteres. Primeiro, chame a mensagem passando **NULL** em *lParam*. Isso retorna o número de caracteres, exceto **NULL,** que são necessários. Em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres. Você deve revisar [considerações de segurança: Controles Windows Microsoft antes](sec-comctls.md) de continuar.

Se o controle de exibição de árvore não estiver no modo de pesquisa incremental, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVM \_ GETISEARCHSTRINGW** (Unicode) e **TVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





