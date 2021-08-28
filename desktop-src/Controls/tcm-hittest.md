---
title: TCM_HITTEST mensagem (Commctrl.h)
description: Determina qual guia, se alguma, está em uma posição de tela especificada. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- TCM_HITTEST controles Windows mensagem
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f0e619303300c5d04fc26a4b32009923422aede2a97b8faeb2175297c87d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104826"
---
# <a name="tcm_hittest-message"></a>Mensagem TCM \_ HITTEST

Determina qual guia, se alguma, está em uma posição de tela especificada. Você pode enviar essa mensagem explicitamente ou usando a [**macro TabCtrl \_ HitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) que especifica a posição da tela a ser testada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice da guia ou -1 se nenhuma guia estiver na posição especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





