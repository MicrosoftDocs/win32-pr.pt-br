---
description: Define os tipos de textura de amostra para sombreadores de vértice.
ms.assetid: 8e9923f9-6f30-45e5-a557-f26d441a534d
title: Enumeração de D3DSAMPLER_TEXTURE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLER_TEXTURE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 5b1755f97ad39a5924367747199cf21c1c46a209a8202cc6b38ef22c73e8ccec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408217"
---
# <a name="d3dsampler_texture_type-enumeration"></a>Enumeração de tipo de \_ textura D3DSAMPLER \_

Define os tipos de textura de amostra para sombreadores de vértice.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSAMPLER_TEXTURE_TYPE { 
  D3DSTT_UNKNOWN,
  D3DSTT_2D,
  D3DSTT_CUBE,
  D3DSTT_VOLUME,
  D3DSTT_FORCE_DWORD
} D3DSAMPLER_TEXTURE_TYPE, *LPD3DSAMPLER_TEXTURE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSTT_UNKNOWN"></span><span id="d3dstt_unknown"></span>**D3DSTT \_ desconhecido**
</dt> <dd>

Valor não inicializado. O valor desse elemento é 0 &lt; &lt; D3DSP \_ TextureType \_ Shift.

</dd> <dt>

<span id="D3DSTT_2D"></span><span id="d3dstt_2d"></span>**D3DSTT \_ 2D**
</dt> <dd>

Declarando uma textura 2D. O valor desse elemento é 2 &lt; &lt; D3DSP \_ TextureType \_ Shift.

</dd> <dt>

<span id="D3DSTT_CUBE"></span><span id="d3dstt_cube"></span>**\_Cubo D3DSTT**
</dt> <dd>

Declarando uma textura de cubo. O valor desse elemento é 3 &lt; &lt; D3DSP \_ TextureType \_ Shift.

</dd> <dt>

<span id="D3DSTT_VOLUME"></span><span id="d3dstt_volume"></span>**\_Volume D3DSTT**
</dt> <dd>

Declarando uma textura de volume. O valor desse elemento é 4 &lt; &lt; D3DSP \_ TextureType \_ Shift.

</dd> <dt>

<span id="D3DSTT_FORCE_DWORD"></span><span id="d3dstt_force_dword"></span>**D3DSTT \_ forçar \_ DWORD**
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
</dt> </dl>

 

 




