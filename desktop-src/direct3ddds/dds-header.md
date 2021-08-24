---
title: Estrutura de DDS_HEADER (DDS. h)
description: Descreve um cabeçalho de arquivo DDS.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS_HEADER de estrutura DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d974c319206d0a0cbe6abda291e9d376bd6478a5b8eb8ba3ef3bb12f182b1288
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745996"
---
# <a name="dds_header-structure"></a>Estrutura do cabeçalho do DDS \_

Descreve um cabeçalho de arquivo DDS.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwSize**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamanho da estrutura. Esse membro deve ser definido como 124.

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Sinalizadores para indicar quais membros contêm dados válidos.



| Sinalizador              | Descrição                                                  | Valor    |
|-------------------|--------------------------------------------------------------|----------|
| DDSD \_ Caps        | Necessário em cada arquivo. DDS.                                 | 0x1      |
| altura de DDSD \_      | Necessário em cada arquivo. DDS.                                 | 0x2      |
| largura de DDSD \_       | Necessário em cada arquivo. DDS.                                 | 0x4      |
| DDSD \_       | Necessário quando pitch é fornecido para uma textura não compactada. | 0x8      |
| \_PIXELFORMAT DDSD | Necessário em cada arquivo. DDS.                                 | 0x1000   |
| DDSD \_ MIPMAPCOUNT | Necessário em uma textura mipmapped.                             | 0x20000  |
| DDSD \_ LINEARSIZE  | Necessário quando pitch é fornecido para uma textura compactada.    | 0x80000  |
| profundidade de DDSD \_       | Necessário em uma textura de profundidade.                                 | 0x800000 |



 

> [!Note]  
> Ao gravar arquivos. DDS, você deve definir os sinalizadores DDSD \_ Caps e DDSD \_ PixelFormats e, para texturas Mipmapped, você também deve definir o \_ sinalizador DDSD MIPMAPCOUNT. No entanto, ao ler um arquivo. DDS, você não deve contar com os \_ sinalizadores DDSD Caps, DDSD \_ PIXELFORMAT e DDSD \_ MIPMAPCOUNT sendo definidos porque alguns gravadores desse arquivo podem não definir esses sinalizadores.

 

O sinalizador de textura de sinalizadores de cabeçalho do DDS \_ \_ \_ , que é definido em DDS. h, é uma combinação de bit-a-or ou de DDSD \_ Caps, DDSD \_ Height, largura de DDSD \_ e sinalizadores de \_ PIXELFORMAT DDSD.

O sinalizador MIPMAP do cabeçalho do DDS sinaliza \_ \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador DDSD MIPMAPCOUNT.

O \_ sinalizador de volume flags de cabeçalho do DDS \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador de profundidade DDSD.

O sinalizador de densidade dos sinalizadores de cabeçalho do DDS \_ \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador de densidade DDSD.

O sinalizador LINEARSIZE do cabeçalho do DDS sinaliza \_ \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador DDSD LINEARSIZE.

</dd> <dt>

**dwHeight**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Altura da superfície (em pixels).

</dd> <dt>

**dwWidth**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Largura da superfície (em pixels).

</dd> <dt>

**dwPitchOrLinearSize**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

A densidade ou o número de bytes por linha de varredura em uma textura não compactada; o número total de bytes na textura de nível superior para uma textura compactada. Para obter informações sobre como calcular o timbre, consulte a seção de layout de arquivo DDS do [Guia de programação do DDS](dx-graphics-dds-pguide.md).

</dd> <dt>

**dwDepth**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profundidade de uma textura de volume (em pixels), caso contrário, não utilizada.

</dd> <dt>

**dwMipMapCount**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de níveis de mipmap, caso contrário, não utilizado.

</dd> <dt>

**dwReserved1 \[ 11\]**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Não utilizado.

</dd> <dt>

**ddspf**
</dt> <dd>

Tipo: o **[ **DDS \_ PIXELFORMAT**](dds-pixelformat.md)**

</dd> <dd>

O formato de pixel (consulte [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)).

</dd> <dt>

**dwCaps**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Especifica a complexidade das superfícies armazenadas.



| Sinalizador             | Descrição                                                                                                                              | Valor    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| DDSCAPS \_ complexo | Adicional deve ser usado em qualquer arquivo que contenha mais de uma superfície (um mipmap, um mapa de ambiente cúbico ou uma textura de volume mipmapped). | 0x8      |
| DDSCAPS \_ MIPMAP  | Adicional deve ser usado para um mipmap.                                                                                                   | 0x400000 |
| \_textura DDSCAPS | Obrigatório                                                                                                                                 | 0x1000   |



 

> [!Note]  
> Ao gravar arquivos. DDS, você deve definir o sinalizador de \_ textura DDSCAPS e, para várias superfícies, você também deve definir o \_ sinalizador complexo DDSCAPS. No entanto, ao ler um arquivo. DDS, você não deve contar com a \_ textura DDSCAPS e os \_ sinalizadores complexos DDSCAPS estão sendo definidos porque alguns gravadores desse arquivo podem não definir esses sinalizadores.

 

