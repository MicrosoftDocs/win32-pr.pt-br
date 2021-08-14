---
title: Alterações de código de bytes no SM 5.1
description: O SM 5.1 altera como os registros de recursos são declarados e referenciados em instruções.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93d7d8533bac3750e743166a9d64b687fc06f0fbf21931d44e7d83d462cf15a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794554"
---
# <a name="bytecode-changes-in-sm51"></a>Alterações de código de bytes no SM 5.1

O SM 5.1 altera como os registros de recursos são declarados e referenciados em instruções.

O SM 5.1 se move para declarar uma "variável" de registro, semelhante ao modo como é feito para registros de memória compartilhada de grupo, ilustrado pelo exemplo a seguir:

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

A desmontagem deste exemplo segue:

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

Cada intervalo de recursos do sombreador agora tem uma ID (um nome) no código de bytes do sombreador. Por exemplo, a matriz de textura tex1 se torna 1 ' no código de byte do sombreador. Atribuir IDs exclusivas a cada intervalo de recursos permite duas coisas:

-   Identifique de forma não ambígua qual intervalo de recursos (consulte o \_ recurso DCL \_ Texture2D) está sendo indexado em uma instrução (consulte a instrução de exemplo).
-   Anexe o conjunto de atributos à declaração, por exemplo, tipo de elemento, tamanho de Stride, modo de operação de varredura, etc..

Observe que a ID do intervalo não está relacionada à declaração de limite inferior do HLSL.

A ordem das associações de recursos de reflexão e as instruções de declaração do sombreador são as mesmas para auxiliar na identificação da correspondência entre as variáveis HLSL e as IDs do código de bytes.

Cada instrução de declaração no SM 5.1 usa um operando 3D para definir: ID de intervalo, limites inferiores e superiores. Um token adicional é emitido para especificar o espaço de registro. Outros tokens podem ser emitidos também para transmitir propriedades adicionais do intervalo, por exemplo, CBuffer ou instrução de declaração de buffer estruturado emite o tamanho do CBuffer ou da estrutura. Os detalhes exatos da codificação podem ser encontrados em d3d12TokenizedProgramFormat. h e D3D10ShaderBinary:: CShaderCodeParser.

As instruções do SM 5.1 não emitirão informações adicionais do operando de recurso como parte da instrução (como no SM 5.0). Essas informações agora são movidas para as instruções de declaração. No SM 5.0, as instruções de indexação de recursos exigiam atributos de recurso a serem descritos em tokens de opcode estendidos, já que a indexação ofusca a associação à declaração. No SM 5.1, cada ID (como ' t 1 ') está inequívocamente associada a uma única declaração que descreve as informações de recurso necessárias. Portanto, os tokens de opcode estendidos usados em instruções para descrever as informações de recursos não são mais emitidos.

Em instruções de não declaração, um operando de recurso para amostras, SRVs e UAVs é um operando 2D. O primeiro índice é uma constante literal que especifica a ID do intervalo. O segundo índice representa o valor linear do índice. O valor é calculado em relação ao início do espaço de registro correspondente (não relativo ao início do intervalo lógico) para correlacionar melhor com a assinatura raiz e para reduzir a carga do compilador de driver de ajustar o índice.

Um operando de recurso para CBVs é um operando 3D: ID literal do intervalo, índice de CBuffer, offset na instância específica de CBuffer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do HLSL Shader Model 5,1 para Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[Modelo do sombreador 5,1](shader-model-5-1.md)
</dt> </dl>

 

 




