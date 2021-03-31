---
title: Mensagem de MCM_GETCALENDARGRIDINFO (commctrl. h)
description: Obtém informações sobre uma grade de calendário.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- Controles de MCM_GETCALENDARGRIDINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645273"
---
# <a name="mcm_getcalendargridinfo-message"></a>\_Mensagem MCM GETCALENDARGRIDINFO

Obtém informações sobre uma grade de calendário.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) que contém informações sobre a grade de calendário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**True** se for bem-sucedido; caso contrário, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





