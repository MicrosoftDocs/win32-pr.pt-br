---
description: Obtenha uma descrição do objeto de fonte atual.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'Método ID3DX10Font:: GetDesc (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d684a0bf485db441a0a6bf23cd36496cc13fdfe766eaa890682259b76b3800c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990436"
---
# <a name="id3dx10fontgetdesc-method"></a>Método ID3DX10Font:: GetDesc

Obtenha uma descrição do objeto de fonte atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* \[ no\]
</dt> <dd>

Tipo: **[ **\_ fonte D3DX10 \_ desc**](d3dx10-font-desc.md)\***

Ponteiro para uma [**estrutura \_ \_ desc de fonte D3DX10**](d3dx10-font-desc.md) que descreve o objeto Font. Se o UNICODE estiver definido, um ponteiro para um D3DX10FONT \_ DESCW será retornado; caso contrário, um ponteiro para um D3DX10FONT \_ desca será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método descreverá os objetos de fonte Unicode se o UNICODE estiver definido. Caso contrário, getdesca é chamado, que retorna um ponteiro para a \_ estrutura desca D3DX10FONT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




