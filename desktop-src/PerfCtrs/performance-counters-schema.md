---
description: Use um manifesto XML para definir os contadores de desempenho que seu provedor fornece.
ms.assetid: fa13d13a-f2e2-4732-8bf7-cb0a0f1d4ed7
title: Esquema de contadores de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 5c41e9d54e259d6e53453a55cc97f7734ce793fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662183"
---
# <a name="performance-counters-schema"></a>Esquema de contadores de desempenho

Os provedores de dados de desempenho v2 têm suporte no Windows Vista ou posterior. Eles usam um. Arquivo de MAN (manifesto de instrumentação XML) para definir o provedor, os conjuntos de linhas e os contadores.

> [!NOTE]
> Os manifestos de instrumentação podem conter informações sobre provedores do ETW (rastreamento de eventos para Windows) e provedores de contador de desempenho. Para obter detalhes sobre os manifestos de instrumentação, consulte [esquema EventManifest](/windows/desktop/WES/eventmanifestschema-schema) e [gravando um manifesto de instrumentação](/windows/desktop/WES/writing-an-instrumentation-manifest)).

Esta seção descreve os seguintes elementos e tipos que você usa na `counters` seção de um manifesto de instrumentação:

- [Elementos de contadores de desempenho](performance-counters-elements.md)
- [Tipos simples de contadores de desempenho](performance-counters-simple-types.md)
- [Tipos complexos de contadores de desempenho](performance-counters-complex-types.md)

Não use as `localization` seções ou `stringTable` do manifesto de instrumentação para cadeias de caracteres de dados de desempenho. Em vez disso, especifique as cadeias de caracteres como valores do atributo que você está definindo.

Depois de criar o manifesto, use a ferramenta [ctrpp](ctrpp.md) para validar o manifesto e gerar o código ( `.h` ) e `.rc` os arquivos de recurso () a serem usados na criação do provedor.

Ao instalar seu aplicativo, execute a [ ferramenta deLodCtr.exe](/windows-server/administration/windows-commands/lodctr) com o `/M:` parâmetro para instalar seus contadores de desempenho. A ferramenta de LodCtr.exe registrará as informações necessárias no registro em `HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{ProviderGuid}` , incluindo o caminho completo para o binário que contém os recursos de cadeia de caracteres para seu provedor (conforme especificado no `applicationIdentity` atributo do manifesto). Você deve ter privilégios de administrador para executar LodCtr.exe. Exemplo de comando de instalação:

**LodCtr.exe** /m: "*manifest*" \[ "*ApplicationIdentityDirectory*"\]

Se você precisar atualizar um CounterSet, não se esqueça de desinstalar o CounterSet antigo usando a [ ferramenta deUnlodCtr.exe](/windows-server/administration/windows-commands/unlodctr_1) com `/G:` os `/P:` parâmetros ou. Depois que o CounterSet antigo for desinstalado, você poderá instalar o CounterSet atualizado.

## <a name="schema"></a>Esquema

Este é o esquema de contadores de desempenho que você pode usar para validar a `counters` seção do seu manifesto. Esse esquema é encontrado na SDK do Windows como `counterman.xsd` . Para obter detalhes sobre o esquema que você usa para validar a seção instrumentação do manifesto, consulte [EventManifest Schema](/windows/desktop/WES/eventmanifestschema-schema).

