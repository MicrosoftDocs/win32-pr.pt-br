---
description: Contém dados de rampa vermelho, verde e azul.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: Estrutura D3DGAMMARAMP (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: fbd3acc35b7fd4998f5ba536c1fe4a28cf2a17153bf24aacde1f9f39bbbcd09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750996"
---
# <a name="d3dgammaramp-structure"></a>Estrutura D3DGAMMARAMP

Contém dados de rampa vermelho, verde e azul.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a>Membros

<dl> <dt>

**Vermelho**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matriz de elemento 256 WORD que descreve a rampa gama vermelha.

</dd> <dt>

**Verde**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matriz de elemento 256 WORD que descreve a rampa gama verde.

</dd> <dt>

**Azul**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matriz de elemento WORD 256 que descreve a rampa gama azul.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
