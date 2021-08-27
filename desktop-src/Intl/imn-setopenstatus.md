---
description: Notifica um aplicativo quando o status de abertura do contexto de entrada é atualizado. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: cc6fa7f4-b85a-486a-985d-53c071321bd1
title: IMN_SETOPENSTATUS código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57797210f9c0595a952315ca75858890b1998fe16e49049b3a22fb8ed72a5aea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107036"
---
# <a name="imn_setopenstatus-notification-code"></a>Código de notificação do IMN \_ SETOPENSTATUS

Notifica um aplicativo quando o status de abertura do contexto de entrada é atualizado. O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
IMN_SETOPENSTATUS
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMN \_ SETOPENSTATUS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Este comando não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

O aplicativo pode obter informações sobre o status aberto usando a função [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Imm. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)
</dt> <dt>

[**\_notificação do IME do WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




