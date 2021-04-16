---
description: Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado ID3DXPRTCompBuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: 'Método ID3DXPRTCompBuffer:: ExtractPCA (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ef949e9f88a843f4636643dadd7d00ffd94d98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772572"
---
# <a name="id3dxprtcompbufferextractpca-method"></a>Método ID3DXPRTCompBuffer:: ExtractPCA

Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartPCA* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice inicial para coeficientes de projeção do PCA para extrair do buffer.

</dd> <dt>

*NumExtract* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de coeficientes de projeção do PCA a serem extraídos do buffer.

</dd> <dt>

*pPCACoefficients* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para o local em que os coeficientes de análise do componente principal clusterizado (CPCA) são gravados. O tamanho dos dados gravados é (número de amostras) \* (número de coeficientes do PCA).

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

 

 
