---
title: RestartStrip (objeto Stream-Output DirectX HLSL)
description: Encerra a faixa primitiva atual e inicia uma nova faixa. Se a faixa atual não tiver vértices suficientes emitidos para preencher a topologia primitiva, o primitivo incompleto no final será Descartado.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aafd6407d556a6d0b4269c38192107edbc7cb1fa
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120191"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a><span data-ttu-id="6341c-104">RestartStrip (objeto Stream-Output DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6341c-104">RestartStrip (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="6341c-105">Encerra a faixa primitiva atual e inicia uma nova faixa.</span><span class="sxs-lookup"><span data-stu-id="6341c-105">Ends the current primitive strip and starts a new strip.</span></span> <span data-ttu-id="6341c-106">Se a faixa atual não tiver vértices suficientes emitidos para preencher a topologia primitiva, o primitivo incompleto no final será Descartado.</span><span class="sxs-lookup"><span data-stu-id="6341c-106">If the current strip does not have enough vertices emitted to fill the primitive topology, the incomplete primitive at the end will be discarded.</span></span>

<span data-ttu-id="6341c-107">RestartStrip();</span><span class="sxs-lookup"><span data-stu-id="6341c-107">RestartStrip();</span></span>



 

## <a name="parameters"></a><span data-ttu-id="6341c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6341c-108">Parameters</span></span>



| <span data-ttu-id="6341c-109">Item</span><span class="sxs-lookup"><span data-stu-id="6341c-109">Item</span></span>                                                                                     | <span data-ttu-id="6341c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6341c-110">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="6341c-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span><span class="sxs-lookup"><span data-stu-id="6341c-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="6341c-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6341c-112">Return Value</span></span>

<span data-ttu-id="6341c-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6341c-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="6341c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6341c-114">Remarks</span></span>

<span data-ttu-id="6341c-115">Um corte de faixa faz com que a faixa atual termine e uma nova faixa seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="6341c-115">A strip cut causes the current strip to end, and a new strip to start.</span></span> <span data-ttu-id="6341c-116">Uma faixa de corte pode ser feita chamando explicitamente esse método ou apenas renderizando até o valor de índice máximo (1, que é 0xFFFFFFFF para índices de 32 bits ou 0xFFFF para índices de 16 bits).</span><span class="sxs-lookup"><span data-stu-id="6341c-116">A strip cut can be done by explicitly calling this method, or just by rendering up to the maximum index value ( 1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices).</span></span> <span data-ttu-id="6341c-117">Cada instância de um desenho de instância indexada gera um corte automático de uma faixa.</span><span class="sxs-lookup"><span data-stu-id="6341c-117">Each instance of an indexed-instanced draw generates a strip cut automatically.</span></span> <span data-ttu-id="6341c-118">Isso é verdadeiro mesmo que a topologia não seja uma faixa de triângulo.</span><span class="sxs-lookup"><span data-stu-id="6341c-118">This is true even if the topology is not a triangle strip.</span></span>

> [!Note]  
> <span data-ttu-id="6341c-119">O suporte para reinicialização e o 1 ' valor mágico ' para um recorte só está disponível no [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 ou dispositivos superiores.</span><span class="sxs-lookup"><span data-stu-id="6341c-119">Support for restart and the  1 'magic value' for a cut is only available on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 or higher devices.</span></span>

 

<span data-ttu-id="6341c-120">A saída é sempre considerada uma faixa de triângulo.</span><span class="sxs-lookup"><span data-stu-id="6341c-120">The output is always assumed to be a triangle strip.</span></span> <span data-ttu-id="6341c-121">Para fazer a saída de uma lista de triângulos, você deve chamar RestartStrip entre cada triângulo.</span><span class="sxs-lookup"><span data-stu-id="6341c-121">To make the output a triangle list, you must call RestartStrip between each triangle.</span></span> <span data-ttu-id="6341c-122">Não há suporte para ventiladores de triângulo.</span><span class="sxs-lookup"><span data-stu-id="6341c-122">Triangle fans are unsupported.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="6341c-123">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6341c-123">Minimum Shader Model</span></span>

<span data-ttu-id="6341c-124">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6341c-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6341c-125">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6341c-125">Shader Model</span></span>                                              | <span data-ttu-id="6341c-126">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6341c-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6341c-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6341c-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6341c-128">yes</span><span class="sxs-lookup"><span data-stu-id="6341c-128">yes</span></span>       |
| [<span data-ttu-id="6341c-129">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6341c-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6341c-130">não</span><span class="sxs-lookup"><span data-stu-id="6341c-130">no</span></span>        |
| [<span data-ttu-id="6341c-131">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6341c-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6341c-132">não</span><span class="sxs-lookup"><span data-stu-id="6341c-132">no</span></span>        |
| [<span data-ttu-id="6341c-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6341c-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6341c-134">não</span><span class="sxs-lookup"><span data-stu-id="6341c-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6341c-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6341c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6341c-136">Fluxo-objeto de saída</span><span class="sxs-lookup"><span data-stu-id="6341c-136">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

