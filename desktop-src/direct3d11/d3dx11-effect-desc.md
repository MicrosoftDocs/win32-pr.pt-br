---
title: Estrutura de D3DX11_EFFECT_DESC (D3dx11effect. h)
description: Descreve um efeito.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- Estrutura D3DX11_EFFECT_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f2c3a205a4849aed755bee01302da813cccf77bbf8255036f287d488b76591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989986"
---
# <a name="d3dx11_effect_desc-structure"></a>\_Estrutura desc de efeito de D3DX11 \_

Descreve um efeito.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**ConstantBuffers**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de buffers de constantes neste efeito.

</dd> <dt>

**GlobalVariables**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de variáveis globais neste efeito.

</dd> <dt>

**InterfaceVariables**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de interfaces globais neste efeito.

</dd> <dt>

**Técnicas**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de técnicas neste efeito.

</dd> <dt>

**Grupos**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de grupos neste efeito.

</dd> </dl>

## <a name="remarks"></a>Comentários

O \_ efeito \_ desc de D3DX11 é usado com [**ID3DX11Effect:: GetDesc**](id3dx11effect-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Efeitos 11 estruturas](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

