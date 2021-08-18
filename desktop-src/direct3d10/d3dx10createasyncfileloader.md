---
description: Crie um carregador de arquivo assíncrono.
ms.assetid: 1b79fba5-e7f0-4160-9cec-ffea94f84fde
title: Função D3DX10CreateAsyncFileLoader (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncFileLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: cfb30de406843831745ab56ced1f3dc0552536ea4a8d45c7f3da4ae078e036e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753386"
---
# <a name="d3dx10createasyncfileloader-function"></a>Função D3DX10CreateAsyncFileLoader

Crie um carregador de arquivo assíncrono.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

O nome do arquivo a ser carregado. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados será resolvido para LPCSTR.

</dd> <dt>

*ppDataLoader* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***

Endereço de um ponteiro para o carregador de dados assíncronos (consulte [**Interface ID3DX10DataLoader**](id3dx10dataloader.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
