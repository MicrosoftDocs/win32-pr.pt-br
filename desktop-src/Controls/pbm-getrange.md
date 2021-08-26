---
title: PBM_GETRANGE mensagem (Commctrl.h)
description: Recupera informações sobre os limites altos e baixos atuais de um determinado controle de barra de progresso.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE controles Windows mensagem
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
ms.openlocfilehash: 007a62386180e7b47edca201236cd1dacc86df696b5705d02ec1da0acb89761c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986396"
---
# <a name="pbm_getrange-message"></a>Mensagem \_ GETRANGE do PBM

Recupera informações sobre os limites altos e baixos atuais de um determinado controle de barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor do sinalizador que especifica qual valor limite deve ser usado como o valor de retorno da mensagem. Esse parâmetro pode ser um dos seguintes valores:



| Valor                                                                                                                                    | Significado                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE****</dt> </dl>    | Retornar o limite baixo.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE****</dt> </dl> | Retornar o limite alto.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que deve ser preenchida com os limites altos e baixos do controle de barra de progresso. Se esse parâmetro for definido como **NULL,** o controle retornará apenas o limite especificado por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um INT que representa o valor de limite especificado por *wParam*. Se *lParam* não for **NULL,** *lParam* deverá apontar para uma estrutura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que deve ser preenchida com ambos os valores de limite.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





