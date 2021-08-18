---
description: Instrui uma janela do IME a obter a posição da janela de status. Para enviar esse comando, o aplicativo usa a mensagem WM \_ IME \_ CONTROL com as configurações de parâmetro mostradas abaixo.
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: IMC_GETSTATUSWINDOWPOS comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfb542ef95a7825e4809e0fa2ce9175493bffeffbbaa36926a91299746026d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068076"
---
# <a name="imc_getstatuswindowpos-command"></a>Comando \_ GETSTATUSWINDOWPOS do IMC

Instrui uma janela do IME a obter a posição da janela de status. Para enviar esse comando, o aplicativo usa a mensagem [**WM \_ IME \_ CONTROL**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

De definido como IMC \_ GETSTATUSWINDOWPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna uma [**estrutura POINTS**](/previous-versions//dd162808(v=vs.85)) que contém a coordenada x e a coordenada y da posição da janela de status nas coordenadas da tela, em relação ao canto superior esquerdo da tela.

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

 

 
