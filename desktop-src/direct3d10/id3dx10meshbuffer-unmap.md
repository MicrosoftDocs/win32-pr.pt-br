---
description: Cancelar o mapeamento de um buffer.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: 'Método ID3DX10MeshBuffer:: inmapeamento (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Unmap
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 62b056b80b5722ce9173a7ca30200ba208cf88cf51c18d52b2a895d975121671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736035"
---
# <a name="id3dx10meshbufferunmap-method"></a>Método ID3DX10MeshBuffer:: remapeamento

Cancelar o mapeamento de um buffer.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Unmap();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários



Diferenças entre o Direct3D 9 e o Direct3D 10:

- O desmapeamento () no Direct3D 10 é análogo ao desbloqueio de recurso () no Direct3D 9.



 

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

 

 




