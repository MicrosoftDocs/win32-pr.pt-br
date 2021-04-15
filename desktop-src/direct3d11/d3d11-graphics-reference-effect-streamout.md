---
title: Sintaxe de fluxo horizontal
description: Um sombreador Geometry com fluxo horizontal é declarado com uma sintaxe específica.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ea78d1b2109e343f01800b3a3d5e1bf6efaba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988511"
---
# <a name="stream-out-syntax"></a><span data-ttu-id="b15e1-103">Sintaxe de fluxo horizontal</span><span class="sxs-lookup"><span data-stu-id="b15e1-103">Stream Out Syntax</span></span>

<span data-ttu-id="b15e1-104">Um sombreador Geometry com fluxo horizontal é declarado com uma sintaxe específica.</span><span class="sxs-lookup"><span data-stu-id="b15e1-104">A geometry shader with stream out is declared with a particular syntax.</span></span> <span data-ttu-id="b15e1-105">Este tópico descreve a sintaxe do.</span><span class="sxs-lookup"><span data-stu-id="b15e1-105">This topic describes the syntax.</span></span> <span data-ttu-id="b15e1-106">No tempo de execução do efeito, essa sintaxe será convertida em uma chamada para [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span><span class="sxs-lookup"><span data-stu-id="b15e1-106">In the effect runtime, this syntax will be converted to a call to [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span></span>

## <a name="construct-syntax"></a><span data-ttu-id="b15e1-107">Sintaxe de construção</span><span class="sxs-lookup"><span data-stu-id="b15e1-107">Construct Syntax</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| <span data-ttu-id="b15e1-108">Name</span><span class="sxs-lookup"><span data-stu-id="b15e1-108">Name</span></span>                   | <span data-ttu-id="b15e1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b15e1-109">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b15e1-110">**StreamingShaderVar**</span><span class="sxs-lookup"><span data-stu-id="b15e1-110">**StreamingShaderVar**</span></span> | <span data-ttu-id="b15e1-111">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b15e1-111">Optional.</span></span> <span data-ttu-id="b15e1-112">Uma cadeia de caracteres ASCI que identifica exclusivamente o nome de uma variável de sombreador de geometria com fluxo de saída. Isso é opcional porque ConstructGSWithSO pode ser colocado diretamente em uma chamada SetGeometryShader ou BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="b15e1-112">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="b15e1-113">**ShaderVar**</span><span class="sxs-lookup"><span data-stu-id="b15e1-113">**ShaderVar**</span></span>          | <span data-ttu-id="b15e1-114">Uma variável de sombreador de geometria ou de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="b15e1-114">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="b15e1-115">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="b15e1-115">**OutputDecl0**</span></span>        | <span data-ttu-id="b15e1-116">Uma cadeia de caracteres que define quais saídas de sombreador no fluxo 0 são transmitidas. Veja abaixo a sintaxe.</span><span class="sxs-lookup"><span data-stu-id="b15e1-116">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |



 

<span data-ttu-id="b15e1-117">Esta é a sintaxe definida em arquivos FX \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="b15e1-117">This is the syntax was defined in fx\_4\_0 files.</span></span> <span data-ttu-id="b15e1-118">Observe que nos \_ \_ sombreadores GS 4 0 e vs \_ x, há apenas um fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="b15e1-118">Note that in gs\_4\_0 and vs\_x shaders, there is only one stream of data.</span></span> <span data-ttu-id="b15e1-119">O sombreador resultante produzirá um fluxo para a unidade de streaming e a unidade do rasterizador.</span><span class="sxs-lookup"><span data-stu-id="b15e1-119">The resulting shader will output one stream to both the stream out unit and the rasterizer unit.</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| <span data-ttu-id="b15e1-120">Name</span><span class="sxs-lookup"><span data-stu-id="b15e1-120">Name</span></span>                   | <span data-ttu-id="b15e1-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="b15e1-121">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b15e1-122">**StreamingShaderVar**</span><span class="sxs-lookup"><span data-stu-id="b15e1-122">**StreamingShaderVar**</span></span> | <span data-ttu-id="b15e1-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b15e1-123">Optional.</span></span> <span data-ttu-id="b15e1-124">Uma cadeia de caracteres ASCI que identifica exclusivamente o nome de uma variável de sombreador de geometria com fluxo de saída. Isso é opcional porque ConstructGSWithSO pode ser colocado diretamente em uma chamada SetGeometryShader ou BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="b15e1-124">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="b15e1-125">**ShaderVar**</span><span class="sxs-lookup"><span data-stu-id="b15e1-125">**ShaderVar**</span></span>          | <span data-ttu-id="b15e1-126">Uma variável de sombreador de geometria ou de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="b15e1-126">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="b15e1-127">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="b15e1-127">**OutputDecl0**</span></span>        | <span data-ttu-id="b15e1-128">Uma cadeia de caracteres que define quais saídas de sombreador no fluxo 0 são transmitidas. Veja abaixo a sintaxe.</span><span class="sxs-lookup"><span data-stu-id="b15e1-128">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="b15e1-129">**OutputDecl1**</span><span class="sxs-lookup"><span data-stu-id="b15e1-129">**OutputDecl1**</span></span>        | <span data-ttu-id="b15e1-130">Uma cadeia de caracteres que define quais saídas de sombreador no fluxo 1 são transmitidas. Veja abaixo a sintaxe.</span><span class="sxs-lookup"><span data-stu-id="b15e1-130">A string defining which shader outputs in stream 1 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="b15e1-131">**OutputDecl2**</span><span class="sxs-lookup"><span data-stu-id="b15e1-131">**OutputDecl2**</span></span>        | <span data-ttu-id="b15e1-132">Uma cadeia de caracteres que define quais saídas de sombreador no fluxo 2 são transmitidas. Veja abaixo a sintaxe.</span><span class="sxs-lookup"><span data-stu-id="b15e1-132">A string defining which shader outputs in stream 2 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="b15e1-133">**OutputDecl3**</span><span class="sxs-lookup"><span data-stu-id="b15e1-133">**OutputDecl3**</span></span>        | <span data-ttu-id="b15e1-134">Uma cadeia de caracteres que define quais saídas de sombreador no fluxo 3 são transmitidas. Veja abaixo a sintaxe.</span><span class="sxs-lookup"><span data-stu-id="b15e1-134">A string defining which shader outputs in stream 3 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="b15e1-135">**RasterizedStream**</span><span class="sxs-lookup"><span data-stu-id="b15e1-135">**RasterizedStream**</span></span>   | <span data-ttu-id="b15e1-136">Um inteiro que especifica qual fluxo será enviado ao rasterizador.</span><span class="sxs-lookup"><span data-stu-id="b15e1-136">An integer specifying which stream will be sent to the rasterizer.</span></span>                                                                                                                                                         |



 

<span data-ttu-id="b15e1-137">Observe que \_ \_ os sombreadores GS 5 0 podem definir até quatro fluxos de dados.</span><span class="sxs-lookup"><span data-stu-id="b15e1-137">Note that gs\_5\_0 shaders can define up to four streams of data.</span></span> <span data-ttu-id="b15e1-138">O sombreador resultante produzirá uma transmissão para a unidade de saída de fluxo para cada declaração de saída não **nula** e uma transmitirá a unidade rasterizadora.</span><span class="sxs-lookup"><span data-stu-id="b15e1-138">The resulting shader will output one stream to the stream out unit for each non-**NULL** output declaration and one stream the rasterizer unit.</span></span>

## <a name="stream-out-declaration-syntax"></a><span data-ttu-id="b15e1-139">Sintaxe de declaração de saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="b15e1-139">Stream Out Declaration Syntax</span></span>


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| <span data-ttu-id="b15e1-140">Name</span><span class="sxs-lookup"><span data-stu-id="b15e1-140">Name</span></span>              | <span data-ttu-id="b15e1-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="b15e1-141">Description</span></span>                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b15e1-142">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="b15e1-142">**Buffer**</span></span>        | <span data-ttu-id="b15e1-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b15e1-143">Optional.</span></span> <span data-ttu-id="b15e1-144">Um número inteiro, 0 <= buffer < 4, especificando o fluxo de buffer de saída ao qual o valor será acessado.</span><span class="sxs-lookup"><span data-stu-id="b15e1-144">An integer, 0 <= Buffer < 4, specifying which stream out buffer the value will go to.</span></span> |
| <span data-ttu-id="b15e1-145">**Semântico**</span><span class="sxs-lookup"><span data-stu-id="b15e1-145">**Semantic**</span></span>      | <span data-ttu-id="b15e1-146">Uma cadeia de caracteres, junto com SemanticIndex, especificando qual valor deve ser impresso.</span><span class="sxs-lookup"><span data-stu-id="b15e1-146">A string, along with SemanticIndex, specifying which value to output.</span></span>                                 |
| <span data-ttu-id="b15e1-147">**SemanticIndex**</span><span class="sxs-lookup"><span data-stu-id="b15e1-147">**SemanticIndex**</span></span> | <span data-ttu-id="b15e1-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b15e1-148">Optional.</span></span> <span data-ttu-id="b15e1-149">O índice associado à semântica.</span><span class="sxs-lookup"><span data-stu-id="b15e1-149">The index associated with Semantic.</span></span>                                                         |
| <span data-ttu-id="b15e1-150">**Mask**</span><span class="sxs-lookup"><span data-stu-id="b15e1-150">**Mask**</span></span>          | <span data-ttu-id="b15e1-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b15e1-151">Optional.</span></span> <span data-ttu-id="b15e1-152">Uma máscara de componente, que indica os componentes do valor a serem gerados.</span><span class="sxs-lookup"><span data-stu-id="b15e1-152">A component mask, indicating which components of the value to output.</span></span>                       |



 

<span data-ttu-id="b15e1-153">Há uma semântica especial, rotulada "$SKIP", que indica uma semântica vazia, deixando a memória correspondente no buffer de saída de fluxo inalterado.</span><span class="sxs-lookup"><span data-stu-id="b15e1-153">There is one special Semantic, labeled "$SKIP" which indicates an empty semantic, leaving the corresponding memory in the stream out buffer untouched.</span></span> <span data-ttu-id="b15e1-154">A semântica de $SKIP não pode ter um SemanticIndex, mas pode ter uma máscara.</span><span class="sxs-lookup"><span data-stu-id="b15e1-154">The $SKIP semantic cannot have a SemanticIndex, but can have a Mask.</span></span>

<span data-ttu-id="b15e1-155">A declaração de saída do fluxo inteiro pode ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="b15e1-155">The entire stream out declaration can be **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="b15e1-156">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b15e1-156">Example</span></span>


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="b15e1-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b15e1-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b15e1-158">Efeitos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="b15e1-158">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




