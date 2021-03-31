---
title: Mensagem de CB_GETCOUNT (WinUser. h)
description: Obtém o número de itens na caixa de listagem de uma caixa de combinação.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- Controles de CB_GETCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7900aadf3ba87cc7603a3fe15f4974911c9f9a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645279"
---
# <a name="cb_getcount-message"></a>\_Mensagem de GETCOUNT CB

Obtém o número de itens na caixa de listagem de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o número de itens na caixa de listagem. Se ocorrer um erro, será CB \_ Err.

## <a name="remarks"></a>Comentários

O índice é baseado em zero, portanto, a contagem retornada é maior que o valor de índice do último item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



 

 





