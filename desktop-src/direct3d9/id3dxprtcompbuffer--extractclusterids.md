---
description: Extrai as IDs de cluster por exemplo de um buffer de dados compactado ID3DXPRTCompBuffer.
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: Método ID3DXPRTCompBuffer::ExtractClusterIDs (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94cbf51aaedd8cc0d5505ca91663eb014e2a3d417a631e93d71b8a0ebc600ceb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987176"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a>Método ID3DXPRTCompBuffer::ExtractClusterIDs

Extrai as IDs de cluster por exemplo de um buffer de dados compactado [**ID3DXPRTCompBuffer.**](id3dxprtcompbuffer.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pClusterIDs* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Ponteiro para o local na memória em que as IDs são escritas. O comprimento da memória necessário é o valor retornado por [**ID3DXPRTCompBuffer::GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).

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

 

 
