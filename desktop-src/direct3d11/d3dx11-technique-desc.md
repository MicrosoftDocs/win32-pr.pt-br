---
title: Estrutura de D3DX11_TECHNIQUE_DESC (D3dx11effect. h)
description: Descreve uma técnica de efeito.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- Estrutura D3DX11_TECHNIQUE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664049"
---
# <a name="d3dx11_technique_desc-structure"></a>\_Estrutura desc de técnica de D3DX11 \_

Descreve uma técnica de efeito.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nome**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nome dessa técnica (nulo se não anônimo).

</dd> <dt>

**Passa**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de passagens contidas na técnica.

</dd> <dt>

**Anotações**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de anotações nesta técnica.

</dd> </dl>

## <a name="remarks"></a>Comentários

\_A técnica \_ de D3DX11 DESC é usada com [**ID3DX11EffectTechnique:: GetDesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Efeitos 11 estruturas](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

