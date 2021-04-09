---
description: Instrui uma janela do IME para recuperar a fonte lógica usada para exibir os caracteres intermediários na janela de composição. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: Comando IMC_GETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164639"
---
# <a name="imc_getcompositionfont-command"></a>\_Comando GETCOMPOSITIONFONT do IMC

Instrui uma janela do IME para recuperar a fonte lógica usada para exibir os caracteres intermediários na janela de composição. Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMC \_ GETCOMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Ponteiro para uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que recebe informações sobre a fonte lógica.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.

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

 

 
