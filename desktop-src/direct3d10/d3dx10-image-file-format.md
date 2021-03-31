---
description: Formatos de arquivo de imagem com suporte pelas funções D3DXCreatexxx e D3DX10Savexxx.
ms.assetid: 39602f3c-5c91-4667-96d0-c3bdba712d88
title: Enumeração de D3DX10_IMAGE_FILE_FORMAT (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_FILE_FORMAT
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: fba878a40f510cc5e76256161255e01deaa7ee04
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664076"
---
# <a name="d3dx10_image_file_format-enumeration"></a>\_Enumeração de \_ formato de arquivo de imagem D3DX10 \_

Formatos de arquivo de imagem com suporte pelas funções D3DXCreatexxx e D3DX10Savexxx.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_IMAGE_FILE_FORMAT { 
  D3DX10_IFF_BMP          = 0,
  D3DX10_IFF_JPG          = 1,
  D3DX10_IFF_PNG          = 3,
  D3DX10_IFF_DDS          = 4,
  D3DX10_IFF_TIFF         = 10,
  D3DX10_IFF_GIF          = 11,
  D3DX10_IFF_WMP          = 12,
  D3DX10_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX10_IMAGE_FILE_FORMAT, *LPD3DX10_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ IFF \_ BMP**
</dt> <dd>

Formato de arquivo de bitmap do Windows (BMP). Contém um cabeçalho que descreve a resolução do dispositivo no qual o retângulo de pixels foi criado, as dimensões do retângulo, o tamanho da matriz de bits, uma paleta lógica e uma matriz de bits que define a relação entre os pixels na imagem de bitmap e as entradas na paleta lógica. A extensão de arquivo para esse formato é. bmp.

</dd> <dt>

<span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10 \_ IFF \_ jpg**
</dt> <dd>

Formato de arquivo compactado JPEG (Joint Experts Group). Especifica a compactação de variável de cores RGB de 24 bits e arquivos de documento de imagem TIFF de escala cinza de 8 bits. A extensão de arquivo para esse formato é. jpg.

</dd> <dt>

<span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10 \_ IFF \_ png**
</dt> <dd>

Formato de arquivo PNG (Portable Network Graphics). Um formato de bitmap não proprietário usando compactação sem perdas. A extensão de arquivo para esse formato é. png.

</dd> <dt>

<span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ IFF \_ DDS**
</dt> <dd>

Formato de arquivo da superfície do DirectDraw (DDS). Armazena texturas, texturas de volume e mapas de ambiente cúbico, com ou sem os níveis de mipmap, e com ou sem a compactação de pixel. A extensão de arquivo para esse formato é. DDS.

</dd> <dt>

<span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10 \_ IFF \_ TIFF**
</dt> <dd>

Formato TIFF (Tagged Image File Format). As extensões de arquivo para esse formato são. tif e. TIFF.

</dd> <dt>

<span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10 \_ IFF \_ GIF**
</dt> <dd>

Graphics Interchange Format (GIF). A extensão de arquivo para esse formato é. gif.

</dd> <dt>

<span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10 \_ IFF \_ WMP**
</dt> <dd>

Windows Media Photo Format (WMP). Esse formato também é conhecido como HD Photo e JPEG XR. As extensões de arquivo para esse formato são. HDP,. jxr e. WDP.

Para funcionar corretamente, o **D3DX10 \_ IFF \_ WMP** exige que você Inicialize com. Portanto, chame [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) em seu aplicativo antes de chamar D3DX.

</dd> <dt>

<span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ IFF \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Consulte [tipos de bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) para obter mais informações sobre alguns desses formatos.

O D3DX10 usa o Windows Imaging Component para implementar a maioria dos tipos de arquivo de bitmap com suporte. Consulte [visão geral do Windows Imaging Component](https://msdn.microsoft.com/library/ms737408.aspx) para obter informações adicionais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
