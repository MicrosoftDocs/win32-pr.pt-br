---
description: Muitas técnicas de renderização e geração de conteúdo exigem um mapa exclusivo e não sobreposto de um sinal 2D (como uma textura) em uma malha.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Usando o UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b335dd6ea94a3db0c0760b0d07a0b8df3fe4c7c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104172391"
---
# <a name="using-uvatlas-direct3d-9"></a>Usando o UVAtlas (Direct3D 9)

Muitas técnicas de renderização e geração de conteúdo exigem um mapa exclusivo e não sobreposto de um sinal 2D (como uma textura) em uma malha. Essas técnicas incluem:

-   Mapeamento normal/de deslocamento
-   Simulações de simulação de espaço de textura e mapas leves
-   Pintura da superfície
-   Textura-iluminação de espaço

A geração manual de um mapeamento UV exclusivo é sempre demorada e entediante; Isso é especialmente verdadeiro quando a geometria de entrada é complexa e eficiente/de textura de distorção. a utilização de espaço é desejada. A ilustração a seguir mostra uma malha de exemplo e seu Atlas de textura correspondente.

![Mostra uma malha de exemplo e seu Atlas de textura correspondente.](images/uvatlas1.jpg)

Este exemplo mostra uma malha (à esquerda) e o mapa normal de um espaço UV correspondente (à direita). Observe que o Atlas de textura contém vários grupos ou clusters de dados; cada cluster é chamado de gráfico e, no exemplo acima, exibe contém os dados normais de uma parte da malha.

As APIs D3DX UVAtlas geram automaticamente um Atlas de textura ideal e não sobreposto. As APIs fornecem parâmetros de entrada que permitem:

-   Minimize o Stretch, distorção e subamostramento de textura.
-   Maximize a densidade de empacotamento de espaço de textura para uso eficiente da memória.
-   Forneça uma amostragem uniforme em toda a malha, minimizando descontinuidades na frequência de amostragem.

## <a name="how-uvatlas-works"></a>Como o UVAtlas funciona

As APIs do UVAtlas (consulte [funções do UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)) geram um Atlas de textura Particionando uma superfície em gráficos e empacotando os gráficos em um Atlas de textura. Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) e [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) para executar essas etapas separadamente; ou use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) para particionar, parametrizar e empacotar em uma única chamada.

