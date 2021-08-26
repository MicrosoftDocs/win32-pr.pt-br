---
title: Inverter Modelo, retângulos sujos, áreas roladas
description: DXGI 1,2 dá suporte a uma nova cadeia de permuta de flip-Model, retângulos sujos e áreas roladas. Explicamos os benefícios de usar a nova cadeia de permuta de flip-Model e de otimizar a apresentação especificando retângulos sujos e áreas roladas.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f191af4a94b1379e2539b8d544163467fe4dc49141f244e8dcc1f13a3e36af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984197"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a>Inverter Modelo, retângulos sujos, áreas roladas

DXGI 1,2 dá suporte a uma nova cadeia de permuta de flip-Model, retângulos sujos e áreas roladas. Explicamos os benefícios de usar a nova cadeia de permuta de flip-Model e de otimizar a apresentação especificando retângulos sujos e áreas roladas.

## <a name="dxgi-flip-model-presentation"></a>Apresentação de modelo de flip-DXGI

DXGI 1,2 adiciona suporte para o modelo de apresentação de flip para Direct3D 10 e APIs posteriores. no Windows 7, o Direct3D 9ex primeiro adotou a [apresentação de flip-model](../direct3darticles/direct3d-9ex-improvements.md) para evitar copiar desnecessariamente o buffer da cadeia de permuta. Usando o modelo de flip, buffers de fundo são invertidos entre o tempo de execução e o Gerenciador de Janelas da Área de Trabalho (DWM), portanto o DWM sempre compõe diretamente do buffer de fundo em vez de copiar o conteúdo do buffer de fundo.

As APIs DXGI 1,2 incluem uma interface da cadeia de permuta DXGI revisada, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1). Você pode usar vários métodos de interface [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) para criar o objeto **IDXGISwapChain1** apropriado a ser usado com um identificador [**HWND**](../winprog/windows-data-types.md) , um objeto [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) , [DirectComposition](../directcomp/directcomposition-portal.md)ou o [**Windows. Conectável. Estrutura XAML**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) .

Selecione o modelo de apresentação inverter especificando o valor de enumeração [**\_ \_ \_ \_ seqüencial de inverter efeito de permuta dxgi**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) no membro **SwapEffect** da estrutura [**DESC1 da cadeia de \_ permuta \_ \_ dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) e definindo o membro **BufferCount** da **cadeia de permuta de dxgi \_ \_ \_ DESC1** para um mínimo de 2. Para obter mais informações sobre como usar o modelo de flip DXGI, consulte [modelo de flip-dxgi](dxgi-flip-model.md). Devido à apresentação mais suave do modelo de apresentação invertida e outras funcionalidades novas, recomendamos que você use o modelo de apresentação de flip para todos os novos aplicativos que você escreve com o Direct3D 10 e as APIs posteriores.

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a>Usando retângulos sujos e o retângulo de rolagem na apresentação da cadeia de permuta

Usando retângulos sujos e o retângulo de rolagem na apresentação da cadeia de permuta, você economiza o uso da largura de banda da memória e o uso relacionado da energia do sistema, pois a quantidade de dados de pixel que o sistema operacional precisa para desenhar o próximo quadro apresentado será reduzida se o sistema operacional não precisar desenhar o quadro inteiro. Para aplicativos que são frequentemente exibidos por meio de Conexão de Área de Trabalho Remota e outras tecnologias de acesso remoto, as economias são particularmente perceptíveis na qualidade da tela, pois essas tecnologias usam retângulos sujos e rolam metadados.

