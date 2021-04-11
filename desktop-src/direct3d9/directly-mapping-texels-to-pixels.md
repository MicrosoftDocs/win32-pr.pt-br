---
description: Ao renderizar a saída 2D usando vértices pré-aprovados, deve-se ter cuidado para garantir que cada área de Texel corresponda corretamente a uma área de pixel única, caso contrário, pode ocorrer distorção de textura.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Mapeamento direto de texels para pixels (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f86e9d05acff402128ddb83fc97898ff6a21d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163805"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a>Mapeamento direto de texels para pixels (Direct3D 9)

Ao renderizar a saída 2D usando vértices pré-aprovados, deve-se ter cuidado para garantir que cada área de Texel corresponda corretamente a uma área de pixel única, caso contrário, pode ocorrer distorção de textura. Ao compreender os conceitos básicos do processo que o Direct3D segue ao rasterizar e texturing triângulos, você pode garantir que seu aplicativo Direct3D processe corretamente a saída 2D.

![ilustração de uma exibição de resolução 6x6](images/maptex-fig1.png)

O diagrama anterior mostra pixels modelados como quadrados. Na realidade, no entanto, os pixels são pontos, e não quadrados. Cada quadrado no diagrama anterior indica a área acesa pelo pixel, mas um pixel é sempre apenas um ponto no centro de um quadrado. Essa distinção, embora aparentemente pequena, é importante. Uma ilustração melhor da mesma exibição é mostrada no diagrama a seguir.

![ilustração de uma exibição que consiste em pixels](images/maptex-fig2.png)

O diagrama anterior mostra corretamente cada pixel físico como um ponto no centro de cada célula. A coordenada de espaço da tela (0, 0) está localizada diretamente no pixel superior esquerdo e, portanto, no centro da célula superior esquerda. O canto superior esquerdo da exibição, portanto, em (-0,5,-0,5) porque é de 0,5 células à esquerda e 0,5 células para cima do pixel superior esquerdo. O Direct3D processará um quad com os cantos em (0, 0) e (4, 4), conforme mostrado na ilustração a seguir.

![ilustração de um contorno de um quádruplo não rasterizado entre (0, 0) e (4, 4)](images/maptex-fig3.png)

A ilustração anterior mostra onde o quádruplo matemático está em relação à exibição, mas não mostra qual será a aparência do Quad quando o Direct3D o rasteriza e o envia para a exibição. Na verdade, é impossível que uma tela de varredura preencha o quad exatamente conforme mostrado, pois as bordas do Quad não coincidem com os limites entre células de pixel. Em outras palavras, como cada pixel só pode exibir uma única cor, cada célula de pixel é preenchida com apenas uma única cor; se a exibição fosse renderizar o quad exatamente como mostrado, as células de pixel ao longo da borda do Quad precisarão mostrar duas cores distintas: azul, quando coberto pelo Quad e branco, onde apenas o plano de fundo está visível.

Em vez disso, o hardware de gráficos é tarefa com a determinação de quais pixels devem ser preenchidos para aproximar o quad. Esse processo é chamado de rasterização e é detalhado em [regras de rasterização (Direct3D 9)](rasterization-rules.md). Para esse caso em particular, o quad rasterizado é mostrado na ilustração a seguir.

![ilustração de um quad desenhado não texturizado de (0, 0) a (4, 4)](images/maptex-fig4.png)

Observe que o quad passado para o Direct3D tem cantos em (0, 0) e (4, 4), mas a saída rasterizada (a ilustração anterior) tem cantos em (-0,5,-0,5) e (3,5, 3,5). Compare as duas ilustrações anteriores para a renderização de diferenças. Você pode ver que a exibição realmente renderiza o tamanho correto, mas foi deslocada por-0,5 células nas direções x e y. No entanto, com exceção das técnicas de várias amostras, essa é a melhor aproximação possível para o quad. (Consulte o [exemplo de antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) para uma cobertura completa de várias amostras.) Lembre-se de que, se o rasterizador preencher cada célula o quádruplo cruzado, a área resultante será da dimensão 5 x 5 em vez dos 4 x 4 desejados.

Se você assumir que as coordenadas de tela se originam no canto superior esquerdo da grade de exibição em vez do pixel superior esquerdo, o quad aparecerá exatamente como esperado. No entanto, a diferença fica clara quando o quad recebe uma textura. A ilustração a seguir mostra a textura 4 x 4 que você mapeará diretamente para o quad.

![ilustração de uma textura 4x4](images/maptex-fig5.png)

Como a textura é 4 x 4 texels e a quádrupla é de 4 x 4 pixels, você pode esperar que o quádruplo texturizado apareça exatamente como a textura, independentemente do local na tela em que o Quad é desenhado. No entanto, esse não é o caso; até mesmo pequenas alterações na posição influenciam como a textura é exibida. A ilustração a seguir mostra como um quad entre (0, 0) e (4, 4) é exibido depois de ser rasterizado e texturizado.

![ilustração de um quad com textura texturizado de (0, 0) e (4, 4)](images/maptex-fig6.png)

O quad desenhado na ilustração anterior mostra a saída texturizada (com um modo de filtragem linear e um modo de endereçamento fixe) com a estrutura de tópicos rasterizada sobreposta. O restante deste artigo explica exatamente por que a saída tem a aparência que ela faz, em vez de se parecer com a textura, mas para aqueles que desejam a solução, aqui está: as bordas da entrada Quad precisam estar sobre as linhas de limite entre células de pixel. Simplesmente deslocando as coordenadas x e y em 0,5 unidades, as células de Texel abordarão perfeitamente as células de pixel e o quad poderá ser perfeitamente recriado na tela. (A última ilustração neste tópico mostra o quad nas coordenadas corrigidas.)

Os detalhes de por que a saída rasterizada só tem ligeira semelhança com a textura de entrada estão diretamente relacionadas à maneira como os endereços e as texturas dos exemplos do Direct3D. O que segue pressupõe que você tenha uma boa compreensão do [espaço de coordenadas de textura](texture-coordinates.md) e da filtragem de [textura bilinear](bilinear-texture-filtering.md).

Voltando à nossa investigação da saída de pixel estranho, faz sentido rastrear a cor de saída de volta para o sombreador de pixel: o sombreador de pixel é chamado para cada pixel selecionado para fazer parte da forma rasterizada. O azul sólido quádruplo ilustrado em uma ilustração anterior poderia ter um sombreador especialmente simples:


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



Para o quad texturizado, o sombreador de pixel precisa ser alterado ligeiramente:


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



Esse código pressupõe que a textura 4 x 4 é armazenada em MyTexture. Como mostrado, a amostra de textura myamostrador é definida para executar a filtragem bilinear em MyTexture. O sombreador de pixel é chamado uma vez para cada pixel rasterizado, e cada vez que a cor retornada é a cor de textura amostrada em vTexCoord. Cada vez que o sombreador de pixel é chamado, o argumento vTexCoord é definido como as coordenadas de textura nesse pixel. Isso significa que o sombreador está solicitando a amostra de textura da cor de textura filtrada no local exato do pixel, conforme detalhado na ilustração a seguir.

![ilustração de locais de amostragem para coordenadas de textura](images/maptex-fig7.png)

A textura (mostrada como sobreposta) é amostrada diretamente em locais de pixel (mostrados como pontos pretos). As coordenadas de textura não são afetadas pela rasterização (elas permanecem no espaço de tela projetado do quádruplo original). Os pontos pretos mostram onde estão os pixels de rasterização. As coordenadas de textura em cada pixel são facilmente determinadas com a interpolação das coordenadas armazenadas em cada vértice: o pixel em (0, 0) coincide com o vértice em (0, 0); Portanto, as coordenadas de textura nesse pixel são simplesmente as coordenadas de textura armazenadas nesse vértice, UV (0,0, 0,0). Para o pixel em (3, 1), as coordenadas interpoladas são UV (0,75, 0,25) porque esse pixel está localizado em três quartos da largura da textura e um quarto de sua altura. Essas coordenadas interpoladas são as que são passadas para o sombreador de pixel.

O texels não se alinha com os pixels neste exemplo; cada pixel (e, portanto, cada ponto de amostragem) está posicionado no canto de quatro texels. Como o modo de filtragem é definido como linear, a amostra calculará a média das cores dos quatro texels compartilhando esse canto. Isso explica por que o pixel esperado para ser vermelho é, na verdade, de três quartos cinzas, além de um quarto de vermelho, o pixel esperado para ser verde é um meio-meio-meio do vermelho, além de um quarto de verde e assim por diante.

Para corrigir esse problema, tudo o que você precisa fazer é mapear corretamente o Quad para os pixels para os quais ele será rasterizado e, assim, mapear corretamente o texels para pixels. A ilustração a seguir mostra os resultados do desenho do mesmo Quad entre (-0,5,-0,5) e (3,5, 3,5), que é o quad planejado desde o início.

![ilustração de um quad texturizado que corresponde ao Quad rasterizado](images/maptex-fig8.png)

A ilustração anterior demonstra que o quad (mostrado descrito a partir de (-0,5,-0,5) a (3,5, 3,5)) corresponde exatamente à área rasterizada.

## <a name="summary"></a>Resumo

Em resumo, pixels e texels são realmente pontos, não blocos sólidos. O espaço da tela é originado no pixel superior esquerdo, mas as coordenadas de textura se originam no canto superior esquerdo da grade da textura. Mais importante, lembre-se de subtrair 0,5 unidades dos componentes x e y de suas posições de vértice ao trabalhar no espaço de tela transformado para alinhar corretamente o texels com pixels.

O código a seguir é um exemplo de deslocamento dos vértices de um quadrado de 256 por 256 para exibir corretamente uma textura 256 por 256 no espaço da tela transformada.


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

 

 



