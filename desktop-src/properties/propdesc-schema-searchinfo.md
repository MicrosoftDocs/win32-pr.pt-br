---
description: Especifica como configurar o mecanismo de pesquisa do Windows com relação a uma determinada definição de propriedade.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783320"
---
# <a name="searchinfo"></a><span data-ttu-id="f5ae1-103">searchInfo</span><span class="sxs-lookup"><span data-stu-id="f5ae1-103">searchInfo</span></span>

<span data-ttu-id="f5ae1-104">Especifica como configurar o mecanismo de pesquisa do Windows com relação a uma determinada definição de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-104">Specifies how to configure the Windows search engine with respect to a given property definition.</span></span> <span data-ttu-id="f5ae1-105">Se nenhum elemento [searchInfo]() for fornecido, a propriedade não será incluída no mecanismo de pesquisa do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-105">If no [searchInfo]() element is provided, then the property is not included in the Windows search engine.</span></span> <span data-ttu-id="f5ae1-106">Esse elemento foi alterado para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-106">This element has changed for Windows 7.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="f5ae1-107">Sintaxe do Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5ae1-107">Syntax for Windows 7</span></span>


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a><span data-ttu-id="f5ae1-108">Sintaxe do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5ae1-108">Syntax for Windows Vista</span></span>


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="f5ae1-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f5ae1-109">Element Information</span></span>



