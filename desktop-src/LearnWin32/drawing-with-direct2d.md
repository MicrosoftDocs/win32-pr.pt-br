---
title: Desenhar com Direct2D
description: Depois de criar seus recursos gráficos, você estará pronto para desenhar.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d8a346300b32fe1c716e51efe6bfb8fdbf6220fb2ff17df6de617de27ba1a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535067"
---
# <a name="drawing-with-direct2d"></a>Desenhar com Direct2D

Depois de criar seus recursos gráficos, você estará pronto para desenhar.

## <a name="drawing-an-ellipse"></a>Desenhando uma elipse

O programa [Circle](your-first-direct2d-program.md) executa uma lógica de desenho muito simples:

1.  Preencha o plano de fundo com uma cor sólida.
2.  Desenhe um círculo preenchido.

![uma captura de tela do programa de círculo.](images/graphics08.png)

Como o destino de renderização é uma janela (em oposição a um bitmap ou outra superfície fora da tela), o desenho é feito em resposta às mensagens do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) . O código a seguir mostra o procedimento de janela para o programa de círculo.


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

Este é o código que desenha o círculo.

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



A interface [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) é usada para todas as operações de desenho. O método do programa `OnPaint` faz o seguinte:

1.  O método [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) sinaliza o início do desenho.
2.  O método [**ID2D1RenderTarget:: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) preenche todo o destino de renderização com uma cor sólida. A cor é fornecida como uma [**estrutura \_ \_ F de cor d2d1**](/windows/desktop/Direct2D/d2d1-color-f) . Você pode usar a classe [**d2d1:: colorf**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) para inicializar a estrutura. Para obter mais informações, consulte [usando a cor em Direct2D](using-color-in-direct2d.md).
3.  O método [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) desenha uma elipse preenchida, usando o pincel especificado para o preenchimento. Uma elipse é especificada por um ponto central e o raios x e y. Se o raios x e y forem os mesmos, o resultado será um círculo.
4.  O método [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) sinaliza a conclusão do desenho para este quadro. Todas as operações de desenho devem ser colocadas entre as chamadas para [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e **EndDraw**.

Todos os métodos [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)e [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) têm um tipo de retorno **void** . Se ocorrer um erro durante a execução de qualquer um desses métodos, o erro será sinalizado pelo valor de retorno do método [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . o `CreateGraphicsResources` método é mostrado no tópico [criando Direct2D recursos](render-targets--devices--and-resources.md). Esse método cria o destino de renderização e o pincel de cor sólida.

O dispositivo pode armazenar em buffer os comandos de desenho e adiar sua execução até que o [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) seja chamado. Você pode forçar o dispositivo a executar qualquer comando de desenho pendente chamando [**ID2D1RenderTarget:: flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush). No entanto, a liberação pode reduzir o desempenho.

## <a name="handling-device-loss"></a>Lidando com a perda de dispositivo

Enquanto o programa está em execução, o dispositivo de gráficos que você está usando pode se tornar indisponível. Por exemplo, o dispositivo poderá ser perdido se a resolução de vídeo for alterada ou se o usuário remover o adaptador de vídeo. Se o dispositivo for perdido, o destino de renderização também se tornará inválido, juntamente com todos os recursos dependentes do dispositivo que foram associados ao dispositivo. Direct2D sinaliza um dispositivo perdido retornando o código de erro **D2DERR \_ recriar \_ destino** do método [**enddraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Se você receber esse código de erro, deverá recriar o destino de renderização e todos os recursos dependentes do dispositivo.

Para descartar um recurso, basta liberar a interface para esse recurso.


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



A criação de um recurso pode ser uma operação cara, portanto, não recrie seus recursos para todas as mensagens do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) . Crie um recurso uma vez e armazene o ponteiro do recurso em cache até que o recurso se torne inválido devido à perda do dispositivo ou até que você não precise mais desse recurso.

## <a name="the-direct2d-render-loop"></a>o Loop de renderização de Direct2D

Independentemente do que você desenhar, o programa deve executar um loop semelhante ao seguinte.

1.  Crie recursos independentes de dispositivo.
2.  Renderizar a cena.
    1.  Verifique se existe um destino de renderização válido. Caso contrário, crie o destino de renderização e os recursos dependentes do dispositivo.
    2.  Chame [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).
    3.  Emitir comandos de desenho.
    4.  Chame [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).
    5.  Se [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) retornar **D2DERR \_ recriar \_ destino**, descarte os recursos de destino de renderização e dependentes do dispositivo.
3.  Repita a etapa 2 sempre que precisar atualizar ou redesenhar a cena.

Se o destino de renderização for uma janela, a etapa 2 ocorrerá sempre que a janela receber uma mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) .

O loop mostrado aqui lida com a perda do dispositivo descartando os recursos dependentes do dispositivo e recriando-os no início do próximo loop (etapa 2a).

## <a name="next"></a>Avançar

[DPI e Device-Independent pixels](dpi-and-device-independent-pixels.md)

 

 