``` syntax
<xs:schema
  targetNamespace="http://schemas.microsoft.com/win/2005/12/counters"
  elementFormDefault="qualified"
  xmlns:man="http://schemas.microsoft.com/win/2005/12/counters"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="GUIDType">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="HexInt32Type">
    <xs:annotation>
      <xs:documentation>Hex 1-8 digits in size</xs:documentation>
    </xs:annotation>
    <xs:restriction base="xs:string">
      <xs:pattern value="0[xX][0-9A-Fa-f]{1,8}"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="UInt32Type">
    <xs:annotation>
      <xs:documentation>Hex 1-8 digits in size or unsignedInt</xs:documentation>
    </xs:annotation>
    <xs:union memberTypes="xs:unsignedInt man:HexInt32Type"/>
  </xs:simpleType>

  <xs:simpleType name="CSymbolType">
    <xs:annotation>
      <xs:documentation>A Valid C Symbol or an empty string</xs:documentation>
    </xs:annotation>
    <xs:restriction base="xs:string">
      <xs:pattern value="()|([_a-zA-Z][_0-9a-zA-Z]*)"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="struct">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="name" type="man:CSymbolType" use="required"/>
        <xs:attribute name="type" type="man:CSymbolType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="structs">
    <xs:choice minOccurs="1" maxOccurs="unbounded">
      <xs:element name="struct" type="man:struct"/>
    </xs:choice>
  </xs:complexType>
  
  <xs:complexType name="counterAttribute">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="name" use="required">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="reference"/>
              <xs:enumeration value="noDisplay"/>
              <xs:enumeration value="noDigitGrouping"/>
              <xs:enumeration value="displayAsHex"/>
              <xs:enumeration value="displayAsReal"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:attribute>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  
  <xs:complexType name="counterAttributes">
    <xs:choice minOccurs="1" maxOccurs="5">
      <xs:element name="counterAttribute" type="man:counterAttribute"/>
    </xs:choice>
  </xs:complexType>
  
  <xs:complexType name="counter">
    <xs:choice minOccurs="0" maxOccurs="1">
      <xs:element name="counterAttributes" type="man:counterAttributes">
        <xs:key name="uniqueCounterAttributeName">
          <xs:annotation>
            <xs:documentation>
              Only five counterAttribute elements allowed, they should all be unique.
            </xs:documentation>
          </xs:annotation>
          <xs:selector xpath="./man:counterAttribute"/>
          <xs:field xpath="@name"/>
        </xs:key>
      </xs:element>
    </xs:choice>
    <xs:attribute name="symbol" type="man:CSymbolType" use="optional"/>
    <xs:attribute name="id" type="man:UInt32Type" use="required"/>
    <xs:attribute name="uri" type="xs:anyURI" use="required"/>
    <xs:attribute name="name" use="optional">
      <xs:annotation>
        <xs:documentation>
            This attribute is required for schemaVersion >= 2.0.
        </xs:documentation>
      </xs:annotation>
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:maxLength value="1023"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="nameID" type="man:UInt32Type" use="optional">
      <xs:annotation>
        <xs:documentation>
            Resource ID of the name string. This attribute is required
            for schemaVersion >= 2.0. It is not allowed for older versions.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="description" type="xs:string" use="optional">
      <xs:annotation>
        <xs:documentation>
            This attribute is required for schemaVersion >= 2.0.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="descriptionID" type="man:UInt32Type" use="optional">
      <xs:annotation>
        <xs:documentation>
            Resource ID of the description string. This attribute is required
            for schemaVersion >= 2.0. It is not allowed for older versions.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="type" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="perf_counter_counter"/>
          <xs:enumeration value="perf_counter_timer"/>
          <xs:enumeration value="perf_counter_queuelen_type"/>
          <xs:enumeration value="perf_counter_large_queuelen_type"/>
          <xs:enumeration value="perf_counter_100ns_queuelen_type"/>
          <xs:enumeration value="perf_counter_obj_time_queuelen_type"/>
          <xs:enumeration value="perf_counter_bulk_count"/>
          <xs:enumeration value="perf_counter_text"/>
          <xs:enumeration value="perf_counter_rawcount"/>
          <xs:enumeration value="perf_counter_large_rawcount"/>
          <xs:enumeration value="perf_counter_rawcount_hex"/>
          <xs:enumeration value="perf_counter_large_rawcount_hex"/>
          <xs:enumeration value="perf_sample_fraction"/>
          <xs:enumeration value="perf_sample_counter"/>
          <xs:enumeration value="perf_counter_timer_inv"/>
          <xs:enumeration value="perf_sample_base"/>
          <xs:enumeration value="perf_average_timer"/>
          <xs:enumeration value="perf_average_base"/>
          <xs:enumeration value="perf_average_bulk"/>
          <xs:enumeration value="perf_obj_time_timer"/>
          <xs:enumeration value="perf_100nsec_timer"/>
          <xs:enumeration value="perf_100nsec_timer_inv"/>
          <xs:enumeration value="perf_counter_multi_timer"/>
          <xs:enumeration value="perf_counter_multi_timer_inv"/>
          <xs:enumeration value="perf_counter_multi_base"/>
          <xs:enumeration value="perf_100nsec_multi_timer"/>
          <xs:enumeration value="perf_100nsec_multi_timer_inv"/>
          <xs:enumeration value="perf_raw_fraction"/>
          <xs:enumeration value="perf_large_raw_fraction"/>
          <xs:enumeration value="perf_raw_base"/>
          <xs:enumeration value="perf_large_raw_base"/>
          <xs:enumeration value="perf_elapsed_time"/>
          <xs:enumeration value="perf_counter_delta"/>
          <xs:enumeration value="perf_counter_large_delta"/>
          <xs:enumeration value="perf_precision_system_timer"/>
          <xs:enumeration value="perf_precision_100ns_timer"/>
          <xs:enumeration value="perf_precision_object_timer"/>
          <xs:enumeration value="perf_counter_composite"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="baseID" type="man:UInt32Type" use="optional"/>
    <xs:attribute name="detailLevel" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="standard"/>
          <xs:enumeration value="advanced"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="defaultScale" use="optional" default="0">
      <xs:simpleType>
        <xs:restriction base="xs:integer">
          <xs:minInclusive value="-10"/>
          <xs:maxInclusive value="10"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="aggregate" use="optional">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="sum"/>
          <xs:enumeration value="avg"/>
          <xs:enumeration value="max"/>
          <xs:enumeration value="min"/>
          <xs:enumeration value="undefined"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="perfTimeID" type="man:UInt32Type" use="optional"/>
    <xs:attribute name="perfFreqID" type="man:UInt32Type" use="optional"/>
    <xs:attribute name="multiCounterID" type="man:UInt32Type" use="optional"/>
    <xs:attribute name="struct" type="man:CSymbolType" use="optional">
      <xs:annotation>
        <xs:documentation>
          If providerType=userMode, required.
          If providerType=kernelMode, not allowed.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="field" type="man:CSymbolType" use="optional">
      <xs:annotation>
        <xs:documentation>
          If providerType=userMode, required.
          If providerType=kernelMode, not allowed.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
  </xs:complexType>

  <xs:complexType name="counterSet">
    <xs:sequence>
      <xs:element name="structs" type="man:structs" minOccurs="0" maxOccurs="1">
        <xs:annotation>
          <xs:documentation>
            If providerType=userMode, required.
            If providerType=kernelMode, not allowed.
          </xs:documentation>
        </xs:annotation>
      </xs:element>
      <xs:element name="counter" type="man:counter" minOccurs="1" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="symbol" type="man:CSymbolType" use="required"/>
    <xs:attribute name="guid" type="man:GUIDType" use="required"/>
    <xs:attribute name="uri" type="xs:anyURI" use="required"/>
    <xs:attribute name="name" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:maxLength value="1023"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="nameID" type="man:UInt32Type" use="optional">
      <xs:annotation>
        <xs:documentation>
            Resource ID of the name string. This attribute is required
            for schemaVersion >= 2.0, and not allowed for older versions.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="description" use="required"/>
    <xs:attribute name="descriptionID" type="man:UInt32Type" use="optional">
      <xs:annotation>
        <xs:documentation>
            Resource ID of the description string. This attribute is required
            for schemaVersion >= 2.0, and not allowed for older versions.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="instances" use="optional" default="single">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="single"/>
          <xs:enumeration value="multiple"/>
          <xs:enumeration value="globalAggregate"/>
          <xs:enumeration value="multipleAggregate"/>
          <xs:enumeration value="globalAggregateHistory"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="provider">
    <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="counterSet" type="man:counterSet"/>
    </xs:choice>
    <xs:attribute name="symbol" type="man:CSymbolType" use="optional">
      <xs:annotation>
        <xs:documentation>
          Provider Symbol is required for User Mode providers.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
    <xs:attribute name="callback" use="optional" default="default">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="custom"/>
          <xs:enumeration value="default"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid" type="man:GUIDType" use="required"/>
    <xs:attribute name="applicationIdentity" type="xs:string" use="required"/>
    <xs:attribute name="providerType" use="optional" default="userMode">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value="userMode"/>
          <xs:enumeration value="kernelMode"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName" type="xs:string" use="optional" default="Counters"/>
    <xs:attribute name="resourceBase" type="man:UInt32Type" use="optional">
      <xs:annotation>
        <xs:documentation>
            This attribute is not allowed for schemaVersion >= 2.0.
        </xs:documentation>
      </xs:annotation>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="counters">
    <xs:choice minOccurs="1" maxOccurs="1">
      <xs:element name="provider" type="man:provider"/>
    </xs:choice>
    <xs:attribute name="schemaVersion" type="xs:string" use="required"/>
  </xs:complexType>
  
  <xs:element name="counters" type="man:counters">
    <xs:key name="uniqueCounterSetGUID">
      <xs:annotation>
        <xs:documentation>
          Counter Set GUID should be unique across the entire document. The
          counter set registration fails if the GUID is already registered.
          To update a counter set that is registered, you must first
          uninstall the counter set and register it again.
        </xs:documentation>
      </xs:annotation>
      <xs:selector xpath="./man:provider/man:counterSet"/>
      <xs:field xpath="@guid"/>
    </xs:key>
  </xs:element>
  
</xs:schema>
```

