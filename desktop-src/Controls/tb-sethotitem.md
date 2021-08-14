---
title: Mensagem de TB_SETHOTITEM (commctrl. h)
description: TB_SETHOTITEM mensagem – define o item ativo em uma barra de ferramentas.
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- controles de Windows de mensagem de TB_SETHOTITEM
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
ms.openlocfilehash: a48de58e07d877d999c2d0388bf32845fce349511da563c3a6b1fa9f9c7b3d20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318836"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





