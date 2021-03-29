---
title: Constantes de D3DCOMPILE_EFFECT (D3DCompiler. h)
description: Essas constantes direcionam como o compilador compila um arquivo de efeito ou como o tempo de execução processa o arquivo de efeito.
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
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968555"
---
# <a name="d3dcompile_effect-constants"></a>Constantes de efeito de D3DCOMPILE \_

Essas constantes direcionam como o compilador compila um arquivo de efeito ou como o tempo de execução processa o arquivo de efeito.

<dl> <dt>

<span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**\_ \_ Efeito filho de efeito de D3DCOMPILE \_**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Compile o arquivo de efeitos (. FX) para um efeito filho. Os efeitos filho não têm inicializadores para nenhum valor compartilhado porque esses efeitos filho são inicializados no efeito mestre (o pool de efeitos).

> [!Note]  
> Os pools de efeitos têm suporte dos efeitos 10 (FX10), mas não dos efeitos 11 (FX11). Para obter mais informações sobre as diferenças entre pools de efeito no Direct3D 10 e em grupos de efeitos no Direct3D 11, consulte [pools de efeitos e grupos](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**\_Efeito D3DCOMPILE \_ permitir \_ operações lentas \_**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Desabilita o modo de desempenho e permite objetos de estado mutável.

Por padrão, o modo de desempenho está habilitado. O modo de desempenho não permite objetos de estado mutável, impedindo que expressões não literais apareçam nas definições de objeto de estado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