## <a name="example-user-mode-manifest"></a>Exemplo de manifesto User-Mode

A seguir é mostrado um exemplo de manifesto que define contadores de desempenho para um provedor de modo de usuário.

```XML
<?xml version="1.0"?>
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events"
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"
    >

  <instrumentation>

    <counters
      xmlns="http://schemas.microsoft.com/win/2005/12/counters"
      schemaVersion="2.0">

      <provider
        callback="custom"
        applicationIdentity="myprovider.exe"
        symbol="MY_PROVIDER"
        providerType="userMode"
        providerGuid="{ab8e1320-965a-4cf9-9c07-fe25378c2a23}">

        <counterSet
          guid="{dd36a036-c923-4794-b696-70577630b5cf}"
          uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1"
          symbol="MY_LOGICALDISK"
          name="My LogicalDisk"
          nameID="100"
          description="This is a sample counter set with multiple instances."
          descriptionID="102"
          instances="multiple">

          <counter
            id="1"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter1"
            symbol="MY_LOGICALDISK_FREE_MB"
            name="My Free Megabytes"
            nameID="104"
            description="First sample counter."
            descriptionID="106"
            type="perf_counter_rawcount"
            detailLevel="standard"
            defaultScale="1"
            />

          <counter
            id="2"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter2"
            symbol="MY_LOGICALDISK_SEC_PER_TRANSFER"
            name="My Avg. Disk sec/Transfer"
            nameID="108"
            description="Second sample counter."
            descriptionID="110"
            type="perf_average_timer"
            baseID="3"
            detailLevel="advanced"
            defaultScale="1">
            <counterAttributes>
              <counterAttribute name="reference" />
              <counterAttribute name="displayAsReal" />
            </counterAttributes>
          </counter>

          <counter
            id="3"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter3"
            symbol="MY_LOGICALDISK_TRANSFER_COUNT"
            type="perf_average_base"
            detailLevel="advanced">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

        </counterSet>

        <counterSet
          guid="{f72fdf55-eaa6-45ba-bf6d-4c7cb0d6ef73}"
          uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2"
          symbol="MY_SYSTEMOBJECTS"
          name="My System Objects"
          nameID="120"
          description="My System Objects Help."
          descriptionID="122"
          instances="single">

          <counter
            id="1"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter1"
            symbol="MY_SYSTEMOBJECTS_PROCESS_COUNT"
            name="Process Count"
            nameID="124"
            description="Process Count Help."
            descriptionID="126"
            type="perf_counter_rawcount"
            detailLevel="standard"
            defaultScale="1">
            <counterAttributes>
              <counterAttribute name="noDigitGrouping" />
              <counterAttribute name="displayAsHex" />
            </counterAttributes>
          </counter>

          <counter
            id="2"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter2"
            symbol="MY_SYSTEMOBJECTS_THREAD_COUNT"
            name="Thread Count"
            nameID="128"
            description="Thread Count Help."
            descriptionID="130"
            type="perf_counter_rawcount"
            detailLevel="standard"
            />

          <counter
            id="3"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter3"
            symbol="MY_SYSTEMOBJECTS_ELAPSED_TIME"
            name="System Elapsed Time"
            nameID="132"
            description="System Elapsed Time Help."
            descriptionID="134"
            type="perf_elapsed_time"
            detailLevel="advanced"
            perfTimeID="4"
            perfFreqID="5"
            defaultScale="1"
            />

          <counter
            id="4"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter4"
            symbol="MY_SYSTEMOBJECTS_PERFTIME"
            type="perf_counter_large_rawcount"
            detailLevel="standard">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

          <counter
            id="5"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter5"
            symbol="MY_SYSTEMOBJECTS_PERFFREQ"
            type="perf_counter_large_rawcount"
            detailLevel="standard">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

        </counterSet>
      </provider>
    </counters>
  </instrumentation>
</instrumentationManifest>
```

