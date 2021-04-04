---
title: Mensagem de TTM_GETCURRENTTOOL (commctrl. h)
description: Recupera as informações da ferramenta atual em um controle ToolTip.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- Controles de TTM_GETCURRENTTOOL de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918471"
---
# <a name="ttm_getcurrenttool-message"></a>\_Mensagem TTM GETCURRENTTOOL

Recupera as informações da ferramenta atual em um controle ToolTip.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que recebe informações sobre a ferramenta atual. Se esse valor for **nulo**, o valor de retorno indicará a existência da ferramenta atual sem realmente recuperar as informações da ferramenta. Se esse valor não for **nulo**, o membro **CbSize** da estrutura **TOOLINFO** deverá ser preenchido antes de enviar essa mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro. Se *lParam* for **nulo**, retornará um valor diferente de zero se existir uma ferramenta atual ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ GETCURRENTTOOLW** (Unicode) e **TTM \_ GETCURRENTTOOLA** (ANSI)<br/>     |



 

 





