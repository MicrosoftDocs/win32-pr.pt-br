---
description: O <property> elemento opcional especifica uma propriedade usada pelo conector de pesquisa. Essas propriedades são específicas para esse conector de pesquisa, portanto, não há nenhum conjunto predefinido de nomes a ser usado. Este elemento não tem elementos filho.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Elemento Property de propertyStore (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501455"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a><span data-ttu-id="87b26-105">Elemento Property de propertyStore (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="87b26-105">property Element of propertyStore (Search Connector Schema)</span></span>

<span data-ttu-id="87b26-106">O <property> elemento opcional especifica uma propriedade usada pelo conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="87b26-106">The optional <property> element specifies a property used by the search connector.</span></span> <span data-ttu-id="87b26-107">Essas propriedades são específicas para esse conector de pesquisa, portanto, não há nenhum conjunto predefinido de nomes a ser usado.</span><span class="sxs-lookup"><span data-stu-id="87b26-107">These properties are specific to this search connector, so there is no predefined set of names to use.</span></span> <span data-ttu-id="87b26-108">Este elemento não tem elementos filho.</span><span class="sxs-lookup"><span data-stu-id="87b26-108">This element has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="87b26-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="87b26-109">Syntax</span></span>


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="87b26-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="87b26-110">Element Information</span></span>



| <span data-ttu-id="87b26-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="87b26-111">Parent Element</span></span>                                                                           | <span data-ttu-id="87b26-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="87b26-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="87b26-113">Elemento propertyStore (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="87b26-113">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a><span data-ttu-id="87b26-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="87b26-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="87b26-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="87b26-115">Attribute</span></span></th>
<th><span data-ttu-id="87b26-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="87b26-116">Description</span></span></th>
<th><span data-ttu-id="87b26-117">Valores</span><span class="sxs-lookup"><span data-stu-id="87b26-117">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87b26-118">name</span><span class="sxs-lookup"><span data-stu-id="87b26-118">name</span></span></td>
<td><span data-ttu-id="87b26-119">Público.</span><span class="sxs-lookup"><span data-stu-id="87b26-119">Public.</span></span> <span data-ttu-id="87b26-120">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="87b26-120">Required.</span></span> <span data-ttu-id="87b26-121">O nome para exibição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="87b26-121">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="87b26-122">tipo</span><span class="sxs-lookup"><span data-stu-id="87b26-122">type</span></span></td>
<td><span data-ttu-id="87b26-123">Público.</span><span class="sxs-lookup"><span data-stu-id="87b26-123">Public.</span></span> <span data-ttu-id="87b26-124">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="87b26-124">Required.</span></span> <span data-ttu-id="87b26-125">O tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="87b26-125">The type of property.</span></span></td>
<td><span data-ttu-id="87b26-126">Any: padrão.</span><span class="sxs-lookup"><span data-stu-id="87b26-126">Any: Default.</span></span> <span data-ttu-id="87b26-127">O valor não será forçado pelo subsistema de propriedades.</span><span class="sxs-lookup"><span data-stu-id="87b26-127">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="87b26-128">VT_NULL será retornado por getpropertytype.</span><span class="sxs-lookup"><span data-stu-id="87b26-128">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="87b26-129">NULL: não há nenhum valor para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="87b26-129">Null: There is no value for this property.</span></span> <span data-ttu-id="87b26-130">VT_NULL será retornado por getpropertytype.</span><span class="sxs-lookup"><span data-stu-id="87b26-130">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="87b26-131">Cadeia de caracteres: o valor deve ser um VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="87b26-131">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="87b26-132">Booliano: o valor deve ser um VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="87b26-132">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="87b26-133">Byte: o valor deve ser um VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="87b26-133">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="87b26-134">Buffer: o valor deve ser um VT_UI1 | Buffer de VT_VECTOR de bytes.</span><span class="sxs-lookup"><span data-stu-id="87b26-134">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="87b26-135">Int16: o valor deve ser um VT_I2.</span><span class="sxs-lookup"><span data-stu-id="87b26-135">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="87b26-136">UInt16: o valor deve ser um VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="87b26-136">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="87b26-137">Int32: o valor deve ser um VT_I4.</span><span class="sxs-lookup"><span data-stu-id="87b26-137">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="87b26-138">UInt32: o valor deve ser um VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="87b26-138">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="87b26-139">Int64: o valor deve ser um VT_I8.</span><span class="sxs-lookup"><span data-stu-id="87b26-139">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="87b26-140">UInt64: o valor deve ser um VT_UI8</span><span class="sxs-lookup"><span data-stu-id="87b26-140">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="87b26-141">Double: o valor deve ser um VT_R8.</span><span class="sxs-lookup"><span data-stu-id="87b26-141">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="87b26-142">DateTime: o valor deve ser um VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="87b26-142">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="87b26-143">GUID: o valor deve ser um VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="87b26-143">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="87b26-144">Blob: o valor deve ser um VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="87b26-144">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="87b26-145">Objeto: o valor deve ser um VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="87b26-145">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="87b26-146">Stream: o valor deve ser um VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="87b26-146">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="87b26-147">Área de transferência: o valor deve ser um VT_CF.</span><span class="sxs-lookup"><span data-stu-id="87b26-147">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87b26-148">schema</span><span class="sxs-lookup"><span data-stu-id="87b26-148">schema</span></span></td>
<td><span data-ttu-id="87b26-149">Público.</span><span class="sxs-lookup"><span data-stu-id="87b26-149">Public.</span></span> <span data-ttu-id="87b26-150">Opcional.</span><span class="sxs-lookup"><span data-stu-id="87b26-150">Optional.</span></span> <span data-ttu-id="87b26-151">O esquema onde a propriedade é definida.</span><span class="sxs-lookup"><span data-stu-id="87b26-151">The schema where the property is defined.</span></span></td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="87b26-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="87b26-152">Remarks</span></span>

<span data-ttu-id="87b26-153">Os conectores de pesquisa do OpenSearch podem usar a propriedade OpenSearchHTMLRolloverTemplate.</span><span class="sxs-lookup"><span data-stu-id="87b26-153">OpenSearch search connectors can use the OpenSearchHTMLRolloverTemplate property.</span></span> <span data-ttu-id="87b26-154">Essa propriedade identifica um modelo que é formatado após a Convenção do modelo OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="87b26-154">This property identifies a template that is formatted following the OpenSearch template convention.</span></span> <span data-ttu-id="87b26-155">O modelo OpenSearchHTMLRolloverTemplate é usado quando o usuário clica no botão "Pesquisar no site" na barra de comandos.</span><span class="sxs-lookup"><span data-stu-id="87b26-155">The OpenSearchHTMLRolloverTemplate template is used when the user clicks on the "Search on website" button in the command bar.</span></span>

## <a name="example"></a><span data-ttu-id="87b26-156">Exemplo</span><span class="sxs-lookup"><span data-stu-id="87b26-156">Example</span></span>

<span data-ttu-id="87b26-157">O exemplo a seguir mostra um <propertyStore> elemento com dois <property> elementos.</span><span class="sxs-lookup"><span data-stu-id="87b26-157">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



