---
description: Calcula uma projeção da iluminação direta do salto de luz anterior em vetores de base de sh (fundamento esférico) que representam a radiação de incidentes em locais especificados.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: Método ID3DXPRTEngine::ComputeVolumeSamples (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edc13e8b6f0e5c725e957be22f1b297f825a4f3b622ced68adf19b34a0b64b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293497"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a>Método ID3DXPRTEngine::ComputeVolumeSamples

Calcula uma projeção da iluminação direta do salto de luz anterior em vetores de base de sh (fundamento esférico) que representam a radiação de incidentes em locais especificados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSurfDataIn* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) entrada que representa o objeto 3D do salto de luz anterior.

</dd> <dt>

*Ordem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordem da avaliação de SH. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes orderâmicos. O grau da avaliação é Order - 1.

</dd> <dt>

*NumVolSamples.xml* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de locais de exemplo.

</dd> <dt>

*pSampleLocs* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posição para cada amostra. Se pSampleLocs for **NULL,** ComputeVolumeSamples calculará matrizes de transferência em cada vértice de malha. No entanto, se pSampleLocs não for **NULL,** você deverá fazer uma amostra em uma esfera (definir UseSphere = **TRUE** e UseCosine = **FALSE** [**em ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); caso contrário, ComputeVolumeSamples retornará D3DERR \_ INVALIDCALL.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que projeta a iluminação direta da luz anterior em vetores de base SH. Esse buffer deve ter o número adequado de canais de cores alocados para a simulação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método calcula como a luz da função de radiação de origem é refletida na superfície que representa a cena (pSurfDataIn) e chega a cada ponto no espaço especificado por pSampleLocs. Os coeficientes SH representam o mapeamento, em cada ponto pSampleLocs, de radiação de origem para radiação de incidente transferida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
