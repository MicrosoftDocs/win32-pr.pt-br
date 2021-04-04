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
# <a name="understanding-the-property-description-schema"></a><span data-ttu-id="1e03c-103">Compreendendo o esquema de descrição da propriedade</span><span class="sxs-lookup"><span data-stu-id="1e03c-103">Understanding the Property Description Schema</span></span>

<span data-ttu-id="1e03c-104">Este tópico apresenta o esquema de descrição de propriedade usado pelo sistema de propriedades do Shell.</span><span class="sxs-lookup"><span data-stu-id="1e03c-104">This topic introduces the property description schema used by the Shell property system.</span></span>

<span data-ttu-id="1e03c-105">A introdução dos novos recursos do Windows Vista e posteriores exigia que o sistema de propriedades Shell existente fosse estendido para:</span><span class="sxs-lookup"><span data-stu-id="1e03c-105">The introduction of new features for Windows Vista and later required that the existing Shell property system be extended to:</span></span>

-   <span data-ttu-id="1e03c-106">Dá suporte a um sistema de descrição de propriedades rica e extensível que fornece informações sobre propriedades, incluindo nomes de exibição, tipo, tipo de exibição, comportamento de classificação e grupo e outros atributos necessários para apresentar e operar nas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1e03c-106">Support a rich and extensible property description system that provides information about properties including display names, type, display type, sort and group behavior, and other attributes needed to present and operate over the properties.</span></span>
-   <span data-ttu-id="1e03c-107">Suporte a uma lista de ações de tipos de propriedade (combinada com a interface do usuário que pode editar esses tipos em diferentes modos de exibição, como ListView, painel de visualização, caixas de diálogo de propriedade e assim por diante) que podem ser associados a várias propriedades.</span><span class="sxs-lookup"><span data-stu-id="1e03c-107">Support a stock list of property types (combined with UI that can edit those types in different views like the listview, preview pane, property dialogs, and so on) that can be associated with various properties.</span></span>
-   <span data-ttu-id="1e03c-108">Forneça as listas de descrição da propriedade, que definem o conjunto de propriedades exibidas em várias exibições.</span><span class="sxs-lookup"><span data-stu-id="1e03c-108">Supply property description lists, which define the set of properties displayed in various views.</span></span>
-   <span data-ttu-id="1e03c-109">Forneça uma interface simplificada, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), portanto, os manipuladores de propriedade podem ser escritos com mais facilidade e, portanto, as propriedades podem persistir em arquivos.</span><span class="sxs-lookup"><span data-stu-id="1e03c-109">Provide a simplified interface, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), so property handlers can be written more easily and so properties can be persisted to files.</span></span>
-   <span data-ttu-id="1e03c-110">Suporte para manipuladores de propriedade que não são de arquivo para expor propriedades na exibição.</span><span class="sxs-lookup"><span data-stu-id="1e03c-110">Support for non-file property handlers to expose properties in the view.</span></span>

<span data-ttu-id="1e03c-111">Esses recursos são obtidos em uma arquitetura que fornece acesso abstrato às propriedades de um item de Shell.</span><span class="sxs-lookup"><span data-stu-id="1e03c-111">These features are achieved on an architecture that provides abstract access to the properties of a Shell item.</span></span> <span data-ttu-id="1e03c-112">Essa abstração é chamada de sistema de propriedades do Shell.</span><span class="sxs-lookup"><span data-stu-id="1e03c-112">This abstraction is called the Shell property system.</span></span>

