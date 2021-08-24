---
title: Função D3DX11SaveTextureToMemory (D3DX11tex.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Observação Em vez de usar essa função, recomendamos que você use a biblioteca DirectXTex, CaptureTexture e SaveToXXXMemory (em que XXX é WIC, DDS ou TGA; O WIC não dá suporte a DDS e TGA; O D3DX 9 é suportado por TGA como um formato de origem de arte comum para jogos). Salve uma textura na memória.
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- Função D3DX11SaveTextureToMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8459b9652701110a27efa88cf75d1bd5eb9214f72e860a5a80c18d0fa6292ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124561"
---
# <a name="d3dx11savetexturetomemory-function"></a>Função D3DX11SaveTextureToMemory

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.

 

> [!Note]  
> Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex,](https://github.com/Microsoft/DirectXTex) **CaptureTexture** e **SaveToXXXMemory** (em que XXX é WIC, DDS ou TGA; O WIC não dá suporte a DDS e TGA; O D3DX 9 é suportado por TGA como um formato de origem de arte comum para jogos).

 

Salve uma textura na memória.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContext* 
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Um ponteiro para um [**objeto ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

</dd> <dt>

*pSrcTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Ponteiro para a textura a ser salva. Consulte [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*DestFormat* \[ Em\]
</dt> <dd>

Tipo: **[ **FORMATO DE ARQUIVO DE IMAGEM D3DX11 \_ \_ \_**](d3dx11-image-file-format.md)**

O formato em que a textura será salva. Consulte [**FORMATO DE ARQUIVO DE IMAGEM D3DX11 \_ \_ \_**](d3dx11-image-file-format.md).

</dd> <dt>

*ppDestBuf* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***

Endereço de um ponteiro para a memória que contém a textura salva.

</dd> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Opcional.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

