---
description: Retorna o número de conjuntos de animação atualmente registrados no controlador de animação.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'Método ID3DXAnimationController:: GetNumAnimationSets (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 07a6eee85c515c4b8e923aa9973eddc648ef95cbc152c27951154a7c41fbcf3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026816"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a>Método ID3DXAnimationController:: GetNumAnimationSets

Retorna o número de conjuntos de animação atualmente registrados no controlador de animação.

## <a name="syntax"></a>Sintaxe


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de conjuntos de animação.

## <a name="remarks"></a>Comentários

O controlador contém qualquer número de conjuntos de animações e faixas. Os conjuntos de animação podem ser registrados com [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md). Um controlador de animação criado por uma chamada para [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) irá registrar automaticamente os conjuntos de animação carregados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
