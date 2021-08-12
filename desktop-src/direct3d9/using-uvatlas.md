---
description: Muitas técnicas de renderização e geração de conteúdo exigem um mapa exclusivo e não sobreposto de um sinal 2D (como uma textura) em uma malha.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Usando UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9516223f6d299f42adf19073dc103e7e13b37d49d2f323d6620b46421be1f722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290589"
---
# <a name="using-uvatlas-direct3d-9"></a>Usando UVAtlas (Direct3D 9)

> [!NOTE]
> UVAtlas foi originalmente enviado na biblioteca de utilty D3DX9 agora preterida. A versão mais recente está disponível na [Ferramenta Command-Line Uv Atlas (uvatlas.exe)](https://github.com/Microsoft/UVAtlas).

Muitas técnicas de renderização e geração de conteúdo exigem um mapa exclusivo e não sobreposto de um sinal 2D (como uma textura) em uma malha. Essas técnicas incluem:

-   Mapeamento normal/deslocamento
-   Simulações de PRT de espaço de textura e mapas de luz
-   Pintura de superfície
-   Iluminação de espaço de textura

Gerar um mapeamento UV exclusivo manualmente geralmente é demorado e entediante; isso é especialmente verdadeiro quando a geometria de entrada é complexa e eficiente/utilização de espaço de textura com baixa distorção é desejada. A ilustração a seguir mostra um exemplo de malha e seu atlas de textura correspondente.

![Mostra um exemplo de malha e seu atlas de textura correspondente.](images/uvatlas1.jpg)

Este exemplo mostra uma malha (à esquerda) e o mapa normal de espaço UV correspondente (à direita). Observe que o atlas de textura contém vários grupos ou clusters de dados; cada cluster é chamado de gráfico e, no exemplo acima, exibe os dados normais para uma parte da malha.

As APIs UVAtlas do D3DX geram automaticamente um atlas de textura ideal e não sobreposto. As APIs fornecem parâmetros de entrada que permitem:

-   Minimize o alongamento de textura, distorção e submampling.
-   Maximizar a densidade de empacotamento de espaço de textura para uso eficiente da memória.
-   Forneça uma amostragem específica na malha, minimizando as descontinuidades na frequência de amostragem.

## <a name="how-uvatlas-works"></a>Como o UVAtlas funciona

As APIs UVAtlas (consulte [Funções UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)) geram um atlas de textura particionando uma superfície em gráficos e empacotando os gráficos em um atlas de textura. Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) e [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) para executar essas etapas separadamente; ou use [**D3DXUVAtlasCriar**](d3dxuvatlascreate.md) para particionar, parametrizar e empacotar em uma única chamada.

