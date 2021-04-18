---
description: Define uma lista de contadores que estão logicamente relacionados.
ms.assetid: d094146a-389e-4053-8ee5-acd29254e817
title: Tipo complexo do CounterSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e753fab4308f1e981ab06e9470742ace46840a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758931"
---
# <a name="counterset-complex-type"></a>Tipo complexo do CounterSet

Define uma lista de contadores que estão logicamente relacionados.

``` syntax
<xs:complexType name="counterSet">
    <xs:sequence>
        <xs:element name="structs"
            type="man:structs"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="counter"
            type="man:counter"
            minOccurs="1"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="required"
     />
    <xs:attribute name="guid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="uri"
        type="xs:anyURI"
        use="required"
     />
    <xs:attribute name="name"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:maxLength
                    value="1023"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="description"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="instances"
        use="optional"
        default="single"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="single"
                 />
                <xs:enumeration
                    value="multiple"
                 />
                <xs:enumeration
                    value="globalAggregate"
                 />
                <xs:enumeration
                    value="multipleAggregate"
                 />
                <xs:enumeration
                    value="globalAggregateHistory"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento     | Type                                                             | Descrição                                                                                            |
|-------------|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| **neutraliza** | [**homem: contador**](performance-counters-counter-complex-type.md) | Define um contador que o provedor fornece.<br/>                                               |
| **structs** | [**homem: structs**](performance-counters-structs-complex-type.md) | Uma lista de elementos de struct que contêm valores para os contadores definidos neste conjunto de contadores.<br/> |



## <a name="attributes"></a>Atributos



| Nome        | Tipo                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| descrição | **xs:string**                                                           | Uma breve descrição do conjunto de contadores. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| guid        | [**Man: GUIDtype**](performance-counters-guidtype-simple-type.md)       | Um GUID que identifica exclusivamente o conjunto de contadores. O registro do conjunto de contadores falhará se o GUID já estiver registrado. Para atualizar um conjunto de contadores registrado, você deve primeiro desinstalar o conjunto de contadores e registrá-lo novamente. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| instances   |                                                                         | Determina se o conjunto de contadores pode conter várias instâncias. O seguinte lista os valores possíveis:<br/> <dl> <dt><span id="single"></span><span id="SINGLE"></span>exclusivo</dt> <dd> Define um conjunto de contadores em que apenas uma instância dos contadores no conjunto de contadores pode existir. Especifique esse valor se os contadores fornecerem medidas em todo o sistema, como memória física. Esse é o padrão.<br/> </dd> <dt><span id="multiple"></span><span id="MULTIPLE"></span>vários</dt> <dd> Define um conjunto de contadores em que podem existir várias instâncias dos contadores no conjunto de contadores. Especifique esse valor se os contadores fornecerem medidas por instância, como tempo de processador por processo.<br/> </dd> <dt><span id="globalAggregate"></span><span id="globalaggregate"></span><span id="GLOBALAGGREGATE"></span>globalAggregate</dt> <dd> Define um conjunto de contadores de instância única em que os contadores no conjunto de contadores devem ser agregados de várias fontes ativas. Por exemplo, você pode criar um conjunto de contadores que contém um contador que conta o número de leituras de disco de um disco rígido. Se o computador tiver três discos rígidos e um consumidor consultar o número de leituras de disco, o PERFLIB obterá o número de leituras de cada disco e somará seus valores individuais. <br/> </dd> <dt><span id="multipleAggregate"></span><span id="multipleaggregate"></span><span id="MULTIPLEAGGREGATE"></span>multipleAggregate</dt> <dd> Define um conjunto de contadores de várias instâncias em que os contadores no conjunto de contadores devem ser agregados em todas as instâncias desse contador. Por exemplo, você pode criar um conjunto de contadores para um aplicativo multi-threaded que contenha um contador que mede o desempenho do thread (cada thread se referiria a uma instância do conjunto de contadores). Quando um consumidor consulta o contador de tempo de execução de thread total, o PERFLIB somará o tempo total de execução do thread de cada instância.<br/> </dd> <dt><span id="globalAggregateHistory"></span><span id="globalaggregatehistory"></span><span id="GLOBALAGGREGATEHISTORY"></span>globalAggregateHistory</dt> <dd> Define um conjunto de contadores de instância única cujos valores de contador são armazenados em cache durante o tempo de vida do consumidor. Observe que todos os contadores no conjunto de contadores são armazenados em cache. Para armazenar em cache apenas contadores específicos, decorar esses contadores com o atributo de histórico.<br/> Usando o exemplo de leitura de disco de globalAggregate, todos os valores de contador no conjunto de contadores seriam armazenados em cache. Se um disco ficou indisponível, o último valor armazenado em cache para o total de bytes lidos por esse disco ainda estaria disponível para o aplicativo consumidor.<br/> </dd> </dl> |
| name        |                                                                         | O nome de exibição do conjunto de contadores. Deve ter menos de 1.024 caracteres. O nome diferencia maiúsculas de minúsculas. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| símbolo      | [**homem: CSymbolType**](performance-counters-csymboltype-simple-type.md) | Um nome simbólico que identifica o conjunto de contadores. A ferramenta [ctrpp](ctrpp.md) cria uma variável GUID que você pode usar ao chamar funções que exigem o GUID do conjunto de contadores (por exemplo, [**PerfCreateInstance**](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)). O nome da variável é do formato *simbóliconame* GUID. <br/> Se você incluir o argumento **-prefix** ao chamar [ctrpp](ctrpp.md), a cadeia de caracteres de prefixo será adicionada ao início do nome simbólico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| uri         | **xs: anyURI**                                                           | Um identificador de recurso uniforme exclusivo que permite aos usuários acessar os contadores no conjunto de contadores de qualquer local.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




