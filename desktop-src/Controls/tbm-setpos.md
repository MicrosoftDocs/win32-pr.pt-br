---
title: Mensagem de TBM_SETPOS (commctrl. h)
description: Define a posição lógica atual do controle deslizante em um TrackBar.
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- Controles de TBM_SETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e8da6e8e231a26b216ca8f9314d59474384857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919196"
---
# <a name="tbm_setpos-message"></a>\_Mensagem tbm SETPOS

Define a posição lógica atual do controle deslizante em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de redesenho. Se esse parâmetro for **true**, a mensagem redesenhará o controle com o controle deslizante na posição fornecida pelo *lParam*. Se esse parâmetro for **false**, a mensagem não redesenhará o controle deslizante na nova posição. Observe que a mensagem define o valor da posição do controle deslizante (como retornado pela mensagem [**tbm \_ GETPOS**](tbm-getpos.md) ), independentemente do parâmetro *wParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Nova posição lógica do controle deslizante. As posições lógicas válidas são os valores inteiros no intervalo de TrackBar de mínimo para o máximo de posições do controle deslizante. Se esse valor estiver fora do intervalo máximo e mínimo do controle, a posição será definida como o valor máximo ou mínimo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





