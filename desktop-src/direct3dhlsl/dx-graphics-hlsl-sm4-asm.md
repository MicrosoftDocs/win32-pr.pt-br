---
title: Assembly do Shader Model 4
description: Assembly do Shader Model 4
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005555"
---
# <a name="shader-model-4-assembly"></a>Assembly do Shader Model 4

O Shader Model 4 exige a programação de sombreadores no HLSL. No entanto, o compilador do sombreador compila o código HLSL no assembly que é executado no dispositivo. Se você estiver usando o PIX para Windows para depurar seus sombreadores, poderá optar por exibir o código do sombreador em HLSL ou assembly. Esta seção lista as instruções de assembly do Shader Model 4 e do Shader Model 4,1 que você pode encontrar ao depurar um sombreador.

<dl>

[Modificadores de instrução](instruction-modifiers.md)  
[add](add--sm4---asm-.md)  
[and](and--sm4---asm-.md)  
[break](break--sm4---asm-.md)  
[breakc](breakc--sm4---asm-.md)  
[call](call--sm4---asm-.md)  
[callc](callc--sm4---asm-.md)  
[case](case--sm4---asm-.md)  
[continua](continue--sm4---asm-.md)  
[continuec](continuec--sm4---asm-.md)  
[migração](cut--sm4---asm-.md)  
[\_constantBuffer DCL](dcl-constantbuffer.md)  
[\_globalFlags DCL](dcl-globalflags.md)  
[\_immediateConstantBuffer DCL](dcl-immediateconstantbuffer.md)  
[\_indexableTemp DCL](dcl-indexabletemp.md)  
[\_indexRange DCL](dcl-indexrange.md)  
[\_entrada DCL](dcl-input.md)  
[\_VA de entrada de DCL \_](dcl-input-sv.md)  
[\_vPrim de entrada DCL](dcl-input-vprim.md)  
[\_maxOutputVertexCount DCL](dcl-maxoutputvertexcount.md)  
[saída de DCL \_](dcl-output.md)  
[\_oDepth de saída de DCL \_](dcl-output-odepth.md)  
[\_SGV de saída de DCL \_](dcl-output-sgv.md)  
[\_SIV de saída de DCL \_](dcl-output-siv.md)  
[\_outputTopology DCL](dcl-outputtopology.md)  
[\_recurso DCL](dcl-resource.md)  
[amostra de DCL \_](dcl-sampler.md)  
[\_pretemps DCL](dcl-temps.md)  
[default](default--sm4---asm-.md)  
[derivar \_ RTX](deriv-rtx--sm4---asm-.md)  
[derivar \_ rty](deriv-rty--sm4---asm-.md)  
[carte](discard--sm4---asm-.md)  
[div](div--sm4---asm-.md)  
[dp2](dp2--sm4---asm-.md)  
[dp3](dp3--sm4---asm-.md)  
[dp4](dp4--sm4---asm-.md)  
[senão](else--sm4---asm-.md)  
[reflexão](emit--sm4---asm-.md)  
[emitThenCut](emitthencut--sm4---asm-.md)  
[endif](endif--sm4---asm-.md)  
[loop de fim](endloop--sm4---asm-.md)  
[troca de](endswitch--sm4---asm-.md)  
[eq](eq--sm4---asm-.md)  
[exp](exp--sm4---asm-.md)  
[frc](frc--sm4---asm-.md)  
[ftoi](ftoi--sm4---asm-.md)  
[ftou](ftou--sm4---asm-.md)  
[ge](ge--sm4---asm-.md)  
[IAdd](iadd--sm4---asm-.md)  
[ibfe](dne--sm5---asm-.md)  
[ieq](ieq--sm4---asm-.md)  
[if](if--sm4---asm-.md)  
[ige](ige--sm4---asm-.md)  
[curso](ilt--sm4---asm-.md)  
[imad](imad--sm4---asm-.md)  
[imin](imin--sm4---asm-.md)  
[imul](imul--sm4---asm-.md)  
[inha](ine--sm4---asm-.md)  
[ineg](ineg--sm4---asm-.md)  
[ishl](ishl--sm4---asm-.md)  
[ishr](ishr--sm4---asm-.md)  
[itof](itof--sm4---asm-.md)  
[label](label--sm4---asm-.md)  
[2](ld--sm4---asm-.md)  
[Façam](log--sm4---asm-.md)  
[loop](loop--sm4---asm-.md)  
[lt](lt--sm4---asm-.md)  
[Mad](mad--sm4---asm-.md)  
[max](max--sm4---asm-.md)  
[min](min--sm4---asm-.md)  
[média](mov--sm4---asm-.md)  
[movc](movc--sm4---asm-.md)  
[mul](mul--sm4---asm-.md)  
[ne](ne--sm4---asm-.md)  
[Nop](nop--sm4---asm-.md)  
[not](not--sm4---asm-.md)  
[or](or--sm4---asm-.md)  
[ResInfo](resinfo--sm4---asm-.md)  
[RET](ret--sm4---asm-.md)  
[retc](retc--sm4---asm-.md)  
[arredondar \_ ne](round-ne--sm4---asm-.md)  
[Ni de ida e volta \_](round-ni--sm4---asm-.md)  
[PI arredondado \_](round-pi--sm4---asm-.md)  
[arredondar \_ z](round-z--sm4---asm-.md)  
[rsq](rsq--sm4---asm-.md)  
[Nova](sample--sm4---asm-.md)  
[exemplo \_ b](sample-b--sm4---asm-.md)  
[exemplo \_ c](sample-c--sm4---asm-.md)  
[exemplo \_ c \_ LZ](sample-c-lz--sm4---asm-.md)  
[exemplo \_ d](sample-d--sm4---asm-.md)  
[exemplo \_ l](sample-l--sm4---asm-.md)  
[sincos](sincos--sm4---asm-.md)  
[sqrt](sqrt--sm4---asm-.md)  
[switch](switch--sm4---asm-.md)  
[udiv](udiv--sm4---asm-.md)  
[uge](uge--sm4---asm-.md)  
[ultados](ult--sm4---asm-.md)  
[umad](umad--sm4---asm-.md)  
[scanner](umax--sm4---asm-.md)  
[umin](umin--sm4---asm-.md)  
[umul](umul--sm4---asm-.md)  
[ushr](ushr--sm4---asm-.md)  
[utof](utof--sm4---asm-.md)  
[XOR](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a>Assembly de modelo do sombreador 4,1

O Shader Model 4,1 dá suporte a todas as instruções do modelo de sombreador 4,0 e às seguintes instruções adicionais:

<dl>

[gather4](gather4--sm4-1---asm-.md)  
[ld2dms](ld2dms--sm4-1---asm-.md)  
[lod](lod--sm4-1---asm-.md)  
[sampleinfo](sampleinfo--sm4-1---asm-.md)  
[samplepos](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do sombreador ASM](dx9-graphics-reference-asm.md)
</dt> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




