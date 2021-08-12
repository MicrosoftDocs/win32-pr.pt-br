---
title: Enumeração de D3DX11_IMAGE_FILE_FORMAT (D3DX11tex. h)
description: observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows. Formatos de arquivo de imagem com suporte pelas funções D3DX11Createxxx e D3DX11Savexxx.
ms.assetid: 89fa9ab8-3be0-4dc5-a533-94edb01df36a
keywords:
- Enumeração D3DX11_IMAGE_FILE_FORMAT Direct3D 11
- Ponteiro de enumeração LPD3DX11_IMAGE_FILE_FORMAT Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_FILE_FORMAT
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e34d3ab49987d499114c4b9eee695bfad02055fbbef785a955407e97843208f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536960"
---
# <a name="d3dx11_image_file_format-enumeration"></a>\_Enumeração de \_ formato de arquivo de imagem D3DX11 \_

> [!Note]  
> a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows.

 

Formatos de arquivo de imagem com suporte pelas funções D3DX11Createxxx e D3DX11Savexxx.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DX11_IMAGE_FILE_FORMAT { 
  D3DX11_IFF_BMP          = 0,
  D3DX11_IFF_JPG          = 1,
  D3DX11_IFF_PNG          = 3,
  D3DX11_IFF_DDS          = 4,
  D3DX11_IFF_TIFF         = 10,
  D3DX11_IFF_GIF          = 11,
  D3DX11_IFF_WMP          = 12,
  D3DX11_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX11_IMAGE_FILE_FORMAT, *LPD3DX11_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ IFF \_ BMP**
</dt> <dd>

formato de arquivo de bitmap Windows (BMP). Contém um cabeçalho que descreve a resolução do dispositivo no qual o retângulo de pixels foi criado, as dimensões do retângulo, o tamanho da matriz de bits, uma paleta lógica e uma matriz de bits que define a relação entre os pixels na imagem de bitmap e as entradas na paleta lógica. A extensão de arquivo para esse formato é .bmp.

</dd> <dt>

<span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ IFF \_ jpg**
</dt> <dd>

Formato de arquivo compactado JPEG (Joint Experts Group). Especifica a compactação de variável de cores RGB de 24 bits e arquivos de documento de imagem TIFF de escala cinza de 8 bits. A extensão de arquivo para esse formato é .jpg.

</dd> <dt>

<span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11 \_ IFF \_ png**
</dt> <dd>

Formato de arquivo PNG (Portable Network Graphics). Um formato de bitmap não proprietário usando compactação sem perdas. A extensão de arquivo para esse formato é .png.

</dd> <dt>

<span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ IFF \_ DDS**
</dt> <dd>

Formato de arquivo da superfície do DirectDraw (DDS). Armazena texturas, texturas de volume e mapas de ambiente cúbico, com ou sem os níveis de mipmap, e com ou sem a compactação de pixel. A extensão de arquivo para esse formato é. DDS.

</dd> <dt>

<span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11 \_ IFF \_ TIFF**
</dt> <dd>

Formato TIFF (Tagged Image File Format). As extensões de arquivo para esse formato são. tif e. TIFF.

</dd> <dt>

<span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11 \_ IFF \_ GIF**
</dt> <dd>

Graphics Interchange Format (GIF). A extensão de arquivo para esse formato é .gif.

</dd> <dt>

<span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11 \_ IFF \_ WMP**
</dt> <dd>

Windows Formato de foto de mídia (WMP). Esse formato também é conhecido como HD Photo e JPEG XR. As extensões de arquivo para esse formato são. HDP,. jxr e. WDP.

Para funcionar corretamente, o **D3DX11 \_ IFF \_ WMP** exige que você Inicialize com. Portanto, chame [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) em seu aplicativo antes de chamar D3DX.

</dd> <dt>

<span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ IFF \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

consulte [tipos de bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) para obter mais informações sobre alguns desses formatos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

