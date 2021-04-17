---
description: A \_ estrutura de cabeçalho bruto do WIA \_ define uma imagem no formato de dados brutos de um dispositivo e permite que os aplicativos usem o formato bruto em transferências do WIA (aquisição de imagem do Windows).
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: Estrutura de WIA_RAW_HEADER (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 8da33f0b257168712f1b16fb7f940df5db862d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798270"
---
# <a name="wia_raw_header-structure"></a>\_Estrutura de \_ cabeçalho bruto WIA

A estrutura de **\_ \_ cabeçalho bruto do WIA** define uma imagem no formato de dados brutos de um dispositivo e permite que os aplicativos usem o formato bruto em transferências do WIA (aquisição de imagem do Windows).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tag**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O nome do formato. Deve ser o ' WRAW ' literal (quatro caracteres ASCII de byte único).

</dd> <dt>

**Versão**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

A versão do formato bruto. Sempre use 0x00010000.

</dd> <dt>

**Cabeçalhosize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O total de bytes válidos no cabeçalho.

</dd> <dt>

**XRes**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

A resolução horizontal em pontos por polegada.

</dd> <dt>

**YRes**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

A resolução vertical em pontos por polegada.

</dd> <dt>

**XExtent**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

A largura da imagem em pixels.

</dd> <dt>

**YExtent**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

A altura da imagem em pixels.

</dd> <dt>

**BytesPerLine**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O número de bytes em uma linha de uma imagem descompactada. Use 0 quando os dados forem compactados para sinalizar que o número de bytes por linha é desconhecido.

</dd> <dt>

**BitsPerPixel**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O número total de bits por pixel para todos os canais do pixel.

</dd> <dt>

**ChannelsPerPixel**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O número de canais de cores em um pixel.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O \_ \_ tipo de dados IPA WIA da imagem. Como \_ o formato IPA do WIA \_ é definido como WiaImgFmt \_ RAW, essa é uma lista de valores permitidos dos quais o aplicativo é escolhido.

</dd> <dt>

**BitsPerChannel \[ 8\]**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

O número de bits em um canal, até um máximo de 8.

</dd> <dt>

**Compactação**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Um \_ \_ valor de compactação IPA WIA que especifica o tipo de compactação usado, se houver.

</dd> <dt>

**PhotometricInterp**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Um \_ \_ valor INTERP IPA da multimetric do WIA \_ que especifica a interpretação fotométrica da imagem.

</dd> <dt>

**LineOrder**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Um valor que representa a ordem da linha da imagem. Essa é sempre a \_ ordem de linha WIA da \_ \_ parte superior \_ ou da \_ \_ \_ ordem de linha WIA \_ inferior \_ para a parte \_ superior.

</dd> <dt>

**RawDataOffset**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

A posição dos dados brutos da imagem em bytes, começando da posição onde o cabeçalho termina ou da posição onde a paleta termina.

</dd> <dt>

**RawDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tamanho, em bytes, dos dados brutos da imagem.

</dd> <dt>

**PaletteOffset**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

A posição da paleta em bytes, a partir da posição onde o cabeçalho termina ou da posição onde os dados são encerrados. (Esse valor será 0, se não houver nenhuma paleta.)

</dd> <dt>

**PaletteSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tamanho, em bytes, da tabela de paleta. (Isso será 0, se não houver nenhuma paleta.)

</dd> </dl>

## <a name="remarks"></a>Comentários

Como esse não é um formato de arquivo, use uma cadeia de caracteres vazia para a \_ propriedade de extensão de arquivo WIA IPA \_ \_ .

A paleta e os dados podem ser obtidos em qualquer ordem.

**RawDataSize** não inclui o cabeçalho ou a paleta. Use esse campo para verificar se a transferência da imagem foi bem-sucedida.

**PaletteSize** é bytes, não o número de entradas na paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




