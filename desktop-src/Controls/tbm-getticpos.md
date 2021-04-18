---
title: Mensagem de TBM_GETTICPOS (commctrl. h)
description: Recupera a posição física atual de uma marca de escala em um TrackBar.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- Controles de TBM_GETTICPOS de mensagens do Windows
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
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750300"
---
# <a name="tbm_getticpos-message"></a>\_Mensagem tbm GETTICPOS

Recupera a posição física atual de uma marca de escala em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice com base em zero que identifica uma marca de escala. As posições da primeira e da última marca de escala não estão diretamente disponíveis por esta mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a distância, em coordenadas do cliente, do lado esquerdo ou superior da área do cliente do TrackBar para a marca de escala especificada. O valor de retorno é a coordenada x da marca de escala para uma TrackBar horizontal ou a coordenada y para um TrackBar vertical. Se *wParam* não for um índice válido, o valor de retorno será-1.

## <a name="remarks"></a>Comentários

Como a primeira e a última marca de escala não estão disponíveis por essa mensagem, os índices válidos são deslocados da posição de tique na TrackBar. Se a diferença entre [**tbm \_ GETRANGEMIN**](tbm-getrangemin.md) e [**tbm \_ GETRANGEMAX**](tbm-getrangemax.md) for menor que dois, não haverá nenhum índice válido e essa mensagem falhará.

O seguinte ilustra a relação entre os tiques em um TrackBar, os tiques disponíveis por essa mensagem e seus índices com base em zero.

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





