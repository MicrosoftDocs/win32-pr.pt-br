---
title: IPN_FIELDCHANGED código de notificação (commctrl. h)
description: Enviado quando o usuário altera um campo no controle ou move de um campo para outro. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED código de notificação Windows controles
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467cf7f14f3ff8d62f85d973e9a9d11c4dc6d20488ad5b7e30b4c0787b4b1a6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085546"
---
# <a name="ipn_fieldchanged-notification-code"></a>\_Código de notificação do campo IPN

Enviado quando o usuário altera um campo no controle ou move de um campo para outro. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) que contém informações sobre o endereço alterado. O membro **iValue** dessa estrutura conterá o valor inserido, mesmo que esteja fora do intervalo do campo. Você pode modificar esse membro para qualquer valor que esteja dentro do intervalo do campo em resposta a este código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Esse código de notificação não é enviado em resposta a uma mensagem de [**\_ SetAddress IPM**](ipm-setaddress.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





