---
description: Classe Image_V0_Load-essa classe é a classe de tipo de evento para eventos de carregamento de imagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Classe Image_V0_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: ed15254ac509334c802ba4c6165c73e681a2c7b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106504"
---
# <a name="image_v0_load-class"></a>\_Classe de carregamento V0 de imagem \_

Essa classe é a classe de tipo de evento para eventos de carregamento de imagem.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a>Membros

A classe de **\_ \_ carga V0 de imagem** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ \_ carregamento V0 de imagem** tem essas propriedades.

<dl> <dt>

BaseAddress
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), ponteiro
</dt> </dl>

Endereço base do aplicativo no qual a imagem é carregada.

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Nome do arquivo e extensão da imagem DLL ou executável a ser carregada.

</dd> <dt>

Módulosize
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2)
</dt> </dl>

Tamanho da imagem.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**V0 de imagem \_**](image-v0.md)
</dt> </dl>

 

 




