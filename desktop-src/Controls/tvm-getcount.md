---
title: Mensagem de TVM_GETCOUNT (commctrl. h)
description: Recupera uma contagem dos itens em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetCount de TreeView.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- Controles de TVM_GETCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455734"
---
# <a name="tvm_getcount-message"></a>\_Mensagem de GETCOUNT TVM

Recupera uma contagem dos itens em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetCount de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a contagem de itens.

## <a name="remarks"></a>Comentários

A contagem de nós retornada por [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) é limitada a valores inteiros. Se você adicionar um nó além de 32767, a macro retornará um valor negativo. Depois de adicionar nós 65536, a contagem retorna para zero. Quando isso ocorre, o controle de exibição de árvore aparece vazio sem barras de rolagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





