---
description: Função D3DXGetImageInfoFromFile – recupera informações sobre um determinado arquivo de imagem.
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: Função D3DXGetImageInfoFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1726fae1697a48d8e4aa406f5eb5cec03f6071fed4b36a199b10e385a24e6249
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027626"
---
# <a name="d3dxgetimageinfofromfile-function"></a>Função D3DXGetImageInfoFromFile

Recupera informações sobre um determinado arquivo de imagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcFile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome do arquivo da imagem para recuperar informações. Se UNICODE ou \_ Unicode estiverem definidos, esse tipo de parâmetro será LPCWSTR, caso contrário, o tipo será LPCSTR.

</dd> <dt>

*pSrcInfo* \[ no\]
</dt> <dd>

Tipo: **[ **\_ informações de D3DXIMAGE**](d3dximage-info.md)\***

Ponteiro para uma estrutura de [**\_ informações de D3DXIMAGE**](d3dximage-info.md) a ser preenchida com a descrição dos dados no arquivo de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

Essa função dá suporte a cadeias de caracteres Unicode e ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFileInMemory**](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[**D3DXGetImageInfoFromResource**](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
