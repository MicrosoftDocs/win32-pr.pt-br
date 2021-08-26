---
title: TVM_GETCOUNT mensagem (Commctrl.h)
description: Recupera uma contagem dos itens em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetCount.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- TVM_GETCOUNT controles Windows mensagem
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
ms.openlocfilehash: 3fce2d3ed6580acc875007ff3962bbeb21e9c0d3c3cb38128a2339da79597f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060346"
---
# <a name="tvm_getcount-message"></a>Mensagem \_ GETCOUNT do TVM

Recupera uma contagem dos itens em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetCount.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a contagem de itens.

## <a name="remarks"></a>Comentários

A contagem de nós retornada [**por TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) é limitada a valores inteiros. Se você adicionar um nó além de 32767, a macro retornará um valor negativo. Depois de adicionar 65536 nós, a contagem retorna para zero. Quando isso ocorre, o controle de exibição de árvore aparece vazio sem barras de rolagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





