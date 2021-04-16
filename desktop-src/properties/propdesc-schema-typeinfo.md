---
description: Especifica as informações de tipo de uma propriedade.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: typeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758362"
---
# <a name="typeinfo"></a>typeInfo

Especifica as informações de tipo de uma propriedade. Deve haver apenas um elemento [TypeInfo]() para cada [propertyDescription](./propdesc-schema-propertydescription.md). Esse elemento foi alterado para o Windows 7.

Se houver vários elementos, o último será usado. Se nenhum elemento [TypeInfo]() for fornecido, as configurações de atributo padrão serão aplicadas à descrição da propriedade.

## <a name="syntax-for-windows-7"></a>Sintaxe do Windows 7


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                   | Elementos filho |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | Nenhum           |



 

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>type</td>
<td>Público. Opcional. O padrão é &quot; Any &quot; . Indica o tipo da propriedade. Veja a seguir os tipos válidos e seus tipos de variantes associados são recuperados por <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: Getpropertytype</strong></a>. 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Qualquer</td>
<td>Padrão. O subsistema de propriedades não impedirá ou imporá o valor da propriedade. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: Getpropertytype</strong></a> retorna VT_NULL. ISVs (fornecedores independentes de software) são altamente incentivados a fornecer um tipo em vez de fazer fallback nesse padrão.</td>
</tr>
<tr class="even">
<td>Nulo</td>
<td>Não há nenhum valor para essa propriedade. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: Getpropertytype</strong></a> retorna VT_NULL.</td>
</tr>
<tr class="odd">
<td>String</td>
<td>O valor deve ser um VT_LPWSTR, que é uma cadeia de caracteres Unicode terminada por uma referência nula.</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>O valor deve ser um VT_BOOL, que é um booliano.</td>
</tr>
<tr class="odd">
<td>Byte</td>
<td>O valor deve ser um VT_UI1, que é um byte.</td>
</tr>
<tr class="even">
<td>Buffer</td>
<td>O valor deve ser um VT_UI1 | Buffer de VT_VECTOR de bytes.</td>
</tr>
<tr class="odd">
<td>Int16</td>
<td>O valor deve ser um VT_I2, que é um inteiro de 16 bits.</td>
</tr>
<tr class="even">
<td>UInt16</td>
<td>O valor deve ser um VT_UI2, que é um inteiro sem sinal de 16 bits.</td>
</tr>
<tr class="odd">
<td>Int32</td>
<td>O valor deve ser um VT_I4, que é um inteiro de 32 bits.</td>
</tr>
<tr class="even">
<td>UInt32</td>
<td>O valor deve ser um VT_UI4, que é um inteiro sem sinal de 32 bits.</td>
</tr>
<tr class="odd">
<td>Int64</td>
<td>O valor deve ser um VT_I8, que é um inteiro de 64 bits.</td>
</tr>
<tr class="even">
<td>UInt64</td>
<td>O valor deve ser um VT_UI8, que é um inteiro sem sinal de 64 bits.</td>
</tr>
<tr class="odd">
<td>Double</td>
<td>O valor deve ser um VT_R8, que é um duplo.</td>
</tr>
<tr class="even">
<td>Datetime</td>
<td>O valor deve ser um VT_FILETIME, que é um <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</td>
</tr>
<tr class="odd">
<td>Guid</td>
<td>O valor deve ser um VT_CLSID, que é um identificador de classe (CLSID).</td>
</tr>
<tr class="even">
<td>Blob</td>
<td>O valor deve ser um VT_BLOB, que são bytes de comprimento fixo.</td>
</tr>
<tr class="odd">
<td>Stream</td>
<td>O valor deve ser um VT_STREAM, que é um objeto que implementa <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</td>
</tr>
<tr class="even">
<td>Área de Transferência</td>
<td>O valor deve ser um VT_CF, que é um formato de área de transferência.</td>
</tr>
<tr class="odd">
<td>Objeto</td>
<td>O valor deve ser um VT_UNKNOWN, que é um objeto que implementa <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>groupingRange</td>
<td>Opcional. O padrão é &quot; discreto &quot; . Especifica como a propriedade é exibida quando uma exibição é agrupada por essa propriedade. Uma vez definido aqui, esses valores são recuperados por <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription:: GetGroupingRange</strong></a>. Os tipos a seguir são válidos.

