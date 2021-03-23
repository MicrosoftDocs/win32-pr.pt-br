---
title: Usar descritores diretamente na assinatura raiz
description: Os aplicativos podem colocar os descritores diretamente na assinatura raiz para evitar ter de passar por um heap de descritor.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/15/2020
ms.locfileid: "104548310"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>Usar descritores diretamente na assinatura raiz

Os aplicativos podem colocar os descritores diretamente na assinatura raiz para evitar ter de passar por um heap de descritor. Esses descritores demoram muito espaço na assinatura raiz (consulte a seção limites de assinatura raiz), de modo que os aplicativos precisam usá-los com moderação.

Um exemplo de uso seria colocar uma constante CBV (exibições de buffer) que está sendo alterada por empate no layout raiz para que o espaço de heap do descritor não precise ser alocado pelo aplicativo por empate (e salve o ponteiro de uma tabela de descritores no novo local no heap do descritor). Ao colocar algo na assinatura de raiz, o aplicativo está apenas entregando a responsabilidade de controle de versão para o driver, mas essa é a infraestrutura que eles já têm.

Para a renderização que usa extremamente poucos recursos, o uso de tabela/heap de descritor poderá não ser necessário se todos os descritores necessários puderem ser colocados diretamente na assinatura raiz.

Os únicos tipos de descritores com suporte na assinatura raiz são:
- CBVs.
- SRVs (Shader Resource views)/unordered Access views (UAVs) de recursos de buffer em que o formato SRV/UAV contém apenas componentes de 32 bit FLOAT/UINT/Santo (não há conversão de formato).
- SRVs de estruturas de aceleração de raytracing, em assinaturas raiz locais ou globais. 

UAVs na raiz não pode ter contadores associados a eles. Os descritores na assinatura raiz aparecem cada um dos descritores individuais separados &mdash; que não podem ser indexados dinamicamente.

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

No exemplo acima, `mySceneData` não pode ser declarado como uma matriz, como em `cbuffer mySceneData[2]` se ele for mapeado para um descritor na assinatura raiz, já que a indexação entre descritores não é suportada na assinatura raiz. O aplicativo pode definir buffers de constantes individuais separados e defini-los como uma entrada separada na assinatura raiz, se desejado. Observe que, dentro de `mySceneData` acima, há uma matriz `bar[2]` . A indexação dinâmica no buffer de constantes é válida-um descritor na assinatura raiz se comporta exatamente como o mesmo descritor se for acessado por meio de um heap de descritor. Isso está em contraste com constantes de inalinhamento diretamente na assinatura raiz, que também aparece como um buffer constante, exceto com a restrição de que a indexação dinâmica dentro das constantes embutidas não é permitida, portanto, `bar[2]` não seria permitida lá.

As APIs a seguir (da interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) são para definir os descritores diretamente na assinatura raiz:

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> Não há nenhum conceito de "matriz de descritor raiz" no Direct3D 12. Só há suporte para matrizes de descritores em heaps de descritores.

## <a name="related-topics"></a>Tópicos relacionados

[Assinaturas raiz](root-signatures.md)
