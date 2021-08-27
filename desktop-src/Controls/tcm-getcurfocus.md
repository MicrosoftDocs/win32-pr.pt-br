---
title: TCM_GETCURFOCUS mensagem (Commctrl.h)
description: Retorna o índice do item que tem o foco em um controle de tabulação. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ GetCurFocus.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- TCM_GETCURFOCUS controles Windows mensagem
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 694fb64b033d279292a687c39959925a68999c0b232c847bdf6ec6b476c725e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104936"
---
# <a name="tcm_getcurfocus-message"></a>Mensagem TCM \_ GETCURFOCUS

Retorna o índice do item que tem o foco em um controle de tabulação. Você pode enviar essa mensagem explicitamente ou usando a [**macro TabCtrl \_ GetCurFocus.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice do item de guia que tem o foco.

## <a name="remarks"></a>Comentários

O item que tem o foco pode ser diferente do item selecionado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





