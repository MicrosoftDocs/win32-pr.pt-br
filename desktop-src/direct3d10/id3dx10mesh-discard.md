---
description: 'Remove os dados de malha do dispositivo que foi confirmado no dispositivo (com ID3DX10Mesh:: CommitToDevice).'
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: 'ID3DX10Mesh: método iscard:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811902"
---
# <a name="id3dx10meshdiscard-method"></a>ID3DX10Mesh: método iscard:D

Remove os dados de malha do dispositivo que foi confirmado no dispositivo (com [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwDiscard* \[ no\]
</dt> <dd>

Tipo: **[ **\_ sinalizadores de \_ descarte \_ de malha D3DX10**](d3dx10-mesh-discard-flags.md)**

Especifica quais partes de dados de malha descartar do dispositivo. Consulte [**\_ sinalizadores de \_ descarte \_ de malha D3DX10**](d3dx10-mesh-discard-flags.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




