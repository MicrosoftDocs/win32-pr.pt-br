---
title: D3DX11_TECHNIQUE_DESC (D3dx11effect.h)
description: Descreve uma técnica de efeito.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- D3DX11_TECHNIQUE_DESC estrutura Direct3D 11
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
ms.openlocfilehash: 2266737a04b28940eeaa3758f5bd3909ec815745cb060836c499cfd4b3142266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124921"
---
# <a name="d3dx11_technique_desc-structure"></a>Estrutura D3DX11 \_ TECHNIQUE \_ DESC

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

Nome dessa técnica (NULL se não anônimo).

</dd> <dt>

**Passa**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de passagens contidas na técnica.

</dd> <dt>

**Anotações**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de anotações nessa técnica.

</dd> </dl>

## <a name="remarks"></a>Comentários

D3DX11 TECHNIQUE DESC é usado \_ com \_ [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas effects 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

