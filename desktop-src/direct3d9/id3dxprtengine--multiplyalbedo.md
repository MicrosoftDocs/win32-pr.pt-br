---
description: Multiplica cada vetor de PRT (transferência radiante em pré-computação) pelo albedo por vértice.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'Método ID3DXPRTEngine:: MultiplyAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771500"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a>Método ID3DXPRTEngine:: MultiplyAlbedo

Multiplica cada vetor de PRT (transferência radiante em pré-computação) pelo albedo por vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDataOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que conterá vetores de PRT multiplicado pelo albedo por vértice. Se esse buffer de saída for um objeto de textura, deve-se tomar cuidado para armazenar o albedo da textura na mesma resolução que o buffer de simulação. Você pode definir a resolução apropriada no albedo com [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), aplicando regiões de medianiz de textura, se apropriado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Os métodos ID3DXPRTEngine:: Computexxx calculam os buffers de saída nos quais o sinal leve não foi multiplicado por albedo. Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que a radiante de origem, gerando assim resultados mais precisos da compactação.

Para incluir albedo no modelo de leve renderizado, chame esse método após um dos métodos Computexxx.

[**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) deve ser chamado antes de chamar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