-   [Particionando e parametrizando uma malha](#partitioning-and-parameterizing-a-mesh)
-   [Usando tempos de métricas integrados para controlar a parametrização](#using-integrated-metric-tensors-to-control-parameterization)
-   [Usando dados de adjacência para vincos especificados pelo usuário](#using-adjacency-data-for-user-specified-creases)
-   [Empacotando gráficos em um Atlas](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a>Particionando e parametrizando uma malha

Primeiro, a malha é particionada em gráficos e, em seguida, cada gráfico é parametrizado em seu próprio \[ 0, 1 \] UV-espaço. Um cilindro pode ser parametrizado por um gráfico; uma esfera por outro lado exigirá dois gráficos, conforme mostrado na ilustração a seguir.

![ilustração de uma esfera particionada em dois gráficos](images/uvatlas3.jpg)

Uma malha que pode ser parametrizada com um único gráfico é classificada como "homeomorphic para um disco", o que significa que você pode distribuir um disco infinitamente flexível e infinitamente expansível no gráfico e abordar a geometria perfeitamente. Esse alongamento, chamado de homeomorphism, é uma função bidirecional; Isso significa que você pode ir de uma parametrização para a outra sem perder informações.

Poucas malhas do mundo real podem ser parametrizadas em duas dimensões sem separar a malha em clusters ou em gráficos. A ilustração a seguir mostra outra malha de exemplo e seu Atlas de textura correspondente.

![Mostra uma malha de exemplo com formas diferentes e seu Atlas de textura correspondente.](images/uvatlas2.jpg)

Há dois parâmetros que determinam o número de gráficos criados:

-   O número máximo de gráficos permitidos para o Atlas
-   A quantidade máxima de ampliação permitida para cada gráfico

A quantidade de ampliação determinará o número de gráficos que são gerados e a qualidade geral da amostragem. Stretch varia de 0,0 (sem Stretch) a 1,0 (qualquer quantidade de Stretch). D3DXUVAtlasCreate e D3DXUVAtlasPartition retornam o Stretch máximo gerado pelo algoritmo. A ilustração a seguir mostra outra malha de exemplo e seu Atlas de textura correspondente.

![ilustração de uma malha de exemplo e seu Atlas de textura correspondente](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a>Usando tempos de métricas integrados para controlar a parametrização

A priorização de espaço de textura pode ser especificada por triângulo. Os tempos de métrica integrados podem ser fornecidos para controlar como os triângulos são esticados no Atlas de espaço de textura resultante. IMT pode ser especificado diretamente ou computado com base em um sinal de entrada usando as funções de computação IMT D3DX. Uma métrica integrada tensor (ou IMT) é uma matriz 2x2 simétrica que descreve como um triângulo é esticado no Atlas. Cada IMT é definido por 3 floats, chamá-los (a, b, c). Eles podem ser organizados em uma matriz de 2x2 simétrica como esta:


```
a b
b c
```



Em seguida, o IMT pode ser usado para localizar a distância entre dois vetores. Considerando dois vetores v1 e v2, em que:


```
vector v1
vector v2 = v1 + (s,t)
```



A distância entre v1 e V2 pode ser calculada como:


```
sqrt((s, t) * M * (s, t)^T)
```



Em outras palavras, o vetor (s, t) pode ser a magnitude da ampliação em uma direção arbitrária no espaço de u-v. Nesse caso, o vetor s é uma direção do primeiro ao segundo vértice, e t é o produto cruzado do normal e do s. Por exemplo:


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



IMT pode ser especificado diretamente ou computado com base em um sinal de entrada usando as funções de computação IMT D3DX: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal e D3DXComputeIMTFromTexture \_ Graphics.

Especifique os dados do IMT diretamente se desejar controlar como a textura-espaço é alocada a triângulos individuais. Ao fazer isso, aloque mais área no Atlas para áreas importantes de uma malha (como o logotipo facial ou conjunto de um caractere, ou regiões de uma cena perto do caminho de percurso de um jogador). Ao especificar IMT que são múltiplos da matriz de identidade, os triângulos resultantes serão dimensionados uniformemente no espaço de textura.

Por exemplo, dado um mapa normal de alta resolução, você pode calcular IMT para fornecer mais espaço de textura para áreas de sinal de frequência mais alta no mapa normal. Os triângulos que são "simples" (mapeados para regiões constantes do mapa normal original) receberão menos espaço de textura. Os triângulos que contêm uma grande quantidade de detalhes do mapa normal receberão mais área de textura no resultado final. Em seguida, você pode reamostrar o mapa normal em uma textura menor, mas manter detalhes, ou pode recalcular o mapa normal com o mapeamento UV ideal.

### <a name="using-adjacency-data-for-user-specified-creases"></a>Usando dados de adjacência para vincos especificados pelo usuário

As informações de adjacência definidas pelo usuário podem ser fornecidas à função de particionamento para descrever os vincos predefinidos na malha e, portanto, definir um limite de gráfico entre rostos adjacentes. Essa é uma maneira simples para o chamador especificar seu próprio particionamento de gráfico como entrada no algoritmo, o que refinará ainda mais os gráficos para trazer a ampliação para o máximo permitido.

### <a name="example"></a>Exemplo

Este exemplo ilustra como você pode usar as APIs UVAtlas e o DirectX Viewer (Dxviewer.exe) para localizar e corrigir descontinuidades em seu modelo que pode afetar drasticamente o tamanho do seu Atlas de textura. Você pode obter Dxviewer.exe e aprender sobre ele no SDK do DirectX. Dxviewer.exe foi removido do SDK do DirectX após a versão de agosto de 2009 para que seja necessário ter pelo menos o SDK do DirectX de agosto de 2009. Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

Suponha que você começou com algum modelo em seu software de geração de conteúdo favorito (Este exemplo usa um modelo de cabeçalho Dwarf que foi criado em Maya). Exporte o modelo texturizado para um arquivo. x e crie um Atlas de textura com D3DXUVAtlasCreate. O Atlas de textura resultante ficaria parecido com a ilustração a seguir.

![ilustração de um Atlas para um modelo Dwarf](images/uvatlas5.jpg)

O Atlas tem 22 gráficos e um Stretch máximo de 0,994.

Agora, examine o modelo texturizado para ver como o Atlas de textura é mapeado para a geometria. Para fazer isso, carregue o modelo na ferramenta de visualização:

-   Abra a ferramenta de visualização dos utilitários do DirectX.
-   Carregue o arquivo. x clicando no botão abrir.
-   Habilitando a opção de exibição de vinco clicando no botão exibir e selecionando vincos de pop-up.

A ilustração a seguir mostra o que você deve ver na ferramenta do visualizador.

![ilustração de uma malha texturizada na ferramenta do Visualizador](images/uvatlas6c.jpg)

Cada linha é um vinco que é uma borda adjacente entre dois gráficos no Atlas de textura. O número de gráficos gerados pelo algoritmo é causado por pequenas diferenças, talvez devido a descontinuidades nos normais. Essas pequenas diferenças podem ser reduzidas por dados de soldagem, ou seja, forçar os dados que são quase iguais a serem iguais. Para soldar os Normals e o skinweights:

-   Execute a ferramenta Ops (dxops.exe) do DirectX com a seguinte linha de comando na malha (substituindo ' ModelName. x ' pelo nome do seu modelo):
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

Isso compara os Normals e skinweights, e onde eles diferem em valor inferior a 2, 1, os dados são feitos iguais. A ilustração a seguir mostra um fechamento do olho para ver os vincos antes do soldagem (à esquerda) e os vincos após a soldagem (à direita):

![ilustração de vincos antes de soldagem](images/uvatlas6a.jpg)![ilustração de vincos após soldagem](images/uvatlas6b.jpg)

Figura 7: removendo vincos por soldagem

Neste exemplo, a soldagem removeu 86 vértices da malha de entrada. Com menos vincos na malha, você pode regenerar o Atlas, como mostra a ilustração a seguir.

![ilustração do novo Atlas com vincos removidos](images/uvatlas8.jpg)

O Atlas tem apenas 7 gráficos e um Stretch máximo de aproximadamente 0, 776. O novo Atlas agora se encaixa em uma textura menor (aproximadamente 30% menor neste exemplo).

### <a name="packing-charts-into-an-atlas"></a>Empacotando gráficos em um Atlas

Depois que uma malha é particionada em gráficos com parâmetros individuais, os gráficos precisam ser empacotados com eficiência em um único mapa de textura. Isso é executado como a segunda etapa de D3DXUVAtlasCreate ou pode ser invocado explicitamente chamando D3DXUVAtlasPack.

Os gráficos empacotados são separados por uma largura de medianiz especificada pelo usuário. A largura da medianiz é a quantidade de separação entre os gráficos e permite a interpolação bilinear e o mapeamento de MIP para evitar a renderização de artefatos em limites do gráfico. O D3DX fornece uma interface para preencher automaticamente essas medianizes-consulte [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) para obter mais informações.

## <a name="integrating-uvatlas-into-your-pipeline"></a>Integrando o UVAtlas ao seu pipeline

Além de ser chamado de artista antes da pintura de textura, essas funções podem ser integradas em um pipeline de arte automatizado. Por exemplo, uma chamada UVAtlas pode ser emitida automaticamente depois que um ativo é atualizado, antes de executar uma simulação de PRT ou uma passagem de mapeamento normal. Isso evita que seja necessário reparar manualmente o mapeamento UV de um objeto se a topologia da malha tiver sido modificada.

Confira a [ferramenta UV Command-Line do Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) , por exemplo, o uso das funções UVAtlas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos avançados](advanced-topics.md)
</dt> </dl>

 

 
