---
description: Conceitualmente, um viewport é um retângulo bidimensional (2D) no qual uma cena 3D é projetada.
ms.assetid: eddadaa1-9181-47fa-8530-44aa46fea286
title: Viewports and Clipping (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6ed7cd5e5a8a3116c07c5b88f3e665e7ba7de7c6dd1d3cd7bf55f936e60386
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068830"
---
# <a name="viewports-and-clipping-direct3d-9"></a>Viewports and Clipping (Direct3D 9)

Conceitualmente, um viewport é um retângulo bidimensional (2D) no qual uma cena 3D é projetada. No Direct3D, o retângulo existe como coordenadas dentro de uma superfície do Direct3D que o sistema usa como um destino de renderização. A transformação da projeção converte os vértices no sistema de coordenadas usado para o visor. Um visor também é usado para especificar o intervalo de valores de profundidade em uma superfície de destino de renderização na qual uma cena será renderizada (geralmente 0.0 a 1.0).

## <a name="the-viewing-frustum"></a>Tronco de exibição

Um tronco de exibição é o volume 3D em uma cena posicionado com relação à câmera do visor. A forma do volume afeta como os modelos são projetados do espaço da câmera na tela. O tipo mais comum de projeção, uma projeção de perspectiva, é responsável por fazer com que os objetos próximos da câmera pareçam maiores que os objetos distantes. Para a exibição de perspectiva, o tronco de exibição pode ser visualizado como uma pirâmide, com a câmera posicionada na ponta conforme mostrado na ilustração a seguir. Esta pirâmide é intersectada por um plano de recorte traseiro e frontal. O volume na pirâmide entre aos planos de recorte dianteiro e traseiro é o tronco de exibição. Os objetos ficam visíveis somente quando estão nesse volume.

![ilustração de um tronco de exibição com um plano de recorte traseiro e frontal](images/frustum.png)

Se você imaginar que está parado em uma sala escura e olhando por uma janela quadrada, estará visualizando um tronco de exibição. Nessa analogia, o plano de recorte próximo é a janela, e o plano de recorte de fundo é tudo o que finalmente interrompe sua visão – os arranha-céus do outro lado da rua, as montanhas distantes, ou nada. Você pode ver tudo dentro da pirâmide truncada que começa na janela e termina com o que quer que interrompa sua visão, impedindo sua visão.

O tronco de exibição é definido por fov (campo de visão) e por distâncias dos planos de recorte traseiro e frontal, especificados em coordenadas de z, conforme mostrado no diagrama a seguir.

![diagrama do tronco de exibição](images/fovdiag.png)

Neste diagrama, a variável D é a distância da câmera até a origem do espaço que foi definido na última parte do pipeline de geometria - a transformação de exibição. Este é o espaço em torno do qual você organiza os limites de seu tronco de exibição. Para obter informações sobre como essa variável D é usada para criar a matriz de projeção, consulte a Transformação [projeção (Direct3D 9)](projection-transform.md)

## <a name="viewport-rectangle"></a>Retângulo do visor

Você define o retângulo do viewport em C++ usando a [**estrutura D3DVIEWPORT9.**](d3dviewport9.md) A estrutura D3DVIEWPORT9 é usada com os métodos de manipulação do viewport a seguir expostos pela interface IDirect3DDevice9.

-   [**IDirect3DDevice9::GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
-   [**IDirect3DDevice9::SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

A estrutura D3DVIEWPORT9 contém quatro membros – X, Y, Largura, Altura – que definem a área da superfície de destino de renderização na qual uma cena será renderizada. Esses valores correspondem ao retângulo de destino ou retângulo do visor, conforme mostrado no diagrama a seguir.

![diagrama do retângulo do visor](images/destrect.png)

Os valores que você especificar para os membros X, Y, largura, altura são coordenadas de tela relativas ao canto superior esquerdo da superfície do destino de renderização. A estrutura define dois membros adicionais (MinZ e MaxZ) que indicam os intervalos de profundidade nos quais a cena será renderizada.

O Direct3D pressupõe que o volume de recorte do visor varia de -1,0 a 1,0 em X e de 1,0 a -1,0 em Y. Essas eram as configurações usadas mais frequentemente por aplicativos no passado. Você pode ajustar a taxa de proporção do visor antes de recortar usando a [transformação da projeção](projection-transform.md).

> [!Note]  
> MinZ e MaxZ indicam os intervalos de profundidade nos quais a cena será renderizada e não são usadas para recorte. A maioria dos aplicativos definirá esses membros como 0,0 e 1.0 para permitir que o sistema renderizar para todo o intervalo de valores de profundidade no buffer de profundidade. Em alguns casos, você pode conseguir efeitos especiais usando outros intervalos de profundidade. Por exemplo, para renderizar um painel transparente em um jogo, você pode definir os dois valores como 0,0 para forçar o sistema a renderizar objetos em uma cena em primeiro plano, ou você pode defini-los como 1,0 para renderizar um objeto que sempre deve estar em segundo plano.

 

As dimensões usadas nos membros X, Y, Largura, Altura da estrutura [**D3DVIEWPORT9**](d3dviewport9.md) para um viewport definem o local e as dimensões do viewport na superfície de destino de renderização. Esses valores são dados em coordenadas de tela, relativas ao canto superior esquerdo da superfície.

O Direct3D usa a localização do visor e as dimensões para dimensionar os vértices para inserir uma cena renderizada no local apropriado na superfície de destino. Internamente, o Direct3D insere esses valores na matriz a seguir, que é aplicada a cada vértice.

![equação da matriz que é aplicada a cada vértice](images/vpscale.png)

Essa matriz dimensiona os vértices de acordo com a dimensão do visor e o intervalo de profundidade desejado, e os move para o local apropriado na superfície do destino de renderização. A matriz também gira a coordenada y para refletir uma origem de tela no canto superior esquerdo com y aumentando para baixo. Depois que essa matriz é aplicada, os vértices ainda são homogêneos , ou seja, eles ainda existem como \[ vértices x,y,z,w e devem ser convertidos em coordenadas não homogêneas antes de serem enviados para o \] rasterizador.

> [!Note]  
> A matriz de dimensionamento do viewport incorpora os membros MinZ e MaxZ da estrutura [**D3DVIEWPORT9**](d3dviewport9.md) para dimensionar vértices para se ajustar ao intervalo de \[ profundidade MinZ, MaxZ \] . Isso representa uma semântica diferente das versões anteriores do DirectX, nas quais esses membros foram usados para recorte.

 

> [!Note]  
> Os aplicativos normalmente configuram MinZ e MaxZ como 0,0 e 1,0, respectivamente, para fazer com que o sistema seja renderizar para todo o intervalo de profundidade. No entanto, você pode usar outros valores para alcançar determinados efeitos. Por exemplo, você pode definir os dois valores como 0,0 para forçar todos os objetos no primeiro plano ou definir ambos como 1,0 para renderizar todos os objetos em segundo plano.

 

## <a name="clearing-a-viewport"></a>Limpar um visor

Limpar o visor redefine o conteúdo do retângulo do visor na superfície do destino de renderização. Ele também pode limpar o retângulo nas superfícies de buffer de estêncil e de profundidade.

Use [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) para limpar o viewport. O método aceita um ou mais retângulos que definem as áreas na superfície que estão sendo limpas. Definir o parâmetro Count como 1 e o parâmetro pRects como o endereço de um único retângulo que abrange toda a área do viewport limpará todo o viewport. Outra maneira de limpar todo o viewport é definir o parâmetro pRects como **NULL** e o parâmetro Count como 0.

O [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) pode ser usado para limpar os bits de estêncil dentro de um buffer de profundidade. Basta definir o parâmetro Flags para determinar como **IDirect3DDevice9::Clear** funciona com o destino de renderização e quaisquer buffers de profundidade ou estêncil associados. O sinalizador D3DCLEAR TARGET limpará o viewport usando uma cor RGBA arbitrária que você fornece no argumento Color (essa não \_ é a cor do material). O sinalizador D3DCLEAR ZBUFFER limpará o buffer de profundidade para uma profundidade arbitrária especificada em Z: 0,0 é a distância mais próxima e \_ 1,0 é a mais distante. O sinalizador STENCIL D3DCLEAR redefinirá os bits de estêncil para o valor que você \_ fornecer no argumento Estêncil. Você pode usar inteiros que variam de 0 a 2n-1, em que n é a profundidade de bits do buffer de estêncil.

Em algumas situações, você pode estar renderizar apenas para pequenas partes das superfícies de buffer de destino e profundidade de renderização. Os métodos claros também permitem limpar várias áreas de suas superfícies em uma única chamada. Faça isso definindo o parâmetro Count como o número de retângulos que você deseja limpar e especifique o endereço do primeiro retângulo em uma matriz de retângulos no parâmetro pRects.

## <a name="set-up-the-viewport-for-clipping"></a>Configurar o visor para o recorte

Os resultados da matriz de projeção determinam o volume de recorte no espaço de projeção:

-w<sub>c</sub><= x<sub>c</sub><= w<sub>c</sub>

-w<sub>c</sub><= y<sub>c</sub><= w<sub>c</sub>

0 <= z<sub>c</sub><= w<sub>c</sub>

Onde: x, y, z e w representam as coordenadas de vértice depois que a transformação da projeção é aplicada. Qualquer vértice que tiver um componente x, y ou z fora desses intervalos será recortado, se o recorte estiver habilitado (comportamento padrão).

Com exceção dos buffers de vértice, os aplicativos habilitam ou desabilitam o recorte por meio do estado de renderização [**\_ de RECORTE D3DRS.**](./d3drenderstatetype.md) Informações de recorte para buffers de vértice são geradas durante o processamento. Para obter mais informações, consulte Processamento de vértice de função [fixa (Direct3D 9)](fixed-function-vertex-processing.md) e Processamento programável de [vértice (Direct3D 9)](programmable-vertex-processing.md).

O Direct3D não cortará vértices transformados de um primitivo de um buffer de vértice, a menos que ele venha de [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices). Se você estiver fazendo suas próprias transformações e precisar do Direct3D para fazer o recorte, não deverá usar buffers de vértice. Nesse caso, o aplicativo percorre os dados para transformá-los. O Direct3D percorre os dados uma segunda vez para retraí-los e, em seguida, o driver renderiza os dados, o que é ineficiente. Portanto, se o aplicativo transformar os dados, também será preciso cortar os dados.

Quando o dispositivo recebe vértices pré-transformados e acesos (Vértices T&L) que precisam ser recortados, para executar a operação de recorte, os vértices são transformados novamente no espaço de recorte usando o RHW (w homogêneo recíproco) do vértice e as informações do viewport. O recorte é então executado. Nem todos os dispositivos são capazes de executar essa transformação de fundo para cortar os vértices T&L.

A funcionalidade do dispositivo D3DPMISCCAPS CLIPTLVERTS indica se o dispositivo é capaz de cortar \_ Vértices T&L. Se essa funcionalidade não estiver definida, o aplicativo será responsável por recortar os vértices T&L que pretende enviar para o dispositivo a ser renderizado. O dispositivo é sempre capaz de cortar vértices T&L no modo de processamento de vértice de software (independentemente de o dispositivo ser criado no modo de processamento de vértice de software ou alternado para o modo de processamento de vértice de software).

O único requisito para configurar os parâmetros do viewport para um dispositivo de renderização é definir o volume de recorte do visualizador. Para fazer isso, você inicializa e configura valores de recorte para o volume de recorte e para a superfície de destino de renderização. Os viewports normalmente são definidos para renderizar para a área completa da superfície de destino de renderização, mas isso não é um requisito.

Você pode usar as configurações a seguir para os membros da [**estrutura D3DVIEWPORT9**](d3dviewport9.md) para conseguir isso no C++.


```
D3DVIEWPORT9 viewData = { 0, 0, width, height, 0.0f, 1.0f };
```



Depois de definir valores na estrutura [**D3DVIEWPORT9,**](d3dviewport9.md) aplique os parâmetros do viewport ao dispositivo chamando seu [**método IDirect3DDevice9::SetViewport.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) O exemplo de código a seguir mostra a aparência dessa chamada.


```
HRESULT hr;

hr = pd3dDevice->SetViewport(&viewData);
if(FAILED(hr))
    return hr;
```



Se a chamada for bem-sucedida, os parâmetros do viewport serão definidos e terão efeito na próxima vez que um método de renderização for chamado. Para fazer alterações nos parâmetros do viewport, basta atualizar os valores na estrutura [**D3DVIEWPORT9**](d3dviewport9.md) e chamar [**IDirect3DDevice9::SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) novamente.

> [!Note]  
> Os membros da estrutura [**D3DVIEWPORT9**](d3dviewport9.md) MinZ e MaxZ indicam os intervalos de profundidade nos quais a cena será renderizada e não serão usadas para recorte. A maioria dos aplicativos configura esses membros como 0,0 e 1.0 para permitir que o sistema renderizar para todo o intervalo de valores de profundidade no buffer de profundidade. Em alguns casos, você pode conseguir efeitos especiais usando outros intervalos de profundidade. Por exemplo, para renderizar um painel transparente em um jogo, você pode definir os dois valores como 0,0 para forçar o sistema a renderizar objetos em uma cena em primeiro plano, ou você pode defini-los como 1,0 para renderizar um objeto que sempre deve estar em segundo plano.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> </dl>

 

 
