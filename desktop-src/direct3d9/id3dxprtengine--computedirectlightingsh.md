---
description: Computa a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica esférica (SH).
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: 'Método ID3DXPRTEngine:: ComputeDirectLightingSH (D3DX9Mesh. h)'
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
ms.openlocfilehash: 01b6c3cff082c40c4df5d9bee1d997599a41965b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813669"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a>Método ID3DXPRTEngine:: ComputeDirectLightingSH

Computa a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica esférica (SH).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação SH. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*pDataOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que modela a contribuição de iluminação direta com a aproximação sh. Esse buffer deve ter o número correto de canais de cores alocados para a simulação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A saída não inclui albedo, e apenas a luz de entrada é integrada ao simulador. Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que a radiante de origem, gerando assim resultados mais precisos da compactação.

Chame [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vetor de PRT (transferência de radiante preputado) pelo albedo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