<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Discreto</td>
<td>Padrão. Exibe valores individuais.</td>
</tr>
<tr class="even">
<td>Alfanumérico</td>
<td>Exibe intervalos alfanuméricos estáticos para valores.</td>
</tr>
<tr class="odd">
<td>Tamanho</td>
<td>Exibe intervalos de tamanho estático para valores.</td>
</tr>
<tr class="even">
<td>Data</td>
<td>Exibe os grupos de mês/ano. Padrão para propriedades de Type = &quot; DateTime &quot; .</td>
</tr>
<tr class="odd">
<td>Timerelativo</td>
<td>Exibe em grupos relativos a tempo.</td>
</tr>
<tr class="even">
<td>Dinâmico</td>
<td>Exibe intervalos criados dinamicamente para os valores.</td>
</tr>
<tr class="odd">
<td>Porcentagem</td>
<td>Exibe o percentual de buckets.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>isInnate</td>
<td>Público. Opcional. O padrão é &quot;false&quot;. Especifica se a propriedade é considerada inato. Uma propriedade inato é uma que é calculada a partir do conteúdo de um arquivo ou de outros recursos ou sistemas. Por exemplo, System. Size é uma propriedade inato fornecida pelo sistema de arquivos; alterar o valor da propriedade não faz nada. Outros exemplos são System. Image. Dimensions e System.Document. PageCount, que são calculados por programas baseados no conteúdo do arquivo, não com base em uma configuração de alteração do usuário. Definir isInnate = &quot; true &quot; significa que o usuário não pode editar essa propriedade diretamente por meio de um controle de propriedade. Esse valor é mapeado para o sinalizador de PDTF_ISINNATE definido em <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usado em <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>canBePurged</td>
<td><strong>Windows Vista com Service Pack 1 (SP1) e posterior somente</strong>. Público. Opcional. Quando definido como &quot; true &quot; , permite que uma propriedade inato seja excluída. As propriedades inato, que são calculadas a partir de outras propriedades, são somente leitura por definição. O valor padrão para esse atributo depende do valor de <em>isInnate</em> .

<table>
<thead>
<tr class="header">
<th>isInnate</th>
<th>Valor padrão de canBePurged</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>true</td>
<td>false</td>
</tr>
<tr class="even">
<td>false</td>
<td>true</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Uma propriedade cujo valor de <em>isInnate</em> é &quot; false &quot; (o que significa que a propriedade é leitura/gravação) também não pode definir o valor de <em>canBePurged</em> como &quot; false &quot; . Essa restrição é imposta pelo sistema operacional.
</blockquote>
</div>
<div>
 
</div>
<p>Embora esse atributo tenha sido introduzido no Windows Vista com Service Pack 1 (SP1), um arquivo. propDesc que inclui esse atributo é compatível com o Windows Vista antes do Windows Vista com SP1. O atributo <em>canBePurged</em> é simplesmente ignorado nessa situação.</p></td>
</tr>
<tr class="odd">
<td>multipleValues</td>
<td>Público. Opcional. O padrão é &quot;false&quot;. Especifica se essa propriedade pode ter vários valores. Esse valor é mapeado para o sinalizador de PDTF_MULTIPLEVALUES definido em <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usado em <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>. Isso também influencia se VT_VECTOR é ou não o VARTYPE do valor da propriedade.</td>
</tr>
<tr class="even">
<td>isGroup</td>
<td>Público. Opcional. O padrão é &quot;false&quot;. Especifica se a propriedade é um título de grupo. Um título de grupo é estritamente usado em proplistes, não tem valor, nunca é armazenado em um arquivo e também deve ter <typeInfo type=&quot;Null&quot;> . Algumas interfaces do usuário no sistema usam o proplistor para indicar a sequência das propriedades a serem exibidas. Essas proplistes podem incluir referências a títulos de grupo (por exemplo, System. propus. Camera), que dizem à interface do usuário para iniciar uma nova seção de grupo (por exemplo, &quot; configurações de câmera &quot; ). Uma descrição de propriedade com IsGroup = &quot; true &quot; deve especificar um <labelInfo label=&quot;Some localized label&quot;> , caso contrário, não é uma propriedade útil. Esse valor é mapeado para o sinalizador de PDTF_ISGROUP definido em <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usado em <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>aggregationType</td>
<td>Público. Opcional. O padrão é &quot; Default &quot; . Especifica como as propriedades de agregação são exibidas quando vários itens são selecionados. Uma vez definido aqui, esses valores são recuperados por <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription:: Getaggregationtype</strong></a> como um <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>. Os tipos a seguir são válidos.

