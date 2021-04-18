---
title: Tipo complexo ChannelPublishingType
description: Define as propriedades de log para a sessão que o canal usa. | Tipo complexo ChannelPublishingType
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- Log de eventos do tipo complexo ChannelPublishingType
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105800197"
---
# <a name="channelpublishingtype-complex-type"></a>Tipo complexo ChannelPublishingType

Define as propriedades de log para a sessão que o canal usa.

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
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



| Elemento                                                                              | Type                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**bufferSize**](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [**UInt32type**](eventmanifestschema-hexint32type-simpletype.md) | A quantidade de memória, em quilobytes, a ser alocada para cada buffer. Se você espera uma taxa de eventos relativamente baixa, o tamanho do buffer deve ser definido como o tamanho da página de memória. Se espera-se que a taxa de eventos seja relativamente alta, você deve especificar um tamanho de buffer maior e aumentar o número máximo de buffers.<br/> O tamanho do buffer afeta a taxa na qual os buffers são preenchidos e devem ser liberados. Embora um pequeno tamanho de buffer exija menos memória, ele aumenta a taxa em que os buffers devem ser liberados.<br/> O tamanho de buffer padrão para os canais analíticos e de depuração é 4 KB e para administração e operacional é 64 KB.<br/>                                                                                                                |
| [**clocktype**](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | A resolução de relógio a ser usada ao registrar em log o carimbo de data/hora para cada evento. Você pode especificar SystemTime ou QPC. O SystemTime fornece um carimbo de data/hora de baixa resolução (10 milissegundos), mas é comparativamente menos dispendioso para ser recuperado. O padrão é SystemTime. <br/> O contador de desempenho de consulta (QPC) fornece um carimbo de data/hora de alta resolução (100 nanossegundos), mas é comparativamente mais caro de recuperar. Você deve QPC se tiver taxas de eventos altas ou se o consumidor mesclar eventos de buffers diferentes.<br/>                                                                                                                                                                                                                                 |
| [**controlGuid**](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [**GUIDtype**](eventmanifestschema-guidtype-simpletype.md)       | Identifica o GUID de sessão para uma sessão de ETW que contém eventos de WPP. Essa configuração só é permitida para canais do tipo Debug. Esses canais não podem ser totalmente habilitados com palavras-chave definidas como zero (0x0000000000000000). Eles devem ser habilitados com palavras-chave definidas como 0xFFFFFFFFFFFFFFFF.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **fileMax**                                                                          | [**UInt32type**](eventmanifestschema-hexint32type-simpletype.md) | O número máximo de vezes que você deseja que o serviço crie um novo arquivo de log quando o canal está habilitado (inclui quando o computador é reiniciado). Se o valor for 0 ou 1, o serviço substituirá o arquivo de log cada vez que o canal for habilitado e os eventos anteriores serão perdidos. Se o valor for maior que 1, o serviço criará um novo arquivo de log cada vez que o canal estiver habilitado para preservar os eventos. O padrão é 1 e o máximo que você pode especificar é 16.<br/> O serviço acrescenta um número decimal de três dígitos entre 0 e fileMax 1 a cada nome de arquivo. Por exemplo, *filename*. etl.xxx, em que xxx é o número decimal de três dígitos. Os arquivos estão localizados em% windir% \\ System32 \\ winevt \\ logs.<br/> |
| [**palavras-chave**](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [**UInt64type**](eventmanifestschema-hexint64type-simpletype.md) | Um bitmask que determina a categoria de eventos que são gravados no canal. Se o valor do atributo **Keywords** for 0, todos os eventos que o provedor gravar serão gravados no canal; caso contrário, somente os eventos que definiram uma palavra-chave que está incluída no bitmask das **palavras-chave** serão gravados no canal. O padrão é 0.<br/> Os canais de depuração que têm o atributo controlGuid definido devem definir o atributo **Keywords** como 0xFFFFFFFFFFFFFFFF.<br/> A sessão passa o valor de palavras-chave para o provedor quando ele habilita o provedor.<br/>                                                                                                                                                                            |
| [**MOLAP**](eventmanifestschema-latency-channelpublishingtype-element.md)         | [**UInt32type**](eventmanifestschema-hexint32type-simpletype.md) | O tempo de espera antes de liberar os buffers, em milissegundos. Se zero, o ETW libera os buffers assim que eles ficam cheios. Se for diferente de zero, o ETW liberará todos os buffers que contêm eventos com base no valor, mesmo se o buffer não estiver cheio. Normalmente, você deseja liberar buffers somente quando eles se tornam cheios. Forçar os buffers a serem liberados pode aumentar o tamanho do arquivo de log com espaço de buffer não preenchido. O valor padrão é 1 segundo para logs de administração e operacionais e 5 segundos para logs analíticos e de depuração.<br/>                                                                                                                                                                                                                               |
| [**nível**](eventmanifestschema-level-channelpublishingtype-element.md)             | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | O nível de severidade dos eventos a serem gravados no canal. O serviço grava eventos no canal que têm um valor de nível menor ou igual ao valor especificado. O padrão é 0, o que significa registrar eventos com qualquer valor de nível.<br/> A sessão passa o valor de nível para o provedor quando ele habilita o provedor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**maxBuffers**](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [**UInt32type**](eventmanifestschema-hexint32type-simpletype.md) | O número máximo de buffers a serem alocados para a sessão. Normalmente, esse valor é o número mínimo de buffers, mais vinte. Esse valor deve ser maior ou igual ao valor especificado para minBuffers.<br/> O número máximo padrão de buffers para canais analíticos e de depuração é 10 KB e para administração e operacional ele é de 64 KB.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**minBuffers**](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [**UInt32type**](eventmanifestschema-hexint32type-simpletype.md) | O número mínimo de buffers a serem alocados para a sessão. O padrão é zero.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**sidType**](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | Determina se um SID (identificador de segurança) do principal deve ser incluído em cada evento gravado no canal. Para incluir o SID com o evento, defina esse atributo como "Publishing". O SID é definido com base na identidade do thread no momento em que o evento é gravado. Se você não quiser incluir o SID com o evento, defina esse atributo como "nenhum". O padrão é "publicação".<br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Comentários

Você pode especificar essas informações de publicação para tipos de canal analíticos e de depuração ou para qualquer canal que especifica o isolamento personalizado.

Embora você possa especificar o nível e as palavras-chave, considere que esses serão os únicos eventos que você receberá do provedor para esse canal.

Quando um buffer está cheio, o ETW libera o buffer para o arquivo de log. Se os buffers forem preenchidos mais rapidamente do que podem ser liberados, novos buffers serão alocados e adicionados ao pool de buffers da sessão, até o número máximo especificado. Além desse limite, a sessão descarta eventos de entrada até que um buffer fique disponível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





