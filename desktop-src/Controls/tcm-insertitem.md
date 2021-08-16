---
title: Mensagem de TCM_INSERTITEM (commctrl. h)
description: Insere uma nova guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- controles de Windows de mensagem de TCM_INSERTITEM
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c3c17714218562d7ddc82497a7ef27e131e30a2ff04daf36970dfbcf5cc354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829097"
---
# <a name="tcm_insertitem-message"></a>\_Mensagem INSERTITEM de TCM

Insere uma nova guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice da nova guia.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica os atributos da guia. Os membros **dwState** e **dwStateMask** dessa estrutura são ignorados por essa mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice da nova guia, se for bem-sucedido, ou-1 caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TCM \_ INSERTITEMW** (Unicode) e **\_ INSERTITEMA TCM** (ANSI)<br/>             |



 

 





