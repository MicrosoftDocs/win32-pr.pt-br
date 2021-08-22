---
description: Instrui uma janela do IME a recuperar a fonte lógica usada para exibir caracteres intermediários na janela de composição. Para enviar esse comando, o aplicativo usa a mensagem WM \_ IME \_ CONTROL com as configurações de parâmetro mostradas abaixo.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: IMC_GETCOMPOSITIONFONT comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ebf26592f2fd000f864685bd79d71b189fc24d695941691fe2e01d48132d00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068096"
---
# <a name="imc_getcompositionfont-command"></a>Comando \_ GETCOMPOSITIONFONT do IMC

Instrui uma janela do IME a recuperar a fonte lógica usada para exibir caracteres intermediários na janela de composição. Para enviar esse comando, o aplicativo usa a mensagem [**WM \_ IME \_ CONTROL**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Definido como IMC \_ GETCOMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Ponteiro para uma [**estrutura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que recebe informações sobre a fonte lógica.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Métodos de Entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de Métodos de Entrada](input-method-manager-commands.md)
</dt> </dl>

 

 
