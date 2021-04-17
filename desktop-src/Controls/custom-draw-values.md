---
title: Valores de desenho personalizados (CommCtrl. h)
description: Esta seção lista os valores usados para identificar as partes de um controle TrackBar.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748099"
---
# <a name="custom-draw-values"></a>Valores de desenho personalizados

Esta seção lista os valores usados para identificar as partes de um controle TrackBar.



| Constante                                                                                                                                                   | Descrição                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**\_canal TBCD**</dt> </dl> | Identifica o canal no qual o marcador de Thumb do controle de TrackBar desliza.<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ Thumb**</dt> </dl>       | Identifica o marcador de miniatura do controle TrackBar. Essa é a parte do controle que o usuário move.<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ TICS**</dt> </dl>          | Identifica as marcas de escala que são exibidas ao longo da borda do controle TrackBar.<br/>                      |



## <a name="remarks"></a>Comentários

Os valores personalizados de desenho, por exemplo, são especificados no membro **dwItemSpec** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





