---
title: Visão geral da API de ampliação
description: Este tópico descreve a API de ampliação e explica como usá-la em um aplicativo.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Amplia
- aplicativos de ampliação de tela
- Amplia
- processamento de imagem personalizada
- Magnification.dll
- criando controles de lupa
- ampliação seletiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105812428"
---
# <a name="magnification-api-overview"></a>Visão geral da API de ampliação

A API de ampliação permite que fornecedores de tecnologia assistencial desenvolvam aplicativos de ampliação de tela que são executados no Microsoft Windows. Este tópico descreve a API de ampliação e explica como usá-la em um aplicativo. Ele contém as seções a seguir:

- [Introdução](#getting-started)
- [Conceitos básicos](#basic-concepts)
  - [Tipos de lupas](#types-of-magnifiers)
  - [Fator de ampliação](#magnification-factor)
  - [Efeitos de cor](#color-effects)
  - [Retângulo de origem](#source-rectangle)
  - [Lista de filtros](#filter-list)
  - [Transformação de entrada](#input-transform)
  - [Cursor do sistema](#system-cursor)
- [Inicializando a biblioteca de tempo de execução da lupa](#initializing-the-magnifier-run-time-library)
- [Usando a Full-Screen lupa](#using-the-full-screen-magnifier)
- [Usando o controle lupa](#using-the-magnifier-control)
  - [Criando o controle lupa](#creating-the-magnifier-control)
  - [Inicializando o controle](#initializing-the-control)
  - [Configurando o retângulo de origem](#setting-the-source-rectangle)
  - [Aplicando efeitos de cor](#applying-color-effects)
  - [Ampliação seletiva](#selective-magnification)
- [Tópicos relacionados](#related-topics)

## <a name="getting-started"></a>Introdução

A versão original da API de ampliação tem suporte no Windows Vista e em sistemas operacionais posteriores. No Windows 8 e posterior, a API dá suporte a recursos adicionais, incluindo a ampliação de tela inteira e a definição da visibilidade do cursor do sistema ampliado.

O suporte para a API de ampliação é fornecido pelo Magnification.dll. Para compilar seu aplicativo, inclua ampliação. h e vincule a ampliação. lib.

> [!Note]  
> A API de ampliação não tem suporte no WOW64; ou seja, um aplicativo de lupa de 32 bits não será executado corretamente em janelas de 64 bits.

## <a name="basic-concepts"></a>Conceitos básicos

Esta seção descreve os conceitos fundamentais em que a API de ampliação se baseia. Ele contém as seguintes partes:

- [Tipos de lupas](#types-of-magnifiers)
- [Fator de ampliação](#magnification-factor)
- [Efeitos de cor](#color-effects)
- [Retângulo de origem](#source-rectangle)
- [Lista de filtros](#filter-list)
- [Transformação de entrada](#input-transform)
- [Cursor do sistema](#system-cursor)

### <a name="types-of-magnifiers"></a>Tipos de lupas

A API dá suporte a dois tipos de ampliadores, à *lupa em tela inteira* e ao *controle de lupa*. A lupa de tela inteira aumenta o conteúdo da tela inteira, enquanto o controle de lupa aumenta o conteúdo de uma área específica da tela e exibe o conteúdo em uma janela. Para Lupas, imagens e texto são ampliados e ambos permitem controlar a quantidade de ampliação. Você também pode aplicar efeitos de cor ao conteúdo da tela ampliado, facilitando a visualização para pessoas que têm deficiências de cor ou precisam de cores com mais ou menos contraste.

> [!Important]  
> A API de controle de lupa está disponível no Windows Vista e em sistemas operacionais posteriores, enquanto a API de lupa de tela inteira está disponível apenas no Windows 8 e em sistemas operacionais posteriores.

### <a name="magnification-factor"></a>Fator de ampliação

Tanto a lupa em tela inteira quanto o controle lupa aplicam uma transformação Scale ao conteúdo da tela de ampliação. A quantidade de ampliação aplicada pela transformação de escala é chamada de *fator de ampliação*. Ele é expresso como um valor de ponto flutuante em que 1,0 corresponde a sem ampliação e valores maiores resultam em uma quantidade correspondente de ampliação. Por exemplo, um valor de 1,5 torna o conteúdo da tela 50% maior. Um fator de ampliação menor que 1,0 não é válido.

### <a name="color-effects"></a>Efeitos de cor

Os efeitos de cor são obtidos com a aplicação de uma matriz de transformação de cor 5 por 5 às cores do conteúdo da tela ampliado. A matriz determina as intensidades dos componentes vermelho, azul, verde e alfa do conteúdo. Para obter mais informações, consulte [usando uma matriz de cores para transformar uma única cor](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) na documentação do Windows GDI+.

### <a name="source-rectangle"></a>Retângulo de origem

A lupa de tela inteira aplica a transformação de escala e a transformação de cores à tela inteira. O controle lupa, por outro lado, copia uma área da tela, chamada de *retângulo de origem*, para um bitmap fora da tela. Em seguida, o controle aplica a transformação escala e a transformação cor, se houver, ao bitmap fora da tela. Por fim, o controle exibe o bitmap escalado e transformado por cor na janela de controle da lupa.

### <a name="filter-list"></a>Lista de filtros

Por padrão, o controle lupa amplia todas as janelas no retângulo de origem especificado. No entanto, ao fornecer uma *lista de filtros* de identificadores de janela, você pode controlar quais janelas estão incluídas no conteúdo ampliado e quais não são. Para obter mais informações, consulte [ampliação seletiva](#selective-magnification).

A lupa de tela inteira não dá suporte a uma lista de filtros; sempre aumenta todas as janelas na tela.

### <a name="input-transform"></a>Transformação de entrada

Normalmente, o conteúdo da tela ampliado é "invisível" à caneta do usuário ou à entrada por toque. Por exemplo, se o usuário tocar na imagem ampliada de um controle, o sistema não passará necessariamente a entrada para o controle. Em vez disso, o sistema passa a entrada para qualquer item (se houver) que resida nas coordenadas de tela tocadas na área de trabalho não ampliada. A função [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) permite que você especifique uma *transformação de entrada* que mapeia o espaço de coordenadas do conteúdo da tela ampliado para o espaço de coordenadas de tela real (não ampliado). Isso permite que o sistema passe a entrada de caneta ou toque que é inserida no conteúdo da tela ampliado, para o elemento da interface do usuário correto na tela.

> [!Note]  
> O processo de chamada deve ter privilégios de UIAccess para definir a transformação de entrada. Para obter mais informações, consulte [considerações de segurança de automação da interface do usuário](../uiauto-securityoverview.md) e [/MANIFESTUAC (incorpora informações do UAC no manifesto)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).

### <a name="system-cursor"></a>Cursor do sistema

A função [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) permite mostrar ou ocultar o cursor do sistema. Se você mostrar o cursor do sistema quando a lupa de tela inteira estiver ativa, o cursor do sistema sempre será ampliado junto com o restante do conteúdo da tela. Se você ocultar o cursor do sistema quando a lupa de tela inteira estiver ativa, o cursor do sistema não estará visível.

Com o controle lupa, a função [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) mostra ou oculta o cursor do sistema não ampliado, mas não tem efeito sobre o cursor do sistema ampliado. A visibilidade do cursor do sistema ampliado depende se o controle de lupa tem o estilo de [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) . Se ele tiver esse estilo, o controle lupa exibirá o cursor do sistema ampliado, juntamente com o conteúdo da tela ampliada, sempre que o cursor do sistema entrar no retângulo de origem.

## <a name="initializing-the-magnifier-run-time-library"></a>Inicializando a biblioteca de tempo de execução da lupa

Antes de poder chamar qualquer outra função de API de lupa, você deve criar e inicializar os objetos de tempo de execução da lupa chamando a função [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) . Da mesma forma, depois de terminar de usar a API de lupa, chame a função [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) para destruir os objetos de tempo de execução da lupa e liberar os recursos do sistema associados.

## <a name="using-the-full-screen-magnifier"></a>Usando a Full-Screen lupa

Para usar a lupa de tela inteira, chame a função [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) . O parâmetro *magLevel* especifica o fator de ampliação. Os parâmetros *xOffset* e *yOffset* especificam como o conteúdo da tela ampliada é posicionado em relação à tela.

Quando o conteúdo da tela é ampliado, ele se torna maior do que a própria tela. Parte do conteúdo ultrapassa as bordas da tela e torna-se invisível para o usuário. Os parâmetros *xOffset* e *YOffset* da função [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) determinam qual parte do conteúdo da tela ampliada aparece na tela. Juntos, os parâmetros especificam as coordenadas de um ponto no conteúdo da tela não ampliada. Quando o conteúdo é ampliado, ele é posicionado com o ponto especificado no canto superior esquerdo da tela.

O exemplo a seguir define o fator de ampliação para a lupa de tela inteira e coloca o centro do conteúdo da tela ampliado no centro da tela.

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

Use a função [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) para aplicar efeitos de cor ao conteúdo de tela inteira definindo uma matriz de transformação de cor definida pelo aplicativo. Por exemplo, o exemplo a seguir define uma matriz de transformação de cor que converte cores em escala de cinza.

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

Você pode recuperar o fator de ampliação e os valores de deslocamento atuais chamando a função [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) . Você pode recuperar a matriz de transformação de cor atual chamando a função [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) .

## <a name="using-the-magnifier-control"></a>Usando o controle lupa

O controle lupa amplia o conteúdo de uma área específica da tela e exibe o conteúdo em uma janela. Esta seção descreve como usar o controle lupa. Ele contém as seguintes partes:

- [Criando o controle lupa](#creating-the-magnifier-control)
- [Inicializando o controle](#initializing-the-control)
- [Configurando o retângulo de origem](#setting-the-source-rectangle)
- [Aplicando efeitos de cor](#applying-color-effects)
- [Ampliação seletiva](#selective-magnification)

### <a name="creating-the-magnifier-control"></a>Criando o controle lupa

O controle lupa deve ser hospedado em uma janela criada com o estilo estendido [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) . Depois de criar a janela do host, chame [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) para definir a opacidade da janela do host. A janela do host é normalmente definida como opacidade total para evitar que o conteúdo da tela subjacente seja mostrado no entanto. O exemplo a seguir mostra como definir a janela do host para opacidade total:

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

Se você aplicar o estilo de [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) à janela do host, os cliques do mouse serão passados para qualquer objeto que esteja atrás da janela do host no local do cursor do mouse. Lembre-se de que, como a janela do host não processa cliques do mouse, o usuário não poderá mover ou redimensionar a janela de ampliação usando o mouse.

A classe Window da janela de controle lupa deve ser **WC_MAGNIFIER**. Se você aplicar o estilo de [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) , o controle lupa incluirá o cursor do sistema no conteúdo da tela ampliada e o cursor será ampliado junto com o conteúdo da tela.

Depois de criar o controle de lupa, mantenha o identificador de janela para que você possa passá-lo para outras funções.

O exemplo a seguir mostra como criar o controle lupa.

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a>Inicializando o controle

Depois de criar o controle lupa, você deve chamar a função [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) para especificar o fator de ampliação. Isso é simplesmente uma questão de especificar uma matriz de

(*n*, 0,0, 0,0)

(0,0, *n*, 0,0)

(0,0, 0,0, 1,0)

onde *n* é o fator de ampliação.

O exemplo a seguir mostra como definir o fator de ampliação para o controle lupa.

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a>Configurando o retângulo de origem

À medida que o usuário move o cursor do mouse pela tela, seu aplicativo chama a função [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) para especificar a parte da tela subjacente que será ampliada.

A função de exemplo a seguir calcula a posição e as dimensões do retângulo de origem (com base na posição do mouse e as dimensões da janela da lupa dividida pelo fator de ampliação) e define o retângulo de origem de acordo. A função também centraliza a área cliente da janela host na posição do mouse. Essa função seria chamada em intervalos para atualizar a janela de ampliação.

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a>Aplicando efeitos de cor

Um controle de lupa com o estilo [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) aplica uma matriz de transformação de cor interna que inverte as cores do conteúdo da tela ampliada. A ilustração a seguir mostra o conteúdo de tela em um controle de lupa que tem o estilo de **MS_INVERTCOLORS** .

![captura de tela do conteúdo ampliado com cores invertidas](images/color-inversion.png)

A função [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) permite que você aplique outros efeitos de cor configurando uma matriz de transformação de cor definida pelo aplicativo. Por exemplo, a função a seguir define uma matriz de transformação de cor que converte cores em escala de cinza.


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

Para obter mais informações sobre como funcionam as transformações de cores, consulte [usando uma matriz de cores para transformar uma única cor](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) na documentação do GDI+.

### <a name="selective-magnification"></a>Ampliação seletiva

Por padrão, a ampliação é aplicada a todas as janelas que não sejam a própria janela de ampliação. Para especificar quais janelas devem ser ampliadas, chame a função [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) . Esse método usa uma lista do Windows para ampliar ou uma lista de janelas a serem excluídas da ampliação.

## <a name="related-topics"></a>Tópicos relacionados

[API de ampliação](entry-magapi-sdk.md)