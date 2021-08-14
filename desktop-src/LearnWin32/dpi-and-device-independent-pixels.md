---
title: DPI e Device-Independent pixels
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'Saiba mais sobre: DPI e Device-Independent pixels'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9b3aebca97ac466f5158b07d1d976994030b4ba2c83b361a5d7a6d88b572fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388334"
---
# <a name="dpi-and-device-independent-pixels"></a>DPI e Device-Independent pixels

para programar com eficiência com gráficos Windows, você deve entender dois conceitos relacionados:

-   Pontos por polegada (DPI)
-   Pixel independente de dispositivo (DIPs).

Vamos começar com DPI. Isso exigirá um breve desvio na tipografia. Na tipografia, o tamanho do tipo é medido em unidades chamadas *pontos*. Um ponto é igual a 1/72 de uma polegada.

<dl> 1 pt = 1/72 polegadas  
</dl>

> [!Note]  
> Esta é a definição do ponto de publicação de área de trabalho. Historicamente, a medida exata de um ponto variava.

 

Por exemplo, uma fonte de 12 pontos foi projetada para caber em uma linha de texto de 1/6 "(12/72). Obviamente, isso não significa que cada caractere na fonte é exatamente 1/6 "de altura. Na verdade, alguns caracteres podem ser mais altos que 1/6 ". Por exemplo, em muitas fontes, o caractere Å é mais alto que a altura nominal da fonte. Para exibir corretamente, a fonte precisa de algum espaço adicional entre o texto. Esse espaço é chamado de *entrelinha*.

A ilustração a seguir mostra uma fonte de ponto de 72. As linhas sólidas mostram uma "delimitadora de altura 1" em volta do texto. A linha tracejada é chamada de *linha de base*. A maioria dos caracteres em uma fonte é REST na linha de base. A altura da fonte inclui a parte acima da linha de base (a *ascendente*) e a parte abaixo da linha de base (o *descendente*). Na fonte mostrada aqui, o ascendente é de 56 pontos e o descendente é de 16 pontos.

![uma ilustração que mostra uma fonte de ponto de 72.](images/graphics11.png)

No entanto, quando se trata de uma exibição de computador, a medição do tamanho do texto é problemática, pois os pixels não têm o mesmo tamanho. O tamanho de um pixel depende de dois fatores: a resolução de vídeo e o tamanho físico do monitor. Portanto, as polegadas físicas não são uma medida útil, pois não há nenhuma relação fixa entre polegadas físicas e pixels. Em vez disso, as fontes são medidas em unidades *lógicas* . Uma fonte de ponto 72 é definida para ter uma polegada lógica de altura. Em seguida, as polegadas lógicas são convertidas em pixels. por muitos anos, Windows usou a seguinte conversão: uma polegada lógica é igual a 96 pixels. Usando esse fator de dimensionamento, uma fonte de ponto de 72 é renderizada como 96 pixels de altura. Uma fonte de 12 pontos tem 16 pixels de altura.

<dl> 12 pontos = 12/72 polegada lógica = 1/6 de polegada lógica = 96/6 pixels = 16 pixels  
</dl>

Esse fator de dimensionamento é descrito como 96 pontos por polegada (DPI). Os pontos de termo derivam da impressão, em que pontos físicos de tinta são colocados em papel. Para o computador ser exibido, seria mais preciso dizer 96 pixels por polegada lógica, mas o termo DPI travou.

Como os tamanhos de pixel reais variam, o texto legível em um monitor pode ser muito pequeno em outro monitor. Além disso, as pessoas têm preferências diferentes — algumas pessoas preferem texto maior. por esse motivo, Windows permite que o usuário altere a configuração de DPI. Por exemplo, se o usuário definir a exibição como 144 DPI, uma fonte de ponto 72 será de 144 pixels de altura. As configurações de DPI padrão são 100% (96 DPI), 125% (120 DPI) e 150% (144 DPI). O usuário também pode aplicar uma configuração personalizada. a partir do Windows 7, o DPI é uma configuração por usuário.

## <a name="dwm-scaling"></a>Dimensionamento do DWM

Se um programa não considerar DPI, os seguintes defeitos podem ser aparentes em configurações de alto DPI:

