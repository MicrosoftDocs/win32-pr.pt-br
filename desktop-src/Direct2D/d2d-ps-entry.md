---
title: Função D2D_PS_ENTRY (D2d1effecthelpers. h)
description: Uma macro que define um ponto de entrada de sombreador de pixel com o nome de função fornecido.
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- Função D2D_PS_ENTRY Direct2D
topic_type:
- apiref
api_name:
- D2D_PS_ENTRY
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7525416eed7700709d02d2ec17823cd57a8c12ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755373"
---
# <a name="d2d_ps_entry-function"></a><span data-ttu-id="36f91-104">Função de entrada do \_ PS D2D \_</span><span class="sxs-lookup"><span data-stu-id="36f91-104">D2D\_PS\_ENTRY function</span></span>

<span data-ttu-id="36f91-105">Uma macro que define um ponto de entrada de sombreador de pixel com o nome de função fornecido.</span><span class="sxs-lookup"><span data-stu-id="36f91-105">A macro that defines a pixel shader entry point with the given function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f91-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36f91-106">Syntax</span></span>

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a><span data-ttu-id="36f91-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36f91-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36f91-108">*Entryname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="36f91-108">*Entryname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36f91-109">O nome do ponto de entrada do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="36f91-109">The pixel shader entry point name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36f91-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36f91-110">Return value</span></span>

<span data-ttu-id="36f91-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="36f91-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36f91-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="36f91-112">Remarks</span></span>

<span data-ttu-id="36f91-113">Use essa macro em vez de especificar a assinatura de entrada do ponto de entrada da maneira normal: todos os parâmetros são implícitos e adicionados pelo Direct2D durante a compilação, dependendo do tipo de destino de compilação (sombreador completo ou função de exportação).</span><span class="sxs-lookup"><span data-stu-id="36f91-113">Use this macro instead of specifying the entry point s input signature in the normal manner: all parameters are implicit and added by Direct2D during compilation depending on the compilation target type (full shader or export function).</span></span>

``` syntax
#define D2D_INPUT_COUNT 1 
#define D2D_INPUT0_SIMPLE 
#include  d2d1effectauthor.hlsli  

D2D_PS_ENTRY(LinkingCompatiblePixelShader) 
{ 
    float4 input = D2DGetInput(0);  

    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="36f91-114">Neste exemplo curto, observe que nenhum parâmetro de função é declarado, que o número de entradas e o tipo de cada entrada é declarado antes da função de entrada, a entrada é recuperada chamando [D2DGetInput](d2dgetinput.md)e as diretivas de pré-processador devem ser definidas antes de o arquivo auxiliar ser incluído.</span><span class="sxs-lookup"><span data-stu-id="36f91-114">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="36f91-115">Um sombreador compatível com vinculação deve fornecer um sombreador de pixel de passagem simples regular e uma função de sombreador de exportação.</span><span class="sxs-lookup"><span data-stu-id="36f91-115">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="36f91-116">A \_ macro de entrada do PS D2D \_ permite que cada um deles seja gerado a partir do mesmo código, quando usado em conjunto com o script de compilação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="36f91-116">The D2D\_PS\_ENTRY macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="36f91-117">Ao compilar um sombreador completo, as macros são expandidas no código a seguir, que tem uma assinatura de entrada compatível com efeitos de D2D.</span><span class="sxs-lookup"><span data-stu-id="36f91-117">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

``` syntax
Texture2D<float4> InputTexture0; 
SamplerState InputSampler0; 

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,   
    float4 posScene : SCENE_POSITION,    
    float4 uv0  : TEXCOORD0 
    ) : SV_Target 
{ 
    float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);  

    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="36f91-118">Ao compilar uma versão de função de exportação do mesmo código, o código a seguir é gerado:</span><span class="sxs-lookup"><span data-stu-id="36f91-118">When compiling an export function version of the same code, the following code is generated:</span></span>

``` syntax
// Shader function version 
export float4 LinkingCompatiblePixelShader_Function( 
    float4 input0 : INPUT0 
    ) 
{ 
    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="36f91-119">Observe que a entrada de textura, normalmente recuperada por amostragem de um Texture2D, foi substituída por um input0 de entrada de função.</span><span class="sxs-lookup"><span data-stu-id="36f91-119">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input input0.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f91-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36f91-120">Requirements</span></span>



| <span data-ttu-id="36f91-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="36f91-121">Requirement</span></span> | <span data-ttu-id="36f91-122">Valor</span><span class="sxs-lookup"><span data-stu-id="36f91-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36f91-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36f91-123">Header</span></span><br/> | <dl> <span data-ttu-id="36f91-124"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="36f91-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="36f91-125">DLL</span><span class="sxs-lookup"><span data-stu-id="36f91-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="36f91-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36f91-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="36f91-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="36f91-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f91-128">Vinculação de Sombreador de Efeito</span><span class="sxs-lookup"><span data-stu-id="36f91-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="36f91-129">Auxiliares de HLSL</span><span class="sxs-lookup"><span data-stu-id="36f91-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





