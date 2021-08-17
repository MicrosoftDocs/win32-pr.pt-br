---
description: Calcula a contribuição de iluminação direta para objetos 3D em que a radiação de origem é representada por uma aproximação de SH (diocidade esférica).
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: Método ID3DXPRTEngine::ComputeDirectLightingSH (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 51eb3121501cee7c56385a9083fc689cd8a06759443250f64bae16901779a3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729708"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a>Método ID3DXPRTEngine::ComputeDirectLightingSH

Calcula a contribuição de iluminação direta para objetos 3D em que a radiação de origem é representada por uma aproximação de SH (diocidade esférica).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ordem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordem da avaliação de SH. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes orderâmicos. O grau da avaliação é Order - 1.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) saída que modela a contribuição de iluminação direta com a aproximação sh. Esse buffer deve ter o número adequado de canais de cores alocados para a simulação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A saída não inclui o albedo e apenas a luz de entrada é integrada ao simulador. Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que o radiance de origem, ingando assim resultados mais precisos da compactação.

Chame [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vetor de PRT (transferência de radiance pré-comutada) pelo albedo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
