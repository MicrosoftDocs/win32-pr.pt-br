---
title: Mensagem de LB_ITEMFROMPOINT (WinUser. h)
description: Obtém o índice de base zero do item mais próximo ao ponto especificado em uma caixa de listagem.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- Controles de LB_ITEMFROMPOINT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645030"
---
# <a name="lb_itemfrompoint-message"></a>ITEMFROMPOINT de mensagens de LB \_

Obtém o índice de base zero do item mais próximo ao ponto especificado em uma caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a coordenada x de um ponto, em relação ao canto superior esquerdo da área do cliente da caixa de listagem.

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a coordenada y de um ponto, em relação ao canto superior esquerdo da área do cliente da caixa de listagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno contém o índice do item mais próximo no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)). O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) será zero se o ponto especificado estiver na área do cliente da caixa de listagem, ou um se estiver fora da área do cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

