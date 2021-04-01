---
description: Especifica opções de simplificação para uma malha.
ms.assetid: f03170bd-7d2a-4839-9aec-c29426b95437
title: Enumeração D3DXMESHSIMP (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHSIMP
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: faf4244d115076b6b04cd04697acf789172d9b11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091963"
---
# <a name="d3dxmeshsimp-enumeration"></a>Enumeração D3DXMESHSIMP

Especifica opções de simplificação para uma malha.

## <a name="syntax"></a>Syntax


```C++
enum _D3DXMESHSIMP {
  D3DXMESHSIMP_VERTEX  = 1, 
  D3DXMESHSIMP_FACE    = 2 

};
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**\_Vértice D3DXMESHSIMP**
</dt> <dd>

A malha será simplificada pelo número de vértices especificado no parâmetro MinValue.

</dd> <dt>

<span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**\_Rosto D3DXMESHSIMP**
</dt> <dd>

A malha será simplificada pelo número de faces especificado no parâmetro MinValue.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 




