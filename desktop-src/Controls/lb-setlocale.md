---
title: LB_SETLOCALE mensagem (Winuser.h)
description: Define a localidade atual da caixa de listagem. Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o estilo SORT LBS) e do texto adicionado pela mensagem \_ \_ ADDSTRING do LB.
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- LB_SETLOCALE controles Windows mensagem
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623b8550b3d5f382ddc8ccc1e1cfcf861a2f8c0a7877ba60c57e393abc1401d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958535"
---
# <a name="lb_setlocale-message"></a>Mensagem \_ LB SETLOCALE

Define a localidade atual da caixa de listagem. Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o estilo [**SORT \_ LBS)**](list-box-styles.md) e do texto adicionado pela mensagem [**\_ ADDSTRING do LB.**](lb-addstring.md)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o identificador de localidade que a caixa de listagem usará para classificação ao adicionar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o identificador de localidade anterior. Se o *parâmetro wParam* especificar uma localidade que não está instalada no sistema, o valor de retorno será LB ERR e a localidade da caixa de listagem atual não \_ será alterada.

## <a name="remarks"></a>Comentários

Use a [**macro MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) para construir um identificador de localidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ GETLOCALE**](lb-getlocale.md)
</dt> </dl>

 

