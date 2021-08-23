---
description: Este tópico apresenta o esquema de descrição da propriedade usado pelo sistema de propriedades do Shell.
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Noções básicas sobre o esquema de descrição da propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85dbb0f20c5c4a206069e80aa308a26908bf90ee0d00cf80712a342e834411e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554556"
---
# <a name="understanding-the-property-description-schema"></a>Noções básicas sobre o esquema de descrição da propriedade

Este tópico apresenta o esquema de descrição da propriedade usado pelo sistema de propriedades do Shell.

A introdução de novos recursos para Windows Vista e posterior exigia que o sistema de propriedades existente do Shell fosse estendido para:

-   Dar suporte a um sistema de descrição de propriedade rico e extensível que fornece informações sobre propriedades, incluindo nomes de exibição, tipo, tipo de exibição, comportamento de classificação e grupo e outros atributos necessários para apresentar e operar sobre as propriedades.
-   Suporte a uma lista de estoque de tipos de propriedade (combinados com a interface do usuário que podem editar esses tipos em diferentes exibições, como o listview, o painel de visualização, as caixas de diálogo de propriedade e assim por diante) que podem ser associados a várias propriedades.
-   Listas de descrição da propriedade de fornecimento, que definem o conjunto de propriedades exibidas em várias exibições.
-   Forneça uma interface simplificada, [**IPropertyStore,**](/windows/win32/api/propsys/nn-propsys-ipropertystore)para que os manipuladores de propriedade possam ser gravados com mais facilidade e, portanto, as propriedades possam ser persistida nos arquivos.
-   Suporte para manipuladores de propriedades que não são de arquivo para expor propriedades na exibição.

Esses recursos são obtidos em uma arquitetura que fornece acesso abstrato às propriedades de um item do Shell. Essa abstração é chamada de sistema de propriedades shell.

