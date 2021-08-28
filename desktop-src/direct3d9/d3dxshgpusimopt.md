---
description: Descreve a resolução da sombra z-buffer que será usada na simulação de iluminação direta do PRT (transferência de radiante de computação) na GPU.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: Enumeração D3DXSHGPUSIMOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a73323dc9d6596f848fa50fe6dc21e236a5b9f2d4362b3c2a27cf773d3939fac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849746"
---
# <a name="d3dxshgpusimopt-enumeration"></a>Enumeração D3DXSHGPUSIMOPT

Descreve a resolução da sombra z-buffer que será usada na simulação de iluminação direta do PRT (transferência de radiante de computação) na GPU. Um buffer z de qualidade superior também pode ser especificado para reduzir o ruído nos resultados da simulação de iluminação direta, embora a simulação seja mais lenta.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES256**
</dt> <dd>

Simulação de baixa resolução. Uma textura de 256 x 256 pixels é usada na simulação para codificar a sombra z-buffer.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES512**
</dt> <dd>

Simulação de resolução média. Uma textura de 512 x 512 pixels é usada na simulação para codificar a sombra z-buffer. Esse é o valor padrão.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES1024**
</dt> <dd>

Simulação de alta resolução. Uma textura de 1024 x 1024 pixels é usada na simulação para codificar a sombra z-buffer.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES2048**
</dt> <dd>

Simulação de resolução mais alta. Uma textura de 2048 x 2048 pixels é usada na simulação para codificar a sombra z-buffer.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT \_ Highquality**
</dt> <dd>

A simulação é de alta precisão, independentemente da resolução selecionada. Definir esse valor reduzirá o ruído nos resultados da simulação de iluminação direta, embora a simulação seja mais lenta. Pode ser combinado com um dos valores de resolução.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Somente um dos valores de resolução pode ser especificado e pode ser combinado com o valor de alta qualidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




