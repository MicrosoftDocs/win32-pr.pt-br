---
title: Função D3DX11SaveTextureToFile (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a biblioteca DirectXTex, CaptureTexture, SaveToXXXFile (em que XXX é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos). Para o cenário simplificado de criação de uma captura de tela de uma textura de destino de renderização, recomendamos que você use a biblioteca DirectXTK, SaveDDSTextureToFile ou SaveWICTextureToFile. Salvar uma textura em um arquivo.
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- Função D3DX11SaveTextureToFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968620"
---
# <a name="d3dx11savetexturetofile-function"></a>Função D3DX11SaveTextureToFile

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

> [!Note]  
> Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** , **SaveToXXXFile** (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos). Para o cenário simplificado de criação de uma captura de tela de uma textura de destino de renderização, recomendamos que você use a biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SaveDDSTextureToFile** ou **SaveWICTextureToFile**.

 

Salvar uma textura em um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
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

O formato em que a textura será salva (consulte [**o \_ \_ \_ formato de arquivo de imagem D3DX11**](d3dx11-image-file-format.md)). D3DX11 \_ IFF \_ DDS é o formato preferencial, pois é a única opção que dá suporte a todos os formatos no [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*pDestFile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nome do arquivo de saída de destino em que a textura será salva. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados será resolvido para LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md); Use o valor de retorno para ver se o *DestFormat* tem suporte.

## <a name="remarks"></a>Comentários

O **D3DX11SaveTextureToFile** grava a estrutura [**\_ \_ DXT10 de cabeçalho DDS**](/windows/desktop/direct3ddds/dds-header-dxt10) extra para a textura de entrada somente se necessário (por exemplo, porque a textura de entrada está no formato RGB padrão (sRGB)). Se **D3DX11SaveTextureToFile** gravar a estrutura **de \_ \_ DXT10 do cabeçalho do DDS** , ele definirá o membro **dwFourCC** da estrutura de [**\_ PIXELFORMAT do DDS**](/windows/desktop/direct3ddds/dds-pixelformat) para a textura a ser **DX10** para indicar o prescense do cabeçalho estendido **\_ \_ DXT10 do cabeçalho DDS** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

