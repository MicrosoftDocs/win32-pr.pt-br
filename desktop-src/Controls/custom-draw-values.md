---
title: Valores de desenho personalizados (CommCtrl.h)
description: Esta seção lista os valores usados para identificar as partes de um controle Trackbar.
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
ms.openlocfilehash: cb714df7c91819a7d459c4c9fbed1fbc1e0d4fd2455f52891030d95991fa6497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831687"
---
# <a name="custom-draw-values"></a>Valores de desenho personalizados

Esta seção lista os valores usados para identificar as partes de um controle Trackbar.



| Constante                                                                                                                                                   | Descrição                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**CANAL \_ TBCD**</dt> </dl> | Identifica o canal ao lado do marcador de miniatura do controle de faixa.<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ THUMB**</dt> </dl>       | Identifica o marcador de miniatura do controle de barra de faixa. Essa é a parte do controle que o usuário move.<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ TICS**</dt> </dl>          | Identifica as marcas de escala exibidas ao longo da borda do controle de barra de faixa.<br/>                      |



## <a name="remarks"></a>Comentários

Os valores de Desenho Personalizados, por exemplo, são especificados no **membro dwItemSpec** da [**estrutura NMCUSTOMDRAW.**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





