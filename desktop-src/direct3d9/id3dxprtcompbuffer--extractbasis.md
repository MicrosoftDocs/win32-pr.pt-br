---
description: Extrai os vetores de base de ACP (análise de componente principal) para um determinado cluster de um buffer de dados compactado ID3DXPRTCompBuffer.
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: 'Método ID3DXPRTCompBuffer:: ExtractBasis (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 288a96a5f56bc04b245eaaf032bbcd946ed227c5b4fcad9e5d5d200dfa9903bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294026"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a>Método ID3DXPRTCompBuffer:: ExtractBasis

Extrai os vetores de base de ACP (análise de componente principal) para um determinado cluster de um buffer de dados compactado [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cluster* \[ do no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Cluster para o qual a base será extraída.

</dd> <dt>

*pClusterBasis* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de dados de vetor de base para cluster. O tamanho dos dados FLUTUANTEs armazenados será: (1 + número de vetores do PCA por cluster) \* (número de coeficientes) \* (número de canais de cores)

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
