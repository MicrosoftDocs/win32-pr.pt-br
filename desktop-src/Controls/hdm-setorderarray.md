---
title: Mensagem de HDM_SETORDERARRAY (commctrl. h)
description: Define a ordem da esquerda para a direita dos itens de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetOrderArray do cabeçalho.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- Controles de HDM_SETORDERARRAY de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455232"
---
# <a name="hdm_setorderarray-message"></a>\_Mensagem HDM SETORDERARRAY

Define a ordem da esquerda para a direita dos itens de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetOrderArray do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tamanho do buffer em *lParam*, em elementos. Esse valor deve ser igual ao valor retornado por [**HDM \_ GetItemCount**](hdm-getitemcount.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma matriz que especifica a ordem na qual os itens devem ser exibidos, da esquerda para a direita. Por exemplo, se o conteúdo da matriz for {2,0,1} , o controle exibirá item 2, item 0 e item 1, da esquerda para a direita.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





