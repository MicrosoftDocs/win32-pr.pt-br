---
title: Mensagem de LB_GETLISTBOXINFO (WinUser. h)
description: Obtém o número de itens por coluna em uma caixa de listagem especificada.
ms.assetid: 925bebd9-2563-4892-a7d7-73d4ef012b42
keywords:
- Controles de LB_GETLISTBOXINFO de mensagens do Windows
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
ms.openlocfilehash: 51f49f96e3f12b1c21e81e8b5358e174e576d07f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009265"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é o número de itens por coluna.

## <a name="remarks"></a>Comentários

Essa mensagem é equivalente a [**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetListBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getlistboxinfo)
</dt> </dl>

 

 





