---
description: Instrui a janela do IME para ocultar a janela de status. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: e3da5962-a652-409e-b0ec-eb93671049b4
title: Comando IMC_CLOSESTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207f04d53f269318f87ed11038cbd6817d5e607e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837511"
---
# <a name="imc_closestatuswindow-command"></a>\_Comando CLOSESTATUSWINDOW do IMC

Instrui a janela do IME para ocultar a janela de status. Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.


```C++
LRESULT IMC_CLOSESTATUSWINDOW
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMC \_ CLOSESTATUSWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.

## <a name="remarks"></a>Comentários

Quando a janela de status do IME já estiver oculta, esse comando não fará nada. Embora um aplicativo possa enviar esse comando para a janela do IME, o aplicativo não recebe o comando [IMN \_ CLOSESTATUSWINDOW](imn-closestatuswindow.md) correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de métodos de entrada](input-method-manager-commands.md)
</dt> </dl>

 

 




