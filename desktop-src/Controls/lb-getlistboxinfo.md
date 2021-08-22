---
title: Mensagem de LB_GETLISTBOXINFO (WinUser. h)
description: Obtém o número de itens por coluna em uma caixa de listagem especificada.
ms.assetid: 925bebd9-2563-4892-a7d7-73d4ef012b42
keywords:
- controles de Windows de mensagem de LB_GETLISTBOXINFO
topic_type:
- apiref
api_name:
- LB_GETLISTBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79339e08ef917780668cd54b6bdfc72cb0f4949aaa446cbc2c34db44b216602d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019314"
---
# <a name="lb_getlistboxinfo-message"></a>GETLISTBOXINFO de mensagens de LB \_

Obtém o número de itens por coluna em uma caixa de listagem especificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o número de itens por coluna.

## <a name="remarks"></a>Comentários

Essa mensagem é equivalente a [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo)
</dt> </dl>

 

 





