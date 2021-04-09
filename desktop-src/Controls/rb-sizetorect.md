---
title: Mensagem de RB_SIZETORECT (commctrl. h)
description: Tenta encontrar o melhor layout das faixas para o retângulo fornecido.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- Controles de RB_SIZETORECT de mensagens do Windows
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
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086413"
---
# <a name="rb_sizetorect-message"></a>\_Mensagem SIZETORECT RB

Tenta encontrar o melhor layout das faixas para o retângulo fornecido.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica o retângulo para o qual o controle rebar deve ser dimensionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará um valor diferente de zero se ocorrer uma alteração de layout ou nenhum outro.

## <a name="remarks"></a>Comentários

As bandas de rebar serão organizadas e encapsuladas conforme necessário para caber no retângulo. As faixas que têm o \_ estilo RBBS VARIABLEHEIGHT serão redimensionadas de maneira uniforme possível para caber no retângulo. A altura de um rebar horizontal ou a largura de um rebar vertical pode ser alterada, dependendo do novo layout.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

