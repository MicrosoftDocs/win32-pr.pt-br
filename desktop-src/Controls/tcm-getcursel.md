---
title: Mensagem de TCM_GETCURSEL (commctrl. h)
description: Determina a guia selecionada no momento em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Getcurseal TabCtrl.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- Controles de TCM_GETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749670"
---
# <a name="tcm_getcursel-message"></a>Mensagem do TCM \_ GETcurseal

Determina a guia selecionada no momento em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ getcurseal TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice da guia selecionada, se for bem-sucedido, ou-1 se nenhuma guia for selecionada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





