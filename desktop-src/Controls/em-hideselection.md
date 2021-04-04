---
title: Mensagem de EM_HIDESELECTION (RichEdit. h)
description: A \_ mensagem em HIDESELECTION oculta ou mostra a seleção em um controle de edição rico.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- Controles de EM_HIDESELECTION de mensagens do Windows
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
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918061"
---
# <a name="em_hideselection-message"></a>\_Mensagem em HIDESELECTION

A mensagem em **\_ HIDESELECTION** oculta ou mostra a seleção em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica se a seleção deve ser ocultada ou mostrada. Se esse parâmetro for zero, a seleção será mostrada. Caso contrário, a seleção ficará oculta.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





