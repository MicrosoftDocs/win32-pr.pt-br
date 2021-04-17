---
title: Mensagem de TCM_INSERTITEM (commctrl. h)
description: Insere uma nova guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- Controles de TCM_INSERTITEM de mensagens do Windows
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
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769027"
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

## <a name="return-value"></a>Retornar valor

Retorna o índice da nova guia, se for bem-sucedido, ou-1 caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TCM \_ INSERTITEMW** (Unicode) e **\_ INSERTITEMA TCM** (ANSI)<br/>             |



 

 