-   [O que é o esquema de descrição da propriedade?](#what-is-the-property-description-schema)
-   [Por que usar um esquema?](#why-use-a-schema)
-   [Quais são as partes principais do esquema?](#what-are-the-major-schema-parts)
-   [Alterações para Windows 7](#changes-for-windows-7)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-the-property-description-schema"></a>O que é o esquema de descrição da propriedade?

O subsistema de esquema consiste no seguinte:

-   Um ou mais arquivos de esquema .propdesc que definem descrições de propriedade. O esquema de descrição da propriedade é definido em uma coleção de arquivos de esquema XML (usando a extensão de arquivo .propdesc) em runtime no sistema. Esses arquivos são carregados de forma lento quando uma parte do sistema de propriedades os exige.
-   Um cache de esquema na memória usado para armazenar os arquivos de esquema analisados, que incluem todas as descrições de propriedade introduzidas no subsistema. Não é necessário reparpar os arquivos de configuração .propdesc que descrevem o esquema. Para obter mais informações, [**consulte PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)e [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).
-   Um objeto de subsistema que implementa [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), que é usado para obter ou trabalhar com descrições de propriedade.
-   Um objeto de subsistema que implementa [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), que é usado para informar e operar com base em uma descrição de propriedade.
-   Um objeto de subsistema que implementa [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), que é usado como uma coleção de descrições de propriedade.

> [!Note]  
> Você deve adicionar `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` ao elemento de esquema raiz de seus arquivos .propdesc.

 

## <a name="why-use-a-schema"></a>Por que usar um esquema?

As propriedades, por si só, não são de tipo seguro. Um componente pode atribuir um valor numérico à propriedade System.Author ou um carimbo de data/hora [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) à propriedade System.Music.AlbumTitle e, sem nenhuma imposição ou orientação, os armazenamentos de propriedades permitirão isso. Portanto, precisávamos de uma noção para "esquematizar" as propriedades, o que nos leva ao subsistema de esquema.

## <a name="what-are-the-major-schema-parts"></a>Quais são as partes principais do esquema?

O esquema de descrição da propriedade usado pelo sistema de propriedades shell é composto por um único elemento [propertyDescriptionList,](./propdesc-schema-propertydescriptionlist.md) bem como um atributo *schemaVersion,* que indica a versão desse formato de definição de esquema. Observação: o valor deve ser "1.0".


```
<!-- schema -->
    <xs:element name="schema">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescriptionList" minOccurs="1" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="schemaVersion"  type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



A [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) é composta por um ou mais elementos [propertyDescription,](./propdesc-schema-propertydescription.md) bem como *atributos de editor* *e* produto.


```
<!-- propertyDescriptionList -->
    <xs:element name="propertyDescriptionList">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product"   type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



Uma [propertyDescription](./propdesc-schema-propertydescription.md) é composta por um [elemento searchInfo](./propdesc-schema-searchinfo.md) e zero ou um [labelInfo,](./propdesc-schema-labelinfo.md) [typeInfo](./propdesc-schema-typeinfo.md)e [displayInfo,](./propdesc-schema-displayinfo.md) bem como os atributos *formatID,* *propID,* *propstr* e *name.*

Deve haver um [elemento propertyDescription](./propdesc-schema-propertydescription.md) para cada nome de propriedade canônico exclusivo que se destina a estar disponível no sistema. Os atributos de cadeia de caracteres têm um limite de 512 caracteres. Valores com mais de 512 caracteres são truncados.


```
<!-- propertyDescription -->
    <xs:element name="propertyDescription">
      <xs:complexType>
        <xs:all>
          <xs:element name="description"    type="xs:string" minOccurs="0" maxOccurs="1"/>
          <xs:element ref="searchInfo"   minOccurs="1" maxOccurs="1"/>
          <xs:element ref="labelInfo"    minOccurs="0" maxOccurs="1"/>
          <xs:element ref="typeInfo"     minOccurs="0" maxOccurs="1"/>
          <xs:element ref="displayInfo"  minOccurs="0" maxOccurs="1"/>
        </xs:all>
        <xs:attribute name="formatID"  type="upcase-uuid" use="required""/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required""/>
        <xs:attribute name="name"      type="canonical-name" use="required"/>
      </xs:complexType>
    </xs:element>
```



## <a name="changes-for-windows-7"></a>Alterações para Windows 7

O esquema de descrição da propriedade foi alterado para Windows 7. Essas são alterações sem quebra. Se um elemento ou atributo de propriedade não tiver mais suporte no Windows 7, o sistema operacional Windows 7 ignorará o elemento ou atributos Windows Vista. Da mesma forma, Windows Vista ignora novos Windows 7 elementos de propriedade ou atributos também.

No entanto, a atualização das propriedades personalizadas Windows 7 é recomendada para uma experiência do usuário melhor e mais consistente.

Veja a seguir novos elementos e atributos:

-   [elementos relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) [e relatedProperty](./propdesc-schema-relatedproperty.md)
-   [elemento image](./propdesc-schema-image.md)
-   Atributo mnemonics do [elemento searchInfo](./propdesc-schema-searchinfo.md)
-   Atributo mnemonics do [elemento enum](./propdesc-schema-enum.md)
-   atributo searchRawValue do [elemento typeInfo](./propdesc-schema-typeinfo.md)

Os seguintes elementos e atributos foram alterados:

-   [elementos enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md)e [enumRange](./propdesc-schema-enumrange.md)
-   [Elemento drawControl](./propdesc-schema-drawcontrol.md)
-   [Elemento editControl](./propdesc-schema-editcontrol.md)
-   atributo propID do [elemento propertyDescription](./propdesc-schema-propertydescription.md)
-   atributo columnIndexType do [elemento searchInfo](./propdesc-schema-searchinfo.md)

Os seguintes elementos e atributos foram removidos:

-   [Elemento queryControl](./propdesc-schema-querycontrol.md)
-   Atributo isQueryable do [elemento typeInfo](./propdesc-schema-typeinfo.md)
-   atributo includeInFullTextQuery do [elemento typeInfo](./propdesc-schema-typeinfo.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propertydescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[Filtercontrol](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[imagem](./propdesc-schema-image.md)
</dt> </dl>

 

 
