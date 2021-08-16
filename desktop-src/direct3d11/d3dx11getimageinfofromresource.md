---
title: Função D3DX11GetImageInfoFromResource (D3DX11tex.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Observação Em vez de usar essa função, recomendamos que você use funções de recurso e, em seguida, use a biblioteca DirectXTex (ferramentas), LoadFromXXXMemory (em que XXX é WIC, DDS ou TGA; O WIC não dá suporte a DDS e TGA; O D3DX 9 é suportado por TGA como um formato de origem de arte comum para jogos). Recupera informações sobre uma determinada imagem em um recurso.
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- Função D3DX11GetImageInfoFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ada8118dac3e39f9f91012bb3ec681db7b156540cffae0fb7c0f1a7bc1819b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535951"
---
# <a name="d3dx11getimageinfofromresource-function"></a>Função D3DX11GetImageInfoFromResource

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.

 

> [!Note]  
> Em vez de usar essa função, recomendamos que você use funções de recurso e, em seguida, use a biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) (ferramentas), [](/windows/desktop/menurc/resources-functions) **LoadFromXXXMemory** (em que XXX é WIC, DDS ou TGA; O WIC não dá suporte a DDS e TGA; O D3DX 9 é suportado por TGA como um formato de origem de arte comum para jogos).

 

Recupera informações sobre uma determinada imagem em um recurso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSrcModule* \[ Em\]
</dt> <dd>

Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

Módulo em que o recurso é carregado. De definir esse parâmetro como **NULL** para especificar o módulo associado à imagem que o sistema operacional usou para criar o processo atual.

</dd> <dt>

*pSrcResource* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*pPump* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Bomba de thread opcional que pode ser usada para carregar as informações de forma assíncrona. Pode ser **NULL.** Consulte [**Interface ID3DX11ThreadPump**](id3dx11threadpump.md).

</dd> <dt>

*pSrcInfo* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

Ponteiro para uma estrutura D3DX11 IMAGE INFO a ser preenchida com a descrição dos \_ dados no arquivo de \_ origem.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Um ponteiro para o valor de retorno. Pode ser **NULL.** Se *pPump* não for **NULL,** *o pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para **D3DX11GetImageInfoFromResourceW.** Caso contrário, a chamada de função será resolvida para **D3DX11GetImageInfoFromResourceA** porque as cadeias de caracteres ANSI estão sendo usadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

