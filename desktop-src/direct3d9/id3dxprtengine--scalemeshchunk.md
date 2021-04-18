---
description: Dimensiona todos os exemplos associados a uma determinada submalha. O método é útil para computar a dispersão da subsuperfície.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'Método ID3DXPRTEngine:: ScaleMeshChunk (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f688a5175e7b50c33dd93d06a4f988a14c062c86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811617"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a>Método ID3DXPRTEngine:: ScaleMeshChunk

Dimensiona todos os exemplos associados a uma determinada submalha. O método é útil para computar a dispersão da subsuperfície.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uMeshChunk* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Local na malha na qual começar a dimensionar amostras.

</dd> <dt>

*fScale* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor pelo qual multiplicar cada vetor na submalha.

</dd> <dt>

*pDataOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) para receber amostras redimensionadas na submalha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
