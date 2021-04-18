---
description: O <property> elemento opcional especifica as propriedades usadas pelo provedor de localização.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Elemento de Propriedade do LocalProvider (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105763941"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a><span data-ttu-id="62d78-103">Elemento de Propriedade do LocalProvider (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="62d78-103">property Element of locationProvider (Search Connector Schema)</span></span>

<span data-ttu-id="62d78-104">O <property> elemento opcional especifica as propriedades usadas pelo provedor de localização.</span><span class="sxs-lookup"><span data-stu-id="62d78-104">The optional <property> element specifies the properties used by the location provider.</span></span> <span data-ttu-id="62d78-105">Essas propriedades são específicas para esse provedor de localização, portanto, não há nenhum conjunto predefinido de nomes a ser usado.</span><span class="sxs-lookup"><span data-stu-id="62d78-105">These properties are specific to this location provider, so there is no predefined set of names to use.</span></span> <span data-ttu-id="62d78-106">O <property> elemento tem dois atributos, conforme descrito neste tópico.</span><span class="sxs-lookup"><span data-stu-id="62d78-106">The <property> element has two attributes, as described in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="62d78-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="62d78-107">Syntax</span></span>


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
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



## <a name="property-element-information"></a><span data-ttu-id="62d78-108"><property> Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="62d78-108"><property> Element Information</span></span>



| <span data-ttu-id="62d78-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="62d78-109">Parent Element</span></span>                                                                                 | <span data-ttu-id="62d78-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="62d78-110">Child Elements</span></span>                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="62d78-111">Elemento LocationProvider (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="62d78-111">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md) | <span data-ttu-id="62d78-112">, descrita neste tópico.</span><span class="sxs-lookup"><span data-stu-id="62d78-112">property, described in this topic.</span></span> |



 


## <a name="property-attributes"></a><span data-ttu-id="62d78-113"><property> Atributos</span><span class="sxs-lookup"><span data-stu-id="62d78-113"><property> Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62d78-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="62d78-114">Attribute</span></span></th>
<th><span data-ttu-id="62d78-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="62d78-115">Description</span></span></th>
<th><span data-ttu-id="62d78-116">Valores</span><span class="sxs-lookup"><span data-stu-id="62d78-116">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="62d78-117">name</span><span class="sxs-lookup"><span data-stu-id="62d78-117">name</span></span></td>
<td><span data-ttu-id="62d78-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="62d78-118">Required.</span></span> <span data-ttu-id="62d78-119">O nome para exibição da propriedade.</span><span class="sxs-lookup"><span data-stu-id="62d78-119">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="62d78-120">tipo</span><span class="sxs-lookup"><span data-stu-id="62d78-120">type</span></span></td>
<td><span data-ttu-id="62d78-121">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="62d78-121">Required.</span></span> <span data-ttu-id="62d78-122">O tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="62d78-122">The type of property.</span></span></td>
<td><span data-ttu-id="62d78-123">Any: padrão.</span><span class="sxs-lookup"><span data-stu-id="62d78-123">Any: Default.</span></span> <span data-ttu-id="62d78-124">O valor não será forçado pelo subsistema de propriedades.</span><span class="sxs-lookup"><span data-stu-id="62d78-124">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="62d78-125">VT_NULL será retornado por getpropertytype.</span><span class="sxs-lookup"><span data-stu-id="62d78-125">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="62d78-126">NULL: não há nenhum valor para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="62d78-126">Null: There is no value for this property.</span></span> <span data-ttu-id="62d78-127">VT_NULL será retornado por getpropertytype.</span><span class="sxs-lookup"><span data-stu-id="62d78-127">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="62d78-128">Cadeia de caracteres: o valor deve ser um VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="62d78-128">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="62d78-129">Booliano: o valor deve ser um VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="62d78-129">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="62d78-130">Byte: o valor deve ser um VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="62d78-130">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="62d78-131">Buffer: o valor deve ser um VT_UI1 | Buffer de VT_VECTOR de bytes.</span><span class="sxs-lookup"><span data-stu-id="62d78-131">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="62d78-132">Int16: o valor deve ser um VT_I2.</span><span class="sxs-lookup"><span data-stu-id="62d78-132">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="62d78-133">UInt16: o valor deve ser um VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="62d78-133">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="62d78-134">Int32: o valor deve ser um VT_I4.</span><span class="sxs-lookup"><span data-stu-id="62d78-134">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="62d78-135">UInt32: o valor deve ser um VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="62d78-135">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="62d78-136">Int64: o valor deve ser um VT_I8.</span><span class="sxs-lookup"><span data-stu-id="62d78-136">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="62d78-137">UInt64: o valor deve ser um VT_UI8</span><span class="sxs-lookup"><span data-stu-id="62d78-137">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="62d78-138">Double: o valor deve ser um VT_R8.</span><span class="sxs-lookup"><span data-stu-id="62d78-138">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="62d78-139">DateTime: o valor deve ser um VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="62d78-139">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="62d78-140">GUID: o valor deve ser um VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="62d78-140">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="62d78-141">Blob: o valor deve ser um VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="62d78-141">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="62d78-142">Objeto: o valor deve ser um VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="62d78-142">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="62d78-143">Stream: o valor deve ser um VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="62d78-143">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="62d78-144">Área de transferência: o valor deve ser um VT_CF.</span><span class="sxs-lookup"><span data-stu-id="62d78-144">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="62d78-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="62d78-145">Remarks</span></span>

<span data-ttu-id="62d78-146">Para o provedor de OpenSearch, as seguintes propriedades são usadas:</span><span class="sxs-lookup"><span data-stu-id="62d78-146">For the OpenSearch provider, the following properties are used:</span></span>

-   <span data-ttu-id="62d78-147">OpenSearchShortName: nome curto do serviço de pesquisa</span><span class="sxs-lookup"><span data-stu-id="62d78-147">OpenSearchShortName: Short name of the search service</span></span>
-   <span data-ttu-id="62d78-148">OpenSearchQueryTemplate: modelo, formatado após a Convenção do modelo de OpenSearch, para o serviço de consulta</span><span class="sxs-lookup"><span data-stu-id="62d78-148">OpenSearchQueryTemplate: Template, formatted following the OpenSearch template convention, for the query service</span></span>
-   <span data-ttu-id="62d78-149">MaximumResultCount: (número) número máximo de resultados retornados pelo serviço de pesquisa</span><span class="sxs-lookup"><span data-stu-id="62d78-149">MaximumResultCount: (number) Maximum number of results returned by the search service</span></span>
-   <span data-ttu-id="62d78-150">LinkIsFilePath: (booliano) se true, o provedor tentará interpretar os itens retornados como arquivos, usando suas extensões para criar o ShellItem apropriado na exibição.</span><span class="sxs-lookup"><span data-stu-id="62d78-150">LinkIsFilePath: (Boolean) If true, the provider tries to interpret returned items as files, using their extensions to create the proper ShellItem in the view.</span></span> <span data-ttu-id="62d78-151">Se for false, os itens serão tratados como atalhos de URL.</span><span class="sxs-lookup"><span data-stu-id="62d78-151">If false, items are treated as URL shortcuts.</span></span>

 

 



