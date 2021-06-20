---
description: Saiba mais sobre o suporte de malha no D3DX. D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente do Direct3D.
ms.assetid: 7892370f-0807-4ab7-b7cd-a7e1182e3f9c
title: Suporte a malha no D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1600b372432d59357a7431c70ce70ce2958002c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408128"
---
# <a name="mesh-support-in-d3dx-direct3d-9"></a>Suporte a malha no D3DX (Direct3D 9)

D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente do Direct3D.

## <a name="meshes"></a>Malhas

O D3DX implementa a construção de malha para carregar, manipular e renderizar o conteúdo do arquivo. x. Uma malha é basicamente uma coleção de vértices que definem uma geometria e um conjunto de índices que definem as faces. Há vários tipos de malha.

O [**ID3DXBaseMesh**](id3dxbasemesh.md) fornece os conceitos básicos. [**ID3DXMesh**](id3dxmesh.md) herda de ID3DXBaseMesh e adiciona otimização de malha usando o cache de vértice por chip. O [**ID3DXSkinInfo**](id3dxskininfo.md) fornece suporte a malhas com revestimento.

O [**ID3DXBaseMesh**](id3dxbasemesh.md) fornece métodos para manipular e consultar objetos de malha [**ID3DXMesh**](id3dxmesh.md) , que herdam da malha base. Isso inclui operações de adjacência, recuperação de buffer de geometria, operações de bloqueio/desbloqueio (vértice e índice) e informações de cópia, renderização, face e vértice.

> [!Note]  
> As interfaces ID3DXPMesh e ID3DXSPMesh (para oferecer suporte a malhas progressivas e simplificadas, respectivamente) disponíveis em versões anteriores do Direct3D 9 foram descartadas.

 

## <a name="mesh-architecture"></a>Arquitetura de malha

Uma malha contém os dados de um modelo complexo. É um contêiner de dados abstratos que contém recursos como texturas e materiais, e atributos como dados de posição e dados de adjacência. Há várias operações de malha que melhoram o desempenho do desenho e a aparência de uma superfície. Além disso, há vários outros conceitos de malha que afetarão a funcionalidade das operações de malha. Compreender esses conceitos de malha para que você possa aplicá-los melhorará o desempenho da malha.

## <a name="mesh-object-data"></a>Dados do objeto de malha

Uma malha contém um buffer de vértice, um buffer de índice e um buffer de atributo.

-   O buffer de vértice contém os dados de vértice, que são os vértices de malha.
-   O buffer de índice contém índices de vértice para acessar o buffer de vértice. Isso pode reduzir o tamanho do buffer de vértices, reduzindo os vértices duplicados. Somente uma malha indexada usa o buffer de índice. Se uma malha for composta de uma lista de triângulos, por exemplo, ela não usará o buffer de índice.
-   O buffer de atributo contém dados de atributo. Os atributos são propriedades dos vértices de malha, em nenhuma ordem específica. Uma malha D3DX armazena atributos em um grupo de DWORDs, para cada face.

### <a name="attribute-tables"></a>Tabelas de atributos

