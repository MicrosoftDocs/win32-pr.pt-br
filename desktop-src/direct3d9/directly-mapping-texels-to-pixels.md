---
description: Ao renderizar a saída 2D usando vértices pré-transformados, é necessário ter cuidado para garantir que cada área de texel corresponda corretamente a uma única área de pixel, caso contrário, poderá ocorrer distorção de textura.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Mapeando diretamente os Texels para Pixels (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7294b88fb8b672aea980dbb23cb4e7c5bbd2bfdbf4d33a5078a09dbfa3084d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988213"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a>Mapeando diretamente os Texels para Pixels (Direct3D 9)

Ao renderizar a saída 2D usando vértices pré-transformados, é necessário ter cuidado para garantir que cada área de texel corresponda corretamente a uma única área de pixel, caso contrário, poderá ocorrer distorção de textura. Ao entender os conceitos básicos do processo que o Direct3D segue ao rasterizar e fazer textização de triângulos, você pode garantir que seu aplicativo Direct3D renderiza corretamente a saída 2D.

![ilustração de uma exibição de resolução 6x6](images/maptex-fig1.png)

O diagrama anterior mostra pixels modelados como quadrados. Na realidade, no entanto, pixels são pontos, não quadrados. Cada quadrado no diagrama anterior indica a área iluminada pelo pixel, mas um pixel é sempre apenas um ponto no centro de um quadrado. Essa distinção, embora aparentemente pequena, é importante. Uma ilustração melhor da mesma exibição é mostrada no diagrama a seguir.

![ilustração de uma exibição que consiste em pixels](images/maptex-fig2.png)

O diagrama anterior mostra corretamente cada pixel físico como um ponto no centro de cada célula. A coordenada de espaço da tela (0, 0) está localizada diretamente no pixel superior esquerdo e, portanto, no centro da célula superior esquerda. O canto superior esquerdo da exibição está, portanto, em (-0,5, -0,5) porque são 0,5 células à esquerda e 0,5 células acima do pixel superior esquerdo. O Direct3D renderizará um quad com cantos em (0, 0) e (4, 4), conforme mostrado na ilustração a seguir.

![ilustração de um contorno de um quadrsterizado entre (0, 0) e (4, 4)](images/maptex-fig3.png)

A ilustração anterior mostra onde o quad matemático está em relação à exibição, mas não mostra a aparência do quad depois que o Direct3D o rasteriza e o envia para a exibição. Na verdade, é impossível para uma exibição de raster preencher o quad exatamente como mostrado porque as bordas do quad não coincidem com os limites entre células de pixel. Em outras palavras, como cada pixel só pode exibir uma única cor, cada célula de pixel é preenchida com apenas uma cor; Se a exibição renderizasse o quádruplo exatamente como mostrado, as células de pixel ao longo da borda do quad precisariam mostrar duas cores distintas: azul, quando coberta pelo quad e branco, em que apenas a tela de fundo está visível.

Em vez disso, o hardware gráfico é encarregado de determinar quais pixels devem ser preenchidos para aproximar o quad. Esse processo é chamado de rasterização e é detalhado em [Regras de Rasterização (Direct3D 9)](rasterization-rules.md). Para esse caso específico, o quad rasterizado é mostrado na ilustração a seguir.

![ilustração de um quad não codificado desenhado de (0,0) a (4,4)](images/maptex-fig4.png)

Observe que o quádruplo passado para Direct3D tem cantos em (0, 0) e (4, 4), mas a saída rasterizada (a ilustração anterior) tem cantos em (-0,5,-0,5) e (3.5,3.5). Compare as duas ilustrações anteriores para diferenças de renderização. Você pode ver que o que a exibição realmente renderiza é o tamanho correto, mas foi deslocado por -0,5 células nas instruções x e y. No entanto, exceto para técnicas de várias amostragem, essa é a melhor aproximação possível para o quad. (Consulte o [Exemplo de Antialias para](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) uma cobertura completa de várias amostragem.) Esteja ciente de que, se o rasterizador preencheu cada célula que o quad cruzou, a área resultante seria da dimensão 5 x 5 em vez do 4 x 4 desejado.

Se você assumir que as coordenadas de tela se originam no canto superior esquerdo da grade de exibição em vez do pixel superior esquerdo, o quad será exibido exatamente conforme o esperado. No entanto, a diferença fica clara quando o quad recebe uma textura. A ilustração a seguir mostra a textura 4 x 4 que você mapeará diretamente para o quad.

![ilustração de uma textura 4x4](images/maptex-fig5.png)

Como a textura é de 4 x 4 texels e o quad é de 4 x 4 pixels, você pode esperar que o quad com textura apareça exatamente como a textura, independentemente do local na tela em que o quad é desenhado. No entanto, esse não é o caso; até mesmo pequenas alterações na posição influenciam como a textura é exibida. A ilustração a seguir mostra como um quad entre (0, 0) e (4, 4) é exibido depois de ser rasterizado e texturizado.

![ilustração de um quad com textura desenhada de (0, 0) e (4, 4)](images/maptex-fig6.png)

O quadramento desenhado na ilustração anterior mostra a saída texturizada (com um modo de filtragem linear e um modo de endereçamento de fixação) com o contorno sobreposto rasterizado. O restante deste artigo explica exatamente por que a saída tem a aparência em vez de parecer com a textura, mas para aqueles que querem a solução, aqui está: as bordas do quad de entrada precisam estar sobre as linhas de limite entre células de pixel. Simplesmente deslocando as coordenadas quad x e y em -0,5 unidades, as células de texel abrangem perfeitamente as células de pixel e o quad pode ser perfeitamente recriado na tela. (A última ilustração neste tópico mostra o quad nas coordenadas corrigidas.)

Os detalhes do motivo pelo qual a saída rasterizada só tem leve semelhança com a textura de entrada estão diretamente relacionados à maneira como o Direct3D aborda e amostras de texturas. O que segue pressu que você tenha uma boa compreensão do espaço de [coordenadas de textura](texture-coordinates.md) e da [filtragem de textura bilinear.](bilinear-texture-filtering.md)

Voltando à nossa investigação da saída de pixel estranho, faz sentido rastrear a cor de saída de volta para o sombreador de pixel: o sombreador de pixel é chamado para cada pixel selecionado para fazer parte da forma rasterizada. O quad azul sólido ilustrado em uma ilustração anterior poderia ter um sombreador particularmente simples:


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



Para o quad com textura, o sombreador de pixel precisa ser ligeiramente alterado:


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



Esse código presume que a textura 4 x 4 seja armazenada em MyTexture. Conforme mostrado, o exemplo de textura MySampler é definido para executar a filtragem bilinear em MyTexture. O sombreador de pixel é chamado uma vez para cada pixel rasterizado e cada vez que a cor retornada é a cor da textura amostrada em vTexCoord. Sempre que o sombreador de pixel é chamado, o argumento vTexCoord é definido como as coordenadas de textura nesse pixel. Isso significa que o sombreador está solicitando ao amostrador de textura a cor da textura filtrada no local exato do pixel, conforme detalhado na ilustração a seguir.

![ilustração dos locais de amostragem para coordenadas de textura](images/maptex-fig7.png)

A textura (mostrada sobreposta) é amostrada diretamente em locais de pixel (mostrados como pontos pretos). As coordenadas de textura não são afetadas pela rasterização (elas permanecem no espaço de tela projetado do quad original). Os pontos pretos mostram onde estão os pixels de rasterização. As coordenadas de textura em cada pixel são facilmente determinadas pela interpolação das coordenadas armazenadas em cada vértice: o pixel em (0,0) coincide com o vértice em (0, 0); portanto, as coordenadas de textura nesse pixel são simplesmente as coordenadas de textura armazenadas nesse vértice, UV (0,0, 0,0). Para o pixel em (3, 1), as coordenadas interpoladas são UV (0,75, 0,25) porque esse pixel está localizado em três quartos da largura da textura e um quarto de sua altura. Essas coordenadas interpoladas são o que é passado para o sombreador de pixel.

Os texels não se alinham com os pixels neste exemplo; cada pixel (e, portanto, cada ponto de amostragem) é posicionado no canto de quatro texels. Como o modo de filtragem está definido como Linear, o amostrador fará a média das cores dos quatro texels que compartilham esse canto. Isso explica por que o pixel esperado para ser vermelho é, na verdade, cinza de três quartos mais um quarto vermelho, o pixel que deve ser verde é meio-cinza mais um quarto vermelho mais um quarto verde e assim por diante.

Para corrigir esse problema, tudo o que você precisa fazer é mapear corretamente o quad para os pixels para os quais ele será rasterizado e, assim, mapear corretamente os texels para pixels. A ilustração a seguir mostra os resultados do desenho do mesmo quádruplo entre (-0,5, -0,5) e (3.5, 3.5), que é o quádruplo pretendido desde o início.

![ilustração de um quad texturizado que corresponde ao quad rasterizado](images/maptex-fig8.png)

A ilustração anterior demonstra que o quad (mostrado descrito de (-0,5, -0,5) a (3.5, 3.5)) corresponde exatamente à área rasterizada.

## <a name="summary"></a>Resumo

Em resumo, pixels e texels são, na verdade, pontos, não blocos sólidos. O espaço na tela é originado no pixel superior esquerdo, mas as coordenadas de textura são originadas no canto superior esquerdo da grade da textura. Mais importante, lembre-se de subtrair 0,5 unidades dos componentes x e y de suas posições de vértice ao trabalhar no espaço de tela transformado para alinhar corretamente os texels com pixels.

O código a seguir é um exemplo de deslocamento dos vértices de um quadrado 256 por 256 para exibir corretamente uma textura 256 por 256 no espaço de tela transformado.


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coordenadas de textura](texture-coordinates.md)
</dt> </dl>

 

 



