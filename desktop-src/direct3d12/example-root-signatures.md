---
title: Exemplo de assinaturas raiz
description: A seção a seguir mostra as assinaturas raiz que variam em complexidade de vazia para completamente completa.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104021"
---
# <a name="example-root-signatures"></a>Exemplo de assinaturas raiz

A seção a seguir mostra as assinaturas raiz que variam em complexidade de vazia para completamente completa.

-   [Uma assinatura raiz vazia](#an-empty-root-signature)
-   [Uma constante](#one-constant)
-   [Adicionando uma exibição de buffer de constante raiz](#adding-a-root-constant-buffer-view)
-   [Tabelas de descritores de associação](#binding-descriptor-tables)
-   [Uma assinatura de raiz mais complexa](#a-more-complex-root-signature)
-   [Exibições de recurso do sombreador de streaming](#streaming-shader-resource-views)
-   [Tópicos relacionados](#related-topics)

## <a name="an-empty-root-signature"></a>Uma assinatura raiz vazia

![uma assinatura raiz vazia não tem associações](images/root-tables-0.png)

Uma assinatura raiz vazia é improvável de ser útil, mas pode ser usada em uma passagem de renderização trivial com o uso apenas do assembler de entrada e do vértice mínimo e dos sombreadores de pixel que não acessam nenhum descritor. Além disso, os estágios de estágio de mesclagem, destino de renderização e estêncil de profundidade estão disponíveis, mesmo com uma assinatura de raiz vazia.

## <a name="one-constant"></a>Uma constante

![uma única constante raiz](images/root-tables-constant.png)

O slot de associação de API é onde o argumento raiz para esse parâmetro será associado no momento do registro da lista de comandos. O número de Slots de ligação de API é implícito, com base na ordem dos parâmetros na assinatura raiz (o primeiro é sempre zero). O slot de ligação do HLSL é onde o sombreador verá que o parâmetro raiz aparece. O tipo ("UINT" no exemplo acima) não é conhecido pelo hardware, mas é apenas um comentário na imagem, o hardware simplesmente verá o único DWORD como o conteúdo.

Para associar uma constante no tempo de registro da lista de comandos, um comando semelhante ao seguinte seria usado:

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a>Adicionando uma exibição de buffer de constante raiz

![Adiciona uma exibição de buffer constante à assinatura raiz](images/root-tables-cbv.png)

Este exemplo mostra duas constantes raiz e uma CBV (exibição de buffer constante) de raiz que custa dois slots DWORD.

Para associar uma exibição de buffer constante, use um comando como o seguinte. Observe que o primeiro parâmetro (2) é o slot mostrado na imagem. Normalmente, uma matriz de constantes será configurada e disponibilizada para os sombreadores em B0 como um CBV.

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a>Tabelas de descritores de associação

![Adiciona tabelas de descritor à assinatura raiz](images/root-tables-2.png)

Este exemplo mostra o uso de duas tabelas de descritor; um declarando uma tabela de cinco descritores que estarão disponíveis no momento da execução em um \_ \_ heap de descritor cbv SRV UAV e outro declarando uma tabela de dois descritores que serão exibidos no momento da execução em um heap de descritor de amostra.

Para associar tabelas de descritor ao gravar uma lista de comandos.

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

Outro recurso da assinatura raiz é a constante raiz FLOAT4 que tem quatro DWORDs de tamanho. O comando a seguir associa apenas os dois DWORDs intermediários dos quatro.

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a>Uma assinatura de raiz mais complexa

![uma assinatura de raiz complexa com muitos elementos](images/root-tables-3.png)

Este exemplo mostra uma assinatura raiz densa com a maioria dos tipos de entradas. Duas das tabelas de descritores (nos slots 3 e 6) incluem matrizes de tamanho não associado. A carga aqui está no aplicativo apenas para tocar descritores válidos em um heap. Matrizes não associadas, ou muito grandes, exigem a camada de hardware 2 + do suporte de associação de recursos.

Há dois exemplos estáticos (vinculados sem a necessidade de Slots de assinatura raiz).

No slot 9, UAV U4 e UAV U5 são declarados no mesmo deslocamento da tabela de descritores. Esse é o uso de um descritor com alias, um descritor na memória aparecerá como U4 e U5 nos sombreadores HLSL. Nesse caso, o sombreador deve ser compilado com a \_ opção d3d10 do sombreador de \_ recursos \_ pode ser \_ alias ou a `/res_may_alias` opção or em FXC. Os descritores com alias permitem a vinculação de uma descrição a vários pontos de ligação, sem a necessidade de fazer nenhuma alteração nos sombreadores.

## <a name="streaming-shader-resource-views"></a>Exibições de recurso do sombreador de streaming

![exibições de recurso do sombreador de streaming nesta assinatura raiz](images/root-tables-4.png)

Essa assinatura raiz ilustra um cenário em que todos os SRVs são transmitidos e estão fora de uma matriz grande. No momento da execução, uma tabela de descritores pode ser definida uma vez quando a assinatura raiz é definida. Em seguida, todas as leituras de textura são feitas pela indexação na matriz por meio de constantes alimentadas por meio dos primeiros argumentos raiz. Apenas um único heap de descritor é necessário e só é atualizado conforme as texturas são transmitidas ou não de Slots de descritor livres.

Os deslocamentos do descritor no heap grande são identificados por sombreadores usando as constantes nas exibições do buffer de constantes. Por exemplo, se um sombreador receber uma ID de material, ele poderá indexar uma matriz grande usando a constante para acessar o descritor necessário (que faz referência à textura necessária).

Este cenário requer hardware com associação de recursos tier2 +.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Camadas de hardware de associação de recursos](hardware-support.md)
</dt> <dt>

[Associação de recursos em HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Assinaturas raiz](root-signatures.md)
</dt> </dl>

 

 