Uma tabela de atributos é uma representação concisa do conteúdo de um buffer de atributo. As tabelas de atributo podem ser criadas chamando um dos métodos Optimize com D3DXMESHOPT \_ ATTRSORT, bloqueando o buffer de atributo e preenchendo-o com dados ou chamando SetAttributeTable. Uma malha contém uma tabela de atributos quando a malha é reordenada em grupos. Isso acontece quando Optimize é chamado, supondo que uma opção de classificação de atributo (D3DXMESHOPT \_ ATTRSORT ou superior) seja fornecida. As malhas D3DX usam listas de triângulo indexadas e, portanto, são desenhadas com [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

As tabelas de atributos são criadas como resultado da chamada de optimize. Os rostos não precisam ser adjacentes, pois Optimize os reordenará para que sejam adjacentes. Por exemplo, as mãos de uma malha humana poderiam usar o mesmo atributo. A ID ajuda a classificar as faces em grupos. As malhas de arquivos. x geraram automaticamente atributos para propriedades de material e de textura. Você precisa chamar Optimize (ATTRSORT) ou a otimização mais eficaz (VERTEXCACHE) para obter um bom desempenho. As funções de carga tentam apresentar os dados na forma exata em que foram salvos. Se você estiver usando uma malha baseada no buffer de buffer/índice, a API de malha fornecerá as funções de otimização e as transformações de aparência com pouca sobrecarga.

Os tipos de otimização são cumulativos, começando pelo menos o ideal (D3DXMESHOPT \_ Compact) ao mais adequado (D3DXMESHOPT \_ IGNOREVERTS). D3DXMESHOPT \_ STRIPREORDER faz uma compactação e uma classificação de atributos. D3DXMESHOPT \_ VERTEXCACHE é sempre recomendado, mesmo em dispositivos sem um verdadeiro cache de vértice.

## <a name="application-data"></a>Dados de aplicativos

Os dados de aplicativo são dados de malha que são gerenciados por um aplicativo. Há um acoplamento rígido entre os dados de vértice de malha e os dados gerenciados por esses buffers.

O buffer de materiais contém n materiais. Os materiais são retornados pela função load quando o arquivo. x é carregado. Cada subconjunto pode ter seus próprios materiais e texturas. O buffer de materiais é estático.

O buffer de adjacência contém informações sobre bordas, rostos e rostos adjacentes. Algumas operações de malha dependem de saber quais faces são adjacentes entre si. Essas informações, chamadas de dados de adjacência, são mantidas em um buffer de adjacência. Ele não faz parte da malha, mas é mantido pelo aplicativo e deve ser fornecido para os métodos de malha quando necessário.

O buffer da instância de efeitos contém uma lista de instâncias de efeito. Uma instância de efeito armazena o estado. Essas informações de estado são usadas para inicializar o pipeline. Uma instância de efeito contém pares de nome-valor em um efeito.

## <a name="advanced-mesh-topics"></a>Tópicos de malha avançada

Malhas otimizadas se baseiam na funcionalidade de malha base e adicionam o recurso de otimização de cache de vértice com dois métodos: Optimize, que cria uma nova malha e OptimizeInPlace, que modifica a malha original.

D3DXGeneratePMesh usa o algoritmo de simplificação de D3DX para gerar uma malha progressiva a partir da malha de entrada. O D3DXSimplifyMesh gera uma malha padrão do nível de detalhe fornecido a partir de uma malha de entrada usando o mesmo algoritmo de simplificação. O usuário tem controle sobre a métrica de erro usada por meio do componente de pesos especificado por vértice e os pesos especificados por vértice. Os pesos por componente são multiplicados na parte dos componentes do erro calculado por recolhimento de borda. Os pesos por vértice são multiplicados em relação ao valor da métrica de erro determinado para remoção desse vértice. Por exemplo, se você nunca quiser que um vértice seja removido, defina o peso do vértice específico como um valor grande. Por outro lado, se você quiser removê-lo anteriormente, defina-o como um valor pequeno (menor que 1).

[**ID3DXSkinInfo**](id3dxskininfo.md) dá suporte a caracteres com revestimento. Um caractere com revestimento é definido por um conjunto de malhas e um conjunto de Bones que afetam os vértices das malhas. Os Bones são representados como uma hierarquia de transformação. Para cada malha, há uma matriz para cada Bone que a afeta, que transforma a malha no espaço de coordenadas local do Bone. Essa matriz é a transformação de espaço do Bone do Bone para a malha. Isso é definido no momento em que o esqueleto é associado à malha no processo de criação.

### <a name="skinning"></a>Aplicação de capas

A aparência é uma técnica para transformar vértices de malha usando Bones. Os Bones normalmente são organizados em um esqueleto hierárquico, muito parecido com os Bones em um corpo humano. Os vértices de objeto são então associados aos Bones, como anexar a capa aos Bones. Quando os Bones são transformados, a capa também é transformada.

As malhas subcapadas usam Bones para influenciar um número de vértices. Os dados de transformação Bone são fornecidos pelo usuário, para influenciar como SRT os Bones. A malha usa os Bones transformados para influenciar os vértices associados aos Bones. As paletas são matrizes de transformações de SRT. As paletas são frequentemente implementadas como matrizes, mas podem conter valores de SRT.

### <a name="progressive-mesh-trimming"></a>Corte de malha progressiva

Áreas de detalhe baixo podem perder vértices que não alteram a aparência renderizada da superfície. Isso é especialmente verdadeiro para objetos à medida que eles se afastam da câmera. Isso é conhecido como nível de detalhe. Os usuários têm controles de renderização no nível de API para definir o nível de detalhe para maximizar a eficiência de renderização.

Os objetos de malha progressiva começam com um alto número de faces e usam simplificação para reduzir o número de faces. Uma malha progressiva que é independente de exibição é chamada de VIPM (malha progressiva independente de exibição).

Outra maneira de reduzir o número de faces é cortar. Isso, na verdade, Remove vértices e rostos da malha. A remoção pode ser feita no high-end (para limitar o número máximo de rostos) ou no low end (para limitar o número mínimo de faces). No entanto, a redução melhora o desempenho do desenho. o cuidado deve ser usado para preservar a qualidade visual. A recortação é demonstrada no Exemplo de SDK de Malha Progressiva.

Para áreas de alta visibilidade, a resolução pode ser aumentada usando o nível progressivo de detalhes (LTDD). Essa é uma técnica para quebrar um único rosto em duas faces.

### <a name="patch-meshes"></a>Malhas de patch

Dois tipos especializados de malhas de patch também são suportados: patches retângulo e triângulo. A malha de patch do retângulo é uma malha de patch cujos pontos de controle são colocados em uma sequência sinunta e retangular. Patches de retângulo e triângulo são usados para criar superfícies de ordem alta. Elas não são tão comumente usadas como malhas de triângulo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[D3dx](d3dx.md)
</dt> </dl>

 

 
