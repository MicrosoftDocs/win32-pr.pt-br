---
title: TVM_GETSCROLLTIME mensagem (Commctrl.h)
description: Recupera o tempo máximo de rolagem para o controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro TreeView GetScrollTime.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- TVM_GETSCROLLTIME controles de Windows mensagem
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
ms.openlocfilehash: e026a463476d5625f7632d7b6679ce94ca2c8ab6d8c6a050d8938bd46d9858b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408493"
---
# <a name="tvm_getscrolltime-message"></a>Mensagem TVM \_ GETSCROLLTIME

Recupera o tempo máximo de rolagem para o controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ TreeView GetScrollTime.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o tempo máximo de rolagem, em milissegundos.

## <a name="remarks"></a>Comentários

O tempo máximo de rolagem é o período mais longo que uma operação de rolagem pode levar. A rolagem será ajustada para que a rolagem ocorrerá dentro do tempo máximo de rolagem. Uma operação de rolagem pode levar menos tempo do que o máximo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETSCROLLTIME**](tvm-setscrolltime.md)
</dt> </dl>

 

 





