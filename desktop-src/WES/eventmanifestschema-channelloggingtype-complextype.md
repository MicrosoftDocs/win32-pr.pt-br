---
title: Tipo complexo ChannelLoggingType
description: Define as propriedades do arquivo de log que faz o backup do canal, como sua capacidade e se ele é sequencial ou circular. | Tipo complexo ChannelLoggingType
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- Log de eventos do tipo complexo ChannelLoggingType
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cfaf6dfa225799befcd0c7fb068c0f779ea33eb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104091931"
---
# <a name="channelloggingtype-complex-type"></a>Tipo complexo ChannelLoggingType

Define as propriedades do arquivo de log que faz o backup do canal, como sua capacidade e se ele é sequencial ou circular.

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                         | Type                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Backup automático**](eventmanifestschema-autobackup-channelloggingtype-element.md) | booleano                                                           | Determina se um novo arquivo de log deve ser criado quando o arquivo de log atual atinge seu tamanho máximo. Defina como **true** para solicitar que o serviço crie um novo arquivo quando o arquivo de log atingir seu tamanho máximo; caso contrário, **false**. Você pode definir o [**backup**](eventmanifestschema-autobackup-channelloggingtype-element.md) único como **true** somente se a [**retenção**](eventmanifestschema-retention-channelloggingtype-element.md) estiver definida como **true**. O padrão é **false**.<br/> Não há nenhum limite para o número de arquivos de backup que o serviço pode criar (limitado apenas pelo espaço em disco disponível). Os nomes dos arquivos de backup estão no formato Archive-*channelName* - *timestamp*. evtx e estão localizados na pasta% windir% \\ System32 \\ winevt \\ logs.<br/> |
| [**maxSize**](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [**UInt64type**](eventmanifestschema-hexint64type-simpletype.md) | O tamanho máximo, em bytes, do arquivo de log. O valor padrão (e mínimo) é 1 MB. Se o tamanho do log físico for menor que o tamanho máximo configurado e o espaço adicional for necessário no log para armazenar eventos, o serviço alocará outro bloco de espaço, mesmo se o tamanho físico resultante do log for maior do que o tamanho máximo configurado. O serviço aloca blocos de 1 MB para que o tamanho físico possa aumentar para até 1 MB maior do que o tamanho máximo configurado. <br/>                                                                                                                                                                                                                                                      |
| [**políticas**](eventmanifestschema-retention-channelloggingtype-element.md)   | booleano                                                           | Determina se o arquivo de log é um arquivo de log seqüencial ou circular. Defina como **true** para um arquivo de log sequencial e **false** para um arquivo de log circular. O padrão é **false** para os tipos de canal de administração e operacionais e **verdadeiro** para os tipos de canal analítico e de depuração.<br/> Para consultar um log circular, primeiro você deve desabilitar o canal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Comentários

Você pode especificar o atributo **MaxSize** para qualquer tipo de canal.

Você pode especificar o atributo de **backup** único somente para os tipos de canal de administrador e operacional.

Você pode definir o atributo de **retenção** como falso (log circular) para os tipos de canal de administrador e operacional. Você pode definir o atributo de **retenção** como falso (log circular) para tipos de canal analíticos e de depuração, mas para exibir os eventos no Visualizador de eventos do Windows, você precisará primeiro desabilitar o canal. Observe que, quando você habilita o canal novamente, os eventos são removidos do canal.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





