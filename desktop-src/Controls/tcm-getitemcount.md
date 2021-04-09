---
title: Mensagem de TCM_GETITEMCOUNT (commctrl. h)
description: Recupera o número de guias no controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ GetItemCount.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- Controles de TCM_GETITEMCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d638a9be81581605b978695c8504f538967c77f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086243"
---
# <a name="tcm_getitemcount-message"></a>Mensagem do TCM \_ GETitemcount

Recupera o número de guias no controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de itens, se for bem-sucedido, ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





