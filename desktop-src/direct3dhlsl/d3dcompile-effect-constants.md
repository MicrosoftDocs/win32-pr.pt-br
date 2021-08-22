---
title: D3DCOMPILE_EFFECT constantes (D3DCompiler.h)
description: Essas constantes direcionam como o compilador compila um arquivo de efeito ou como o runtime processa o arquivo de efeito.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7d5c31efb17d2f852ac3903a5946ce5fb72fcef86ef083c474328859472c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286910"
---
# <a name="d3dcompile_effect-constants"></a>Constantes D3DCOMPILE \_ EFFECT

Essas constantes direcionam como o compilador compila um arquivo de efeito ou como o runtime processa o arquivo de efeito.

<dl> <dt>

<span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**EFEITO FILHO D3DCOMPILE \_ \_ \_**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Compile o arquivo effects (.fx) para um efeito filho. Os efeitos filho não têm inicializadores para nenhum valor compartilhado porque esses efeitos filho são inicializados no efeito mestre (o pool de efeitos).

> [!Note]  
> Os pools de efeito são suportados pelos Efeitos 10 (FX10), mas não pelos Efeitos 11 (FX11). Para obter mais informações sobre as diferenças entre pools de efeito no Direct3D 10 e grupos de efeito no Direct3D 11, consulte [Pools de efeito e grupos](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**EFEITO D3DCOMPILE \_ \_ PERMITIR OPERAÇÕES \_ \_ LENTAS**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Desabilita o modo de desempenho e permite objetos de estado mutáveis.

Por padrão, o modo de desempenho está habilitado. O modo de desempenho não permite objetos de estado mutáveis impedindo que expressões não literais apareçam em definições de objeto de estado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DCompiler.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

