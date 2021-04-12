---
description: Obtenha um ponteiro para a memória do buffer de malha para modificar seu conteúdo.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'Método ID3DX10MeshBuffer:: Map (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b8cb03e128a6673963ce2d3cde993babb03da5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298638"
---
# <a name="id3dx10meshbuffermap-method"></a>Método ID3DX10MeshBuffer:: map

Obtenha um ponteiro para a memória do buffer de malha para modificar seu conteúdo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppData* \[ fora\]
</dt> <dd>

Tipo: **void \* \***

Ponteiro para os dados do buffer.

</dd> <dt>

*psize* \[ fora\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***

O tamanho do buffer em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> O MAP () no Direct3D 10 é análogo ao mapa de recursos () no Direct3D 9.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10MeshBuffer](id3dx10meshbuffer.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
