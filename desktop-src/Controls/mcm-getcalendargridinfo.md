---
title: Mensagem de MCM_GETCALENDARGRIDINFO (commctrl. h)
description: Obtém informações sobre uma grade de calendário.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- controles de Windows de mensagem de MCM_GETCALENDARGRIDINFO
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
ms.openlocfilehash: 26365b940b17617b1f00b93697fc78fa759dd2599d3398ccb8d92725159a70cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170163"
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

## <a name="return-value"></a>Valor retornado

**True** se for bem-sucedido; caso contrário, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





