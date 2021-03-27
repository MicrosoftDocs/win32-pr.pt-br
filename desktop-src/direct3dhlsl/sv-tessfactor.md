---
title: SV_TessFactor
description: Define o valor do mosaico em cada borda de um patch.
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8fa49b19109985b590747098826199b33a32dd2d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104967066"
---
# <a name="sv_tessfactor"></a>\_TESSFACTOR VA

Define o valor do mosaico em cada borda de um patch.

## <a name="type"></a>Tipo



|            |                |
|------------|----------------|
| Tipo       | Topologia de entrada |
| float \[ 4\] | patch quádruplo     |
| float \[ 3\] | Tri patch      |
| float \[ 2\] | isoline        |



 

Os fatores de mosaico devem ser declarados como uma matriz; Eles não podem ser empacotados em um único vetor.

## <a name="remarks"></a>Comentários

O valor do fator de mosaico deve ser definido durante a função constante patch do sombreador envoltória.

Valor de saída necessário para o sombreador envoltória se estiver usando patches Quad ou tri. Esse valor também é um valor de entrada necessário para o sombreador de domínio corresponder às assinaturas de dados de constante de patch entre os estágios de mosaico.

Para um Isoline, o primeiro valor em VA \_ TessFactor é o fator de mosaico de densidade de linha, o segundo valor é o fator de mosaico de detalhes de linha.

### <a name="tri-patch-tessellation-factors"></a>Três fatores de mosaico de patch

O primeiro componente fornece o fator geométrica para a borda u = = 0 do patch. O segundo componente fornece o fator geométrica para a borda v = = 0 do patch. O terceiro componente fornece o fator geométrica para a borda w = = 0 do patch.

### <a name="quad-patch-tessellation-factors"></a>Fatores de mosaico de patch quádruplo

O primeiro componente fornece o fator geométrica para a borda u = = 0 do patch. O segundo componente fornece o fator geométrica para a borda v = = 0 do patch. O terceiro componente fornece o fator geométrica para a borda u = = 1 do patch. O quarto componente fornece o fator geométrica para a borda v = = 1 do patch. A ordenação das bordas é no sentido horário, começando na borda u = = 0, que é o lado esquerdo do patch e da borda v = = 0, que é a parte superior do patch.

Essa função tem suporte nos seguintes tipos de sombreadores:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Semântica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




