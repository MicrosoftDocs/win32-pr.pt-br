---
title: EM_HIDESELECTION mensagem (Richedit.h)
description: A mensagem EM \_ HIDESELECTION oculta ou mostra a seleção em um controle de edição rico.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- EM_HIDESELECTION controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9e33ba0fd8f9a97dcc7ef9ba0a76acfd76110a4d718fa282f3ba66d8f1ef6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437926"
---
# <a name="em_hideselection-message"></a>Mensagem EM \_ HIDESELECTION

A **mensagem EM \_ HIDESELECTION** oculta ou mostra a seleção em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica se a seleção deve ser ocultada ou mostrada. Se esse parâmetro for zero, a seleção será mostrada. Caso contrário, a seleção fica oculta.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





