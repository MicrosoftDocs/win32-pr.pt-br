---
description: Fazer commit das alterações feitas em uma malha no dispositivo para que as alterações possam ser renderizadas. Isso deve ser chamado depois que os dados de uma malha são alterados e antes de serem renderizados. Uma malha não pode ser renderizada, a menos que esteja comprometida com o dispositivo. Consulte Observações.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: Método ID3DX10Mesh::CommitToDevice (D3DX10.h)
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
ms.openlocfilehash: 50dde79e57ca7edf838f05b1fa1b4d10f5da5cc936b3cbf563c7838703650806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567026"
---
# <a name="id3dx10meshcommittodevice-method"></a>Método ID3DX10Mesh::CommitToDevice

Fazer commit das alterações feitas em uma malha no dispositivo para que as alterações possam ser renderizadas. Isso deve ser chamado depois que os dados de uma malha são alterados e antes de serem renderizados. Uma malha não pode ser renderizada, a menos que esteja comprometida com o dispositivo. Consulte Observações.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Quando uma malha é carregada, seus dados são carregados em recursos de preparação, o que significa que os dados podem ser alterados, mas não renderizados. Quando CommitToDevice é chamado, os dados dos recursos de preparação são copiados nos recursos do dispositivo para que possam ser renderizados. Embora os dados sejam confirmados no dispositivo, os recursos de preparação permanecem e podem ser modificados. Se alguma modificação for feita nos recursos de preparação, os recursos de preparação deverão ser confirmados no dispositivo novamente para que essas alterações sejam renderizadas na tela.

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

 

 




