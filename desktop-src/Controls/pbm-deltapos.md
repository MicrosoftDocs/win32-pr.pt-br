---
title: Mensagem de PBM_DELTAPOS (commctrl. h)
description: Avança a posição atual de uma barra de progresso por um incremento especificado e redesenha a barra para refletir a nova posição.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- Controles de PBM_DELTAPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009559"
---
# <a name="pbm_deltapos-message"></a>Mensagem do DELTAPOS do PBM \_

Avança a posição atual de uma barra de progresso por um incremento especificado e redesenha a barra para refletir a nova posição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor para avançar a posição.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a posição anterior.

## <a name="remarks"></a>Comentários

Se o incremento resultar em um valor fora do intervalo do controle, a posição será definida como o limite mais próximo.

O comportamento dessa mensagem será indefinido se for enviado a um controle que tenha o estilo de [**\_ letreiro do PBS**](progress-bar-control-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





