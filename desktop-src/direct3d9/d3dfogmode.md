---
description: Define constantes que descrevem o modo de neblina.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Enumeração D3DFOGMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298697"
---
# <a name="d3dfogmode-enumeration"></a>Enumeração D3DFOGMODE

Define constantes que descrevem o modo de neblina.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ nenhum**
</dt> <dd>

Nenhum efeito de neblina.

</dd> <dt>

<span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ exp**
</dt> <dd>

O efeito de neblina intensifica exponencialmente, de acordo com a fórmula a seguir.

![fórmula de intensidade de efeito de neblina](images/fogexp.png)

</dd> <dt>

<span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**
</dt> <dd>

O efeito de neblina intensifica exponencialmente com o quadrado da distância, de acordo com a fórmula a seguir.

![fórmula da intensidade do efeito de neblina com base no quadrado de distância](images/fogexp2.png)

</dd> <dt>

<span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ linear**
</dt> <dd>

O efeito de neblina intensifica linearmente entre os pontos inicial e final, de acordo com a fórmula a seguir.

![fórmula da intensidade do efeito de neblina com base nos pontos inicial e final](images/fogliner.png)

Esse é o único modo de neblina com suporte no momento.

</dd> <dt>

<span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores neste tipo enumerado são usados pelos \_ Estados de RENDERIZAÇÃO D3DRS FOGTABLEMODE e \_ D3DRS FOGVERTEXMODE.

A neblina pode ser considerada uma medida de visibilidade: quanto menor o valor de neblina produzido por uma equação de neblina, menos visível é um objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
