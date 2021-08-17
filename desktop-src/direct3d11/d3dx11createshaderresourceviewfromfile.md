---
title: Função D3DX11CreateShaderResourceViewFromFile (D3DX11tex.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Observação Em vez de usar essa função, recomendamos que você use essas bibliotecas directXTK (runtime), CreateXXXTextureFromFile (em que XXX é DDS ou WIC)Biblioteca DirectXTex (ferramentas), LoadFromXXXFile (em que XXX é WIC, DDS ou TGA; O WIC não dá suporte a DDS e TGA; TGA com suporte para D3DX 9 como um formato de origem de arte comum para jogos) em seguida, CreateShaderResourceView Criar uma exibição de sombreador-recurso de um arquivo.
ms.assetid: c6a23503-f511-49dc-a0dc-19932cf8f313
keywords:
- Função D3DX11CreateShaderResourceViewFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6862b5008ed74687e30a9f233e3544ecd69719a20cdcb3f4dd9409de31f6d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124741"
---
# <a name="d3dx11createshaderresourceviewfromfile-function"></a>Função D3DX11CreateShaderResourceViewFromFile

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.

 

> [!Note]  
> Em vez de usar essa função, recomendamos que você use estes:
>
> -   [Biblioteca directXTK](https://github.com/Microsoft/DirectXTK) (runtime), **CreateXXXTextureFromFile** (em que XXX é DDS ou WIC)
> -   [Biblioteca DirectXTex](https://github.com/Microsoft/DirectXTex) (ferramentas), **LoadFromXXXFile** (em que XXX é WIC, DDS ou TGA; O WIC não dá suporte a DDS e TGA; TGA com suporte do D3DX 9 como um formato de origem de arte comum para jogos) e **CreateShaderResourceView**

 

Crie uma exibição sombreador-recurso de um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11CreateShaderResourceViewFromFile(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Um ponteiro para o dispositivo (consulte [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) que usará o recurso.

</dd> <dt>

*pSrcFile* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome do arquivo que contém a exibição sombreador-recurso. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados será resolvido para LPCSTR.

</dd> <dt>

*pLoadInfo* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)\***

Opcional. Identifica as características de uma textura (consulte [**D3DX11 \_ IMAGE \_ LOAD \_ INFO**](d3dx11-image-load-info.md)) quando o processador de dados é criado; de definido como **NULL** para ler as características de uma textura quando a textura é carregada.

</dd> <dt>

*pPump* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Ponteiro para uma interface thread-pump (consulte Interface [**ID3DX11ThreadPump**](id3dx11threadpump.md)). Se **NULL** for especificado, essa função se comportará de forma síncrona e não retornará até que seja concluída.

</dd> <dt>

*ppShaderResourceView* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***

Endereço de um ponteiro para a exibição sombreador-recurso (consulte [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Um ponteiro para o valor de retorno. Pode ser **NULL.** Se *pPump* não for **NULL,** *o pHResult* deverá ser um local de memória válido até que a execução assíncrona seja concluída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Para ver uma lista dos formatos de imagem com suporte, consulte FORMATO DE ARQUIVO DE IMAGEM [**D3DX11 \_ \_ \_**](d3dx11-image-file-format.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

