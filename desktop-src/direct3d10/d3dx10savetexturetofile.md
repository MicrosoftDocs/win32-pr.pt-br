---
description: Salve uma textura em um arquivo.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: Função D3DX10SaveTextureToFile (D3DX10Tex.h)
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
ms.openlocfilehash: 4d1adb4a490b047329277c4092a68563ffc4bf5d4bb1dbfd866bb849d9f561a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634556"
---
# <a name="d3dx10savetexturetofile-function"></a>Função D3DX10SaveTextureToFile

Salve uma textura em um arquivo.

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

*pSrcTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***

Ponteiro para a textura a ser salva. Consulte [**Interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*DestFormat* \[ Em\]
</dt> <dd>

Tipo: **[ **FORMATO DE ARQUIVO DE IMAGEM D3DX10 \_ \_ \_**](d3dx10-image-file-format.md)**

O formato em que a textura será salva (consulte FORMATO DE ARQUIVO DE IMAGEM [**D3DX10 \_ \_ \_**](d3dx10-image-file-format.md)). D3DX10 IFF DDS é o formato preferencial, pois é a única opção que dá suporte a todos os \_ \_ formatos em [**FORMATO DXGI. \_**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)

</dd> <dt>

*pDestFile* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nome do arquivo de saída de destino em que a textura será salva. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados será resolvido para LPCSTR.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10](d3d10-graphics-reference-returnvalues.md); use o valor de retorno para ver se há suporte para *o DestFormat.*

## <a name="remarks"></a>Comentários

**D3DX10SaveTextureToFile** grava a estrutura [**\_ \_ DXT10 de HEADER DDS**](../direct3ddds/dds-header-dxt10.md) extra somente se necessário (por exemplo, porque a textura de entrada está no formato RGB (sRGB) padrão). Se **D3DX10SaveTextureToFile** grava a estrutura **\_ \_ DXT10 do HEADER DDS,** ele define o membro **dwNixCC** da estrutura [**\_ PIXELFORMAT do DDS**](../direct3ddds/dds-pixelformat.md) para a textura como **DX10** para indicar o pré-requisito do **\_ header \_ DDS DXT10** estendido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
