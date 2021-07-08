---
title: Usando descritores diretamente na assinatura raiz
description: Para evitar a necessidade de passar por um heap de descritor, você pode colocar um descritor diretamente na assinatura raiz.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9d459f3195a4cf722ea210edbe63e5c1bf3cc8
ms.sourcegitcommit: 170bc12e9724d00cecbb96d57c7226c51e135dee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113489163"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Usando descritores diretamente na assinatura raiz

Para evitar a necessidade de passar por um heap de descritor, você pode colocar um descritor diretamente na assinatura raiz. Esses descritores ocupam muito espaço na assinatura raiz (consulte [limites de assinatura raiz](/windows/win32/direct3d12/root-signature-limits)), portanto, recomendamos que você os use com moderação.

Um exemplo de uso seria colocar no layout raiz uma CBV (exibição de buffer constante) que está sendo alterada por empate. Isso é para que o espaço de heap do descritor não precise ser alocado pelo aplicativo por empate (e salva o apontador de uma tabela de descritores no novo local no heap do descritor). Ao colocar algo na assinatura de raiz, o aplicativo está apenas entregando a responsabilidade de controle de versão para o driver; Mas essa é a infraestrutura que os drivers já têm.

Para a renderização que usa extremamente poucos recursos, o uso de tabela/heap de descritor pode não ser necessário se todos os descritores necessários puderem ser colocados diretamente na assinatura raiz.

Esses são os únicos tipos de descritores com suporte na assinatura raiz.

- CBVs (exibição de buffer constante).
- Modos de exibição de recurso do sombreador (SRVs)/exibições de acesso não ordenado (UAVs) de recursos de buffer em que a conversão de formato não é necessária (buffers não tipados). Alguns exemplos de buffers não tipados que podem ser associados a descritores raiz incluem `StructuredBuffer<type>` , `RWStructuredBuffer<type>` `ByteAddressBuffer` e `RWByteAddressBuffer` . Buffers tipados como `Buffer<uint>` e `Buffer<float2>` não podem.
- SRVs de estruturas de aceleração de raytracing, em assinaturas raiz locais ou globais. 

Um UAV na raiz não pode ter contadores associados a ele. Os descritores na assinatura raiz aparecem cada um dos descritores individuais separados &mdash; que não podem ser indexados dinamicamente.

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

No exemplo acima, `mySceneData` não pode ser declarado como uma matriz, como em `cbuffer mySceneData[2]` se ele for mapeado para um descritor na assinatura raiz. Isso ocorre porque a indexação entre descritores não tem suporte na assinatura raiz. Se desejar, você pode definir buffers de constantes individuais separados e defini-los como uma entrada separada na assinatura raiz. Observe que, dentro de `mySceneData` acima, há uma matriz `bar[2]` . A indexação dinâmica dentro do buffer de constantes é válida &mdash; um descritor na assinatura raiz se comporta exatamente como o mesmo descritor se ele fosse acessado por meio de um heap de descritor. Isso está em contraste com constantes de inalinhamento diretamente na assinatura raiz, que também aparece como um buffer constante, exceto com a restrição de que a indexação dinâmica dentro das constantes embutidas não é permitida, portanto, não seria `bar[2]` permitida lá.

Essas APIs (da interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) são para definir descritores diretamente na assinatura raiz.

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!NOTE]  
> Não há nenhum conceito de uma *matriz de descritor raiz* no Direct3D 12. As matrizes de descritores têm suporte apenas em heaps de descritor.

## <a name="related-topics"></a>Tópicos relacionados

* [Assinaturas raiz](root-signatures.md)
