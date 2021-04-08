---
description: Instrui uma janela do IME para definir a posição da janela de status. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: Comando IMC_SETSTATUSWINDOWPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c57eef1a4748bb58018ee47aaee21eb677016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010565"
---
# <a name="imc_setstatuswindowpos-command"></a>\_Comando SETSTATUSWINDOWPOS do IMC

Instrui uma janela do IME para definir a posição da janela de status. Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMC \_ SETSTATUSWINDOWPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Ponteiro para uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) que contém a coordenada x e a coordenada y da posição da janela de status. As coordenadas são em coordenadas de tela, em relação ao canto superior esquerdo da exibição.

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
</dt> <dt>

[**\_controle IME do WM \_**](wm-ime-control.md)
</dt> </dl>

 

 
