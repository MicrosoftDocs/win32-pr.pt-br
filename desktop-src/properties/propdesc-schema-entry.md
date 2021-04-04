---
description: Este tópico apresenta o esquema de descrição de propriedade usado pelo sistema de propriedades do Shell.
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Compreendendo o esquema de descrição da propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51d9e7c2b6fb4b599f977c0c49ad1cb2514fe8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010791"
---
# <a name="understanding-the-property-description-schema"></a>Compreendendo o esquema de descrição da propriedade

Este tópico apresenta o esquema de descrição de propriedade usado pelo sistema de propriedades do Shell.

A introdução dos novos recursos do Windows Vista e posteriores exigia que o sistema de propriedades Shell existente fosse estendido para:

-   Dá suporte a um sistema de descrição de propriedades rica e extensível que fornece informações sobre propriedades, incluindo nomes de exibição, tipo, tipo de exibição, comportamento de classificação e grupo e outros atributos necessários para apresentar e operar nas propriedades.
-   Suporte a uma lista de ações de tipos de propriedade (combinada com a interface do usuário que pode editar esses tipos em diferentes modos de exibição, como ListView, painel de visualização, caixas de diálogo de propriedade e assim por diante) que podem ser associados a várias propriedades.
-   Forneça as listas de descrição da propriedade, que definem o conjunto de propriedades exibidas em várias exibições.
-   Forneça uma interface simplificada, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), portanto, os manipuladores de propriedade podem ser escritos com mais facilidade e, portanto, as propriedades podem persistir em arquivos.
-   Suporte para manipuladores de propriedade que não são de arquivo para expor propriedades na exibição.

Esses recursos são obtidos em uma arquitetura que fornece acesso abstrato às propriedades de um item de Shell. Essa abstração é chamada de sistema de propriedades do Shell.

-   [O que é o esquema de descrição de propriedade?](#what-is-the-property-description-schema)
-   [Por que usar um esquema?](#why-use-a-schema)
-   [Quais são as principais partes de esquema?](#what-are-the-major-schema-parts)
-   [Alterações no Windows 7](#changes-for-windows-7)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-the-property-description-schema"></a>O que é o esquema de descrição de propriedade?

O subsistema de esquema consiste no seguinte:

-   Um ou mais arquivos de esquema. propDesc que definem descrições de propriedade. O esquema de descrição de propriedade é definido em uma coleção de arquivos de esquema XML (usando a extensão de arquivo. propDesc) em tempo de execução no sistema. Esses arquivos são carregados de forma lenta quando uma parte do sistema de propriedades os exige.
-   Um cache de esquema na memória usado para armazenar os arquivos de esquema analisados, que incluem todas as descrições de propriedade introduzidas no subsistema. Não é necessário reanalisar os arquivos de configuração. propDesc que descrevem o esquema. Para obter mais informações, consulte [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)e [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).
-   Um objeto de subsistema que implementa [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), que é usado para obter ou trabalhar com descrições de propriedade.
-   Um objeto de subsistema que implementa [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), que é usado para informar e operar com base em uma descrição de propriedade.
-   Um objeto de subsistema que implementa [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), que é usado como uma coleção de descrições de propriedade.

> [!Note]  
> Você deve adicionar `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` ao elemento de esquema raiz dos seus arquivos. propDesc.

 

## <a name="why-use-a-schema"></a>Por que usar um esquema?

As propriedades, por si só, não são de tipo seguro. Um componente pode atribuir um valor numérico à propriedade System. Author ou um carimbo de data-hora [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) à propriedade System. Music. campos AlbumTitle e, sem nenhuma outra aplicação ou orientação, os repositórios de propriedades permitirão isso. Portanto, precisávamos de uma noção para "schematize" as propriedades, que nos leva ao subsistema de esquema.

## <a name="what-are-the-major-schema-parts"></a>Quais são as principais partes de esquema?

O esquema de descrição da propriedade usado pelo sistema de propriedades do Shell é composto por um único elemento [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) , bem como um atributo *SchemaVersion* , que indica a versão desse formato de definição de esquema. Observação: o valor deve ser "1,0".


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



O [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) é composto por um ou mais elementos do [propertyDescription](./propdesc-schema-propertydescription.md) , bem como pelos atributos do *Editor* e do *produto* .


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



Um [propertyDescription](./propdesc-schema-propertydescription.md) é composto por um [searchInfo](./propdesc-schema-searchinfo.md) e zero ou um dos elementos [labelInfo](./propdesc-schema-labelinfo.md), [TypeInfo](./propdesc-schema-typeinfo.md)e [DisplayInfo](./propdesc-schema-displayinfo.md) , bem como *FormatID*, *propID*, *propstr* e atributos *Name* .

Deve haver um elemento [propertyDescription](./propdesc-schema-propertydescription.md) para cada nome de propriedade canônico exclusivo que se destina a estar disponível no sistema. Os atributos de cadeia de caracteres têm um limite de 512 caracteres. Valores com mais de 512 caracteres são truncados.


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



## <a name="changes-for-windows-7"></a>Alterações no Windows 7

O esquema de descrição da propriedade foi alterado para o Windows 7. Essas são alterações não significativas. Se um elemento de propriedade ou atributo não tiver mais suporte no Windows 7, o sistema operacional Windows 7 ignorará o elemento ou os atributos do Windows Vista. Da mesma forma, o Windows Vista também ignora novos elementos ou atributos de Propriedade do Windows 7.

No entanto, a atualização de propriedades personalizadas para o Windows 7 é recomendada para uma experiência de usuário melhor e mais consistente.

A seguir estão os novos elementos e atributos:

-   elementos [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) e [relatedproperty](./propdesc-schema-relatedproperty.md)
-   elemento [Image](./propdesc-schema-image.md)
-   atributo mnemônicos do elemento [searchInfo](./propdesc-schema-searchinfo.md)
-   atributo mnemônicos do elemento [enum](./propdesc-schema-enum.md)
-   atributo searchRawValue do elemento [TypeInfo](./propdesc-schema-typeinfo.md)

Os seguintes elementos e atributos foram alterados:

-   elementos [enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md)e [enumRange](./propdesc-schema-enumrange.md)
-   elemento [drawControl](./propdesc-schema-drawcontrol.md)
-   elemento [editControl](./propdesc-schema-editcontrol.md)
-   atributo propID do elemento [propertyDescription](./propdesc-schema-propertydescription.md)
-   atributo columnIndexType do elemento [searchInfo](./propdesc-schema-searchinfo.md)

Os seguintes elementos e atributos foram removidos:

-   elemento [queryControl](./propdesc-schema-querycontrol.md)
-   atributo isconsultáable do elemento [TypeInfo](./propdesc-schema-typeinfo.md)
-   atributo includeInFullTextQuery do elemento [TypeInfo](./propdesc-schema-typeinfo.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[imagem](./propdesc-schema-image.md)
</dt> </dl>

 

 
