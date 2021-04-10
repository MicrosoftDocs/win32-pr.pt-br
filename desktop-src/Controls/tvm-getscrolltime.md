---
title: Mensagem de TVM_GETSCROLLTIME (commctrl. h)
description: Recupera o tempo máximo de rolagem para o controle de exibição em árvore. Você pode enviar essa mensagem explicitamente ou usando a macro do TreeView \_ getrolation.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- Controles de TVM_GETSCROLLTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085328"
---
# <a name="tvm_getscrolltime-message"></a>\_Mensagem TVM GETscrolltime

Recupera o tempo máximo de rolagem para o controle de exibição em árvore. Você pode enviar essa mensagem explicitamente ou usando a macro do [**TreeView \_ getrolation**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o tempo máximo de rolagem, em milissegundos.

## <a name="remarks"></a>Comentários

O tempo máximo de rolagem é a quantidade mais longa de tempo que uma operação de rolagem pode tomar. A rolagem será ajustada para que a rolagem ocorra dentro do tempo máximo de rolagem. Uma operação de rolagem pode levar menos tempo do que o máximo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETrolatime**](tvm-setscrolltime.md)
</dt> </dl>

 

 





