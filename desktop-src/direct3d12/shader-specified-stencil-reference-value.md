---
title: Sombreador especificado valor de referência de estêncil (gráficos do Direct3D 12)
description: Saiba mais sobre o valor de referência de estêncil nos gráficos do Direct3D 12. A habilitação de sombreadores de pixel para usar o valor de referência de estêncil permite um controle fino sobre as operações de estêncil.
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee212d7c2573402ad38bc19040e5c60a89c090
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408309"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a><span data-ttu-id="5baac-104">Sombreador especificado valor de referência de estêncil (gráficos do Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="5baac-104">Shader Specified Stencil Reference Value (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="5baac-105">A habilitação de sombreadores de pixel para produzir o valor de referência do estêncil, em vez de usar o especificado pela API, permite um controle muito refinado sobre as operações de estêncil.</span><span class="sxs-lookup"><span data-stu-id="5baac-105">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="5baac-106">O valor de referência de estêncil normalmente é especificado pelo método [**ID3D12GraphicsCommandList:: OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) .</span><span class="sxs-lookup"><span data-stu-id="5baac-106">The Stencil Reference Value is normally specified by the [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) method.</span></span> <span data-ttu-id="5baac-107">Esse método define o valor de referência do estêncil em uma granularidade por empate.</span><span class="sxs-lookup"><span data-stu-id="5baac-107">This method sets the stencil reference value on a per-draw granularity.</span></span> <span data-ttu-id="5baac-108">No entanto, esse valor pode ser substituído pelo sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="5baac-108">However, this value can be overwritten by the pixel shader.</span></span>

<span data-ttu-id="5baac-109">Esse recurso D3D12 (e D3D 11.3) permite que os desenvolvedores leiam e usem o valor de referência do estêncil (*VA \_ StencilRef*) que é impresso a partir de um sombreador de pixel, permitindo uma granularidade por pixel ou por amostra.</span><span class="sxs-lookup"><span data-stu-id="5baac-109">This D3D12 (and D3D11.3) feature enables developers to read and use the Stencil Reference Value (*SV\_StencilRef*) that is output from a pixel shader, enabling a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="5baac-110">O valor especificado do sombreador substitui o valor de referência especificado pela API para essa invocação, o que significa que a alteração afeta o teste de estêncil e quando a operação de estêncil D3D12 do \_ estêncil \_ op \_ replace (um membro de [**\_ \_ op D3D12 stencil**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) é usada para gravar o valor de referência no buffer do estêncil.</span><span class="sxs-lookup"><span data-stu-id="5baac-110">The shader specified value replaces the API-specified reference value for that invocation, which means the change affects both the stencil test, and when the stencil operation D3D12\_STENCIL\_OP\_REPLACE (one member of [**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="5baac-111">Esse recurso é opcional no D3D12 e no D3D 11.3.</span><span class="sxs-lookup"><span data-stu-id="5baac-111">This feature is optional in both D3D12 and D3D11.3.</span></span> <span data-ttu-id="5baac-112">Para testar seu suporte, verifique o campo booliano *PSSpecifiedStencilRefSupported* das [**\_ Opções de \_ \_ D3D12 de \_ dados de recurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) usando [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="5baac-112">To test for its support, check the *PSSpecifiedStencilRefSupported* boolean field of [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

<span data-ttu-id="5baac-113">Aqui está um exemplo do uso de *\_ StencilRef de VA* em um sombreador de pixel:</span><span class="sxs-lookup"><span data-stu-id="5baac-113">Here is an example of the use of *SV\_StencilRef* in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="5baac-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5baac-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5baac-115">Renderização</span><span class="sxs-lookup"><span data-stu-id="5baac-115">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="5baac-116">Associação de recursos no HLSL</span><span class="sxs-lookup"><span data-stu-id="5baac-116">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="5baac-117">Modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="5baac-117">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="5baac-118">Como especificar assinaturas raiz no HLSL</span><span class="sxs-lookup"><span data-stu-id="5baac-118">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
