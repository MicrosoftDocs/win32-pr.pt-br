---
title: Elemento AcceptServerName (PeapExtensionsType)
description: O elemento AcceptServerName (PeapExtensionsType) indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada em ServerNames no esquema mspeapconnectionpropertiesv2.
ms.assetid: 24409775-d00d-439f-bb0b-a9fe5fb736a7
keywords:
- Elemento AcceptServerName EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64e82defae9c5ae9f7cf60056cfdac8b58373602
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989471"
---
# <a name="acceptservername-peapextensionstype-element"></a>Elemento AcceptServerName (PeapExtensionsType)

O **elemento AcceptServerName (PeapExtensionsType)** indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento [**ServerNames (ServerValidationParameters).**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

O **elemento AcceptServerName** é definido pelo [**elemento PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)

## <a name="remarks"></a>Comentários

O **elemento AcceptServerName** é opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos \[ da área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Somente aplicativos da área de trabalho do Windows Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