-   Elementos de interface do usuário recortados.
-   Layout incorreto.
-   Bitmaps e ícones pixelado.
-   Coordenadas incorretas do mouse, que podem afetar os testes de clique, arrastar e soltar e assim por diante.

Para garantir que os programas mais antigos funcionem em configurações de alto DPI, o DWM implementa um fallback útil. Se um programa não estiver marcado como tendo reconhecimento de DPI, o DWM dimensionará toda a interface do usuário para corresponder à configuração de DPI. Por exemplo, às 144 DPI, a interface do usuário é dimensionada por 150%, incluindo texto, elementos gráficos, controles e tamanhos de janelas. Se o programa criar uma janela 500 × 500, a janela aparecerá na verdade como 750 × 750 pixels e o conteúdo da janela será dimensionado de acordo.

Esse comportamento significa que os programas mais antigos "simplesmente funcionam" em configurações de alto DPI. No entanto, o dimensionamento também resulta em uma aparência um pouco borrada, pois o dimensionamento é aplicado depois que a janela é desenhada.

## <a name="dpi-aware-applications"></a>DPI-Aware aplicativos

Para evitar o dimensionamento do DWM, um programa pode se marcar como com reconhecimento de DPI. Isso diz ao DWM para não executar nenhum dimensionamento automático de DPI. Todos os novos aplicativos devem ser criados para reconhecer DPI, pois o reconhecimento de DPI melhora a aparência da interface do usuário em configurações de DPI mais altas.

Um programa declara a si mesmo o reconhecimento de DPI por meio de seu manifesto do aplicativo. Um *manifesto* é simplesmente um arquivo XML que descreve uma DLL ou um aplicativo. O manifesto normalmente é inserido no arquivo executável, embora possa ser fornecido como um arquivo separado. um manifesto contém informações como dependências de DLL, o nível de privilégio solicitado e a qual versão do Windows programa foi projetado.

Para declarar que o seu programa tem reconhecimento de DPI, inclua as seguintes informações no manifesto.

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

a listagem mostrada aqui é apenas um manifesto parcial, mas o vinculador Visual Studio gera o restante do manifesto para você automaticamente. Para incluir um manifesto parcial em seu projeto, execute as etapas a seguir em Visual Studio.

1.  no menu **Project** , clique em **propriedade**.
2.  No painel esquerdo, expanda **Propriedades de configuração**, expanda **ferramenta de manifesto** e clique em **entrada e saída**.
3.  Na caixa de texto **arquivos de manifesto adicionais** , digite o nome do arquivo de manifesto e clique em **OK**.

Ao marcar seu programa como reconhecimento de DPI, você está dizendo ao DWM para não dimensionar a janela do aplicativo. Agora, se você criar uma janela 500 × 500, a janela ocupará 500 × 500 pixels, independentemente da configuração de DPI do usuário.

## <a name="gdi-and-dpi"></a>GDI e DPI

O desenho GDI é medido em pixels. Isso significa que se o seu programa estiver marcado como reconhecimento de DPI e você solicitar que a GDI desenhe um retângulo de 200 × 100, o retângulo resultante terá 200 pixels de largura e 100 pixels de altura na tela. No entanto, os tamanhos de fonte GDI são dimensionados para a configuração de DPI atual. Em outras palavras, se você criar uma fonte de ponto 72, o tamanho da fonte será 96 pixels em 96 DPI, mas 144 pixels em 144 DPI. Aqui está uma fonte de 72 pontos renderizada em 144 DPI usando GDI.

![um diagrama que mostra o dimensionamento da fonte de DPI em GDI.](images/graphics12.png)

Se seu aplicativo reconhece DPI e você usa GDI para desenhar, dimensione todas as suas coordenadas de desenho para corresponder ao DPI.

## <a name="direct2d-and-dpi"></a>Direct2D e DPI

Direct2D executa automaticamente o dimensionamento para corresponder à configuração de DPI. em Direct2D, as coordenadas são medidas em unidades chamadas de DIPs ( *pixels independentes de dispositivo* ). Um DIP é definido como 1/1/96 de uma polegada *lógica* . em Direct2D, todas as operações de desenho são especificadas em DIPs e, em seguida, dimensionadas para a configuração de DPI atual.



