---
title: Renderizar Alvos, Dispositivos e Recursos
description: Renderizar Alvos, Dispositivos e Recursos
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293991"
---
# <a name="render-targets-devices-and-resources"></a>Renderizar Alvos, Dispositivos e Recursos

Um *destino de renderização* é simplesmente o local onde o programa será desenhado. Normalmente, o destino de renderização é uma janela (especificamente, a área cliente da janela). Também pode ser um bitmap na memória que não é exibido. Um destino de renderização é representado pela interface [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) .

Um *dispositivo* é uma abstração que representa o que realmente desenha os pixels. Um dispositivo de hardware usa a GPU para um desempenho mais rápido, enquanto que um dispositivo de software usa a CPU. O aplicativo não cria o dispositivo. Em vez disso, o dispositivo é criado implicitamente quando o aplicativo cria o destino de renderização. Cada destino de renderização é associado a um dispositivo específico, de hardware ou software.

![um diagrama que mostra a relação entre um destino de renderização e um dispositivo.](images/graphics09.png)

Um *recurso* é um objeto que o programa usa para desenhar. Aqui estão alguns exemplos de recursos que são definidos em Direct2D:

-   **Pincel**. Controla como as linhas e regiões são pintadas. Os tipos de pincel incluem pincéis de cor sólida e pincéis de gradiente.
-   **Estilo do traço**. Controla a aparência de uma linha, por exemplo, tracejada ou sólida.
-   **Geometry**. Representa uma coleção de linhas e curvas.
-   **Malha**. Uma forma formada fora dos triângulos. Os dados de malha podem ser consumidos diretamente pela GPU, ao contrário dos dados de geometria, que devem ser convertidos antes da renderização.

Os destinos de renderização também são considerados um tipo de recurso.

Alguns recursos se beneficiam da aceleração de hardware. Um recurso desse tipo é sempre associado a um dispositivo específico, hardware (GPU) ou software (CPU). Esse tipo de recurso é chamado *de dependente de dispositivo*. Pincéis e malhas são exemplos de recursos dependentes do dispositivo. Se o dispositivo ficar indisponível, o recurso deverá ser recriado para um novo dispositivo.

Outros recursos são mantidos na memória da CPU, independentemente de qual dispositivo é usado. Esses recursos são *independentes de dispositivo*, pois não estão associados a um dispositivo específico. Não é necessário recriar recursos independentes de dispositivo quando o dispositivo é alterado. Estilos e geometrias de traço são recursos independentes de dispositivo.

A documentação do MSDN para cada recurso informa se o recurso é dependente de dispositivo ou independente de dispositivo. Cada tipo de recurso é representado por uma interface que deriva de [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource). Por exemplo, os pincéis são representados pela interface [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) .

## <a name="the-direct2d-factory-object"></a>O objeto de fábrica Direct2D

A primeira etapa ao usar Direct2D é criar uma instância do objeto de fábrica Direct2D. Na programação de computador, uma *fábrica* é um objeto que cria outros objetos. A fábrica Direct2D cria os seguintes tipos de objetos:

-   Processar destinos.
-   Recursos independentes de dispositivo, como estilos de traço e geometrias.

Recursos dependentes do dispositivo, como pincéis e bitmaps, são criados pelo objeto de destino render.

![um diagrama que mostra a fábrica Direct2D.](images/graphics10.png)

Para criar o objeto de fábrica Direct2D, chame a função [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



O primeiro parâmetro é um sinalizador que especifica as opções de criação. O sinalizador de **\_ \_ \_ \_ thread único do tipo de fábrica d2d1** significa que você não chamará Direct2D de vários threads. Para dar suporte a chamadas de vários threads, especifique o **tipo de fábrica d2d1 com \_ \_ \_ vários \_ threads**. Se o seu programa usar um único thread para chamar o Direct2D, a opção de thread único será mais eficiente.

O segundo parâmetro para a função [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) recebe um ponteiro para a interface [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) .

Você deve criar o objeto de fábrica Direct2D antes da primeira mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) . O manipulador de [**\_ criação**](/windows/desktop/winmsg/wm-create) de mensagem do WM é um bom local para criar a fábrica:


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a>Criando recursos do Direct2D

O programa Circle usa os seguintes recursos dependentes do dispositivo:

-   Um destino de renderização associado à janela do aplicativo.
-   Um pincel de cor sólida para pintar o círculo.

Cada um desses recursos é representado por uma interface COM:

-   A interface [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) representa o destino de renderização.
-   A interface [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) representa o pincel.

O programa Circle armazena ponteiros para essas interfaces como variáveis de membro da `MainWindow` classe:


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



O código a seguir cria esses dois recursos.


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



Para criar um destino de renderização para uma janela, chame o método [**ID2D1Factory:: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) na fábrica Direct2D.

-   O primeiro parâmetro especifica opções que são comuns a qualquer tipo de destino de renderização. Aqui, passamos as opções padrão chamando a função auxiliar [**d2d1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).
-   O segundo parâmetro especifica o identificador para a janela mais o tamanho do destino de renderização, em pixels.
-   O terceiro parâmetro recebe um ponteiro [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) .

Para criar o pincel de cor sólida, chame o método [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) no destino de renderização. A cor é fornecida como um [**valor \_ \_ F de cor d2d1**](/windows/desktop/Direct2D/d2d1-color-f) . Para obter mais informações sobre cores em Direct2D, consulte [usando a cor em Direct2D](using-color-in-direct2d.md).

Além disso, observe que, se o destino de renderização já existir, o `CreateGraphicsResources` método retornará **S \_ OK** sem fazer nada. O motivo para esse design ficará claro no próximo tópico.

## <a name="next"></a>Avançar

[Desenhar com Direct2D](drawing-with-direct2d.md)

 

 