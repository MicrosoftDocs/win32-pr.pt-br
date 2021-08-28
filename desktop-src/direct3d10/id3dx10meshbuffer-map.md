---
description: Obter um ponteiro para a memória do buffer de malha para modificar seu conteúdo.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: Método ID3DX10MeshBuffer::Map (D3DX10.h)
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
ms.openlocfilehash: 38be37d9d11e40f336eab58691d18113664ff49138704ea563efe083800d7c14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096596"
---
# <a name="id3dx10meshbuffermap-method"></a>Método ID3DX10MeshBuffer::Map

Obter um ponteiro para a memória do buffer de malha para modificar seu conteúdo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppData* \[ out\]
</dt> <dd>

Tipo: **\* \* void**

Ponteiro para os dados do buffer.

</dd> <dt>

*pSize* \[ out\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

O tamanho do buffer em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários



 Diferenças entre o Direct3D 9 e o Direct3D 10:

- Map() no Direct3D 10 é análogo ao recurso Map() no Direct3D 9.



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10MeshBuffer](id3dx10meshbuffer.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
