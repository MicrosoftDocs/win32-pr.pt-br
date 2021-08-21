---
title: Tipo complexo ChannelListType
description: Define uma lista de canais para os quais os provedores podem registrar eventos. | Tipo complexo ChannelListType
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- Tipo complexo ChannelListType EventLog
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8602594bdbdf6d39532213b0be660b5b3cfb6a90cd8281d9555ed2ff3a9d401
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121046"
---
# <a name="channellisttype-complex-type"></a>Tipo complexo ChannelListType

Define uma lista de canais para os quais os provedores podem registrar eventos.

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                            | Type                                                                           | Descrição                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Canal**](eventmanifestschema-channel-channellisttype-element.md)             | [**ChannelType**](eventmanifestschema-channeltype-complextype.md)             | Define um canal no qual os eventos podem ser registrados.<br/>                                                                  |
| [**importChannel**](eventmanifestschema-importchannel-channellisttype-element.md) | [**ImportChannelType**](eventmanifestschema-importchanneltype-complextype.md) | Identifica um canal que foi definido por outro provedor ou em um manifesto que contém uma seção de metadados.<br/> |



## <a name="remarks"></a>Comentários

Você pode especificar até oito canais (qualquer combinação de canais importados ou canais que você definir).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