<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Padrão</td>
<td>Padrão. Exibe um espaço reservado de <strong>vários valores</strong> na interface do usuário. Esse será o padrão se o <em>tipo</em> for incompatível com o <em>AggregationType</em>especificado.</td>
</tr>
<tr class="even">
<td>Primeiro</td>
<td>Exibe o valor da Propriedade do primeiro item na seleção ou coleção.</td>
</tr>
<tr class="odd">
<td>Somar</td>
<td>Exibe a soma dos valores numéricos. Útil para propriedades como System. Media. Duration ou System. Size. Esse valor não é compatível com tipos não numéricos.</td>
</tr>
<tr class="even">
<td>Média</td>
<td>Exibe a média dos valores numéricos. Útil para propriedades como System. rating. Esse valor não é compatível com tipos não numéricos.</td>
</tr>
<tr class="odd">
<td>DateRange</td>
<td>Exibe um intervalo de datas. Útil para propriedades como System. Photo. DateTaken. Esse valor não é compatível com nada exceto Type = &quot; DateTime &quot; e é o padrão para propriedades desse tipo.</td>
</tr>
<tr class="even">
<td>Union</td>
<td>Exibe uma União de todos os valores na seleção ou na coleção. A ordem na qual os valores são mostrados é indefinida. Esse valor é o padrão para propriedades de Type = &quot; String &quot; e multipleValues = &quot; true &quot; .</td>
</tr>
<tr class="odd">
<td>Máximo</td>
<td>Exibe o valor máximo na coleção. Útil para propriedades como System. DateModified. Não compatível com tipos não numéricos ou não de data.</td>
</tr>
<tr class="even">
<td>Mínimo</td>
<td>Exibe o valor mínimo na coleção. Não compatível com tipos não numéricos ou não de data.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>istreeproperty</td>
<td>Público. Opcional. O valor padrão é &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>isviewable</td>
<td>Público. Opcional. O valor padrão é &quot;false&quot;. Especifica se esta propriedade deve ser visível para o usuário. Por exemplo, a interface do usuário do seletor de coluna mostra apenas as propriedades que têm isviewable = &quot; true &quot; . A exceção é a interface do usuário que é controlada por uma PropList, que sempre mostrará a propriedade. Se você tiver uma propriedade que serve apenas para modelar dados entre dois objetos e nunca se destina a ser visualizada pelo usuário, esse atributo deverá ser false. Esse valor é mapeado para o sinalizador de PDTF_ISVIEWABLE definido em <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usado em <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>isconsultáable</td>
<td>Somente Windows Vista. Sem suporte no Windows 7 e posterior. Público. Opcional. O valor padrão é &quot;false&quot;. Especifica se esta propriedade deve estar disponível na interface do usuário do Construtor de Consultas de pesquisa. Uma propriedade deve ter isviewable = &quot; true &quot; antes de isconsultáable = &quot; true &quot; ser respeitada. Esse valor é mapeado para o sinalizador de PDTF_ISQUERYABLE definido em <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usado em <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>searchRawValue</td>
<td><strong>Windows 7 e posterior.</strong> Público. Opcional. O valor padrão é &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>includeInFullTextQuery</td>
<td>Somente Windows Vista. Sem suporte no Windows 7 e posterior. Público. Opcional. O valor padrão é &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>conditionType</td>
<td>Público. Opcional. O padrão é &quot; cadeia de caracteres &quot; . Especifica uma dica para a interface do usuário de Construtor de Consultas de pesquisa para que ela possa determinar a lista de possíveis operadores de condição dentro de um predicado. Os valores a seguir são reconhecidos. 
<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Padrão. Os seguintes operadores serão usados: is, is,,,,, &quot; &quot; &quot; &quot; &quot; &lt; &quot; &quot; &gt; &quot; &quot; <= &quot; &quot; >= &quot; , começa com, &quot; &quot; &quot; termina com &quot; , &quot; Contains &quot; , &quot; não contém, &quot; &quot; é como &quot; .</td>
</tr>
<tr class="even">
<td>Número</td>
<td>Padrão para propriedades numéricas. Os seguintes operadores serão usados: Equals, não é igual a, é menor que, é maior que, é &quot; &quot; menor que &quot; &quot; &quot; &quot; &quot; &quot; &quot; ou igual a &quot; , &quot; é maior ou igual a &quot; .</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Padrão para propriedades de Type = &quot; DateTime &quot; . Os operadores a seguir serão usados: is, is, is, is before, for After, é &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; before, mas includes &quot; , &quot; é After, mas inclui &quot; .</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Padrão para propriedades de Type = &quot; Boolean &quot; . O mesmo que o número.</td>
</tr>
<tr class="odd">
<td>Tamanho</td>
<td>O mesmo que o número.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>defaultoperation</td>
<td>Público. Opcional. O padrão é &quot; igual &quot; . Especifica uma dica para a ferramenta de Construtor de Consultas de pesquisa para que ela possa determinar o operador padrão. Os valores possíveis são os seguintes:

<table>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Igual</td>
<td>Padrão. Indica o equivalente.</td>
</tr>
<tr class="even">
<td>NotEqual</td>
<td>Indica não equivalente.</td>
</tr>
<tr class="odd">
<td>LessThan</td>
<td>Indica menor que.</td>
</tr>
<tr class="even">
<td>GreaterThan</td>
<td>Padrão para propriedades de ConditionType = &quot; Size &quot; . Indica maior que.</td>
</tr>
<tr class="odd">
<td>Contém</td>
<td>Padrão para propriedades de ConditionType = &quot; String &quot; . Indica a inclusão.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
