---
title: Pintando a janela
description: Você criou sua janela. Agora você deseja mostrar algo dentro dele. Na terminologia do Windows, isso é chamado de pintura da janela. Para misturar metáforas, uma janela é uma tela em branco, esperando que você a preencha.
ms.assetid: db97a4c9-7592-42d1-a5de-9c468169eefc
ms.topic: article
ms.date: 08/16/2019
ms.openlocfilehash: f0f9d5c2759ea1735e370eb258743364980daee8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104567073"
---
# <a name="painting-the-window"></a>Pintando a janela

Você criou sua janela. Agora você deseja mostrar algo dentro dele. Na terminologia do Windows, isso é chamado de pintura da janela. Para misturar metáforas, uma janela é uma tela em branco, esperando que você a preencha.

Às vezes, o programa começará a pintar para atualizar a aparência da janela. Em outras ocasiões, o sistema operacional o notificará de que você deve redesenhar uma parte da janela. Quando isso ocorre, o sistema operacional envia a janela uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) . A parte da janela que deve ser pintada é chamada de *região de atualização*.

Na primeira vez em que uma janela é mostrada, toda a área do cliente da janela deve ser pintada. Portanto, você sempre receberá pelo menos uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) quando mostrar uma janela.

![ilustração mostrando a região de atualização de uma janela](images/painting01.png)

Você só é responsável por pintar a área do cliente. O quadro ao redor, incluindo a barra de título, é pintado automaticamente pelo sistema operacional. Depois de terminar a pintura da área do cliente, desmarque a região de atualização, que informa ao sistema operacional que ele não precisa enviar outra mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) até que algo seja alterado.

Agora suponha que o usuário mova outra janela para que ela oculte uma parte da sua janela. Quando a parte obscurecida se tornar visível novamente, essa parte será adicionada à região de atualização e sua janela receberá outra mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) .

![ilustração que mostra como a região de atualização muda quando duas janelas se sobrepõem](images/painting02.png)

A região de atualização também será alterada se o usuário alongar a janela. No diagrama a seguir, o usuário alonga a janela para a direita. A área exposta recentemente no lado direito da janela é adicionada à região de atualização:

![ilustração que mostra como a região de atualização é alterada quando uma janela é redimensionada](images/painting03.png)

Em nosso primeiro programa de exemplo, a rotina de pintura é muito simples. Ele apenas preenche toda a área do cliente com uma cor sólida. Ainda assim, esse exemplo é suficiente para demonstrar alguns dos conceitos importantes.

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

Inicie a operação de pintura chamando a função [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) . Essa função preenche a estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) com informações sobre a solicitação Repaint. A região de atualização atual é fornecida no membro **rcPaint** de **PAINTSTRUCT**. Essa região de atualização é definida em relação à área do cliente:

![ilustração mostrando a origem da área do cliente](images/painting04.png)

No seu código de pintura, você tem duas opções básicas:

- Pinte toda a área do cliente, independentemente do tamanho da região de atualização. Qualquer coisa que esteja fora da região de atualização é recortada. Ou seja, o sistema operacional o ignora.
- Otimizar pintando apenas a parte da janela dentro da região de atualização.

Se você sempre pintar toda a área do cliente, o código será mais simples. No entanto, se você tiver uma lógica de pintura complicada, poderá ser mais eficiente ignorar as áreas fora da região de atualização.

A linha de código a seguir preenche a região de atualização com uma única cor, usando a cor de plano de fundo da janela definida pelo sistema (**\_ janela de cores**). A cor real indicada pela **\_ janela de cores** depende do esquema de cores atual do usuário.

```C++
FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
```

Os detalhes de [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) não são importantes para este exemplo, mas o segundo parâmetro fornece as coordenadas do retângulo a preencher. Nesse caso, passamos toda a região de atualização (o membro **rcPaint** de [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)). Na primeira mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , toda a área do cliente precisa ser pintada, portanto, **rcPaint** conterá toda a área do cliente. Em mensagens **de \_ pintura do WM** subsequentes, **rcPaint** pode conter um retângulo menor.

A função [**FillRect**](/windows/desktop/api/winuser/nf-winuser-fillrect) faz parte do Graphics Device Interface (GDI), que tem gráficos do Windows alimentados por muito tempo. No Windows 7, a Microsoft introduziu um novo mecanismo de gráficos, chamado Direct2D, que dá suporte a operações gráficas de alto desempenho, como aceleração de hardware. O Direct2D também está disponível para o Windows Vista por meio da [atualização de plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md) e windows Server 2008 por meio da atualização de plataforma para o windows Server 2008. (A GDI ainda tem suporte total.)

Depois de terminar a pintura, chame a função [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) . Essa função limpa a região de atualização, que sinaliza ao Windows que a janela concluiu a pintura em si.

## <a name="next"></a>Avançar

[Fechando a janela](closing-the-window.md)