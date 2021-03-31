---
title: Exemplo de código de renderização
description: Exemplo de código de renderização
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- visualizações, código de exemplo
- visualizações personalizadas, código de exemplo
- visualizações, função render
- visualizações personalizadas, função render
- Função render, código de exemplo
- exemplos, processar função para visualizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005760"
---
# <a name="sample-render-code"></a>Exemplo de código de renderização

Aqui está um código de exemplo que usa a função **render** para desenhar uma linha na tela. A altura da linha é definida pelo valor de formato de onda.


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



A função **render** é onde ocorre o trabalho principal do seu código. Sempre que o Windows Media Player usar um instantâneo do áudio, ele chamará essa função e seu código será executado.

Esse código executa as seguintes tarefas. Consulte o SDK da plataforma Microsoft Windows para Windows de 32 bits para obter mais detalhes sobre funções específicas.

## <a name="creating-objects"></a>Criando objetos

Normalmente, você usará as funções de desenho que vêm com a interface gráfica de vídeo (GDI) do Microsoft Windows. Você precisa criar canetas para desenhar linhas e pincéis para preencher áreas.

Um pincel preto sólido é criado para preencher o plano de fundo.

Uma caneta sólida é criada para desenhar uma linha. A cor será a cor de primeiro plano, conforme definido pela capa que vai exibir a visualização.

## <a name="adding-the-object-to-the-dc"></a>Adicionando o objeto ao controlador de domínio

Você precisa adicionar a caneta ao contexto do dispositivo (DC). O DC é a parte da memória em que todos os dados e objetos de desenho são armazenados. Essencialmente, o DC é o Gerenciador de tráfego de janela que mantém o controle de tudo gráfico.

Você precisa *converter* o objeto de caneta criado e armazená-lo como uma caneta antiga. Use esta técnica de codificação para todas as novas canetas. Essa técnica é necessária para a programação de 32 bits.

## <a name="filling-in-the-background"></a>Preenchendo o plano de fundo

Agora você está pronto para desenhar. A função **FillRect** preencherá o retângulo da janela, conforme definido pelos parâmetros da função **render** . O retângulo é preenchido com um pincel preto.

## <a name="getting-audio-data"></a>Obtendo dados de áudio

Em seguida, o código obtém alguns dados de áudio do Windows Media Player. Usando a matriz de formato de onda, você pode obter o valor atual da energia de áudio no momento em que o instantâneo foi tirado. Nesse caso, você está pegando os dados de áudio do canal esquerdo. O primeiro valor na matriz é o primeiro 1024th do instantâneo de energia de áudio.

Essas informações serão usadas para exibir uma linha cuja altura corresponderá ao instantâneo de energia de áudio.

## <a name="draw-the-line"></a>Desenhar a linha

A linha é desenhada da esquerda para a direita usando as funções **MoveToEx** e **LineTo** GDI.

Primeiro, mova a caneta para o ponto de partida. Nesse caso, x e y são usados para definir os valores da esquerda para a direita e de cima para baixo que o usuário verá na tela. X é definido pelo retângulo PRC e especificamente pelo valor de PRC->esquerda. Y é definido como o valor dos dados da forma de onda nesse momento.

Em seguida, você desenha uma linha para o outro lado da janela. O ponto para o qual você desenha a linha é novamente um valor x, y. X é definido pelo retângulo PRC, mas desta vez por prc->direito. Y ainda é definido pelos dados de forma de onda e é o mesmo que o ponto de início, pois você está desenhando uma linha reta da esquerda para a direita.

## <a name="clean-up-everything"></a>Limpar tudo

Você deve excluir os objetos que criar. Especificamente, você deve excluir todos os pincéis e canetas que criar. É uma boa prática excluir canetas e pincéis quando você terminar de usá-las.

Se você não excluí-las antes de concluir a implementação da função **render** , sua visualização falhará em um minuto ou menos. Você deve manter uma contagem de canetas e pincéis e destruir cada uma delas. Tenha cuidado especialmente para não criar canetas dentro de um loop de código.

Use a técnica de codificação fornecida no exemplo para destruir suas canetas e pincéis.

-   **Importante** Destrua suas canetas e pincéis!

Quando terminar de limpar, não se esqueça de retornar S \_ OK para que o Windows Media Player saiba que você concluiu o desenho. Depois de concluir, o desenho será transferido para a janela, outro instantâneo será criado, o **processamento** solicitará que seu código desenhe novamente e assim por diante.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando renderização**](implementing-render.md)
</dt> </dl>

 

 