| <span data-ttu-id="f5ae1-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f5ae1-110">Parent Element</span></span>                                                   | <span data-ttu-id="f5ae1-111">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f5ae1-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="f5ae1-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f5ae1-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="f5ae1-113">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f5ae1-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="f5ae1-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="f5ae1-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f5ae1-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="f5ae1-115">Attribute</span></span></th>
<th><span data-ttu-id="f5ae1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5ae1-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f5ae1-117">inInvertedIndex</span><span class="sxs-lookup"><span data-stu-id="f5ae1-117">inInvertedIndex</span></span></td>
<td><span data-ttu-id="f5ae1-118">Público.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-118">Public.</span></span> <span data-ttu-id="f5ae1-119">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-119">Optional.</span></span> <span data-ttu-id="f5ae1-120">Indica se o valor da propriedade deve ser armazenado no índice invertido.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-120">Indicates whether the property value should be stored in the inverted index.</span></span> <span data-ttu-id="f5ae1-121">Isso permite que os usuários finais executem consultas de texto completo sobre os valores dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-121">This lets end users perform full-text queries over the values of this property.</span></span> <span data-ttu-id="f5ae1-122">O padrão é &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-122">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5ae1-123">IsColumn</span><span class="sxs-lookup"><span data-stu-id="f5ae1-123">isColumn</span></span></td>
<td><span data-ttu-id="f5ae1-124">Público.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-124">Public.</span></span> <span data-ttu-id="f5ae1-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-125">Optional.</span></span> <span data-ttu-id="f5ae1-126">Indica se a propriedade também deve ser armazenada no banco de dados do Windows Search como uma coluna, de modo que os ISVs (fornecedores independentes de software) possam criar consultas baseadas em predicado (por exemplo, &quot; Selecione \*, em que &quot; System. title &quot; = ' qqq ' &quot; ).</span><span class="sxs-lookup"><span data-stu-id="f5ae1-126">Indicates whether the property should also be stored in the Windows search database as a column, so that independent software vendors (ISVs) can create predicate-based queries (for example, &quot;Select \* Where &quot;System.Title&quot;='qqq'&quot;).</span></span> <span data-ttu-id="f5ae1-127">Se o criador do esquema quiser permitir que os usuários finais (ou desenvolvedores) criem consultas baseadas em predicado nas propriedades, isso precisará ser definido como &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="f5ae1-127">If the schema creator wants to enable end users (or developers) to create predicate based queries on the properties, then this needs to be set to &quot;true&quot;.</span></span> <span data-ttu-id="f5ae1-128">O padrão é &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-128">The default is &quot;false&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5ae1-129">isColumnSparse</span><span class="sxs-lookup"><span data-stu-id="f5ae1-129">isColumnSparse</span></span></td>
<td><span data-ttu-id="f5ae1-130">Público.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-130">Public.</span></span> <span data-ttu-id="f5ae1-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-131">Optional.</span></span> <span data-ttu-id="f5ae1-132">O padrão é &quot;true&quot;.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-132">The default is &quot;true&quot;.</span></span> <span data-ttu-id="f5ae1-133">Se a propriedade tiver valores múltiplos, esse atributo será sempre &quot; verdadeiro &quot; .</span><span class="sxs-lookup"><span data-stu-id="f5ae1-133">If the property is multi-valued, this attribute is always &quot;true&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5ae1-134">columnIndexType</span><span class="sxs-lookup"><span data-stu-id="f5ae1-134">columnIndexType</span></span></td>
<td><span data-ttu-id="f5ae1-135">Público.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-135">Public.</span></span> <span data-ttu-id="f5ae1-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-136">Optional.</span></span> <span data-ttu-id="f5ae1-137">Para otimizar a classificação e o agrupamento, o mecanismo de pesquisa do Windows pode criar índices secundários para propriedades que têm IsColumn = &quot; true &quot; .</span><span class="sxs-lookup"><span data-stu-id="f5ae1-137">To optimize sorting and grouping, the Windows search engine can create secondary indexes for properties that have isColumn=&quot;true&quot;.</span></span> <span data-ttu-id="f5ae1-138">Esse atributo só é útil quando inInvertedIndex é &quot; verdadeiro &quot; no Windows Vista ou quando IsColumn é &quot; true &quot; no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-138">This attribute is only useful when inInvertedIndex is &quot;true&quot; in Windows Vista or when isColumn is &quot;true&quot; in Windows 7.</span></span> <span data-ttu-id="f5ae1-139">Se a propriedade tende a ser classificada frequentemente pelos usuários, esse atributo deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-139">If the property tends to be sorted frequently by users, this attribute should be specified.</span></span> <span data-ttu-id="f5ae1-140">O valor padrão no Windows Vista é não &quot; indexado &quot; .</span><span class="sxs-lookup"><span data-stu-id="f5ae1-140">The default value in Windows Vista is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="f5ae1-141">O valor padrão no Windows 7 é &quot; OnDemand &quot; .</span><span class="sxs-lookup"><span data-stu-id="f5ae1-141">The default value in Windows 7 is &quot;OnDemand&quot;.</span></span> <span data-ttu-id="f5ae1-142">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-142">The following values are valid.</span></span>
<ul>
<li><span data-ttu-id="f5ae1-143">Não <strong>indexado</strong>: nunca compile um índice de valor.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-143"><strong>NotIndexed</strong>: Never build a value index.</span></span></li>
<li><span data-ttu-id="f5ae1-144">Em <strong>disco</strong>: Crie um índice de valor por padrão para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-144"><strong>OnDisk</strong>: Build a value index by default for this property.</span></span></li>
<li><span data-ttu-id="f5ae1-145"><strong>OnDiskAll</strong> (somente Windows 7 e posterior): Crie um índice de valor por padrão para essa propriedade e, se for uma propriedade de vetor, também um índice de valor para todos os valores de vetor concatenados.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-145"><strong>OnDiskAll</strong> (Windows 7 and later only): Build a value index by default for this property, and if it is a vector property, also a value index for all concatenated vector values.</span></span></li>
<li><span data-ttu-id="f5ae1-146"><strong>OnDiskVector</strong> (somente Windows 7 e posterior): Crie um índice de valor por padrão para os valores de vetor concatenados.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-146"><strong>OnDiskVector</strong> (Windows 7 and later only): Build a value index by default for the concatenated vector values.</span></span></li>
<li><span data-ttu-id="f5ae1-147"><strong>OnDemand</strong> (somente Windows 7 e posterior): somente compilar índices de valor por demanda, ou seja, somente primeira vez que eles são usados para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-147"><strong>OnDemand</strong> (Windows 7 and later only): Only build value indices by demand, that is, only first time they are used for a query.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5ae1-148">maxSize</span><span class="sxs-lookup"><span data-stu-id="f5ae1-148">maxSize</span></span></td>
<td><span data-ttu-id="f5ae1-149">Público.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-149">Public.</span></span> <span data-ttu-id="f5ae1-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-150">Optional.</span></span> <span data-ttu-id="f5ae1-151">O tamanho máximo, em bytes, permitido para uma determinada propriedade que é armazenada no banco de dados do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-151">The maximum size, in bytes, allowed for a certain property that is stored in the Windows search database.</span></span> <span data-ttu-id="f5ae1-152">O padrão é:</span><span class="sxs-lookup"><span data-stu-id="f5ae1-152">The default is:</span></span>
<ul>
<li><span data-ttu-id="f5ae1-153"><strong>Windows Vista</strong>: 128 bytes</span><span class="sxs-lookup"><span data-stu-id="f5ae1-153"><strong>Windows Vista</strong>: 128 bytes</span></span></li>
<li><span data-ttu-id="f5ae1-154"><strong>Windows 7 e posterior</strong>: 512 bytes</span><span class="sxs-lookup"><span data-stu-id="f5ae1-154"><strong>Windows 7 and later</strong>: 512 bytes</span></span></li>
</ul>
<span data-ttu-id="f5ae1-155">Observe que esse tamanho máximo é medido em bytes, não em caracteres.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-155">Note that this maximum size is measured in bytes, not characters.</span></span> <span data-ttu-id="f5ae1-156">O número máximo de caracteres depende de sua codificação.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-156">The maximum number of characters depends on their encoding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5ae1-157">mnemônico</span><span class="sxs-lookup"><span data-stu-id="f5ae1-157">mnemonics</span></span></td>
<td><span data-ttu-id="f5ae1-158"><strong>Windows 7 e posterior.</strong></span><span class="sxs-lookup"><span data-stu-id="f5ae1-158"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="f5ae1-159">Público.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-159">Public.</span></span> <span data-ttu-id="f5ae1-160">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-160">Optional.</span></span> <span data-ttu-id="f5ae1-161">Uma lista de valores mnemônicos que podem ser usados para fazer referência à propriedade em consultas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-161">A list of mnemonic values that can be used to refer to the property in search queries.</span></span> <span data-ttu-id="f5ae1-162">A lista é delimitada com o caractere ' | '.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-162">The list is delimited with the '|' character.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
