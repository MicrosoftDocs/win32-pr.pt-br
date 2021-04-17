---
title: Mensagem de TVM_SETSCROLLTIME (commctrl. h)
description: Define o tempo máximo de rolagem para o controle de exibição em árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setrolation do TreeView.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- Controles de TVM_SETSCROLLTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753783"
---
# <a name="tvm_setscrolltime-message"></a>TVM de \_ mensagem de AUTOrolagem

Define o tempo máximo de rolagem para o controle de exibição em árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setrolation do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Novo tempo máximo de rolagem, em milissegundos.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o tempo máximo de rolagem anterior, em milissegundos.

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

[**TVM \_ GETrolatime**](tvm-getscrolltime.md)
</dt> </dl>

 

 





