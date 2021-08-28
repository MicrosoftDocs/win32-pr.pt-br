---
title: Estrutura de D3DX11_GROUP_DESC (D3dx11effect. h)
description: Descreve um grupo de efeitos.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- Estrutura D3DX11_GROUP_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a189417b997647fd9c48a55010e96b32053c64031a03a8ac845e48c9a8e870a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096306"
---
# <a name="d3dx11_group_desc-structure"></a>\_Estrutura desc de grupo D3DX11 \_

Descreve um grupo de efeitos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nome deste grupo ( **nulo** somente se global).

</dd> <dt>

**Técnicas**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de técnicas contidas no grupo.

</dd> <dt>

**Anotações**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de anotações neste grupo.

</dd> </dl>

## <a name="remarks"></a>Comentários

O \_ grupo \_ de D3DX11 DESC é usado com [**ID3DX11EffectTechnique:: GetDesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Efeitos 11 estruturas](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

