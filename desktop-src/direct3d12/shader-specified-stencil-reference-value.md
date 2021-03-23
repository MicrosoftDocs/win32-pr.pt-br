---
title: Sombreador especificado valor de referência de estêncil (gráficos do Direct3D 12)
description: A habilitação de sombreadores de pixel para produzir o valor de referência do estêncil, em vez de usar o especificado pela API, permite um controle muito refinado sobre as operações de estêncil.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a8b7697cc06594b3e2ffc717cbded9e6832129
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548267"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a><span data-ttu-id="a222d-103">Sombreador especificado valor de referência de estêncil (gráficos do Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="a222d-103">Shader Specified Stencil Reference Value (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="a222d-104">A habilitação de sombreadores de pixel para produzir o valor de referência do estêncil, em vez de usar o especificado pela API, permite um controle muito refinado sobre as operações de estêncil.</span><span class="sxs-lookup"><span data-stu-id="a222d-104">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="a222d-105">O valor de referência de estêncil normalmente é especificado pelo método [**ID3D12GraphicsCommandList:: OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) .</span><span class="sxs-lookup"><span data-stu-id="a222d-105">The Stencil Reference Value is normally specified by the [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) method.</span></span> <span data-ttu-id="a222d-106">Esse método define o valor de referência do estêncil em uma granularidade por empate.</span><span class="sxs-lookup"><span data-stu-id="a222d-106">This method sets the stencil reference value on a per-draw granularity.</span></span> <span data-ttu-id="a222d-107">No entanto, esse valor pode ser substituído pelo sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="a222d-107">However, this value can be overwritten by the pixel shader.</span></span>

<span data-ttu-id="a222d-108">Esse recurso D3D12 (e D3D 11.3) permite que os desenvolvedores leiam e usem o valor de referência do estêncil (*VA \_ StencilRef*) que é impresso a partir de um sombreador de pixel, permitindo uma granularidade por pixel ou por amostra.</span><span class="sxs-lookup"><span data-stu-id="a222d-108">This D3D12 (and D3D11.3) feature enables developers to read and use the Stencil Reference Value (*SV\_StencilRef*) that is output from a pixel shader, enabling a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="a222d-109">O valor especificado do sombreador substitui o valor de referência especificado pela API para essa invocação, o que significa que a alteração afeta o teste de estêncil e quando a operação de estêncil D3D12 do \_ estêncil \_ op \_ replace (um membro de [**\_ \_ op D3D12 stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) é usada para gravar o valor de referência no buffer do estêncil.</span><span class="sxs-lookup"><span data-stu-id="a222d-109">The shader specified value replaces the API-specified reference value for that invocation, which means the change affects both the stencil test, and when the stencil operation D3D12\_STENCIL\_OP\_REPLACE (one member of [**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="a222d-110">Esse recurso é opcional no D3D12 e no D3D 11.3.</span><span class="sxs-lookup"><span data-stu-id="a222d-110">This feature is optional in both D3D12 and D3D11.3.</span></span> <span data-ttu-id="a222d-111">Para testar seu suporte, verifique o campo booliano *PSSpecifiedStencilRefSupported* das [**\_ Opções de \_ \_ D3D12 de \_ dados de recurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) usando [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="a222d-111">To test for its support, check the *PSSpecifiedStencilRefSupported* boolean field of [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

<span data-ttu-id="a222d-112">Aqui está um exemplo do uso de *\_ StencilRef de VA* em um sombreador de pixel:</span><span class="sxs-lookup"><span data-stu-id="a222d-112">Here is an example of the use of *SV\_StencilRef* in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="a222d-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a222d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a222d-114">Renderização</span><span class="sxs-lookup"><span data-stu-id="a222d-114">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="a222d-115">Associação de recursos em HLSL</span><span class="sxs-lookup"><span data-stu-id="a222d-115">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="a222d-116">Modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="a222d-116">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="a222d-117">Especificando assinaturas raiz em HLSL</span><span class="sxs-lookup"><span data-stu-id="a222d-117">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
