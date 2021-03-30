---
title: Mensagem de HDM_INSERTITEM (commctrl. h)
description: Insere um novo item em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro InsertItem do cabeçalho.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- Controles de HDM_INSERTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455180"
---
# <a name="hdm_insertitem-message"></a>\_Mensagem HDM INSERTITEM

Insere um novo item em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ InsertItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice do item após o qual o novo item deve ser inserido. O novo item será inserido no final do controle de cabeçalho se *wParam* for maior ou igual ao número de itens no controle. Se *wParam* for zero, o novo item será inserido no início do controle de cabeçalho.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que contém informações sobre o novo item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do novo item se for bem-sucedido ou-1 caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDM \_ INSERTITEMW** (Unicode) e **HDM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





