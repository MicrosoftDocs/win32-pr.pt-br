---
title: Estrutura de DDS_PIXELFORMAT (DDS. h)
description: Formato de pixel de superfície.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS_PIXELFORMAT de estrutura DDS
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
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815505"
---
# <a name="dds_pixelformat-structure"></a>Estrutura de PIXELFORMAT do DDS \_

Formato de pixel de superfície.

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

**dwSize**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamanho da estrutura; Defina como 32 (bytes).

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valores que indicam que tipo de dados está na superfície.



| Sinalizador              | Descrição                                                                                                                                                                                                                                | Valor   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| DDPF \_ ALPHAPIXELS | A textura contém dados alfa; **dwRGBAlphaBitMask** contém dados válidos.                                                                                                                                                                    | 0x1     |
| DDPF \_ alfa       | Usado em alguns arquivos DDS mais antigos para dados não compactados somente do canal alfa (dwRGBBitCount contém o canal alfa BitCount; dwABitMask contém dados válidos)                                                                                  | 0x2     |
| DDPF \_ FOURCC      | A textura contém dados RGB compactados; **dwFourCC** contém dados válidos.                                                                                                                                                                    | 0x4     |
| DDPF \_ RGB         | A textura contém dados RGB descompactados; **dwRGBBitCount** e as máscaras RGB (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contêm dados válidos.                                                                                           | 0x40    |
| \_YUV DDPF         | Usado em alguns arquivos DDS mais antigos para dados não compactados YUV (dwRGBBitCount contém a contagem de bits YUV; dwRBitMask contém a máscara Y, dwGBitMask contém a máscara U, dwBBitMask contém a máscara V)                                          | 0x200   |
| luminância de DDPF \_   | Usado em alguns arquivos DDS mais antigos para dados descompactados de cor de canal único (dwRGBBitCount contém a contagem de bits de canal de luminescência; dwRBitMask contém a máscara de canal). Pode ser combinado com DDPF \_ ALPHAPIXELS para um arquivo DDS de dois canais. | 0x20000 |



 

</dd> <dt>

**dwFourCC**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Códigos de quatro caracteres para especificar formatos compactados ou personalizados. Os valores possíveis incluem: *DXT1*, *DXT2*, *DXT3*, *DXT4* ou *DXT5*. Um FourCC de DX10 indica o prescense do cabeçalho [**DDS \_ \_ DXT10**](dds-header-dxt10.md) Header e o membro dxgiFormat dessa estrutura indica o formato verdadeiro. Ao usar um código de quatro caracteres, o dwFlags deve incluir *DDPF \_ FOURCC*.

</dd> <dt>

**dwRGBBitCount**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bits em um formato RGB (possivelmente incluindo alfa). Válido quando **dwFlags** inclui *DDPF \_ RGB*, *DDPF \_ luminescência* ou *DDPF \_ YUV*.

</dd> <dt>

**dwRBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara vermelha (ou lumiannce ou Y) para a leitura de dados de cores. Por exemplo, considerando o formato A8R8G8B8, a máscara vermelha seria 0x00ff0000.

</dd> <dt>

**dwGBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara verde (ou U) para leitura de dados de cor. Por exemplo, considerando o formato A8R8G8B8, a máscara verde seria 0x0000ff00.

</dd> <dt>

**dwBBitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara azul (ou V) para leitura de dados de cor. Por exemplo, considerando o formato A8R8G8B8, a máscara azul seria 0x000000FF.

</dd> <dt>

**dwABitMask**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara alfa para leitura de dados alfa. dwFlags deve incluir *DDPF \_ ALPHAPIXELS* ou *DDPF \_ Alpha*. Por exemplo, dado o formato A8R8G8B8, a máscara alfa seria 0xff000000.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para armazenar formatos DXGI, como dados de ponto flutuante, use um **dwFlags** de DDPF \_ FOURCC e defina **dwFourCC** como ' d', ' X ', ' 1 ', ' 0 '. Use o cabeçalho de extensão [**\_ \_ DXT10 de cabeçalho DDS**](dds-header-dxt10.md) para armazenar o formato dxgi no membro **dxgiFormat** .

Observe que há variantes não padrão de arquivos DDS em que **dwFlags** tem DDPF \_ FOURCC e o valor **dwFourCC** é definido diretamente para um valor de enumeração de formato D3DFORMAT ou dxgi \_ . Não é possível desambiguar os valores de formato D3DFORMAT versus DXGI \_ usando esse esquema não padrão, portanto, o cabeçalho de extensão DX10 é recomendado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência para DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

