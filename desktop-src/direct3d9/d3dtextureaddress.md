---
description: Define constantes que descrevem os modos de endereçamento de textura com suporte.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: Enumeração D3DTEXTUREADDRESS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012082"
---
# <a name="d3dtextureaddress-enumeration"></a>Enumeração D3DTEXTUREADDRESS

Define constantes que descrevem os modos de endereçamento de textura com suporte.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**\_Encapsulamento de D3DTADDRESS**
</dt> <dd>

Peça a textura a cada junção de número inteiro. Por exemplo, para você valores entre 0 e 3, a textura é repetida três vezes; Nenhum espelhamento é executado.

</dd> <dt>

<span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS \_ Mirror**
</dt> <dd>

Semelhante ao D3DTADDRESS \_ Wrap, exceto que a textura é invertida a cada junção de inteiro. para você valores entre 0 e 1, por exemplo, a textura é resolvida normalmente; entre 1 e 2, a textura é invertida (espelhada); entre 2 e 3, a textura é normal novamente; e assim por diante.

</dd> <dt>

<span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS \_ fixe**
</dt> <dd>

As coordenadas de textura fora do intervalo de \[ 0,0, 1,0 \] são definidas como a cor de textura em 0,0 ou 1,0, respectivamente.

</dd> <dt>

<span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**\_Borda D3DTADDRESS**
</dt> <dd>

As coordenadas de textura fora do intervalo de \[ 0,0, 1,0 \] são definidas como a cor da borda.

</dd> <dt>

<span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ MIRRORONCE**
</dt> <dd>

Semelhante a D3DTADDRESS \_ Mirror e D3DTADDRESS \_ fixe. Obtém o valor absoluto da coordenada de textura (assim, espelhamento em cerca de 0) e, em seguida, coloca ao valor máximo. O uso mais comum é para texturas de volume, em que o suporte para o \_ modo de endereçamento de textura D3DTADDRESS MIRRORONCE completo não é necessário, mas os dados são simétricos em relação a um eixo.

</dd> <dt>

<span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