-   [<span data-ttu-id="1e03c-113">O que é o esquema de descrição de propriedade?</span><span class="sxs-lookup"><span data-stu-id="1e03c-113">What Is the Property Description Schema?</span></span>](#what-is-the-property-description-schema)
-   [<span data-ttu-id="1e03c-114">Por que usar um esquema?</span><span class="sxs-lookup"><span data-stu-id="1e03c-114">Why Use a Schema?</span></span>](#why-use-a-schema)
-   [<span data-ttu-id="1e03c-115">Quais são as principais partes de esquema?</span><span class="sxs-lookup"><span data-stu-id="1e03c-115">What Are the Major Schema Parts?</span></span>](#what-are-the-major-schema-parts)
-   [<span data-ttu-id="1e03c-116">Alterações no Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e03c-116">Changes for Windows 7</span></span>](#changes-for-windows-7)
-   [<span data-ttu-id="1e03c-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e03c-117">Related topics</span></span>](#related-topics)

## <a name="what-is-the-property-description-schema"></a><span data-ttu-id="1e03c-118">O que é o esquema de descrição de propriedade?</span><span class="sxs-lookup"><span data-stu-id="1e03c-118">What Is the Property Description Schema?</span></span>

<span data-ttu-id="1e03c-119">O subsistema de esquema consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="1e03c-119">The schema subsystem consists of the following:</span></span>

-   <span data-ttu-id="1e03c-120">Um ou mais arquivos de esquema. propDesc que definem descrições de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1e03c-120">One or more .propdesc schema files that define property descriptions.</span></span> <span data-ttu-id="1e03c-121">O esquema de descrição de propriedade é definido em uma coleção de arquivos de esquema XML (usando a extensão de arquivo. propDesc) em tempo de execução no sistema.</span><span class="sxs-lookup"><span data-stu-id="1e03c-121">The property description schema is defined in a collection of XML schema files (using the .propdesc file extension) at runtime on the system.</span></span> <span data-ttu-id="1e03c-122">Esses arquivos são carregados de forma lenta quando uma parte do sistema de propriedades os exige.</span><span class="sxs-lookup"><span data-stu-id="1e03c-122">These files are lazy-loaded when a part of the property system requires them.</span></span>
-   <span data-ttu-id="1e03c-123">Um cache de esquema na memória usado para armazenar os arquivos de esquema analisados, que incluem todas as descrições de propriedade introduzidas no subsistema.</span><span class="sxs-lookup"><span data-stu-id="1e03c-123">An in-memory schema cache used to store the parsed schema files, which include all property descriptions introduced to the subsystem.</span></span> <span data-ttu-id="1e03c-124">Não é necessário reanalisar os arquivos de configuração. propDesc que descrevem o esquema.</span><span class="sxs-lookup"><span data-stu-id="1e03c-124">There is no need to reparse the .propdesc config files that describe the schema.</span></span> <span data-ttu-id="1e03c-125">Para obter mais informações, consulte [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)e [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span><span class="sxs-lookup"><span data-stu-id="1e03c-125">For more information, see [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema), and [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span></span>
-   <span data-ttu-id="1e03c-126">Um objeto de subsistema que implementa [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), que é usado para obter ou trabalhar com descrições de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1e03c-126">A subsystem object that implements [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), which is used to obtain or work with property descriptions.</span></span>
-   <span data-ttu-id="1e03c-127">Um objeto de subsistema que implementa [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), que é usado para informar e operar com base em uma descrição de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1e03c-127">A subsystem object that implements [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), which is used to inform and operate based on a property description.</span></span>
-   <span data-ttu-id="1e03c-128">Um objeto de subsistema que implementa [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), que é usado como uma coleção de descrições de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1e03c-128">A subsystem object that implements [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which is used as a collection of property descriptions.</span></span>

> [!Note]  
> <span data-ttu-id="1e03c-129">Você deve adicionar `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` ao elemento de esquema raiz dos seus arquivos. propDesc.</span><span class="sxs-lookup"><span data-stu-id="1e03c-129">You must add `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` to the root schema element of your .propdesc files.</span></span>

 

## <a name="why-use-a-schema"></a><span data-ttu-id="1e03c-130">Por que usar um esquema?</span><span class="sxs-lookup"><span data-stu-id="1e03c-130">Why Use a Schema?</span></span>

<span data-ttu-id="1e03c-131">As propriedades, por si só, não são de tipo seguro.</span><span class="sxs-lookup"><span data-stu-id="1e03c-131">Properties, by themselves, are not type-safe.</span></span> <span data-ttu-id="1e03c-132">Um componente pode atribuir um valor numérico à propriedade System. Author ou um carimbo de data-hora [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) à propriedade System. Music. campos AlbumTitle e, sem nenhuma outra aplicação ou orientação, os repositórios de propriedades permitirão isso.</span><span class="sxs-lookup"><span data-stu-id="1e03c-132">A component can assign a numerical value to the System.Author property, or a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) date-stamp to the System.Music.AlbumTitle property, and, without any further enforcement or guidance, the property stores will allow it.</span></span> <span data-ttu-id="1e03c-133">Portanto, precisávamos de uma noção para "schematize" as propriedades, que nos leva ao subsistema de esquema.</span><span class="sxs-lookup"><span data-stu-id="1e03c-133">So, we needed a notion to "schematize" the properties, which brings us to the schema subsystem.</span></span>

## <a name="what-are-the-major-schema-parts"></a><span data-ttu-id="1e03c-134">Quais são as principais partes de esquema?</span><span class="sxs-lookup"><span data-stu-id="1e03c-134">What Are the Major Schema Parts?</span></span>

<span data-ttu-id="1e03c-135">O esquema de descrição da propriedade usado pelo sistema de propriedades do Shell é composto por um único elemento [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) , bem como um atributo *SchemaVersion* , que indica a versão desse formato de definição de esquema.</span><span class="sxs-lookup"><span data-stu-id="1e03c-135">The property description schema used by the Shell property system is composed of a single [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) element, as well as a *schemaVersion* attribute, which indicates the version of this schema definition format.</span></span> <span data-ttu-id="1e03c-136">Observação: o valor deve ser "1,0".</span><span class="sxs-lookup"><span data-stu-id="1e03c-136">Note: value must be "1.0".</span></span>


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



<span data-ttu-id="1e03c-137">O [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) é composto por um ou mais elementos do [propertyDescription](./propdesc-schema-propertydescription.md) , bem como pelos atributos do *Editor* e do *produto* .</span><span class="sxs-lookup"><span data-stu-id="1e03c-137">The [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) is composed of one or more [propertyDescription](./propdesc-schema-propertydescription.md) elements, as well as *publisher* and *product* attributes.</span></span>


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



<span data-ttu-id="1e03c-138">Um [propertyDescription](./propdesc-schema-propertydescription.md) é composto por um [searchInfo](./propdesc-schema-searchinfo.md) e zero ou um dos elementos [labelInfo](./propdesc-schema-labelinfo.md), [TypeInfo](./propdesc-schema-typeinfo.md)e [DisplayInfo](./propdesc-schema-displayinfo.md) , bem como *FormatID*, *propID*, *propstr* e atributos *Name* .</span><span class="sxs-lookup"><span data-stu-id="1e03c-138">A [propertyDescription](./propdesc-schema-propertydescription.md) is composed of one [searchInfo](./propdesc-schema-searchinfo.md) and zero or one [labelInfo](./propdesc-schema-labelinfo.md), [typeInfo](./propdesc-schema-typeinfo.md), and [displayInfo](./propdesc-schema-displayinfo.md) elements, as well as *formatID*, *propID*, *propstr*, and *name* attributes.</span></span>

<span data-ttu-id="1e03c-139">Deve haver um elemento [propertyDescription](./propdesc-schema-propertydescription.md) para cada nome de propriedade canônico exclusivo que se destina a estar disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="1e03c-139">There should be one [propertyDescription](./propdesc-schema-propertydescription.md) element for every unique canonical property name that is intended to be available in the system.</span></span> <span data-ttu-id="1e03c-140">Os atributos de cadeia de caracteres têm um limite de 512 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1e03c-140">The string attributes have a limit of 512 characters.</span></span> <span data-ttu-id="1e03c-141">Valores com mais de 512 caracteres são truncados.</span><span class="sxs-lookup"><span data-stu-id="1e03c-141">Values longer than 512 characters are truncated.</span></span>


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



## <a name="changes-for-windows-7"></a><span data-ttu-id="1e03c-142">Alterações no Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e03c-142">Changes for Windows 7</span></span>

<span data-ttu-id="1e03c-143">O esquema de descrição da propriedade foi alterado para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e03c-143">The property description schema has been changed for Windows 7.</span></span> <span data-ttu-id="1e03c-144">Essas são alterações não significativas.</span><span class="sxs-lookup"><span data-stu-id="1e03c-144">These are non-breaking changes.</span></span> <span data-ttu-id="1e03c-145">Se um elemento de propriedade ou atributo não tiver mais suporte no Windows 7, o sistema operacional Windows 7 ignorará o elemento ou os atributos do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1e03c-145">If a property element or attribute is no longer supported in Windows 7, the Windows 7 operating system ignores the Windows Vista element or attributes.</span></span> <span data-ttu-id="1e03c-146">Da mesma forma, o Windows Vista também ignora novos elementos ou atributos de Propriedade do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e03c-146">Similarly, Windows Vista ignores new Windows 7 property elements or attributes as well.</span></span>

<span data-ttu-id="1e03c-147">No entanto, a atualização de propriedades personalizadas para o Windows 7 é recomendada para uma experiência de usuário melhor e mais consistente.</span><span class="sxs-lookup"><span data-stu-id="1e03c-147">However, updating custom properties for Windows 7 is recommended for a better and more consistent user experience.</span></span>

<span data-ttu-id="1e03c-148">A seguir estão os novos elementos e atributos:</span><span class="sxs-lookup"><span data-stu-id="1e03c-148">The following are new elements and attributes:</span></span>

-   <span data-ttu-id="1e03c-149">elementos [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) e [relatedproperty](./propdesc-schema-relatedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-149">[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) and [relatedProperty](./propdesc-schema-relatedproperty.md) elements</span></span>
-   <span data-ttu-id="1e03c-150">elemento [Image](./propdesc-schema-image.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-150">[image](./propdesc-schema-image.md) element</span></span>
-   <span data-ttu-id="1e03c-151">atributo mnemônicos do elemento [searchInfo](./propdesc-schema-searchinfo.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-151">mnemonics attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>
-   <span data-ttu-id="1e03c-152">atributo mnemônicos do elemento [enum](./propdesc-schema-enum.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-152">mnemonics attribute of the [enum](./propdesc-schema-enum.md) element</span></span>
-   <span data-ttu-id="1e03c-153">atributo searchRawValue do elemento [TypeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-153">searchRawValue attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

<span data-ttu-id="1e03c-154">Os seguintes elementos e atributos foram alterados:</span><span class="sxs-lookup"><span data-stu-id="1e03c-154">The following elements and attributes have changed:</span></span>

-   <span data-ttu-id="1e03c-155">elementos [enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md)e [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-155">[enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md), and [enumRange](./propdesc-schema-enumrange.md) elements</span></span>
-   <span data-ttu-id="1e03c-156">elemento [drawControl](./propdesc-schema-drawcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-156">[drawControl](./propdesc-schema-drawcontrol.md) element</span></span>
-   <span data-ttu-id="1e03c-157">elemento [editControl](./propdesc-schema-editcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-157">[editControl](./propdesc-schema-editcontrol.md) element</span></span>
-   <span data-ttu-id="1e03c-158">atributo propID do elemento [propertyDescription](./propdesc-schema-propertydescription.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-158">propID attribute of the [propertyDescription](./propdesc-schema-propertydescription.md) element</span></span>
-   <span data-ttu-id="1e03c-159">atributo columnIndexType do elemento [searchInfo](./propdesc-schema-searchinfo.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-159">columnIndexType attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>

<span data-ttu-id="1e03c-160">Os seguintes elementos e atributos foram removidos:</span><span class="sxs-lookup"><span data-stu-id="1e03c-160">The following elements and attributes have been removed:</span></span>

-   <span data-ttu-id="1e03c-161">elemento [queryControl](./propdesc-schema-querycontrol.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-161">[queryControl](./propdesc-schema-querycontrol.md) element</span></span>
-   <span data-ttu-id="1e03c-162">atributo isconsultáable do elemento [TypeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-162">isQueryable attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>
-   <span data-ttu-id="1e03c-163">atributo includeInFullTextQuery do elemento [TypeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="1e03c-163">includeInFullTextQuery attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e03c-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e03c-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e03c-165">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="1e03c-165">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1e03c-166">searchInfo</span><span class="sxs-lookup"><span data-stu-id="1e03c-166">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1e03c-167">labelInfo</span><span class="sxs-lookup"><span data-stu-id="1e03c-167">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1e03c-168">typeInfo</span><span class="sxs-lookup"><span data-stu-id="1e03c-168">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1e03c-169">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1e03c-169">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1e03c-170">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1e03c-170">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1e03c-171">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="1e03c-171">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1e03c-172">numberFormat</span><span class="sxs-lookup"><span data-stu-id="1e03c-172">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1e03c-173">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1e03c-173">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1e03c-174">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="1e03c-174">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1e03c-175">drawControl</span><span class="sxs-lookup"><span data-stu-id="1e03c-175">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1e03c-176">editControl</span><span class="sxs-lookup"><span data-stu-id="1e03c-176">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1e03c-177">filterControl</span><span class="sxs-lookup"><span data-stu-id="1e03c-177">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1e03c-178">queryControl</span><span class="sxs-lookup"><span data-stu-id="1e03c-178">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="1e03c-179">imagem</span><span class="sxs-lookup"><span data-stu-id="1e03c-179">image</span></span>](./propdesc-schema-image.md)
</dt> </dl>

 

 
