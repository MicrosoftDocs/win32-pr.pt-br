---
description: Instrui uma janela do IME a definir a posição da janela de status. Para enviar esse comando, o aplicativo usa a mensagem WM \_ IME \_ CONTROL com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: d77de7ab-1fbc-42f4-829e-e9fb51668d21
title: IMC_SETSTATUSWINDOWPOS comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee41deac781f7885185df429c5b5231a36f9d5008b5754b718398e7ab4cd060a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107226"
---
# <a name="imc_setstatuswindowpos-command"></a>Comando IMC \_ SETSTATUSWINDOWPOS

Instrui uma janela do IME a definir a posição da janela de status. Para enviar esse comando, o aplicativo usa a mensagem [**WM \_ IME \_ CONTROL**](wm-ime-control.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
LRESULT IMC_SETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Definido como IMC \_ SETSTATUSWINDOWPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Ponteiro para uma [**estrutura POINTS**](/previous-versions//dd162808(v=vs.85)) que contém a coordenada x e a coordenada y da posição da janela de status. As coordenadas estão em coordenadas de tela, em relação ao canto superior esquerdo da exibição.

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
</dt> <dt>

[**CONTROLE \_ WM IME \_**](wm-ime-control.md)
</dt> </dl>

 

 
