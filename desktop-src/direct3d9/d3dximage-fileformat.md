---
description: Descreve os formatos de arquivo de imagem com suporte. Consulte comentários para obter descrições desses formatos.
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: Enumeração de D3DXIMAGE_FILEFORMAT (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_FILEFORMAT
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 715b9f0f6d8c56153d51c9c19b70ba253e508619229f52201a28f23c1902d26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123162"
---
# <a name="d3dximage_fileformat-enumeration"></a>\_Enumeração de FILEformat D3DXIMAGE

Descreve os formatos de arquivo de imagem com suporte. Consulte comentários para obter descrições desses formatos.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXIMAGE_FILEFORMAT { 
  D3DXIFF_BMP          = 0,
  D3DXIFF_JPG          = 1,
  D3DXIFF_TGA          = 2,
  D3DXIFF_PNG          = 3,
  D3DXIFF_DDS          = 4,
  D3DXIFF_PPM          = 5,
  D3DXIFF_DIB          = 6,
  D3DXIFF_HDR          = 7,
  D3DXIFF_PFM          = 8,
  D3DXIFF_FORCE_DWORD  = 0x7fffffff
} D3DXIMAGE_FILEFORMAT, *LPD3DXIMAGE_FILEFORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**
</dt> <dd>

formato de arquivo de bitmap Windows (BMP).

</dd> <dt>

<span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ jpg**
</dt> <dd>

Formato de arquivo compactado do JPEG (Joint Experts Group).

</dd> <dt>

<span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF \_ TGA**
</dt> <dd>

Formato de arquivo de imagem Truevision (Targa ou TGA).

</dd> <dt>

<span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ png**
</dt> <dd>

Formato de arquivo PNG (Portable Network Graphics).

</dd> <dt>

<span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**
</dt> <dd>

Formato de arquivo da superfície do DirectDraw (DDS).

</dd> <dt>

<span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**\_Ppm D3DXIFF**
</dt> <dd>

formato de arquivo pixmap (PPM portátil).

</dd> <dt>

<span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**\_DIB D3DXIFF**
</dt> <dd>

Windows formato de arquivo DIB (bitmap independente de dispositivo).

</dd> <dt>

<span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**\_HDR D3DXIFF**
</dt> <dd>

Formato de arquivo de intervalo dinâmico alto (HDR).

</dd> <dt>

<span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**
</dt> <dd>

Formato de arquivo do mapa float portátil.

</dd> <dt>

<span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Funções que começam com D3DXLoadxxx dão suporte a todos os formatos listados. Funções que começam com D3DXSavexxx dão suporte a todos os formatos listados, exceto os formatos Truevision (. tga) e pixmap portátil (. ppm).

A tabela a seguir lista os formatos de entrada e saída disponíveis.



| Extensão do arquivo | Descrição                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .bmp           | Windows formato de bitmap. Contém um cabeçalho que descreve a resolução do dispositivo no qual o retângulo de pixels foi criado, as dimensões do retângulo, o tamanho da matriz de bits, uma paleta lógica e uma matriz de bits que define a relação entre os pixels na imagem de bitmap e as entradas na paleta lógica. |
| .dds           | Formato do arquivo de superfície do DirectDraw. Armazena texturas, texturas de volume e mapas de ambiente cúbico, com ou sem os níveis de mipmap, e com ou sem a compactação de pixel. Consulte [DDS](../direct3ddds/dx-graphics-dds.md).                                                                                                                                       |
| .dib           | Windows DIB. Contém uma matriz de bits combinada com estruturas que especificam a largura e a altura da imagem de bitmap, o formato de cor do dispositivo no qual a imagem foi criada e a resolução do dispositivo usado para criar essa imagem.                                                                                                              |
| . HDR           | Formato HDR. Codifica cada pixel como uma cor de RGBE de 32 bits, com 8 bits de mantissa para vermelho, verde e azul, e um expoente de 8 bits compartilhado. Cada canal é compactado separadamente com RLE (codificação de comprimento de execução).                                                                                                                                       |
| .jpg           | Padrão JPEG. Especifica a compactação de variável de cores RGB de 24 bits e arquivos de documento de imagem TIFF de escala cinza de 8 bits.                                                                                                                                                                                                       |
| . PFM           | Formato de mapa float portátil. Um formato de imagem de ponto flutuante não processado, sem nenhuma compactação. O cabeçalho do arquivo especifica a largura da imagem, a altura, o monocromático ou a cor e a ordem das palavras do computador. Os dados de pixel são armazenados como valores de ponto flutuante de 32 bits, com 3 valores por pixel para cor e um valor por pixel para monocromático.                                |
| .png           | Formato PNG. Um formato de bitmap não proprietário usando compactação sem perdas.                                                                                                                                                                                                                                                                            |
| . ppm           | Formato pixmap portátil. Um formato de arquivo binário ou ASCII para imagens coloridas que inclui a altura e a largura da imagem e o valor do componente de cor máximo.                                                                                                                                                                                                 |
| .tga           | Formato de adaptador gráfico Targa ou Truevision. Dá suporte a profundidades de 8, 15, 16, 24 e 32 bits, incluindo a escala de cinza de 8 bits e contém dados de paleta de cores opcionais, dados de origem (x, y) e de tamanho e dados de pixel.                                                                                                                               |



 

Consulte [tipos de bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) para obter mais informações sobre alguns desses formatos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
