---
title: RB_SIZETORECT mensagem (Commctrl.h)
description: Tenta encontrar o melhor layout das faixas para o retângulo determinado.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- RB_SIZETORECT controles de Windows mensagem
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63630fc64f56dff914b4fb576ecc6cef43d12d192606a5088924fd6a5832e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078540"
---
# <a name="rb_sizetorect-message"></a>Mensagem RB \_ SIZETORECT

Tenta encontrar o melhor layout das faixas para o retângulo determinado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que especifica o retângulo para o qual o controle de barra de rebar deve ser dimensionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se ocorrer uma alteração de layout ou zero caso contrário.

## <a name="remarks"></a>Comentários

As faixas de barra de rebar serão organizadas e empacotadas conforme necessário para caber no retângulo. As faixas que têm o estilo RBBS VARIABLEHEIGHT serão resized da maneira mais adequada \_ possível para se ajustarem ao retângulo. A altura de uma barra de rebar horizontal ou a largura de uma barra vertical pode mudar, dependendo do novo layout.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

