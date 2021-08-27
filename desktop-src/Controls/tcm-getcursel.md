---
title: Mensagem de TCM_GETCURSEL (commctrl. h)
description: Determina a guia selecionada no momento em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Getcurseal TabCtrl.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- controles de Windows de mensagem de TCM_GETCURSEL
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
ms.openlocfilehash: 6555194972467486789296377b5aaf87ca5520846ec9bf4c03ec345f635b6557
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104896"
---
# <a name="tcm_getcursel-message"></a>Mensagem do TCM \_ GETcurseal

Determina a guia selecionada no momento em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ getcurseal TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice da guia selecionada, se for bem-sucedido, ou-1 se nenhuma guia for selecionada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





