---
title: Usando constantes diretamente na assinatura raiz
description: Os aplicativos podem definir constantes raiz na assinatura raiz, cada uma como um conjunto de valores de 32 bits. Eles aparecem na HLSL (linguagem de sombreamento de alto nível) como um buffer constante. Observe que os buffers de constante por motivos históricos são exibidos como conjuntos de valores de 4x32 bits.
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103949"
---
# <a name="using-constants-directly-in-the-root-signature"></a>Usando constantes diretamente na assinatura raiz

Os aplicativos podem definir constantes raiz na assinatura raiz, cada uma como um conjunto de valores de 32 bits. Eles aparecem na HLSL (linguagem de sombreamento de alto nível) como um buffer constante. Observe que os buffers de constante por motivos históricos são exibidos como conjuntos de valores de 4x32 bits.

Cada conjunto de constantes de usuário é tratado como uma matriz escalar de valores de 32 bits, indexáveis e somente leitura dinamicamente do sombreador. A indexação fora dos limites que indexa um determinado conjunto de constantes raiz produz resultados indefinidos. No HLSL, as definições de estrutura de dados podem ser fornecidas para que as constantes do usuário forneçam tipos. Por exemplo, se a assinatura raiz definir um conjunto de 4 constantes raiz, HLSL poderá sobrepor a estrutura a seguir.

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

As matrizes não são permitidas em buffers constantes que são mapeados para constantes raiz, pois não há suporte para a indexação dinâmica no espaço de assinatura raiz. Por exemplo, é inválido ter uma entrada no buffer de constantes como `float myArray[2];` . Um buffer de constantes que é mapeado para constantes raiz não pode ser uma matriz; Portanto, é inválido mapear para `cbuffer myCBArray[2]` constantes raiz.

As constantes podem ser parcialmente definidas. Por exemplo, se a assinatura raiz definir valores de 4 32 bits em *RootTableBindSlot* 2, qualquer subconjunto das quatro constantes poderá ser definido de cada vez (os outros permanecem inalterados). Isso pode ser útil em pacotes que herdam o estado da assinatura raiz e podem alterá-lo parcialmente.

Ao definir constantes, tenha cuidado com o layout de buffer constante esperado pelo sombreador. É possível que as constantes sejam preenchidas em `vec4` limites, por exemplo. Para verificar o layout esperado, verifique as informações de reflexo do sombreador HLSL.

As APIs a seguir (da interface [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) são para definir constantes diretamente na assinatura raiz:

-   [**SetGraphicsRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [**SetGraphicsRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [**SetComputeRoot32BitConstant**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

Além disso, consulte a estrutura de [**\_ \_ constantes raiz do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assinaturas raiz](root-signatures.md)
</dt> </dl>

 

 




