---
description: Obter o buffer de representante de ponto da malha.
ms.assetid: 4be7bee5-15ea-496f-83c2-a3a9bafd97c6
title: Método ID3DX10Mesh::GetPointRepBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetPointRepBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4e3c23f4ac4e77d97d290075ba6970062af9ea3a44c608d02e98c05e8f248b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540232"
---
# <a name="id3dx10meshgetpointrepbuffer-method"></a>Método ID3DX10Mesh::GetPointRepBuffer

Obter o buffer de representante de ponto da malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPointRepBuffer(
  [out] ID3DX10MeshBuffer **ppPointReps
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppPointReps* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Ponteiro para um buffer de malha que contém os dados do representante de ponto da malha. Consulte [**ID3DX10MeshBuffer.**](id3dx10meshbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




