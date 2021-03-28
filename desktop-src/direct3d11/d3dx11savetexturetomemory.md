---
title: Função D3DX11SaveTextureToMemory (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a biblioteca DirectXTex, CaptureTexture, SaveToXXXMemory (em que XXX é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos). Salve uma textura na memória.
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
ms.openlocfilehash: 4718f32f8d8288f83b30e3d742ebbe619421dc48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173114"
---
# <a name="d3dx11savetexturetomemory-function"></a>Função D3DX11SaveTextureToMemory

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

> [!Note]  
> Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** , **SaveToXXXMemory** (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).

 

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

Um ponteiro para um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*pSrcTexture* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***

Ponteiro para a textura a ser salva. Consulte [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).

</dd> <dt>

*DestFormat* \[ no\]
</dt> <dd>

Tipo: **[ **\_ formato de \_ arquivo \_ de imagem D3DX11**](d3dx11-image-file-format.md)**

O formato em que a textura será salva. Consulte [**\_ formato de \_ arquivo \_ de imagem D3DX11**](d3dx11-image-file-format.md).

</dd> <dt>

*ppDestBuf* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***

Endereço de um ponteiro para a memória que contém a textura salva.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Opcional.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

