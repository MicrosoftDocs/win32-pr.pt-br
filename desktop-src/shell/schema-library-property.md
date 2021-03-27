---
description: O <property> elemento Especifica uma propriedade usada pela biblioteca. Essas propriedades são específicas para a biblioteca, portanto, não há nenhum conjunto predefinido de nomes de propriedade a ser usado. Esse elemento é opcional e não tem nenhum elemento filho.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Elemento Property (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b269e8914cf1f5da92d96e1922f7347a161daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988754"
---
# <a name="property-element-library-schema"></a><span data-ttu-id="0eedb-105">Elemento Property (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="0eedb-105">property Element (Library Schema)</span></span>

<span data-ttu-id="0eedb-106">O <property> elemento Especifica uma propriedade usada pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0eedb-106">The <property> element specifies a property used by the library.</span></span> <span data-ttu-id="0eedb-107">Essas propriedades são específicas para a biblioteca, portanto, não há nenhum conjunto predefinido de nomes de propriedade a ser usado.</span><span class="sxs-lookup"><span data-stu-id="0eedb-107">These properties are specific to the library, so there is no predefined set of property names to use.</span></span> <span data-ttu-id="0eedb-108">Esse elemento é opcional e não tem nenhum elemento filho.</span><span class="sxs-lookup"><span data-stu-id="0eedb-108">This element is optional and has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eedb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0eedb-109">Syntax</span></span>

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="0eedb-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0eedb-110">Element Information</span></span>



| <span data-ttu-id="0eedb-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="0eedb-111">Parent Element</span></span>                                                             | <span data-ttu-id="0eedb-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0eedb-112">Child Elements</span></span> |
|----------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="0eedb-113">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="0eedb-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) | <span data-ttu-id="0eedb-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0eedb-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="0eedb-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="0eedb-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0eedb-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="0eedb-116">Attribute</span></span></th>
<th><span data-ttu-id="0eedb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0eedb-117">Description</span></span></th>
<th><span data-ttu-id="0eedb-118">Valores</span><span class="sxs-lookup"><span data-stu-id="0eedb-118">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0eedb-119">name</span><span class="sxs-lookup"><span data-stu-id="0eedb-119">name</span></span></td>
<td><span data-ttu-id="0eedb-120">Público.</span><span class="sxs-lookup"><span data-stu-id="0eedb-120">Public.</span></span> <span data-ttu-id="0eedb-121">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0eedb-121">Required.</span></span> <span data-ttu-id="0eedb-122">O nome para exibição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="0eedb-122">The display name of the property.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="0eedb-123">tipo</span><span class="sxs-lookup"><span data-stu-id="0eedb-123">type</span></span></td>
<td><span data-ttu-id="0eedb-124">Público.</span><span class="sxs-lookup"><span data-stu-id="0eedb-124">Public.</span></span> <span data-ttu-id="0eedb-125">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0eedb-125">Required.</span></span> <span data-ttu-id="0eedb-126">O tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0eedb-126">The type of property.</span></span></td>
<td><ul>
<li><span data-ttu-id="0eedb-127">Any: padrão.</span><span class="sxs-lookup"><span data-stu-id="0eedb-127">Any: Default.</span></span> <span data-ttu-id="0eedb-128">O valor não será forçado pelo subsistema de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0eedb-128">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="0eedb-129">VT_NULL será retornado por getpropertytype.</span><span class="sxs-lookup"><span data-stu-id="0eedb-129">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="0eedb-130">NULL: não há nenhum valor para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0eedb-130">Null: There is no value for this property.</span></span> <span data-ttu-id="0eedb-131">VT_NULL será retornado por getpropertytype.</span><span class="sxs-lookup"><span data-stu-id="0eedb-131">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="0eedb-132">Cadeia de caracteres: o valor deve ser um VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="0eedb-132">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="0eedb-133">Booliano: o valor deve ser um VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="0eedb-133">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="0eedb-134">Byte: o valor deve ser um VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="0eedb-134">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="0eedb-135">Buffer: o valor deve ser um VT_UI1 | Buffer de VT_VECTOR de bytes.</span><span class="sxs-lookup"><span data-stu-id="0eedb-135">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="0eedb-136">Int16: o valor deve ser um VT_I2.</span><span class="sxs-lookup"><span data-stu-id="0eedb-136">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="0eedb-137">UInt16: o valor deve ser um VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="0eedb-137">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="0eedb-138">Int32: o valor deve ser um VT_I4.</span><span class="sxs-lookup"><span data-stu-id="0eedb-138">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="0eedb-139">UInt32: o valor deve ser um VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="0eedb-139">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="0eedb-140">Int64: o valor deve ser um VT_I8.</span><span class="sxs-lookup"><span data-stu-id="0eedb-140">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="0eedb-141">UInt64: o valor deve ser um VT_UI8.</span><span class="sxs-lookup"><span data-stu-id="0eedb-141">UInt64: The value must be a VT_UI8.</span></span></li>
<li><span data-ttu-id="0eedb-142">Double: o valor deve ser um VT_R8.</span><span class="sxs-lookup"><span data-stu-id="0eedb-142">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="0eedb-143">DateTime: o valor deve ser um VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="0eedb-143">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="0eedb-144">GUID: o valor deve ser um VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="0eedb-144">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="0eedb-145">Blob: o valor deve ser um VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="0eedb-145">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="0eedb-146">Objeto: o valor deve ser um VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="0eedb-146">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="0eedb-147">Stream: o valor deve ser um VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="0eedb-147">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="0eedb-148">Área de transferência: o valor deve ser um VT_CF.</span><span class="sxs-lookup"><span data-stu-id="0eedb-148">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="0eedb-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="0eedb-149">Remarks</span></span>

<span data-ttu-id="0eedb-150">Os requisitos para o elemento de> de nome canônico <correspondem aos requisitos do Windows Search e do sistema de propriedades do Windows.</span><span class="sxs-lookup"><span data-stu-id="0eedb-150">The requirements for the <canonical-name> element match the requirements for Windows Search and the Windows property system.</span></span> <span data-ttu-id="0eedb-151">A cadeia de caracteres deve ser do tipo canônico.</span><span class="sxs-lookup"><span data-stu-id="0eedb-151">The string must be of type canonical-type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0eedb-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0eedb-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0eedb-153">Esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="0eedb-153">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="0eedb-154">Esquemas de propriedade</span><span class="sxs-lookup"><span data-stu-id="0eedb-154">Property Schemas</span></span>](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="0eedb-155">Esquema de descrição do conector de pesquisa</span><span class="sxs-lookup"><span data-stu-id="0eedb-155">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
