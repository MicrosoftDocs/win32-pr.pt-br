---
description: Extrai os coeficientes de projeção de PCA (análise de componente principal) por exemplo de um buffer de dados compactado ID3DXPRTCompBuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: Método ID3DXPRTCompBuffer::ExtractPCA (D3DX9Mesh.h)
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
ms.openlocfilehash: 6b172682883c5e5272ece103879aefbbdfb79193b0576e9be04432b5d48b1bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856136"
---
# <a name="id3dxprtcompbufferextractpca-method"></a>Método ID3DXPRTCompBuffer::ExtractPCA

Extrai os coeficientes de projeção de PCA (análise de componente principal) por exemplo de um buffer de dados compactado [**ID3DXPRTCompBuffer.**](id3dxprtcompbuffer.md)

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

*StartPCA* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice inicial para coeficientes de projeção PCA a extrair do buffer.

</dd> <dt>

*NumExtract* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de coeficientes de projeção PCA a extrair do buffer.

</dd> <dt>

*pPCACoefficients* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para o local em que os coeficientes de CPCA (análise de componente principal) clustered são gravados. O tamanho dos dados gravados é (número de amostras) \* (número de coeficientes pca).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