| Configuração de DPI | Tamanho do DIP    |
|-------------|-------------|
| 96          | 1 pixel     |
| 120         | 1,25 pixels |
| 144         | 1,5 pixels  |



 

por exemplo, se a configuração de DPI do usuário for 144 DPI e você solicitar que Direct2D desenhe um retângulo 200 × 100, o retângulo será de 300 × 150 pixels físicos. além disso, DirectWrite mede os tamanhos de fonte em DIPs, em vez de pontos. Para criar uma fonte de 12 pontos, especifique 16 DIPs (12 pontos = 1/6 polegada lógica = 96/6 DIPs). quando o texto é desenhado na tela, Direct2D converte o DIPs em pixels físicos. O benefício desse sistema é que as unidades de medida são consistentes para o texto e o desenho, independentemente da configuração de DPI atual.

Uma palavra de cuidado: as coordenadas do mouse e da janela ainda são dadas em pixels físicos, não DIPs. Por exemplo, se você processar a mensagem do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) , a posição do mouse para baixo será fornecida em pixels físicos. Para desenhar um ponto nessa posição, você deve converter as coordenadas de pixel em DIPs.

## <a name="converting-physical-pixels-to-dips"></a>Convertendo pixels físicos em DIPs

A conversão de pixels físicos para DIPs usa a fórmula a seguir.

<dl> DIPs = pixels/(DPI/96.0)  
</dl>

Para obter a configuração de DPI, chame o método [**ID2D1Factory:: GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) . O DPI é retornado como dois valores de ponto flutuante, um para o eixo x e outro para o eixo y. Teoricamente, esses valores podem diferir. Calcule um fator de dimensionamento separado para cada eixo.


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



Aqui está uma maneira alternativa de obter a configuração de DPI se você não estiver usando Direct2D:


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> no Windows 10, a versão 1903, [**ID2D1Factory:: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) foi preterida e a recomendação é [**DisplayInformation:: LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) para aplicativos da loja Windows ou [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) para aplicativos da área de trabalho. Se você ainda quiser usá-lo, suprime a mensagem de erro do compilador escrevendo a linha [**#pragma Aviso (suprimir: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) logo antes da chamada [**ID2D1Factory:: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) . Embora não seja recomendado, é possível definir o reconhecimento de DPI padrão programaticamente usando [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext). Depois que uma janela (um HWND) tiver sido criada em seu processo, não haverá mais suporte para a alteração do modo de reconhecimento de DPI. Se você estiver configurando o modo de reconhecimento de DPI de processo padrão programaticamente, deverá chamar a API correspondente antes que quaisquer HWNDs tenham sido criados. Para obter informações, consulte [definindo o reconhecimento de DPI padrão para um processo](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).

## <a name="resizing-the-render-target"></a>Redimensionando o destino de renderização

Se o tamanho da janela for alterado, você deverá redimensionar o destino de renderização para corresponder. Na maioria dos casos, também será necessário atualizar o layout e redesenhar a janela. O código a seguir mostra essas etapas.


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



A função [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) Obtém o novo tamanho da área do cliente, em pixels físicos (não DIPs). O método [**ID2D1HwndRenderTarget:: Resize**](../direct2d/id2d1hwndrendertarget-resize.md) atualiza o tamanho do destino de renderização, também especificado em pixels. A função [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) força um redesenho adicionando toda a área do cliente à região de atualização da janela. (Consulte [pintando a janela](painting-the-window.md), no módulo 1.)

À medida que a janela aumenta ou diminui, normalmente, você precisará recalcular a posição dos objetos desenhados. Por exemplo, no programa de círculo, o raio e o ponto central devem ser atualizados:


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



O método [**ID2D1RenderTarget:: GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) retorna o tamanho do destino de renderização em DIPs (não pixels), que é a unidade apropriada para calcular o layout. Há um método fortemente relacionado, [**ID2D1RenderTarget:: Getpixelize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), que retorna o tamanho em pixels físicos. Para um destino de renderização **HWND** , esse valor corresponde ao tamanho retornado por [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect). Mas lembre-se de que o desenho é executado em DIPs, e não em pixels.

## <a name="next"></a>Avançar

[Usando a cor em Direct2D](using-color-in-direct2d.md)

 

 
