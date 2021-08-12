---
description: Computa coeficientes de LDPRT (transferência de radiante precomputada) de forma local em relação aos vetores normais por amostra para minimizar o erro de quadrados mínimos em relação aos dados de ID3DXPRTBuffer de entrada.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'Método ID3DXPRTEngine:: ComputeLDPRTCoeffs (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a432f1df1ad905ca3200789aa6245212cc180d4c7ef5a8723cf02695aeeb7454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294027"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a>Método ID3DXPRTEngine:: ComputeLDPRTCoeffs

Computa coeficientes de LDPRT (transferência de radiante precomputada) de forma local em relação aos vetores normais por amostra para minimizar o erro de quadrados mínimos em relação aos dados de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada. Esses coeficientes podem ser usados com vetores normais de aparência ou transformação para modelar efeitos globais em objetos dinâmicos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDataIn* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto de dados de [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada esférico harmônica (SH) radiante.

</dd> <dt>

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação SH. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*pNormOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Matriz de vetor opcional a ser preenchida com sombreador-vetores normais ideais para os quais os coeficientes LDPRT são otimizados. Essa matriz deve ter o mesmo tamanho que o número de amostras em pDataIn. Se for **NULL**, os vetores normais da superfície serão usados.

</dd> <dt>

*pDataOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que contém os coeficientes de ordem harmônica por canal de cor por amostra.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

As soluções para sombreamento de vetores normais podem, opcionalmente, ser obtidas com esse método. Esses vetores normais, juntamente com os coeficientes de LDPRT, podem representar com mais precisão o sinal de PRT. Nesse caso, os coeficientes representam as harmônicas zonais orientadas na direção normal.

Este método não pode ser usado com resultados de [**ID3DXPRTEngine:: ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) ou [**ID3DXPRTEngine:: ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
