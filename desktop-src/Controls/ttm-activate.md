---
title: TTM_ACTIVATE mensagem (Commctrl.h)
description: Ativa ou desativa um controle de dica de ferramenta.
ms.assetid: f37da001-748c-4c51-bb32-dc49031ff2fb
keywords:
- TTM_ACTIVATE controles de Windows mensagem
topic_type:
- apiref
api_name:
- TTM_ACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1b2a0c67fec22b11adc54f04ed7a6e4f3cb299ad67018b29f1239cebe0f8604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166389"
---
# <a name="ttm_activate-message"></a>Mensagem TTM \_ ACTIVATE

Ativa ou desativa um controle de dica de ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de ativação. Se esse parâmetro for **TRUE,** o controle de dica de ferramenta será ativado. Se for **FALSE,** o controle de dica de ferramenta será desativado.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





