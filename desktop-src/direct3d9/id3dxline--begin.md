---
description: Prepara um dispositivo para linhas de desenho.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'Método ID3DXLine:: Begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9daa65558c58849d406056ce3358c26fdf2ce1c604342f993babe6af553d130f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629646"
---
# <a name="id3dxlinebegin-method"></a>Método ID3DXLine:: Begin

Prepara um dispositivo para linhas de desenho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Begin();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Chamar **ID3DXLine:: Begin** é opcional. Se chamado fora de uma sequência ID3DXLine:: Begin/ID3DXLine:: end, as funções de desenho chamarão internamente ID3DXLine:: Begin e ID3DXLine:: end. Para evitar sobrecarga extra, esse método deve ser usado se mais de uma função de desenho for chamada sucessivamente.

Esse método deve ser chamado de dentro de uma sequência [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) e [**IDirect3DDevice9:: endcena**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .

ID3DXLine:: Begin não pode ser usado como um substituto para [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) ou [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