-   [Particionamento e parametrização de uma malha](#partitioning-and-parameterizing-a-mesh)
-   [Usando tensores de métrica integrados para controlar a parametrização](#using-integrated-metric-tensors-to-control-parameterization)
-   [Usando dados de adjacency para edados especificados pelo usuário](#using-adjacency-data-for-user-specified-creases)
-   [Empacotando gráficos em um Atlas](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a>Particionamento e parametrização de uma malha

Primeiro, a malha é particionada em gráficos e, em seguida, cada gráfico é parametrizado em seu próprio espaço UV de \[ 0,1. \] Um cilindro pode ser parametrizado por um gráfico; Uma esfera, por outro lado, exigirá dois gráficos, conforme mostrado na ilustração a seguir.

![ilustração de uma esfera particionada em dois gráficos](images/uvatlas3.jpg)

Uma malha que pode ser parametrizada com um único gráfico é classificada como "homeomórfica para um disco", o que significa que você pode difundir um disco infinitamente flexível e infinitamente alongável no gráfico e cobrir perfeitamente a geometria. Esse alongamento, chamado homeomorfismo, é uma função bidirecional; o que significa que você pode passar de uma parametrização para a outra sem perder informações.

Muito poucas malhas do mundo real podem ser parametrizadas em duas dimensões sem separar a malha em clusters ou gráficos. A ilustração a seguir mostra outro exemplo de malha e seu atlas de textura correspondente.

![Mostra um exemplo de malha com diferentes formas e seu atlas de textura correspondente.](images/uvatlas2.jpg)

Há dois parâmetros que determinam o número de gráficos criados:

-   O número máximo de gráficos permitidos para o atlas
-   A quantidade máxima de alongamento permitida para cada gráfico

A quantidade de alongamento determinará o número de gráficos gerados e a qualidade geral da amostragem. O stretch varia de 0,0 (sem alongamento) a 1,0 (qualquer quantidade de alongamento). D3DXUVAtlasCreate e D3DXUVAtlasPartition retornam o alongamento máximo gerado pelo algoritmo. A ilustração a seguir mostra outro exemplo de malha e seu atlas de textura correspondente.

![ilustração de uma malha de exemplo e seu atlas de textura correspondente](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a>Usando tensores de métrica integrados para controlar a parametrização

A priorização de espaço de textura pode ser especificada por triângulo. Tensores de métrica integrados podem ser fornecidos para controlar como os triângulos são estendidos no atlas de espaço de textura resultante. IMTs podem ser especificadas diretamente ou computadas com base em um sinal de entrada usando as funções de computação IMT do D3DX. Um tensor de métrica integrado (ou IMT) é uma matriz simétrica 2x2 que descreve como um triângulo é estendido no atlas. Cada IMT é definido por 3 floats, chame-os (a,b,c). Eles podem ser organizados em uma matriz simétrica 2x2 como esta:


```
a b
b c
```



Em seguida, a IMT pode ser usada para encontrar a distância entre dois vetores. Dado dois vetores v1 e v2, em que :


```
vector v1
vector v2 = v1 + (s,t)
```



A distância entre v1 e v2 pode ser calculada como:


```
sqrt((s, t) * M * (s, t)^T)
```



Em outras palavras, o vetor (s,t) pode ser a magnitude do alongamento em uma direção arbitrária no espaço u-v. Nesse caso, o vetor s é uma direção do primeiro ao segundo vértice e t é o produto cruzado do normal e s. Por exemplo:


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



As IMTs podem ser especificadas diretamente ou computadas com base em um sinal de entrada usando as funções de computação IMT D3DX: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal e D3DXComputeIMTFromTexture \_ gráficos.

Especifique os dados de IMT diretamente se você quiser controlar como o espaço de textura é alocado a triângulos individuais. Ao fazer isso, aloque mais área no atlas para áreas importantes de uma malha (como o rosto ou logotipo de um caractere ou o logotipo da cabeça ou regiões de uma cena perto do caminho de um jogador). Ao especificar IMTs que são múltiplos da matriz de identidade, os triângulos resultantes serão dimensionados uniformemente no espaço de textura.

Por exemplo, dado um mapa normal de alta resolução, você pode calcular a IMT para fornecer mais espaço de textura para áreas de sinal de frequência mais alta no mapa normal. Triângulos que são "simples" (mapeados para regiões constantes do mapa normal original) receberão menos espaço de textura. Triângulos que contêm uma grande quantidade de detalhes de mapa normal receberão mais área de textura no resultado final. Em seguida, você pode recomputar o mapa normal em uma textura menor, mas manter os detalhes, ou pode recomputar o mapa normal com o mapeamento UV mais ideal.

### <a name="using-adjacency-data-for-user-specified-creases"></a>Usando dados de adjacency para edados especificados pelo usuário

As informações de adjacency definidas pelo usuário podem ser fornecidas à função de particionamento para descrever os rostos pré-definidos na malha e, portanto, definir um limite de gráfico entre faces adjacentes. Essa é uma maneira simples para o chamador especificar seu próprio particionamento de gráfico como entrada no algoritmo, o que refina ainda mais os gráficos para colocar o stretch abaixo do máximo permitido.

### <a name="example"></a>Exemplo

Este exemplo ilustra como você pode usar as APIs UVAtlas e o DirectX Viewer (Dxviewer.exe) para encontrar e corrigir descontinuidades em seu modelo que podem afetar drasticamente o tamanho do atlas de textura. Você pode obter Dxviewer.exe e saber mais sobre ele no SDK do DirectX. Dxviewer.exe foi removido do SDK do DirectX após a versão de agosto de 2009, portanto, para obter isso, você precisará de pelo menos o SDK do DirectX de agosto de 2009. Para obter informações sobre o SDK do DirectX, consulte [Onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

Suponha que você começou com algum modelo em seu software de geração de conteúdo favorito (este exemplo usa um modelo de cabeça de ouro que foi criado no Maya). Exporte o modelo com textura para um arquivo .x e crie um atlas de textura com D3DXUVAtlasCriar. O atlas de textura resultante seria algo parecido com a ilustração a seguir.

![ilustração de um atlas para um modelo de foguete](images/uvatlas5.jpg)

O atlas tem 22 gráficos e um trecho máximo de 0,994.

Agora, veja o modelo com textura para ver como o atlas de textura é mapeado para a geometria. Para fazer isso, carregue o modelo na ferramenta do visualizador:

-   Abra a ferramenta visualizador nos Utilitários DirectX.
-   Carregue o arquivo .x clicando no botão Abrir.
-   Habilitando a opção de exibição de exibição clicando no botão de exibição e selecionando Pausas no pop-up.

A ilustração a seguir mostra o que você deve ver na ferramenta do visualizador.

![ilustração de uma malha com textura na ferramenta do visualizador](images/uvatlas6c.jpg)

Cada linha é uma fenda que é uma borda adjacente entre dois gráficos no atlas de textura. O número de gráficos gerados pelo algoritmo é causado por pequenas diferenças, talvez devido a descontinuidades nos normais. Essas pequenas diferenças podem ser reduzidas pela redução dos dados, ou seja, forçando os dados que são quase iguais a serem iguais. Para manter os normais e os pesos de capa:

-   Execute a ferramenta directX Ops (dxops.exe) com a seguinte linha de comando na malha (substituindo 'modelName.x' pelo nome do seu modelo):
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

Isso compara os normais e os pesos-da-capa e, quando eles diferem no valor por menos de 2,01, os dados são iguais. As ilustrações a seguir mostram um close-up do olho para ver as máscaras antes da máscara (à esquerda) e as marcas após a desembreia (à direita):

![ilustração de desenhos antes da máscara](images/uvatlas6a.jpg)![ilustração de desenhos após a máscara](images/uvatlas6b.jpg)

Figura 7: Removendo as máscaras por meio de uma máscara

Neste exemplo, a remoção de 86 vértices da malha de entrada foi removida. Com menos moscos na malha, você pode regenerar o atlas, como mostra a ilustração a seguir.

![ilustração do novo atlas com remoção de amostras](images/uvatlas8.jpg)

O atlas tem apenas 7 gráficos e um trecho máximo de aproximadamente 0,0776. O novo atlas agora se encaixa em uma textura menor (aproximadamente 30% menor neste exemplo).

### <a name="packing-charts-into-an-atlas"></a>Empacotando gráficos em um Atlas

Depois que uma malha tiver sido particionada em gráficos com parâmetros individuais, os gráficos precisarão ser empacotados com eficiência em um único mapa de textura. Isso é executado como a segunda etapa de D3DXUVAtlasCriar ou pode ser invocado explicitamente chamando D3DXUVAtlasPack.

Gráficos empacotados são separados por uma largura de medianiz especificada pelo usuário. A largura da media mediana é a quantidade de separação entre gráficos e permite interpolação bilinear e mapeamento mip para evitar a renderização de artefatos nos limites do gráfico. O D3DX fornece uma interface para preencher automaticamente essas medianizes – consulte [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) para obter mais informações.

## <a name="integrating-uvatlas-into-your-pipeline"></a>Integrando UVAtlas ao pipeline

Além de serem invocadas por um artista antes da pintura de textura, essas funções podem ser integradas a um pipeline de arte automatizado. Por exemplo, uma chamada UVAtlas pode ser emitida automaticamente depois que um ativo é atualizado, antes de executar uma simulação de PRT ou uma passagem de mapeamento normal. Isso evita qualquer necessidade de reparo manual do mapeamento UV de um objeto se a topologia da malha tiver sido modificada.

Consulte a [Ferramenta Command-Line uv atlas (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) para ver o uso de exemplo das funções UVAtlas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos avançados](advanced-topics.md)
</dt> </dl>

 

 
