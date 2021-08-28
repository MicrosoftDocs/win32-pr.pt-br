---
description: Define um contador.
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: tipo complexo de contador
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1a2af7ec5f9945257a94d1c65823ecad3c9a05f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481522"
---
# <a name="counter-complex-type"></a>tipo complexo de contador

Define um contador.

``` syntax
<xs:complexType name="counter">
    <xs:choice
        minOccurs="0"
        maxOccurs="1"
    >
        <xs:element name="counterAttributes"
            type="man:counterAttributes"
        >
            <xs:key name="uniqueCounterAttributeName">
                <xs:selector
                    xpath="./man:counterAttribute"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="id"
        type="man:UInt32Type"
        use="required"
     />
    <xs:attribute name="uri"
        type="xs:anyURI"
        use="required"
     />
    <xs:attribute name="name"
        use="optional"
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
        use="optional"
     />
    <xs:attribute name="type"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="perf_counter_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer"
                 />
                <xs:enumeration
                    value="perf_counter_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_large_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_100ns_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_obj_time_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_bulk_count"
                 />
                <xs:enumeration
                    value="perf_counter_text"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_sample_fraction"
                 />
                <xs:enumeration
                    value="perf_sample_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer_inv"
                 />
                <xs:enumeration
                    value="perf_sample_base"
                 />
                <xs:enumeration
                    value="perf_average_timer"
                 />
                <xs:enumeration
                    value="perf_average_base"
                 />
                <xs:enumeration
                    value="perf_average_bulk"
                 />
                <xs:enumeration
                    value="perf_obj_time_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_base"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_large_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_raw_base"
                 />
                <xs:enumeration
                    value="perf_large_raw_base"
                 />
                <xs:enumeration
                    value="perf_elapsed_time"
                 />
                <xs:enumeration
                    value="perf_counter_delta"
                 />
                <xs:enumeration
                    value="perf_counter_large_delta"
                 />
                <xs:enumeration
                    value="perf_precision_system_timer"
                 />
                <xs:enumeration
                    value="perf_precision_100ns_timer"
                 />
                <xs:enumeration
                    value="perf_precision_object_timer"
                 />
                <xs:enumeration
                    value="perf_counter_composite"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="baseID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="detailLevel"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="standard"
                 />
                <xs:enumeration
                    value="advanced"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="defaultScale"
        use="optional"
        default="0"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:integer"
            >
                <xs:minInclusive
                    value="-10"
                 />
                <xs:maxInclusive
                    value="10"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="aggregate"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="sum"
                 />
                <xs:enumeration
                    value="avg"
                 />
                <xs:enumeration
                    value="max"
                 />
                <xs:enumeration
                    value="min"
                 />
                <xs:enumeration
                    value="undefined"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="perfTimeID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="perfFreqID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="multiCounterID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="struct"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="field"
        type="man:CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento               | Type                                                                                 | Descrição                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| **counterAttributes** | [**man:counterAttributes**](performance-counters-counterattributes-complex-type.md) | Lista os atributos exclusivos que especificam como os dados do contador são exibidos em um aplicativo de consumidor.<br/> |



## <a name="attributes"></a>Atributos




| Nome | Type | Descrição | 
|------|------|-------------|
| aggregate | A função de agregação a ser aplicada se o atributo <strong>de instâncias</strong> de <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> for globalAggregate, multipleAggregate ou globalAggregateHistory. A seguir estão as possíveis funções de agregação que você pode aplicar:<br /><dl><dt><span id="max"></span><span id="MAX"></span>Max</dt><dd> O valor máximo do contador é retornado.<br /></dd><dt><span id="min"></span><span id="MIN"></span>min</dt><dd> O valor mínimo do contador é retornado.<br /></dd><dt><span id="avg"></span><span id="AVG"></span>Avg</dt><dd> O valor médio do contador é retornado.<br /></dd><dt><span id="sum"></span><span id="SUM"></span>Soma</dt><dd> A soma dos valores do contador é retornada.<br /></dd><dt><span id="undefined"></span><span id="UNDEFINED"></span>Indefinido</dt><dd> Não agregregre esse contador.<br /></dd></dl> | 
| baseID | <a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a> | O identificador de outro contador dentro do mesmo conjunto de contadores, cujo valor é usado para calcular o valor desse contador. Os seguintes tipos de contador exigem um contador base:<br /><dl><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt><dd> Requer o contador PERF_AVERAGE_BASE base.<br /></dd><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt><dd> Requer o contador PERF_AVERAGE_BASE base.<br /></dd><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt><dd> Requer o contador PERF_COUNTER_MULTI_BASE base.<br /></dd><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt><dd> Requer o contador PERF_LARGE_RAW_BASE base.<br /></dd><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt><dd> Requer o contador PERF_LARGE_RAW_BASE base.<br /></dd><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt><dd> Requer o contador PERF_RAW_BASE base.<br /></dd><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt><dd> Requer o contador PERF_SAMPLE_BASE base.<br /></dd></dl> | 
| defaultScale | O fator de escala a ser aplicado ao valor do contador (fator * valor do contador). O padrão será zero se nenhuma escala for aplicada. Os valores válidos variam de 10 a 10 (0,00000000001 a 100000000). Se esse valor for zero, o valor de escala será 1; se esse valor for 1, o valor de escala será 10; se esse valor for 1, o valor de escala será .10; e assim por diante.<br /> | 
| descrição | <strong>xs:string</strong> | Uma breve descrição do contador. Você não precisa especificar esse atributo se o contador incluir o <a href="performance-counters-counterattribute-complex-type.md"><strong>atributo noDisplay.</strong></a><br /> | 
| detailLevel | Especifica o público-alvo para os detalhes do contador. O valores possíveis são os seguintes:<br /><dl><dt><span id="standard"></span><span id="STANDARD"></span>Padrão</dt><dd> Exibir detalhes sobre o contador que um usuário típico compreenderia.<br /></dd><dt><span id="advanced"></span><span id="ADVANCED"></span>Avançado</dt><dd> Exibir detalhes sobre o contador que apenas um usuário avançado compreenderia.<br /></dd></dl> | 
| field | <a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a> | O nome de um campo dentro do struct que contém o valor do contador. Esse atributo não é permitido para provedores de modo de usuário.<br /> | 
| id | <a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a> | Um número exclusivo que identifica o contador dentro do conjunto de contadores.<br /> | 
| multiCounterID | <a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a> | O identificador de outro contador dentro do mesmo conjunto de contadores, cujo valor multiplicador é usado para calcular o valor desse contador. Os tipos de contador a seguir exigem um valor multiplicador. O contador referenciado deve ser do tipo PERF_COUNTER_RAWCOUNT.<br /><ul><li>PERF_COUNTER_MULTI_TIMER</li><li>PERF_COUNTER_MULTI_TIMER_INV</li><li>PERF_100NSEC_MULTI_TIMER</li><li>PERF_100NSEC_MULTI_TIMER_INV</li></ul> | 
| name | O nome do contador. O nome deve ser exclusivo e menor que 1.024 caracteres. O nome diferencia maiúsculas de minúsculas. Você não precisa especificar esse atributo se o contador incluir o <a href="performance-counters-counterattribute-complex-type.md"><strong>atributo noDisplay.</strong></a><br /> | 
| perfFreqID | <a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a> | O identificador de outro contador dentro do mesmo conjunto de contadores, cujo valor de frequência é usado para calcular o valor desse contador. Os tipos de contador a seguir exigem uma frequência. O PERF_COUNTER_LARGE_RAWCOUNT de contadores contém o valor do carimbo de data/hora.<br /><ul><li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li><li>PERF_ELAPSED_TIME</li><li>PERF_OBJ_TIME_TIMER</li><li>PERF_PRECISION_OBJECT_TIMER</li></ul> | 
| perfTimeID | <a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a> | O identificador de outro contador dentro do mesmo conjunto de contadores, cujo valor de carimbo de data/hora é usado para calcular o valor desse contador. Os seguintes tipos de contador exigem um carimbo de data/hora. O PERF_COUNTER_LARGE_RAWCOUNT de contadores contém o valor do carimbo de data/hora.<br /><ul><li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li><li>PERF_ELAPSED_TIME</li><li>PERF_OBJ_TIME_TIMER</li><li>PERF_PRECISION_OBJECT_TIMER</li></ul> | 
| struct | <a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a> | O nome de um elemento struct que contém esse valor de contador. Esse atributo não é permitido para provedores de modo de usuário.<br /> | 
| símbolo | <a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a> | Um nome simbólico que identifica o contador. A <a href="ctrpp.md">ferramenta CTRPP</a> cria uma constante que você pode usar ao chamar funções que exigem um identificador de contador (por exemplo, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>). O nome da constante é o nome simbólico.<br /> | 
| tipo | O nome do tipo de contador. Para valores possíveis, consulte o bloco de sintaxe acima. Para obter detalhes de cada tipo, consulte <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Tipos de contador</a> no Guia Windows implantação do 2003. O nome faz uso em minúsculas que faz uso de maiúsculas e minúsculas. <br /> | 
| uri | <strong>xs:anyURI</strong> | Um identificador de recurso uniforme exclusivo que permite que os usuários recuperem valores de contador de qualquer local.<br /> | 




## <a name="remarks"></a>Comentários

Para fornecer compatibilidade com compatibilidade com vertida, cada contador no conjunto de contadores deve especificar os mesmos **valores perfFreqID** e **perfTimeID.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

