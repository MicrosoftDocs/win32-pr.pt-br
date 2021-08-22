---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362cffa8d4b34d70111505a60fd5eadc68a220cd45c3beb519e5e39ba62f1a81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749810"
---
# <a name="iagentexshowdefaultcharacterproperties"></a>IAgentEx::ShowDefaultCharacterProperties

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

Exibe a janela de propriedades de caractere padrão.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

A coordenada X da janela em pixels, em relação à origem da tela (superior esquerdo).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

A coordenada Y da janela em pixels, em relação à origem da tela (superior esquerdo).

</dd> <dt>

<span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*
</dt> <dd>

Sinalizador de posição padrão. Se esse parâmetro for **True,** o Microsoft Agent exibirá a janela da folha de propriedades para o caractere padrão no último local em que ele apareceu.

> [!Note]  
> Por Windows 2000, pode ser necessário chamar a nova API [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) para garantir que essa janela se torne a janela de primeiro plano. Para obter mais informações sobre como definir a janela de primeiro plano em Windows 2000, consulte a documentação do SDK da plataforma.

 

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 