---
title: Usando descritores diretamente na assinatura raiz
description: Para evitar a necessidade de passar por um heap de descritor, você pode colocar um descritor diretamente na assinatura raiz.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3f32b423b017477e66ea3ae32eee509ec455d85
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813227"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Usando descritores diretamente na assinatura raiz

Para evitar a necessidade de passar por um heap de descritor, você pode colocar um descritor diretamente na assinatura raiz. Esses descritores usam muito espaço na assinatura raiz (consulte Limites de assinatura [raiz),](./root-signature-limits.md)portanto, recomendamos que você os use com moderação.

Um exemplo de uso seria colocar no layout raiz uma exibição de buffer constante (CBV) que está mudando por desenho. Isso é para que o espaço de heap do descritor não tenha que ser alocado pelo aplicativo por desenho (e salva apontando uma tabela de descritor para o novo local no heap do descritor). Ao colocar algo na assinatura raiz, o aplicativo está simplesmente entregando a responsabilidade de controle de versão ao driver; mas essa é a infraestrutura que os drivers já têm.

Para renderização que usa poucos recursos, o uso de tabela/heap do descritor poderá não ser necessário se todos os descritores necessários puderem ser colocados diretamente na assinatura raiz.

Esses são os únicos tipos de descritores com suporte na assinatura raiz.

- Exibição de buffer constante (CBVs).
- Exibições de recursos do sombreador (SRVs) /UAVs (exibições de acesso não organizados) de recursos de buffer em que a conversão de formato não é necessária (buffers sem tipo). Alguns exemplos de buffers sem tipo que podem ser vinculados com descritores raiz incluem `StructuredBuffer<type>` `RWStructuredBuffer<type>` , e `ByteAddressBuffer` `RWByteAddressBuffer` . Buffers digitados, `Buffer<uint>` como e não `Buffer<float2>` podem.
- SRVs de estruturas de aceleração de raytracing, em assinaturas raiz locais ou globais. 

Um UAV na raiz não pode ter contadores associados a ele. Os descritores na assinatura raiz aparecem cada um como descritores separados individuais &mdash; que não podem ser indexados dinamicamente.

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

No exemplo acima, não pode ser declarado como uma matriz, como em se ela for mapeada para um descritor na `mySceneData` `cbuffer mySceneData[2]` assinatura raiz. Isso porque a indexação entre descritores não tem suporte na assinatura raiz. Se desejado, você pode definir buffers constantes individuais separados e defini-los como uma entrada separada na assinatura raiz. Observe que, `mySceneData` acima, há uma matriz `bar[2]` . A indexação dinâmica dentro do buffer constante é válida, um descritor na assinatura raiz se comporta da mesma forma que o mesmo descritor se comportaria se fosse acessado por meio de um &mdash; heap de descritor. Isso contrasta com constantes em inlining diretamente na assinatura raiz, que também aparece como um buffer constante, exceto pela restrição de que a indexação dinâmica dentro das constantes em inlined não é permitida, portanto, não seria permitido `bar[2]` lá.

Essas APIs (da interface [**ID3D12GraphicsCommandList)**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) são para definir descritores diretamente na assinatura raiz.

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!NOTE]  
> Não há nenhum conceito de uma matriz *de descritor raiz* no Direct3D 12. As matrizes de descritor têm suporte apenas em heaps de descritor.

## <a name="related-topics"></a>Tópicos relacionados

* [Assinaturas raiz](root-signatures.md)