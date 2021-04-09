---
description: Confirme as alterações feitas em uma malha para o dispositivo para que as alterações possam ser processadas. Isso deve ser chamado depois que os dados de uma malha são alterados e antes de serem renderizados. Uma malha não pode ser renderizada a menos que seja confirmada no dispositivo. Consulte Observações.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'Método ID3DX10Mesh:: CommitToDevice (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012104"
---
# <a name="id3dx10meshcommittodevice-method"></a>Método ID3DX10Mesh:: CommitToDevice

Confirme as alterações feitas em uma malha para o dispositivo para que as alterações possam ser processadas. Isso deve ser chamado depois que os dados de uma malha são alterados e antes de serem renderizados. Uma malha não pode ser renderizada a menos que seja confirmada no dispositivo. Consulte Observações.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Quando uma malha é carregada, os dados são carregados em recursos de preparo, o que significa que os dados podem ser alterados, mas não renderizados. Quando CommitToDevice é chamado, os dados dos recursos de preparo são copiados nos recursos do dispositivo para que possam ser renderizados. Embora os dados sejam confirmados no dispositivo, os recursos de preparo permanecem e podem ser modificados. Se forem feitas modificações nos recursos de preparo, os recursos de preparo deverão ser confirmados no dispositivo novamente para que essas alterações sejam processadas na tela.

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

 

 




