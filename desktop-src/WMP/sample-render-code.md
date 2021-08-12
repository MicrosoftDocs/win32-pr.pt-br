---
title: Código de renderização de exemplo
description: Código de renderização de exemplo
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- visualizações, código de exemplo
- visualizações personalizadas, código de exemplo
- visualizações, função Renderizar
- visualizações personalizadas, função Renderizar
- Função renderizar, código de exemplo
- samples,Render function for visualizations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51265191ba7fd8b5eb9e4b1140990a7713eba08356d01c58097c727ec2fe533e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569782"
---
# <a name="sample-render-code"></a>Código de renderização de exemplo

Aqui está um código de exemplo que usa a **função Render** para desenhar uma linha na tela. A altura da linha é definida pelo valor waveform.


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



A **função Render** é o local em que o trabalho principal do seu código ocorre. Sempre que Windows Media Player tirar um instantâneo do áudio, ele chamará essa função e seu código será executado.

Esse código executa as tarefas a seguir. Consulte o SDK do Microsoft Windows Platform para 32 bits Windows para obter mais detalhes sobre funções específicas.

## <a name="creating-objects"></a>Criando objetos

Normalmente, você estará usando as funções de desenho que vêm com a GDI (Interface de Exibição Gráfica) do Microsoft Windows. Você precisa criar canetas para desenhar linhas e pincéis para preencher áreas.

Um pincel preto sólido é criado para preencher a plano de fundo.

Uma caneta sólida é criada para desenhar uma linha. A cor será a cor de primeiro plano, conforme definido pela capa que exibirá a visualização.

## <a name="adding-the-object-to-the-dc"></a>Adicionando o objeto ao DC

Você precisa adicionar a caneta ao DC (contexto do dispositivo). O DC é a parte da memória em que todos os dados de desenho e objetos são armazenados. Essencialmente, o DC é o gerenciador de tráfego de janela que acompanha tudo gráfico.

Você precisa lançar *o* objeto de caneta criado e armazená-lo como uma caneta antiga. Use essa técnica de codificação para todas as novas canetas. Essa técnica é necessária para programação de 32 bits.

## <a name="filling-in-the-background"></a>Preenchendo a segundo plano

Agora você está pronto para desenhar. A **função FillRect** preencherá o retângulo da janela, conforme definido pelos parâmetros da função **Renderizar.** O retângulo é preenchido com um pincel preto.

## <a name="getting-audio-data"></a>Obter dados de áudio

Em seguida, o código obtém alguns dados de áudio Windows Media Player. Usando a matriz waveform, você pode obter o valor atual da potência de áudio no momento em que o instantâneo foi tirado. Nesse caso, você está levando os dados de áudio do canal esquerdo. O primeiro valor na matriz é o primeiro 1024º do instantâneo de energia de áudio.

Essas informações serão usadas para exibir uma linha cuja altura corresponderá ao instantâneo de energia de áudio.

## <a name="draw-the-line"></a>Estabelecer o limite

A linha é desenhada da esquerda para a direita usando as **funções MoveToEx** **e LineTo** GDI.

Primeiro, mova a caneta para o ponto de partida. Nesse caso, x e y são usados para definir os valores da esquerda para a direita e de cima para baixo que o usuário verá na tela. X é definido pelo retângulo prc e especificamente pelo valor de prc->esquerda. Y é definido como o valor dos dados de forma de onda nesse momento.

Em seguida, você desenha uma linha para o outro lado da janela. O ponto para o que você desenha a linha é novamente um valor x, y. X é definido pelo retângulo prc, mas desta vez por prc->direita. Y ainda é definido pelos dados de forma de onda e é o mesmo que o ponto de partida, porque você está desenhando uma linha reta da esquerda para a direita.

## <a name="clean-up-everything"></a>Limpar tudo

Você deve excluir os objetos que criar. Especificamente, você deve excluir todos os pincéis e canetas criados. É uma boa prática excluir canetas e pincéis quando você terminar de usá-las.

Se você não excluí-los antes de concluir a implementação da **função Renderizar,** sua visualização falhará em um minuto ou menos. Você deve manter uma contagem de canetas e pincéis e destruir cada uma delas. Tenha especialmente cuidado para não criar canetas dentro de um loop de código.

Use a técnica de codificação determinada no exemplo para destruir suas canetas e pincéis.

-   **Importante** Destruir suas canetas e pincéis!

Quando terminar de limpar, certifique-se de retornar S OK para que Windows Media Player \_ que você tenha terminado de desenhar. Depois de concluir, o desenho será transferido para a janela, outro instantâneo será tirado, **Renderizar** solicitará que seu código desenheça novamente e assim por diante.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando renderização**](implementing-render.md)
</dt> </dl>

 

 




