---
title: IPN_FIELDCHANGED código de notificação (commctrl. h)
description: Enviado quando o usuário altera um campo no controle ou move de um campo para outro. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED de código de notificação controles do Windows
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
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009615"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Esse código de notificação não é enviado em resposta a uma mensagem de [**\_ SetAddress IPM**](ipm-setaddress.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