## <a name="example-kernel-mode-manifest"></a>Exemplo de manifesto Kernel-Mode

Veja a seguir um exemplo de manifesto que define contadores de desempenho para um provedor de modo kernel.

```XML
<?xml version="1.0"?>
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events"
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"
    >

  <instrumentation>

    <counters
      xmlns="http://schemas.microsoft.com/win/2005/12/counters"
      schemaVersion="2.0">

      <provider
        applicationIdentity="myprovider.exe"
        providerType="kernelMode"
        providerGuid="{ab8e1320-965a-4cf9-9c07-fe25378c2a23}">

        <counterSet
          guid="{dd36a036-c923-4794-b696-70577630b5cf}"
          uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1"
          symbol="MY_LOGICALDISK"
          name="My LogicalDisk"
          nameID="100"
          description="This is a sample counter set with multiple instances."
          descriptionID="102"
          instances="multiple">

          <structs>
            <struct name="LogicalDiskData" type="MY_LOGICALDISK_DATA" />
          </structs>

          <counter
            id="1"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter1"
            field="FreeMegabytes"
            name="My Free Megabytes"
            nameID="104"
            description="First sample counter."
            descriptionID="106"
            type="perf_counter_rawcount"
            detailLevel="standard"
            defaultScale="1"
            />

          <counter
            id="2"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter2"
            field="TransferTime"
            name="My Avg. Disk sec/Transfer"
            nameID="108"
            description="Second sample counter."
            descriptionID="110"
            type="perf_average_timer"
            baseID="3"
            detailLevel="advanced"
            defaultScale="1">
            <counterAttributes>
              <counterAttribute name="reference" />
              <counterAttribute name="displayAsReal" />
            </counterAttributes>
          </counter>

          <counter
            id="3"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet1.MyCounter3"
            field="TransferCount"
            type="perf_average_base"
            detailLevel="advanced">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

        </counterSet>

        <counterSet
          guid="{f72fdf55-eaa6-45ba-bf6d-4c7cb0d6ef73}"
          uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2"
          symbol="MY_SYSTEMOBJECTS"
          name="My System Objects"
          nameID="120"
          description="My System Objects Help."
          descriptionID="122"
          instances="single">

          <structs>
            <struct name="SystemObjectsData" type="MY_SYSTEMOBJECTS_DATA" />
          </structs>

          <counter
            id="1"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter1"
            field="ProcessCount"
            name="Process Count"
            nameID="124"
            description="Process Count Help."
            descriptionID="126"
            type="perf_counter_rawcount"
            detailLevel="standard"
            defaultScale="1">
            <counterAttributes>
              <counterAttribute name="noDigitGrouping" />
              <counterAttribute name="displayAsHex" />
            </counterAttributes>
          </counter>

          <counter
            id="2"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter2"
            field="ThreadCount"
            name="Thread Count"
            nameID="128"
            description="Thread Count Help."
            descriptionID="130"
            type="perf_counter_rawcount"
            detailLevel="standard"
            />

          <counter
            id="3"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter3"
            field="SystemElapsedTime"
            name="System Elapsed Time"
            nameID="132"
            description="System Elapsed Time Help."
            descriptionID="134"
            type="perf_elapsed_time"
            detailLevel="advanced"
            perfTimeID="4"
            perfFreqID="5"
            defaultScale="1"
            />

          <counter
            id="4"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter4"
            field="PerfTime"
            type="perf_counter_large_rawcount"
            detailLevel="standard">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

          <counter
            id="5"
            uri="Microsoft.Windows.System.PerfCounters.MyCounterSet2.MyCounter5"
            field="PerfFreq"
            type="perf_counter_large_rawcount"
            detailLevel="standard">
            <counterAttributes>
              <counterAttribute name="noDisplay" />
            </counterAttributes>
          </counter>

        </counterSet>
      </provider>
    </counters>
  </instrumentation>
</instrumentationManifest>
```
