---
title: TBM_GETTOOLTIPS mensagem (Commctrl.h)
description: Recupera o alça para o controle de dica de ferramenta atribuído à barra de faixas, se for o caso.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- TBM_GETTOOLTIPS controles de Windows mensagem
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c97c94ab3a696f5967f724e76d2d8702a01275bedc06ad7c13907d57710a078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078060"
---
# <a name="tbm_gettooltips-message"></a>Mensagem \_ GETTOOLTIPS do TBM

Recupera o alça para o controle de dica de ferramenta atribuído à barra de faixas, se for o caso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para o controle de dica de ferramenta atribuído à barra de faixa ou **NULL** se as dicas de ferramenta não estão em uso. Se o controle trackbar não usar o estilo [**DICAS DE FERRAMENTA TBS, \_**](trackbar-control-styles.md) o valor de retorno será **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





