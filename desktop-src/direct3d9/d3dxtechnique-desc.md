---
description: Descreve uma técnica usada por um efeito.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: Estrutura de D3DXTECHNIQUE_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 7e835c0eac067825942568464df8d5d345a06b530b71b7eaf7f319eae5f5d366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630726"
---
# <a name="d3dxtechnique_desc-structure"></a>\_Estrutura desc de D3DXTECHNIQUE

Descreve uma técnica usada por um efeito.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Cadeia de caracteres que contém o nome da técnica.

</dd> <dt>

**Passa**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

O número de renderização que a técnica exige. Consulte Observações.

</dd> <dt>

**Anotações**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

O número de anotações. Consulte [adicionar informações para parâmetros de efeito com \_ anotações](using-an-effect.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Algumas placas de vídeo podem renderizar duas texturas em uma única passagem. No entanto, se um cartão não tiver esse recurso, geralmente é possível renderizar o mesmo efeito em duas passagens, usando uma textura para cada passagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de efeito](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
