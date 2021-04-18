---
description: Extrai as IDs de cluster por amostra de um buffer de dados compactado ID3DXPRTCompBuffer.
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'Método ID3DXPRTCompBuffer:: ExtractClusterIDs (D3DX9Mesh. h)'
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
ms.openlocfilehash: ef68a972109e89e318adb83ab388c653c6a3deed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771393"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a>Método ID3DXPRTCompBuffer:: ExtractClusterIDs

Extrai as IDs de cluster por amostra de um buffer de dados compactado [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pClusterIDs* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Ponteiro para o local na memória em que as IDs são gravadas. O tamanho da memória necessária é o valor retornado por [**ID3DXPRTCompBuffer:: GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).

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

 

 
