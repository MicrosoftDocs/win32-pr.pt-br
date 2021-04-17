---
title: Mensagem de TCM_HITTEST (commctrl. h)
description: Determina qual guia, se houver, está em uma posição de tela especificada. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- Controles de TCM_HITTEST de mensagens do Windows
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
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754372"
---
# <a name="tcm_hittest-message"></a>\_Mensagem de HITTEST TCM

Determina qual guia, se houver, está em uma posição de tela especificada. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) que especifica a posição da tela a ser testada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice da guia ou-1 se nenhuma guia estiver na posição especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





