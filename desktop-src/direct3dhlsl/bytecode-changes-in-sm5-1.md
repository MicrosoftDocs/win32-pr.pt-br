---
title: Alterações de código de bytes no SM 5.1
description: O SM 5.1 altera como os registros de recursos são declarados e referenciados em instruções.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d66db788b0012a1c3221e37d4c2dd4e41566c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292886"
---
# <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="e5b14-103">Alterações de código de bytes no SM 5.1</span><span class="sxs-lookup"><span data-stu-id="e5b14-103">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="e5b14-104">O SM 5.1 altera como os registros de recursos são declarados e referenciados em instruções.</span><span class="sxs-lookup"><span data-stu-id="e5b14-104">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span>

<span data-ttu-id="e5b14-105">O SM 5.1 se move para declarar uma "variável" de registro, semelhante ao modo como é feito para registros de memória compartilhada de grupo, ilustrado pelo exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="e5b14-105">SM5.1 moves towards declaring a register “variable”, similar to how it is done for group shared memory registers, illustrated by the following example:</span></span>

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

<span data-ttu-id="e5b14-106">A desmontagem deste exemplo segue:</span><span class="sxs-lookup"><span data-stu-id="e5b14-106">The disassembly of this example follows:</span></span>

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim Space Slot  Elements
// ------------------------------ ---------- ------- ----------- ----- ---- ---------
// samp0                             sampler      NA          NA     0    5         1
// tex0                              texture  float4          2d     0    5         1
// tex1[0][5][3]                     texture  float4          2d     0   10 unbounded
// tex2[8]                           texture  float4          2d     1    0         8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots used
```

<span data-ttu-id="e5b14-107">Cada intervalo de recursos do sombreador agora tem uma ID (um nome) no código de bytes do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e5b14-107">Each shader resource range now has an ID (a name) in the shader bytecode.</span></span> <span data-ttu-id="e5b14-108">Por exemplo, a matriz de textura tex1 se torna 1 ' no código de byte do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e5b14-108">For example, tex1 texture array becomes ‘t1’ in the shader byte code.</span></span> <span data-ttu-id="e5b14-109">Atribuir IDs exclusivas a cada intervalo de recursos permite duas coisas:</span><span class="sxs-lookup"><span data-stu-id="e5b14-109">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="e5b14-110">Identifique de forma não ambígua qual intervalo de recursos (consulte o \_ recurso DCL \_ Texture2D) está sendo indexado em uma instrução (consulte a instrução de exemplo).</span><span class="sxs-lookup"><span data-stu-id="e5b14-110">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="e5b14-111">Anexe o conjunto de atributos à declaração, por exemplo, tipo de elemento, tamanho de Stride, modo de operação de varredura, etc..</span><span class="sxs-lookup"><span data-stu-id="e5b14-111">Attach set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc..</span></span>

<span data-ttu-id="e5b14-112">Observe que a ID do intervalo não está relacionada à declaração de limite inferior do HLSL.</span><span class="sxs-lookup"><span data-stu-id="e5b14-112">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="e5b14-113">A ordem das associações de recursos de reflexão e as instruções de declaração do sombreador são as mesmas para auxiliar na identificação da correspondência entre as variáveis HLSL e as IDs do código de bytes.</span><span class="sxs-lookup"><span data-stu-id="e5b14-113">The order of reflection resource bindings and shader declaration instructions is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="e5b14-114">Cada instrução de declaração no SM 5.1 usa um operando 3D para definir: ID de intervalo, limites inferiores e superiores.</span><span class="sxs-lookup"><span data-stu-id="e5b14-114">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="e5b14-115">Um token adicional é emitido para especificar o espaço de registro.</span><span class="sxs-lookup"><span data-stu-id="e5b14-115">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="e5b14-116">Outros tokens podem ser emitidos também para transmitir propriedades adicionais do intervalo, por exemplo, CBuffer ou instrução de declaração de buffer estruturado emite o tamanho do CBuffer ou da estrutura.</span><span class="sxs-lookup"><span data-stu-id="e5b14-116">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="e5b14-117">Os detalhes exatos da codificação podem ser encontrados em d3d12TokenizedProgramFormat. h e D3D10ShaderBinary:: CShaderCodeParser.</span><span class="sxs-lookup"><span data-stu-id="e5b14-117">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and D3D10ShaderBinary::CShaderCodeParser.</span></span>

<span data-ttu-id="e5b14-118">As instruções do SM 5.1 não emitirão informações adicionais do operando de recurso como parte da instrução (como no SM 5.0).</span><span class="sxs-lookup"><span data-stu-id="e5b14-118">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="e5b14-119">Essas informações agora são movidas para as instruções de declaração.</span><span class="sxs-lookup"><span data-stu-id="e5b14-119">This information is now moved to the declaration instructions.</span></span> <span data-ttu-id="e5b14-120">No SM 5.0, as instruções de indexação de recursos exigiam atributos de recurso a serem descritos em tokens de opcode estendidos, já que a indexação ofusca a associação à declaração.</span><span class="sxs-lookup"><span data-stu-id="e5b14-120">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="e5b14-121">No SM 5.1, cada ID (como ' t 1 ') está inequívocamente associada a uma única declaração que descreve as informações de recurso necessárias.</span><span class="sxs-lookup"><span data-stu-id="e5b14-121">In SM5.1 each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="e5b14-122">Portanto, os tokens de opcode estendidos usados em instruções para descrever as informações de recursos não são mais emitidos.</span><span class="sxs-lookup"><span data-stu-id="e5b14-122">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="e5b14-123">Em instruções de não declaração, um operando de recurso para amostras, SRVs e UAVs é um operando 2D.</span><span class="sxs-lookup"><span data-stu-id="e5b14-123">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="e5b14-124">O primeiro índice é uma constante literal que especifica a ID do intervalo.</span><span class="sxs-lookup"><span data-stu-id="e5b14-124">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="e5b14-125">O segundo índice representa o valor linear do índice.</span><span class="sxs-lookup"><span data-stu-id="e5b14-125">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="e5b14-126">O valor é calculado em relação ao início do espaço de registro correspondente (não relativo ao início do intervalo lógico) para correlacionar melhor com a assinatura raiz e para reduzir a carga do compilador de driver de ajustar o índice.</span><span class="sxs-lookup"><span data-stu-id="e5b14-126">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="e5b14-127">Um operando de recurso para CBVs é um operando 3D: ID literal do intervalo, índice de CBuffer, offset na instância específica de CBuffer.</span><span class="sxs-lookup"><span data-stu-id="e5b14-127">A resource operand for CBVs is a 3D operand: literal ID of the range, index of the cbuffer, offset into the particular instance of cbuffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5b14-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5b14-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5b14-129">Recursos do HLSL Shader Model 5,1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e5b14-129">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="e5b14-130">Modelo do sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="e5b14-130">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> </dl>

 

 




