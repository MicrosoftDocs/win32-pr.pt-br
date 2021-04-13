---
description: Computa, em um ponto arbitrário que não está em uma malha, um vetor de transferência que mapeia radiante de origem (representado por uma aproximação harmônica esférica (SH)) para sair de radiante.
ms.assetid: 44790465-440d-4426-b780-ed872fbf8efb
title: 'Método ID3DXPRTEngine:: ComputeSurfSamplesDirectSH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03adb1729a8a2e771ea681ccbdd180999d3adcbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298858"
---
# <a name="id3dxprtenginecomputesurfsamplesdirectsh-method"></a>Método ID3DXPRTEngine:: ComputeSurfSamplesDirectSH

Computa, em um ponto arbitrário que não está em uma malha, um vetor de transferência que mapeia radiante de origem (representado por uma aproximação harmônica esférica (SH)) para sair de radiante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComputeSurfSamplesDirectSH(
  [in]            UINT            SHOrder,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SHOrder* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da aproximação de SH a ser usada.

</dd> <dt>

*NumSamples* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de locais de exemplo.

</dd> <dt>

*pSampleLocs* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posição de cada exemplo.

</dd> <dt>

*pSampleNorms* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Vetor normal para cada local de exemplo.

</dd> <dt>

*pDataOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que modela a contribuição de iluminação direta até o ponto, usando a aproximação sh.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Não use um buffer de textura ao chamar esse método.

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
</dt> <dt>

[**ID3DXPRTEngine::ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md)
</dt> </dl>

 

 
