---
title: Pintar a janela
description: Você criou sua janela. Agora você deseja mostrar algo dentro dele. Na Windows terminologia, isso é chamado de pintura da janela. Para misturar metáforas, uma janela é uma tela em branco, aguardando você preenchê-la.
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: 93d0cb0234975b61ee7ffc05a680b5e1e6b1e01b9d4de7235fc4239ec5573f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896988"
---
# <a name="painting-the-window"></a>Pintar a janela

Você criou sua janela. Agora você deseja mostrar algo dentro dele. Na Windows terminologia, isso é chamado de pintura da janela. Para misturar metáforas, uma janela é uma tela em branco, aguardando você preenchê-la.

Às vezes, seu programa iniciará a pintura para atualizar a aparência da janela. Em outros momentos, o sistema operacional notificará você de que você deve repintar uma parte da janela. Quando isso ocorre, o sistema operacional envia à janela uma mensagem [**WM \_ PAINT.**](/windows/desktop/gdi/wm-paint) A parte da janela que deve ser pintada é chamada de região *de atualização*.

Na primeira vez que uma janela é mostrada, toda a área do cliente da janela deve ser pintada. Portanto, você sempre receberá pelo menos uma mensagem [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) quando mostrar uma janela.

![ilustração mostrando a região de atualização de uma janela](images/painting01.png)

Você só é responsável por pintar a área do cliente. O quadro ao redor, incluindo a barra de título, é pintado automaticamente pelo sistema operacional. Depois de terminar de pintar a área do cliente, você limpa a região de atualização, que informa ao sistema operacional que ele não precisa enviar outra mensagem [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) até que algo mude.

Agora, suponha que o usuário mova outra janela para que ela obscureça uma parte da janela. Quando a parte obscurecida se torna visível novamente, essa parte é adicionada à região de atualização e sua janela recebe outra [**mensagem WM \_ PAINT.**](/windows/desktop/gdi/wm-paint)

![ilustração mostrando como a região de atualização muda quando duas janelas se sobrepõem](images/painting02.png)

A região de atualização também será muda se o usuário alongar a janela. No diagrama a seguir, o usuário alonga a janela à direita. A área recém-exposta no lado direito da janela é adicionada à região de atualização:

![ilustração mostrando como a região de atualização muda quando uma janela é resized](images/painting03.png)

Em nosso primeiro programa de exemplo, a rotina de pintura é muito simples. Ele apenas preenche toda a área do cliente com uma cor sólida. Ainda assim, este exemplo é suficiente para demonstrar alguns dos conceitos importantes.

```C++
switch (uMsg)
{
    case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);

        // All painting occurs here, between BeginPaint and EndPaint.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

        EndPaint(hwnd, &ps);
    }
    return 0;
}
```

Inicie a operação de pintura chamando a [**função BeginPaint.**](/windows/desktop/api/winuser/nf-winuser-beginpaint) Essa função preenche a estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) com informações sobre a solicitação de reint. A região de atualização atual é dada no **membro rcPaint** de **PAINTSTRUCT.** Essa região de atualização é definida em relação à área do cliente:

![ilustração mostrando a origem da área do cliente](images/painting04.png)

No código de pintura, você tem duas opções básicas:

- Paint toda a área do cliente, independentemente do tamanho da região de atualização. Tudo o que está fora da região de atualização é recortado. Ou seja, o sistema operacional o ignora.
- Otimize pintando apenas a parte da janela dentro da região de atualização.

Se você sempre pintar toda a área do cliente, o código será mais simples. No entanto, se você tiver uma lógica de pintura complicada, poderá ser mais eficiente ignorar as áreas fora da região de atualização.

A linha de código a seguir preenche a região de atualização com uma única cor, usando a cor da tela de fundo da janela definida pelo sistema **(COLOR \_ WINDOW).** A cor real indicada por **COLOR \_ WINDOW** depende do esquema de cores atual do usuário.

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

Os detalhes de [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) não são importantes para este exemplo, mas o segundo parâmetro fornece as coordenadas do retângulo a ser preenchida. Nesse caso, passamos toda a região de atualização (o membro **rcPaint** de [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)). Na primeira mensagem [**WM \_ PAINT,**](/windows/desktop/gdi/wm-paint) toda a área do cliente precisa ser pintada, **portanto, rcPaint** conterá toda a área do cliente. Em mensagens **WM \_ PAINT subsequentes,** **rcPaint** pode conter um retângulo menor.

A [**função FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) faz parte do Graphics Device Interface (GDI), que tem Windows gráficos por muito tempo. No Windows 7, a Microsoft introduziu um novo mecanismo gráfico, chamado Direct2D, que dá suporte a operações gráficas de alto desempenho, como aceleração de hardware. Direct2D também está disponível para o Windows Vista por meio da Atualização de Plataforma para [Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) e para o Windows Server 2008 por meio da Atualização de Plataforma para Windows Server 2008. (A GDI ainda tem suporte total.)

Depois de terminar a pintura, chame a [**função EndPaint.**](/windows/desktop/api/winuser/nf-winuser-endpaint) Essa função limpa a região de atualização, que sinaliza Windows que a janela concluiu a pintura em si.

## <a name="next"></a>Avançar

[Fechando a janela](closing-the-window.md)