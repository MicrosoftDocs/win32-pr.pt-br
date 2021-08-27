---
description: Define um provedor e os contadores que ele fornece.
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: tipo complexo do provedor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94654c538cc0637e6c90e0b14d3433b979762b00
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622712"
---
# <a name="provider-complex-type"></a>tipo complexo do provedor

Define um provedor e os contadores que ele fornece.

``` syntax
<xs:complexType name="provider">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="counterSet"
            type="man:counterSet"
        >
            <xs:key name="uniqueCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@id"
                 />
            </xs:key>
            <xs:unique name="uniqueCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:unique>
            <xs:keyref name="existBaseID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@baseID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfTimeID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfTimeID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfFreqID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfFreqID"
                 />
            </xs:keyref>
            <xs:keyref name="existMultiCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@multiCounterID"
                 />
            </xs:keyref>
            <xs:key name="uniqueStructNames">
                <xs:selector
                    xpath="./man:structs/man:struct"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
            <xs:keyref name="existCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@struct"
                 />
            </xs:keyref>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="callback"
        use="optional"
        default="default"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="custom"
                 />
                <xs:enumeration
                    value="default"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="applicationIdentity"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="providerType"
        use="optional"
        default="userMode"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="userMode"
                 />
                <xs:enumeration
                    value="kernelMode"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName"
        type="xs:string"
        use="optional"
        default="Counters"
     />
    <xs:attribute name="resourceBase"
        type="man:UInt32Type"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento        | Type                                                                   | Descrição                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **Counterset** | [**man:counterSet**](performance-counters-counterset-complex-type.md) | Identifica o conjunto de contadores que contém um ou mais contadores relacionados logicamente.<br/> |



## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Type</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Applicationidentity</td>
<td><strong>xs:string</strong></td>
<td>O nome do arquivo binário que contém as cadeias de caracteres de recurso localizadas, um arquivo .exe ou .dll (não inclua o caminho para o binário).<br/> O Lodctr.exe utilitário usa o caminho do parâmetro opcional [<em>path</em>] para pesquisar o arquivo binário. Por exemplo, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>path</em>]]. Se você não incluir o parâmetro [<em>path</em>] , Lodctr.exe pesquisa a pasta que contém o manifesto.<br/></td>
</tr>
<tr class="even">
<td>retorno de chamada</td>

<td>Esse atributo indica que você deseja receber uma notificação quando um consumidor executa determinadas ações. <br/> Se você incluir esse atributo, a ferramenta CTRPP usará a assinatura de função <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> alternativa, que você usa para passar o nome da função que implementa a função de retorno de chamada <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback.</strong></a><br/> Como alternativa à especificação desse atributo, você pode usar o <strong>argumento -NotificationCallback</strong><a href="ctrpp.md">CTRPP.</a><br/> <strong>Windows Vista:</strong> O único valor válido para esse atributo é &quot; &quot; personalizado. O <a href="ctrpp.md">utilitário CTRPP</a> gera o modelo para uma função de retorno de chamada <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback.</strong></a> O modelo está incluído no arquivo .c que CTRPP gerou. <br/> <br/></td>
</tr>
<tr class="odd">
<td>providerGuid</td>
<td><a href="performance-counters-guidtype-simple-type.md"><strong>man:GUIDType</strong></a></td>
<td>GUID de cadeia de caracteres que identifica exclusivamente o provedor no manifesto. O GUID deve ser exclusivo dentro do manifesto.<br/> Você precisa fornecer um novo GUID somente quando a versão do aplicativo for modificada (se você oferecer suporte a instalações lado a lado).<br/></td>
</tr>
<tr class="even">
<td>providerName</td>
<td><strong>xs:string</strong></td>
<td>O nome usado para criar o nome de classe WMI Win32_PerfRawData classe. Se você não especificar um nome, &quot; Contadores &quot; será usado como o nome da classe.<br/></td>
</tr>
<tr class="odd">
<td>Providertype</td>

<td>Identifica se o provedor é um provedor de modo de usuário, provedor de modo kernel ou provedor de driver. Os valores possíveis são os seguintes.<br/> 
<table>
<thead>
<tr class="header">
<th>Termo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>Usermode<br/></td>
<td>Especifique esse modo para um componente de modo de usuário, como um aplicativo, uma DLL ou um driver de modo de usuário. As extensões típicas para componentes de modo de usuário .exe ou .dll. Esse é o padrão.<br/></td>
</tr>
<tr class="even">
<td><span id="kernel"></span><span id="KERNEL"></span>Kernel<br/></td>
<td>Especifique esse modo para um componente de modo kernel, como um driver WDM ou WDF. A extensão típica para componentes do modo kernel é .sys.<br/> <strong>Windows Vista e Windows Server 2008:</strong> Esse valor não tem suporte até Windows 7 e Windows Server 2008 R2.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>resourceBase</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td><p>Define o valor de índice de recurso inicial que <a href="ctrpp.md">CTRPP</a> usa para gerar os identificadores de recurso.</p></td>
</tr>
<tr class="odd">
<td>símbolo</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></td>
<td><p>Um nome simbólico que identifica o provedor. A <a href="ctrpp.md">ferramenta CTRPP</a> cria uma variável HANDLE que você pode usar ao chamar funções que exigem um alçamento para o provedor (por exemplo, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>). O nome simbólico é o nome da variável.</p>
<p>Se você incluir o <strong>argumento -prefix</strong> ao chamar <a href="ctrpp.md">CTRPP</a>, a cadeia de caracteres de prefixo será adicionada ao início do nome simbólico.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 




