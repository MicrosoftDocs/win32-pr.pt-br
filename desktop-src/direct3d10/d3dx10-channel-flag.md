---
description: Esses sinalizadores são usados por funções que operam em um ou mais canais em uma textura.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: Enumeração de D3DX10_CHANNEL_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 4b29cbb958b2aa8af02000fc62d4d3a848c2efba585bd927674c9ceca9d65d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634956"
---
# <a name="d3dx10_channel_flag-enumeration"></a>Enumeração de sinalizador de \_ canal D3DX10 \_

Esses sinalizadores são usados por funções que operam em um ou mais canais em uma textura.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10 do \_ canal \_ vermelho**
</dt> <dd>

Indica que o canal vermelho deve ser usado.

</dd> <dt>

<span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10 de \_ canal \_ azul**
</dt> <dd>

Indica que o canal azul deve ser usado.

</dd> <dt>

<span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10 de \_ canal \_ verde**
</dt> <dd>

Indica que o canal verde deve ser usado.

</dd> <dt>

<span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10 \_ canal \_ alfa**
</dt> <dd>

Indica que o canal alfa deve ser usado.

</dd> <dt>

<span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**\_Luminância de canal D3DX10 \_**
</dt> <dd>

Indica que o luminaces dos canais vermelho, verde e azul deve ser usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




