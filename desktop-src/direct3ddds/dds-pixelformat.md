---
title: DDS_PIXELFORMAT estrutura (Dds.h)
description: Formato de pixel da superfície.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS_PIXELFORMAT estrutura DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e2c8d4b5e30a3a5a9a039e27f5704019a6300c
ms.sourcegitcommit: 205567a2a76ad672a493a0203ff9d61271d9df98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/18/2021
ms.locfileid: "122358902"
---
# <a name="dds_pixelformat-structure"></a>Estrutura DDS \_ PIXELFORMAT

Formato de pixel da superfície.

## <a name="syntax"></a>Sintaxe


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwsize**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamanho da estrutura; definido como 32 (bytes).

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valores que indicam que tipo de dados estão na superfície.



| Sinalizador              | Descrição                                                                                                                                                                                                                                | Valor   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| ALFAPIXELS DDPF \_ | A textura contém dados alfa; **dwRGBAlphaBitMask** contém dados válidos.                                                                                                                                                                    | 0x1     |
| DDPF \_ ALPHA       | Usado em alguns arquivos DDS mais antigos para o canal alfa apenas dados descompactados (dwRGBBitCount contém a contagem de bits do canal alfa; dwABitMask contém dados válidos)                                                                                  | 0x2     |
| DDPF \_ FOURCC      | A textura contém dados RGB compactados; **dwEarCC contém** dados válidos.                                                                                                                                                                    | 0x4     |
| DDPF \_ RGB         | A textura contém dados RGB descompactados; **dwRGBBitCount** e as máscaras RGB (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contêm dados válidos.                                                                                           | 0x40    |
| DDPF \_ YUV         | Usado em alguns arquivos DDS mais antigos para dados descompactados YUV (dwRGBBitCount contém a contagem de bits YUV; dwRBitMask contém a máscara Y, dwGBitMask contém a máscara U, dwBBitMask contém a máscara V)                                          | 0x200   |
| LUMINÂNCIA DDPF \_   | Usado em alguns arquivos DDS mais antigos para dados descompactados de cor de canal único (dwRGBBitCount contém a contagem de bits do canal de luminância; dwRBitMask contém a máscara de canal). Pode ser combinado com o \_ DDPF ALPHAPIXELS para um arquivo DDS de dois canais. | 0x20000 |



 

</dd> <dt>

**dwEarCC**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Códigos de quatro caracteres para especificar formatos compactados ou personalizados. Os valores possíveis incluem: *DXT1,* *DXT2,* *DXT3,* *DXT4* ou *DXT5.* Um FourCC de DX10 indica o pré-requisito do [**\_ header \_ DDS DXT10**](dds-header-dxt10.md) estendido e o membro dxgiFormat dessa estrutura indica o formato verdadeiro. Ao usar um código de quatro caracteres, dwFlags deve incluir *DDPF \_ FOURCC*.

</dd> <dt>

**dwRGBBitCount**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bits em um formato RGB (possivelmente, incluindo alfa). Válido quando **dwFlags** inclui *DDPF \_ RGB,* *DDPF \_ LUMINANCE* ou *DDPF \_ YUV.*

</dd> <dt>

**dwRBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara vermelha (ou luminância ou Y) para ler dados de cores. Por exemplo, considerando o formato A8R8G8B8, a máscara vermelha seria 0x00ff0000.

</dd> <dt>

**dwGBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara verde (ou U) para ler dados de cores. Por exemplo, considerando o formato A8R8G8B8, a máscara verde seria 0x0000ff00.

</dd> <dt>

**dwBBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara azul (ou V) para ler dados de cor. Por exemplo, considerando o formato A8R8G8B8, a máscara azul seria 0x000000ff.

</dd> <dt>

**dwABitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara alfa para leitura de dados alfa. dwFlags deve incluir *DDPF \_ ALPHAPIXELS* ou *DDPF \_ ALPHA.* Por exemplo, considerando o formato A8R8G8B8, a máscara alfa seria 0xff000000.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para armazenar formatos DXGI, como dados de ponto flutuante, use **um dwFlags** de DDPF FOURCC e defina \_ **dwNixCC** como 'D','X','1','0'. Use o [**header de extensão \_ \_ DXT10 do HEADER DDS**](dds-header-dxt10.md) para armazenar o formato DXGI no **membro dxgiFormat.**

Observe que há variantes não padrão de arquivos DDS em que **dwFlags** tem DDPF FOURCC e o valor dwMaxCC é definido diretamente como um valor de \_ enumeração D3DFORMAT ou DXGI  \_ FORMAT. Não é possível desambiguar os valores D3DFORMAT versus DXGI FORMAT usando esse esquema não padrão, portanto, o header de extensão DX10 é recomendado em vez \_ disso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dds.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência para DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