Você pode usar a rolagem somente com cadeias de permuta DXGI que são executadas no modelo de apresentação de flip. Você pode usar retângulos sujos com cadeias de permuta DXGI que são executados no modelo de flip e BitBlt (definido com [**\_ \_ \_ sequencial de efeito de permuta dxgi**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).

Neste cenário e ilustração, mostramos a funcionalidade de usar retângulos sujos e rolar. Aqui, um aplicativo rolável contém texto e animação de vídeo. O aplicativo usa retângulos sujos para apenas atualizar o vídeo de animação e a nova linha para a janela, em vez de atualizar a janela inteira. O retângulo de rolagem permite que o sistema operacional Copie e traduza o conteúdo renderizado anteriormente no novo quadro e processe apenas a nova linha no novo quadro.

O aplicativo executa a apresentação chamando o método [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . Nesta chamada, o aplicativo passa um ponteiro para uma estrutura [**de \_ \_ parâmetros presente de dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) que inclui retângulos sujos e o número de retângulos sujos, ou o retângulo de rolagem e o deslocamento de rolagem associado, ou ambos os retângulos sujos e o retângulo de rolagem. Nosso aplicativo passa 2 retângulos sujos e o retângulo de rolagem. O retângulo de rolagem é a área do quadro anterior que o sistema operacional precisa copiar para o quadro atual antes de renderizar o quadro atual. O aplicativo especifica o vídeo animador e a nova linha como retângulos sujos, e o sistema operacional os renderiza no quadro atual.

![ilustração de sobreposição de retângulos de rolagem e sujos](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

O retângulo tracejado mostra o retângulo de rolagem no quadro atual. O retângulo de rolagem é especificado pelo membro **pScrollRect** dos [**\_ \_ parâmetros presentes de dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters). A seta mostra o deslocamento de rolagem. O deslocamento de rolagem é especificado pelo membro **pScrollOffset** dos **\_ \_ parâmetros presentes de dxgi**. Os retângulos preenchidos mostram os retângulos sujos que o aplicativo atualizou com o novo conteúdo. Os retângulos preenchidos são especificados pelos membros **DirtyRectsCount** e **pDirtyRects** dos **\_ \_ parâmetros presentes de dxgi**.

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a>Exemplo 2-cadeia de permuta de modelo invertida de buffer com retângulos sujos e retângulo de rolagem

A próxima ilustração e sequência mostra um exemplo de uma operação de apresentação de flip-Model DXGI que usa retângulos sujos e um retângulo de rolagem. Neste exemplo, usamos o número mínimo de buffers para apresentação de flip-Model, que é uma contagem de buffer de dois, um buffer frontal que contém o conteúdo de exibição do aplicativo e um buffer de fundo que contém o quadro atual que o aplicativo deseja renderizar.

1.  Conforme mostrado no buffer frontal no início do quadro, o aplicativo rolável inicialmente mostra um quadro com um vídeo de texto e animação.
2.  Para renderizar o próximo quadro, o aplicativo é renderizado no buffer de fundo os retângulos sujos que atualizam o vídeo de animação e a nova linha para a janela.
3.  Quando o aplicativo chama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), ele especifica os retângulos sujos e o retângulo de rolagem e o deslocamento. Em seguida, o tempo de execução copia o retângulo de rolagem do quadro anterior menos os retângulos sujos atualizados para o buffer de fundo atual.
4.  O tempo de execução finalmente permuta os buffers frontal e traseiro.

![exemplo de cadeia de permuta de flip-Model com retângulos de rolagem e sujos](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a>Acompanhamento de retângulos com problemas e retângulos de rolagem em vários quadros

Ao usar retângulos sujos em seu aplicativo, você deve acompanhar os retângulos sujos para dar suporte à renderização incremental. Quando seu aplicativo chama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) com retângulos sujos, você deve garantir que cada pixel dentro dos retângulos sujos esteja atualizado. Se você não estiver reprocessando completamente toda a área do retângulo sujo ou se não puder saber para determinadas áreas sujos, deverá copiar alguns dados do buffer de fundo totalmente coerente anterior para o buffer de fundo atual e obsoleto antes de iniciar a renderização.

O tempo de execução copia apenas as diferenças entre as áreas atualizadas do quadro anterior e as áreas atualizadas do quadro atual para o buffer de fundo atual. Se essas áreas se interseccionarem, o tempo de execução copiará apenas a diferença entre elas. Como você pode ver no diagrama e na sequência a seguir, você deve copiar a interseção entre o retângulo sujo do quadro 1 e o retângulo sujo do quadro 2 para o retângulo sujo do quadro 2.

1.  Há um retângulo sujo no quadro 1.
2.  Copie a interseção entre o retângulo sujo do quadro 1 e o retângulo sujo do quadro 2 para o retângulo sujo do quadro 2.
3.  Há um retângulo sujo no quadro 2.

![acompanhamento de retângulos de rolagem e sujos em vários quadros](images/track-dirty-rects-scroll-rects.png)

Para generalizar, para uma cadeia de permuta com N buffers, a área em que o tempo de execução copia do último quadro para o quadro atual no presente do quadro atual é:

![equação para calcular a área em que o tempo de execução copia](images/runtime-copy-equation.png)

em que buffer indica o índice de buffer em uma cadeia de permuta, começando com o índice de buffer atual em zero.

Você pode manter o controle de todas as interseções entre o quadro anterior e os retângulos sujos do quadro atual mantendo uma cópia dos retângulos sujos do quadro anterior ou renderizando novamente os retângulos sujos do novo quadro com o conteúdo apropriado do quadro anterior.

Da mesma forma, nos casos em que a cadeia de permuta tem mais de 2 buffers de fundo, você deve garantir que as áreas sobrepostas entre os retângulos sujos do buffer atual e os retângulos sujos de todos os quadros anteriores sejam copiados ou reprocessados.

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a>Acompanhamento de uma única interseção entre 2 retângulos sujos

No caso mais simples, quando você atualiza um único retângulo sujo por quadro, os retângulos sujos em dois quadros podem se Interseccionar. Para descobrir se o retângulo sujo do quadro anterior e o retângulo sujo do quadro atual se sobrepõem, você precisa verificar se o retângulo sujo do quadro anterior está interseccionado com o retângulo sujo do quadro atual. Você pode chamar a função [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) do GDI para determinar se duas estruturas [**Rect**](/previous-versions//dd162897(v=vs.85)) que representam os dois retângulos sujos se cruzam.

Nesse trecho de código, uma chamada para [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) retorna a interseção de dois retângulos sujos em outro [**Rect**](/previous-versions//dd162897(v=vs.85)) chamado dirtyRectCopy. Depois que o trecho de código determina que os dois retângulos sujos se cruzam, ele chama o método [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) para copiar a região da interseção no quadro atual.

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

Se você usar esse trecho de código em seu aplicativo, o aplicativo estará pronto para chamar [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para atualizar o quadro atual com o retângulo sujo atual.

### <a name="tracking-intersections-between-n-dirty-rectangles"></a>Acompanhamento de interseções entre N retângulos sujos

Se você especificar vários retângulos sujos, que podem incluir um retângulo sujo para a linha de rolagem recentemente revelada, por quadro, você precisará verificar e rastrear as sobreposições que podem ocorrer entre todos os retângulos sujos do quadro anterior e todos os retângulos sujos do quadro atual. Para calcular as interseções entre os retângulos sujos do quadro anterior e os retângulos sujos do quadro atual, você pode agrupar os retângulos sujos em regiões.

Neste trecho de código, chamamos a função [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) do GDI para converter cada retângulo sujo em uma região retangular e, em seguida, chamamos a função [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) do GDI para combinar todas as regiões retangulares sujas em um grupo.

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

Agora você pode usar a função [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) do GDI para determinar a interseção entre a região suja do quadro anterior e a região suja do quadro atual. Depois de obter a região de interseção, chame a função [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) do GDI para obter cada retângulo individual da região de interseção e, em seguida, chame o método [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) para copiar cada retângulo de interseção no buffer de fundo atual. O próximo trecho de código mostra como usar essas funções GDI e Direct3D.

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a>Cadeia de troca de modelo BitBlt com retângulos sujos

Você pode usar retângulos sujos com cadeias de permuta DXGI que são executados no modelo BitBlt (definido com [**\_ \_ \_ sequencial de efeito de permuta dxgi**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)). As cadeias de troca de modelo BitBlt que usam mais de um buffer também devem controlar os retângulos sujos sobrepostos entre quadros da mesma maneira como descrito em [acompanhamento de retângulos sujos e retângulos de rolagem em vários quadros](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) para cadeias de troca de modelo de flip. Cadeias de troca de modelo BitBlt com apenas um buffer não precisam rastrear retângulos sujos sobrepostos porque todo o buffer é redesenhado a cada quadro.

## <a name="related-topics"></a>Tópicos relacionados

[Aprimoramentos de DXGI 1,2](dxgi-1-2-improvements.md)
