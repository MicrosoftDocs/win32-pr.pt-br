---
title: Mensagem de TB_SETHOTITEM (commctrl. h)
description: TB_SETHOTITEM mensagem – define o item ativo em uma barra de ferramentas.
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- Controles de TB_SETHOTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90e5b38675d33a361857c4303fa2a89f22cff29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104174"
---
# <a name="tb_sethotitem-message"></a>TB de \_ mensagem SETHOTITEM

Define o item ativo em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item que se tornará quente. Se esse valor for-1, nenhum dos itens será quente.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice do item ativo anterior, ou-1 se não houver nenhum item ativo.

## <a name="remarks"></a>Comentários

O comportamento dessa mensagem não é definido para barras de ferramentas que não têm o estilo [**\_ simples TBSTYLE**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





