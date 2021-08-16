---
title: TBM_CLEARTICS mensagem (Commctrl.h)
description: Remove as marcas de escala atuais de uma barra de faixa. Essa mensagem não remove as primeiras e as últimas marcas de escala, que são criadas automaticamente pela barra de faixa.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- TBM_CLEARTICS controles de Windows mensagem
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9390fc45c5b96a7b85d3b1b366e34d24c3b4bf0bc60ec066ead28357bcec1439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046766"
---
# <a name="tbm_cleartics-message"></a>Mensagem \_ TBM CLEARTICS

Remove as marcas de escala atuais de uma barra de faixa. Essa mensagem não remove as primeiras e as últimas marcas de escala, que são criadas automaticamente pela barra de faixa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Redesenhar sinalizador. Se esse parâmetro for **TRUE,** a barra de faixa será redesenhada depois que as marcas de escala são limpas. Se esse parâmetro for **FALSE,** a mensagem limpará as marcas de escala, mas não redesenhará a barra de faixa.

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



 

 





