---
description: Especifica como os rótulos da propriedade são exibidos.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750881"
---
# <a name="labelinfo"></a>labelInfo

Especifica como os rótulos da propriedade são exibidos. Deve haver apenas um elemento [labelInfo]() para cada elemento [propertyDescription](./propdesc-schema-propertydescription.md) .

Se houver vários elementos, o último será usado. Se nenhum elemento [labelInfo]() for fornecido, o rótulo da propriedade não será exibido; no entanto, isso normalmente seria um defeito.

## <a name="syntax"></a>Syntax


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
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
<td>label</td>
<td>Público. Opcional. O rótulo como é exibido na interface do usuário (por exemplo, o rótulo de coluna de detalhes ou o painel de visualização). A sintaxe permite uma cadeia de caracteres de exibição direta ou uma referência de cadeia de caracteres de exibição indireta. Use a cadeia de caracteres de exibição indireta porque ela pode ser localizada. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription:: GetDisplayName</strong></a> retorna o nome de exibição resolvido.</td>
</tr>
<tr class="even">
<td>sortDescription</td>
<td>Opcional. Especifica as cadeias de caracteres oferecidas como opções de classificação. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription:: GetSortDescription</strong></a> retorna essa descrição de classificação. Os valores a seguir fornecem as cadeias de caracteres da interface do usuário correspondentes.
<ul>
<li>Geral: &quot; classificação indo até a &quot;  /  &quot; classificação ficar inativa&quot;</li>
<li>AToZ: &quot; A na parte superior &quot;  /  &quot; Z no início&quot;</li>
<li>LowestHighest: &quot; mais baixo no topo superior &quot;  /  &quot; no início&quot;</li>
<li>OldestNewest: mais &quot; antigo no início superior &quot;  /  &quot; na parte superior&quot;</li>
<li>SmallestLargest: &quot; menor no &quot;  /  &quot; maior no início&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>invitationText</td>
<td>Opcional. O texto da cadeia de caracteres de ajuda que é exibido como uma instrução para o usuário para o controle ou dica de ferramenta (por exemplo, &quot; Insira o nome do autor. &quot; ). A sintaxe permite uma cadeia de caracteres de exibição direta ou uma referência de cadeia de caracteres de exibição indireta. Use a cadeia de caracteres de exibição indireta porque ela pode ser localizada. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription:: GetEditInvitation</strong></a> retorna o texto de convite resolvido.</td>
</tr>
<tr class="even">
<td>hideLabel</td>
<td>Opcional. O padrão é &quot;false&quot;. Indica se o rótulo está oculto.</td>
</tr>
</tbody>
</table>



 

 

 
