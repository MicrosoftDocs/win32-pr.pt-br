---
title: Mensagem de PBM_SETSTATE (commctrl. h)
description: Define o estado da barra de progresso.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- controles de Windows de mensagem de PBM_SETSTATE
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794006517eaa23789f3a25425b1213fede7f8dde9893587def02ebc9605b28f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986056"
---
# <a name="pbm_setstate-message"></a>Mensagem do estado do PBM \_

Define o estado da barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Estado da barra de progresso que está sendo definida. Um dos valores a seguir.



| Valor                                                                                                                                                   | Significado                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ normal**</dt> </dl> | Em andamento.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**erro de PBST \_**</dt> </dl>    | Erro.<br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST em \_ pausa**</dt> </dl> | Em pausa.<br/>      |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o estado anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





