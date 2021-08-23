---
description: Computa uma projeção de iluminação distante em vetores de base esféricas (SH) que representam o radiante do incidente em locais especificados.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'Método ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3aaa8f9332a80e35ffde43d145be1ed885caeaca6d61e4eb9190baba09b73ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747756"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a>Método ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH

Computa uma projeção de iluminação distante em vetores de base esféricas (SH) que representam o radiante do incidente em locais especificados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ordenar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da representação de SH de iluminação distante. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. O grau da avaliação é o pedido-1.

</dd> <dt>

*Pedido* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da representação de SH da iluminação local. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. O grau da avaliação é Order out-1.

</dd> <dt>

*NumVolSamples.xml* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de locais de exemplo.

</dd> <dt>

*pSampleLocs* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posição de cada exemplo.

</dd> <dt>

*pDataOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que projeta a iluminação distante em vetores de base de sh. Esse buffer deve ter o número correto de canais de cores alocados para a simulação. Esse método gera o pedido \* de pedido ² "² escalars por canal em cada local de exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método computa como a luz de uma fonte distante chega em cada ponto no espaço especificado por pSampleLocs. Os coeficientes de SH representam o mapeamento, em cada ponto de pSampleLocs, do radiante de origem para transferir o incidente radiante.

Para usar esse método com êxito, você deve definir a amostragem em uma esfera com UseSphere = **true** e UseCosine = **false** em [**ID3DXPRTEngine:: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); caso contrário, esse método retornará um erro com D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
