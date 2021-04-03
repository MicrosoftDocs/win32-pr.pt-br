---
title: Mensagem de PBM_GETRANGE (commctrl. h)
description: Recupera informações sobre os limites altos e baixos atuais de um determinado controle de barra de progresso.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- Controles de PBM_GETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918795"
---
# <a name="pbm_getrange-message"></a>\_Mensagem GETrange do PBM

Recupera informações sobre os limites altos e baixos atuais de um determinado controle de barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor do sinalizador que especifica qual valor de limite deve ser usado como o valor de retorno da mensagem. Esse parâmetro pode ser um dos seguintes valores:



| Valor                                                                                                                                    | Significado                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>VERDADEIRO * * * *</dt> </dl>    | Retornar o limite baixo.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Retornar o limite alto.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que deve ser preenchida com os limites alto e baixo do controle de barra de progresso. Se esse parâmetro for definido como **NULL**, o controle retornará apenas o limite especificado por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um INT que representa o valor de limite especificado por *wParam*. Se *lParam* não for **NULL**, *lParam* deverá apontar para uma estrutura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que será preenchida com ambos os valores de limite.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





