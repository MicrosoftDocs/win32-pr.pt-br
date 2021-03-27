---
description: Essa classe é a classe de tipo de evento para eventos de carregamento de imagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Classe Image_V1_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd0a2a61b263ce78c2cf28cdf1cd5df4b702140d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967292"
---
# <a name="image_v1_load-class"></a>\_Classe de \_ carga Image v1

Essa classe é a classe de tipo de evento para eventos de carregamento de imagem.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a>Membros

A classe de **\_ \_ carga Image v1** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ \_ carga Image v1** tem essas propriedades.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Nome do arquivo e extensão da imagem DLL ou executável a ser carregada.

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

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Imagem \_ v1**](image-v1.md)
</dt> </dl>

 

 




