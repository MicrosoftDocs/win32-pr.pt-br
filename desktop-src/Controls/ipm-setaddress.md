---
title: IPM_SETADDRESS mensagem (Commctrl.h)
description: Define os valores de endereço para todos os quatro campos no controle de endereço IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- IPM_SETADDRESS controles Windows mensagem
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
ms.openlocfilehash: 54817d2206295432e9b477532268a000fc43047ae928ab02224d668912474519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434486"
---
# <a name="ipm_setaddress-message"></a>Mensagem \_ SETADDRESS do IPM

Define os valores de endereço para todos os quatro campos no controle de endereço IP.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um **valor DWORD** que contém o novo endereço. O valor do campo 3 está contido nos bits 0 a 7. O valor do campo 2 está contido nos bits 8 a 15. O valor do campo 1 está contido nos bits 16 a 23. O valor do campo 0 está contido nos bits 24 a 31. A [**macro MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) também pode ser usada para criar as informações de endereço.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

Essa mensagem não gera uma [**notificação \_ IPN FIELDCHANGED.**](ipn-fieldchanged.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





