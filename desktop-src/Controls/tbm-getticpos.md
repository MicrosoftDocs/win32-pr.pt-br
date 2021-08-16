---
title: TBM_GETTICPOS mensagem (Commctrl.h)
description: Recupera a posição física atual de uma marca de escala em uma barra de faixa.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- TBM_GETTICPOS controles de Windows mensagem
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d191034fc1551d4ffc1840498e352e2f3cd82985f1bbc5a7ae8d5350a41fb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046336"
---
# <a name="tbm_getticpos-message"></a>Mensagem \_ GETTICPOS do TBM

Recupera a posição física atual de uma marca de escala em uma barra de faixa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero que identifica uma marca de escala. As posições da primeira e da última marca de escala não estão diretamente disponíveis por meio dessa mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a distância, nas coordenadas do cliente, da esquerda ou superior da área de cliente da barra de faixas para a marca de escala especificada. O valor de retorno é a coordenada x da marca de escala para uma barra de faixa horizontal ou a coordenada y para uma barra de faixa vertical. Se *wParam* não for um índice válido, o valor de retorno será -1.

## <a name="remarks"></a>Comentários

Como a primeira e a última marca de escala não estão disponíveis por meio dessa mensagem, os índices válidos são deslocamentos de sua posição de escala na barra de faixa. Se a diferença entre [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md) e [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) for menor que dois, não haverá nenhum índice válido e essa mensagem falhará.

O exemplo a seguir ilustra a relação entre os tiques em uma barra de faixa, os tiques disponíveis por meio dessa mensagem e seus índices baseados em zero.

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





