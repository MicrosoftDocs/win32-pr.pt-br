---
title: Tipo complexo ChannelLoggingType
description: Define as propriedades do arquivo de log que faz o retorno do canal, como sua capacidade e se ele é sequencial ou circular. | Tipo complexo ChannelLoggingType
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- Tipo complexo ChannelLoggingType EventLog
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e696837b1132a0b82ad428e7404892ae73de88e4435325d988b7936b3a6ba534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032276"
---
# <a name="channelloggingtype-complex-type"></a>Tipo complexo ChannelLoggingType

Define as propriedades do arquivo de log que faz o retorno do canal, como sua capacidade e se ele é sequencial ou circular.

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
| [**Autobackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) | booleano                                                           | Determina se um novo arquivo de log deve ser criado quando o arquivo de log atual atingir seu tamanho máximo. Definido como **true para** solicitar que o serviço crie um novo arquivo quando o arquivo de log atingir seu tamanho máximo; caso contrário, **false.** Você poderá definir [**autoBackup como**](eventmanifestschema-autobackup-channelloggingtype-element.md) true somente **se** [**a retenção**](eventmanifestschema-retention-channelloggingtype-element.md) for definida como **true.** O padrão é **false**.<br/> Não há nenhum limite para o número de arquivos de backup que o serviço pode criar (limitado apenas pelo espaço em disco disponível). Os nomes de arquivo de backup são do formato *Archive-channelName* timestamp .evtx e estão localizados na pasta - Logs winevt %windir% \\ System32 \\ winevt. \\<br/> |
| [**Maxsize**](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | O tamanho máximo, em bytes, do arquivo de log. O valor padrão (e mínimo) é 1 MB. Se o tamanho do log físico for menor que o tamanho máximo configurado e for necessário espaço adicional no log para armazenar eventos, o serviço alocará outro bloco de espaço mesmo que o tamanho físico resultante do log seja maior que o tamanho máximo configurado. O serviço aloca blocos de 1 MB para que o tamanho físico possa aumentar para até 1 MB maior que o tamanho máximo configurado. <br/>                                                                                                                                                                                                                                                      |
| [**Retenção**](eventmanifestschema-retention-channelloggingtype-element.md)   | booleano                                                           | Determina se o arquivo de log é um arquivo de log sequencial ou circular. Definido como **true para** um arquivo de log sequencial e **false para** um arquivo de log circular. O padrão é **false para** tipos de canal Admin e Operacional e **true para** tipos de canal Depuração e Análise.<br/> Para consultar um log circular, primeiro você deve desabilitar o canal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Comentários

Você pode especificar o **atributo maxSize** para qualquer tipo de canal.

Você pode especificar o **atributo autoBackup** somente para os tipos de canal Admin e Operational.

Você pode definir o atributo **de retenção** como false (registro em log circular) para os tipos de canal Admin e Operational. Você pode definir o atributo **de** retenção como false (log circular) para tipos de canal Depuração e Análise, mas para exibir os eventos no Windows Visualizador de Eventos, primeiro você precisará desabilitar o canal. Observe que, quando você habilita o canal novamente, os eventos são removidos do canal.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





