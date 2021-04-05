---
title: Mensagem de TVM_GETISEARCHSTRING (commctrl. h)
description: Recupera a cadeia de caracteres de pesquisa incremental para um controle de exibição de árvore.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- Controles de TVM_GETISEARCHSTRING de mensagens do Windows
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
ms.openlocfilehash: aa968d78a1a99dd3b1eb90055cf2c1d2de51db86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086315"
---
# <a name="tvm_getisearchstring-message"></a>\_Mensagem TVM GETISEARCHSTRING

Recupera a cadeia de caracteres de pesquisa incremental para um controle de exibição de árvore. O controle de exibição de árvore usa a cadeia de caracteres de pesquisa incremental para selecionar um item com base em caracteres digitados pelo usuário. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para o buffer que recebe a cadeia de caracteres de pesquisa incremental.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de caracteres na cadeia de caracteres de pesquisa incremental.

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do seu programa. Você deve alocar um buffer grande o suficiente para manter a cadeia de caracteres. Primeiro, chame a mensagem transmitindo **NULL** em *lParam*. Isso retorna o número de caracteres, excluindo **NULL**, que são necessários. Em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres. Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.

Se o controle de exibição de árvore não estiver no modo de pesquisa incremental, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVM \_ GETISEARCHSTRINGW** (Unicode) e **TVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





