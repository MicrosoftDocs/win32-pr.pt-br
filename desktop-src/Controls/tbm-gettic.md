---
title: Mensagem de TBM_GETTIC (commctrl. h)
description: Recupera a posição lógica de uma marca de escala em um TrackBar. A posição lógica pode ser qualquer um dos valores inteiros na faixa de TrackBar de mínimo para máximo de posições do controle deslizante.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- controles de Windows de mensagem de TBM_GETTIC
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7cdd2c28f9add787c41da3cde3fabc3a5dff33812b3dd9c07a26a603d3a79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829600"
---
# <a name="tbm_gettic-message"></a>\_Mensagem tbm GETTIC

Recupera a posição lógica de uma marca de escala em um TrackBar. A posição lógica pode ser qualquer um dos valores inteiros na faixa de TrackBar de mínimo para máximo de posições do controle deslizante.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice com base em zero que identifica uma marca de escala. Os índices válidos estão no intervalo de zero a dois menores que a contagem de tiques retornada pela mensagem [**tbm \_ GETNUMTICS**](tbm-getnumtics.md) .

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a posição lógica da marca de escala especificada, ou-1 se *wParam* não especificar um índice válido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





