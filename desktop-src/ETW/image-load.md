---
description: Essa classe é a classe de tipo de evento para eventos de imagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Classe Image_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505727"
---
# <a name="image_load-class"></a>Classe de carregamento de imagem \_

Essa classe é a classe de tipo de evento para eventos de imagem.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a>Membros

A classe de **\_ carregamento de imagem** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ carregamento de imagem** tem essas propriedades.

<dl> <dt>

Defaultbase
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (7), ponteiro
</dt> </dl>

Endereço base padrão.

</dd> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (12), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Nome do arquivo e extensão da imagem DLL ou executável.

</dd> <dt>

ImageBase
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

Endereço base do aplicativo no qual a imagem é carregada.

</dd> <dt>

ImageCheckSum
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4)
</dt> </dl>

Soma da verificação de imagem.

</dd> <dt>

ImageSize
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), ponteiro
</dt> </dl>

Tamanho da imagem que está sendo carregada.

Ao consumir essa propriedade, o tipo de dados para essa propriedade é realmente o tamanho \_ t. O qualificador de ponteiro é usado para determinar se o tamanho \_ t é de 4 bytes ou 8 bytes.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3)
</dt> </dl>

Identifica o processo no qual a imagem é carregada.

</dd> <dt>

Reserved0
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (6)
</dt> </dl>

Reservado.

</dd> <dt>

Reserved1
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (8)
</dt> </dl>

Reservado.

</dd> <dt>

Reserved2
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (9)
</dt> </dl>

Reservado.

</dd> <dt>

Reserved3
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (10)
</dt> </dl>

Reservado.

</dd> <dt>

Reserved4
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (11)
</dt> </dl>

Reservado.

</dd> <dt>

TimeDateStamp
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (5)
</dt> </dl>

Hora e data em que a imagem foi carregada ou descarregada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os eventos DCStart e DCEnd enumeram todas as imagens carregadas no início e no final do rastreamento, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Imagem**](image.md)
</dt> <dt>

[**V0 de imagem \_**](image-v0.md)
</dt> <dt>

[**Imagem \_ v1**](image-v1.md)
</dt> </dl>

 

 




