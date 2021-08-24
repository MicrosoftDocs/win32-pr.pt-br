---
description: Bloqueia um intervalo de dados de exemplo de vértice ou Texel e Obtém um ponteiro para o local na memória de buffer.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: 'Método ID3DXPRTBuffer:: LockBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d8e3b6310951a5784af99b913298c20d5556baa10b012926f3b68e44d402dbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606886"
---
# <a name="id3dxprtbufferlockbuffer-method"></a>Método ID3DXPRTBuffer:: LockBuffer

Bloqueia um intervalo de dados de exemplo de vértice ou Texel e Obtém um ponteiro para o local na memória de buffer.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Iniciar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice da amostra de dados de vértice ou Texel.

</dd> <dt>

*NumSamples* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices (ou texels) amostrados.

</dd> <dt>

*ppData* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\*\***

Ponteiro para o local na memória em que começa a amostra inicial. O layout de memória dos dados de buffer é:


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado:

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumChannels**](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumCoeffs**](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumSamples**](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
