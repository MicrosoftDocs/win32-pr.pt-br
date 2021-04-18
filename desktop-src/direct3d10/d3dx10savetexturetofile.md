---
description: Salvar uma textura em um arquivo.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: Função D3DX10SaveTextureToFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764004"
---
# <a name="d3dx10savetexturetofile-function"></a>Função D3DX10SaveTextureToFile

Salvar uma textura em um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcTexture* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Ponteiro para a textura a ser salva. Consulte a [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*DestFormat* \[ no\]
</dt> <dd>

Tipo: **[ **\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md)**

O formato em que a textura será salva (consulte [**o \_ \_ \_ formato de arquivo de imagem D3DX10**](d3dx10-image-file-format.md)). D3DX10 \_ IFF \_ DDS é o formato preferencial, pois é a única opção que dá suporte a todos os formatos no [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

*pDestFile* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nome do arquivo de saída de destino em que a textura será salva. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados será resolvido para LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md); Use o valor de retorno para ver se o *DestFormat* tem suporte.

## <a name="remarks"></a>Comentários

O **D3DX10SaveTextureToFile** grava a estrutura [**\_ \_ DXT10 de cabeçalho DDS**](../direct3ddds/dds-header-dxt10.md) extra para a textura de entrada somente se necessário (por exemplo, porque a textura de entrada está no formato RGB padrão (sRGB)). Se **D3DX10SaveTextureToFile** gravar a estrutura **de \_ \_ DXT10 do cabeçalho do DDS** , ele definirá o membro **dwFourCC** da estrutura de [**\_ PIXELFORMAT do DDS**](../direct3ddds/dds-pixelformat.md) para a textura a ser **DX10** para indicar o prescense do cabeçalho estendido **\_ \_ DXT10 do cabeçalho DDS** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Funções de Uso Geral](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
