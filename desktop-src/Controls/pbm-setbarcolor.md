---
title: PBM_SETBARCOLOR mensagem (Commctrl.h)
description: Define a cor da barra de indicadores de progresso no controle da barra de progresso.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- PBM_SETBARCOLOR controles de Windows mensagem
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babff5ad74d943d64f5ad61354447498e91e1325c99c82b32183fbc62eabafdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830197"
---
# <a name="pbm_setbarcolor-message"></a>Mensagem PBM \_ SETBARCOLOR

Define a cor da barra de indicadores de progresso no controle da barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

O **valor COLORREF** que especifica a nova cor da barra do indicador de progresso. Especificar o valor CLR DEFAULT faz com que a barra de progresso use sua cor da barra de \_ indicadores de progresso padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a cor da barra do indicador de progresso anterior ou CLR DEFAULT se a cor da barra do indicador de progresso \_ for a cor padrão.

## <a name="remarks"></a>Comentários

Quando os estilos visuais estão habilitados, essa mensagem não tem nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





