---
description: Projeta uma função representada em um mapa de cubo em harmônicas esféricas.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: Função D3DX10SHProjectCubeMap (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fa30724bed56e86d16626133ab32e3494d3c71d6ffa839be1520518c97a77fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990456"
---
# <a name="d3dx10shprojectcubemap-function"></a>Função D3DX10SHProjectCubeMap

Projeta uma função representada em um mapa de cubo em harmônicas esféricas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ordem* 
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação SH, gera a ordem ^ 2 coefs, o grau é a ordem 1.

</dd> <dt>

*pCubeMap* 
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Cubemap que vai ser projetado em harmônicas esféricas. Consulte [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).

</dd> <dt>

*pROut* 
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Vetor SH de saída para vermelho.

</dd> <dt>

*pGOut* 
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Gerar vetor de saída para verde.

</dd> <dt>

*pBOut* 
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Vetor SH de saída para azul.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