O \_ \_ sinalizador MIPMAP dos sinalizadores de superfície do DDS \_ , que é definido em DDS. h, é uma combinação bit-a-or dos \_ sinalizadores DDSCAPS complexos e DDSCAPS \_ MIPMAP.

O sinalizador de textura de sinalizadores de superfície de DDS \_ \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador de textura DDSCAPS.

O \_ sinalizador CUBEMAP dos sinalizadores de superfície do DDS \_ \_ , que é definido em DDS. h, é igual ao \_ sinalizador complexo DDSCAPS.

</dd> <dt>

**dwCaps2**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Detalhes adicionais sobre as superfícies armazenadas.



| Sinalizador                         | Descrição                                            | Valor    |
|------------------------------|--------------------------------------------------------|----------|
| DDSCAPS2 \_ CUBEMAP            | Necessário para um mapa de cubo.                               | 0x200    |
| DDSCAPS2 \_ CUBEMAP \_ POSITIVEX | Necessário quando essas superfícies são armazenadas em um mapa de cubo. | 0x400    |
| DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX | Necessário quando essas superfícies são armazenadas em um mapa de cubo. | 0x800    |
| DDSCAPS2 \_ CUBEMAP \_ positiva | Necessário quando essas superfícies são armazenadas em um mapa de cubo. | 0x1000   |
| DDSCAPS2 \_ CUBEMAP \_ negativa | Necessário quando essas superfícies são armazenadas em um mapa de cubo. | 0x2000   |
| DDSCAPS2 \_ CUBEMAP \_ POSITIVEZ | Necessário quando essas superfícies são armazenadas em um mapa de cubo. | 0x4000   |
| DDSCAPS2 \_ CUBEMAP \_ NEGATIVEZ | Necessário quando essas superfícies são armazenadas em um mapa de cubo. | 0x8000   |
| \_Volume DDSCAPS2             | Necessário para uma textura de volume.                         | 0x200000 |



 

O \_ sinalizador de POSITIVEX DDS CUBEMAP \_ , que é definido em DDS. h, é uma combinação bit-a-or de DDSCAPS2 \_ CUBEMAP e DDSCAPS2 CUBEMAP POSITIVEX \_ \_ flags.

O \_ sinalizador de NEGATIVEX DDS CUBEMAP \_ , que é definido em DDS. h, é uma combinação bit-a-or de DDSCAPS2 \_ CUBEMAP e DDSCAPS2 CUBEMAP NEGATIVEX \_ \_ flags.

O \_ sinalizador de positiva CUBEMAP de DDS \_ , que é definido em DDS. h, é uma combinação de bit-a-or ou DDSCAPS2 \_ CUBEMAP e DDSCAPS2 \_ CUBEMAP de \_ sinalizadores positivos.

O \_ sinalizador de \_ negativo CUBEMAP de DDS, que é definido em DDS. h, é uma combinação de bit-a-or ou DDSCAPS2 \_ CUBEMAP e DDSCAPS2 \_ CUBEMAP de \_ sinalizadores negativos.

O \_ sinalizador de POSITIVEZ DDS CUBEMAP \_ , que é definido em DDS. h, é uma combinação bit-a-or de DDSCAPS2 \_ CUBEMAP e DDSCAPS2 CUBEMAP POSITIVEZ \_ \_ flags.

O \_ sinalizador de NEGATIVEZ DDS CUBEMAP \_ , que é definido em DDS. h, é uma combinação bit-a-or de DDSCAPS2 \_ CUBEMAP e DDSCAPS2 CUBEMAP NEGATIVEZ \_ \_ flags.

O sinalizador de CUBEMAP de DDS \_ \_ , que é definido em DDS. h, é uma combinação de bit-a-or ou de DDS \_ CUBEMAP \_ POSITIVEX, DDS \_ CUBEMAP \_ NEGATIVEX, DDS \_ CUBEMAP \_ positivo, DDS \_ CUBEMAP \_ negativo, DDS \_ CUBEMAP \_ POSITIVEZ e DDSCAPS2 CUBEMAP \_ NEGATIVEZ \_ flags.

O \_ sinalizador de volume de sinalizadores DDS \_ , que é definido em DDS. h, é igual ao \_ sinalizador de volume DDSCAPS2.

> [!Note]  
> Embora o Direct3D 9 ofereça suporte a mapas de cubos parciais, o Direct3D 10, o 10,1 e o 11 exigem que você defina todas as seis faces do mapa de cubos (ou seja, você deve definir o DDS \_ CUBEMAP \_ ).

 

</dd> <dt>

**dwCaps3**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Não utilizado.

</dd> <dt>

**dwCaps4**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Não utilizado.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Não utilizado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Inclua sinalizadores no **dwFlags** para os membros da estrutura que contêm dados válidos.

Use essa estrutura em combinação com um [**\_ cabeçalho DDS \_ DXT10**](dds-header-dxt10.md) para armazenar uma matriz de recursos em um arquivo DDS. Para obter mais informações, consulte [matrizes de textura](dx-graphics-dds-pguide.md).

**DDS \_ O cabeçalho** é idêntico à estrutura DDSURFACEDESC2 do DirectDraw sem dependências do DirectDraw.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência para DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

