---
description: Computa uma projeção da iluminação direta da luz anterior devolvida em vetores de base esféricas (SH) que representam o radiante do incidente em locais especificados.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'Método ID3DXPRTEngine:: ComputeVolumeSamples (D3DX9Mesh. h)'
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
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810862"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a>Método ID3DXPRTEngine:: ComputeVolumeSamples

Computa uma projeção da iluminação direta da luz anterior devolvida em vetores de base esféricas (SH) que representam o radiante do incidente em locais especificados.

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

*pSurfDataIn* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa o objeto 3D do salto claro anterior.

</dd> <dt>

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação SH. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*NumVolSamples.xml* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de locais de exemplo.

</dd> <dt>

*pSampleLocs* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posição de cada exemplo. Se pSampleLocs for **nulo**, o ComputeVolumeSamples computará as matrizes de transferência em cada vértice de malha. No entanto, se pSampleLocs não for **nulo**, você deverá obter uma amostra em uma esfera (Set UseSphere = **true** e UseCosine = **false** em [**ID3DXPRTEngine:: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); caso contrário, ComputeVolumeSamples retornará D3DERR \_ INVALIDCALL.

</dd> <dt>

*pDataOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que projeta a iluminação direta da luz anterior, saltou para vetores de base sh. Esse buffer deve ter o número correto de canais de cores alocados para a simulação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método computa como a luz da função radiante de origem é refletida na superfície que representa a cena (pSurfDataIn) e chega em cada ponto no espaço especificado por pSampleLocs. Os coeficientes de SH representam o mapeamento, em cada ponto de pSampleLocs, do radiante de origem para transferir o incidente radiante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
