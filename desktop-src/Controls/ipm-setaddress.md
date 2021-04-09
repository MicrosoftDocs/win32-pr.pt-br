---
title: Mensagem de IPM_SETADDRESS (commctrl. h)
description: Define os valores de endereço para todos os quatro campos no controle de endereço IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- Controles de IPM_SETADDRESS de mensagens do Windows
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085817"
---
# <a name="ipm_setaddress-message"></a>\_Mensagem de SETADDRESS IPM

Define os valores de endereço para todos os quatro campos no controle de endereço IP.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um valor **DWORD** que contém o novo endereço. O valor do campo 3 está contido em bits 0 a 7. O valor do campo 2 está contido em bits 8 a 15. O valor do campo 1 está contido nos bits 16 a 23. O valor do campo 0 está contido em bits 24 a 31. A macro [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) também pode ser usada para criar as informações de endereço.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

Essa mensagem não gera uma notificação [**\_ FieldChanged IPN**](ipn-fieldchanged.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





