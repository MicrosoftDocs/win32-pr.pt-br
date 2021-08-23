---
title: Mensagem de HDM_ORDERTOINDEX (commctrl. h)
description: Recupera um valor de índice para um item com base em sua ordem no controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro OrderToIndex do cabeçalho.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- controles de Windows de mensagem de HDM_ORDERTOINDEX
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7afd006c90684137ffc484dac62ab40c04d90c0cdbc87f51102d8e9119e8b14d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576255"
---
# <a name="hdm_ordertoindex-message"></a>\_Mensagem HDM ORDERTOINDEX

Recupera um valor de índice para um item com base em sua ordem no controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ OrderToIndex do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A ordem na qual o item aparece dentro do controle de cabeçalho, da esquerda para a direita. Por exemplo, o valor de índice do item na coluna da extrema esquerda seria 0. O valor do próximo item à direita seria 1 e assim por diante.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna INT que indica o índice do item. Se *wParam* for inválido (negativo ou muito grande), o retorno será igual a *wParam*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





