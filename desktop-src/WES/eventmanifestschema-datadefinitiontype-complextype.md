---
title: Tipo complexo datadefinitiontype
description: Define um item de dados que você deseja incluir com o evento. | Tipo complexo datadefinitiontype
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- Log de eventos de tipo complexo datadefinitiontype
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19584c28a7bdf7ae01b87d1f414b9464b7b4271d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781482"
---
# <a name="datadefinitiontype-complex-type"></a><span data-ttu-id="b00ee-105">Tipo complexo datadefinitiontype</span><span class="sxs-lookup"><span data-stu-id="b00ee-105">DataDefinitionType Complex Type</span></span>

<span data-ttu-id="b00ee-106">Define um item de dados que você deseja incluir com o evento.</span><span class="sxs-lookup"><span data-stu-id="b00ee-106">Defines a data item that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="DataDefinitionType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="inType"
                type="QName"
                use="required"
             />
            <xs:attribute name="outType"
                type="QName"
                use="optional"
             />
            <xs:attribute name="map"
                type="string"
                use="optional"
             />
            <xs:attribute name="length"
                type="LengthType"
                use="optional"
             />
            <xs:attribute name="count"
                type="CountType"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="b00ee-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="b00ee-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b00ee-108">Nome</span><span class="sxs-lookup"><span data-stu-id="b00ee-108">Name</span></span></th>
<th><span data-ttu-id="b00ee-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b00ee-109">Type</span></span></th>
<th><span data-ttu-id="b00ee-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b00ee-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b00ee-111">count</span><span class="sxs-lookup"><span data-stu-id="b00ee-111">count</span></span></td>
<td><span data-ttu-id="b00ee-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>Número de contagem</strong></a></span><span class="sxs-lookup"><span data-stu-id="b00ee-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></span></span></td>
<td><span data-ttu-id="b00ee-113">O número de elementos na matriz se o item de dados for uma matriz.</span><span class="sxs-lookup"><span data-stu-id="b00ee-113">The number of elements in the array if the data item is an array.</span></span> <span data-ttu-id="b00ee-114">Você pode especificar a contagem real ou o nome de outro item de dados que contém a contagem.</span><span class="sxs-lookup"><span data-stu-id="b00ee-114">You can specify the actual count or the name of another data item that contains the count.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b00ee-115">intipo</span><span class="sxs-lookup"><span data-stu-id="b00ee-115">inType</span></span></td>
<td><span data-ttu-id="b00ee-116"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="b00ee-116"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="b00ee-117">O tipo de dados para este item de dados.</span><span class="sxs-lookup"><span data-stu-id="b00ee-117">The data type for this data item.</span></span> <span data-ttu-id="b00ee-118">Para obter uma lista de tipos de dados de entrada predefinidos, consulte o tipo complexo <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b00ee-118">For a list of predefined input data types, see the <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b00ee-119">comprimento</span><span class="sxs-lookup"><span data-stu-id="b00ee-119">length</span></span></td>
<td><span data-ttu-id="b00ee-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>Comprimentotype</strong></a></span><span class="sxs-lookup"><span data-stu-id="b00ee-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></span></span></td>
<td><span data-ttu-id="b00ee-121">O comprimento de um item de dados de comprimento variável, como um blob binário.</span><span class="sxs-lookup"><span data-stu-id="b00ee-121">The length of a variable length data item, such as a binary blob.</span></span> <span data-ttu-id="b00ee-122">Para dados binários, especifique o comprimento em bytes e para dados de cadeia de caracteres, especifique o comprimento em caracteres.</span><span class="sxs-lookup"><span data-stu-id="b00ee-122">For binary data, specify the length in bytes and for string data, specify the length in characters.</span></span> <span data-ttu-id="b00ee-123">Você pode especificar o comprimento real ou o nome de outro item de dados que contém o comprimento.</span><span class="sxs-lookup"><span data-stu-id="b00ee-123">You can specify the actual length or the name of another data item that contains the length.</span></span><br/> <span data-ttu-id="b00ee-124">Se você usar o atributo Length para especificar uma cadeia de caracteres de comprimento fixo, será necessário preencher a cadeia de caracteres para seu comprimento fixo, permitindo o caractere de terminador nulo no final (por exemplo, se o comprimento for 5, a cadeia de caracteres &quot; ABC &quot; deverá ser preenchida como &quot; ABC &quot; .</span><span class="sxs-lookup"><span data-stu-id="b00ee-124">If you use the length attribute to specify a fixed length string, you must pad the string to its fixed length allowing for the null-terminator character at the end (for example, if the length is 5, the string &quot;abc&quot; must be padded as &quot;abc &quot;.</span></span> <span data-ttu-id="b00ee-125">O comprimento da cadeia de caracteres deve incluir o caractere de terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="b00ee-125">The string length must include the null-terminator character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b00ee-126">mapa</span><span class="sxs-lookup"><span data-stu-id="b00ee-126">map</span></span></td>
<td><span data-ttu-id="b00ee-127">string</span><span class="sxs-lookup"><span data-stu-id="b00ee-127">string</span></span></td>
<td><span data-ttu-id="b00ee-128">O nome do mapa de nome/valor a ser usado para mapear valores inteiros para cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b00ee-128">The name of the name/value map to use to map integer values to strings.</span></span> <span data-ttu-id="b00ee-129">O tipo de dados do item de dados deve ser de um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="b00ee-129">The data type of the data item must be of one of the following types:</span></span><br/>
<ul>
<li><span data-ttu-id="b00ee-130">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="b00ee-130">win:UInt8</span></span></li>
<li><span data-ttu-id="b00ee-131">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="b00ee-131">win:UInt16</span></span></li>
<li><span data-ttu-id="b00ee-132">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="b00ee-132">win:UInt32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b00ee-133">name</span><span class="sxs-lookup"><span data-stu-id="b00ee-133">name</span></span></td>
<td><span data-ttu-id="b00ee-134">string</span><span class="sxs-lookup"><span data-stu-id="b00ee-134">string</span></span></td>
<td><span data-ttu-id="b00ee-135">O nome do item de dados.</span><span class="sxs-lookup"><span data-stu-id="b00ee-135">The name of the data item.</span></span> <span data-ttu-id="b00ee-136">Você pode usar o nome para fazer referência a este item de dados no fragmento XML se especificar uma seção <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> em seu modelo.</span><span class="sxs-lookup"><span data-stu-id="b00ee-136">You can use the name to reference this data item in your XML fragment if you specify a <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> section in your template.</span></span> <span data-ttu-id="b00ee-137">Você também pode referenciar esse nome em um atributo Length ou Count de outro item de dados se esse item de dados contiver seu comprimento ou valor de contagem.</span><span class="sxs-lookup"><span data-stu-id="b00ee-137">You can also reference this name in a length or count attribute of another data item if this data item contains its length or count value.</span></span><br/> <span data-ttu-id="b00ee-138"><strong>Windows Vista:</strong> Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="b00ee-138"><strong>Windows Vista:</strong> This attribute is optional.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b00ee-139">outtipo</span><span class="sxs-lookup"><span data-stu-id="b00ee-139">outType</span></span></td>
<td><span data-ttu-id="b00ee-140"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="b00ee-140"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="b00ee-141">O tipo de dados a ser usado ao renderizar este item de dados.</span><span class="sxs-lookup"><span data-stu-id="b00ee-141">The data type to use when rendering this data item.</span></span> <span data-ttu-id="b00ee-142">Para obter uma lista de tipos de dados de saída predefinidos, consulte o tipo de <a href="eventmanifestschema-outputtype-complextype.md"><strong>saída</strong></a> complexo.</span><span class="sxs-lookup"><span data-stu-id="b00ee-142">For a list of predefined output data types, see the <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> complex type.</span></span><br/> <span data-ttu-id="b00ee-143"><strong>Windows Vista:</strong> O tipo de saída é ignorado e o serviço determina o tipo com base no tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="b00ee-143"><strong>Windows Vista:</strong> The output type is ignored, and the service determines the type based on the input type.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="b00ee-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="b00ee-144">Remarks</span></span>

<span data-ttu-id="b00ee-145">Para tipos de entrada de comprimento variável, como blobs binários, você deve usar o atributo Length para especificar explicitamente o tamanho dos dados.</span><span class="sxs-lookup"><span data-stu-id="b00ee-145">For variable length input types, such as binary blobs, you must use the length attribute to explicitly specify the size of the data.</span></span> <span data-ttu-id="b00ee-146">Para cadeias de caracteres, especifique o atributo Length somente se as cadeias de caracteres tiverem um comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="b00ee-146">For strings, specify the length attribute only if the strings are of a fixed length.</span></span>

## <a name="examples"></a><span data-ttu-id="b00ee-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b00ee-147">Examples</span></span>

<span data-ttu-id="b00ee-148">Veja a seguir alguns exemplos das definições de item de dados.</span><span class="sxs-lookup"><span data-stu-id="b00ee-148">The following are a few examples of the data item definitions.</span></span>


```XML
<!-- The data item is an 8-bit integer -->
<data name="binaryChar" inType="win:UInt8">
 
<!-- The data item is a single ANSI character -->
<data name="ansiChar" inType="win:UInt8" outtype="xs:string">
 
<!-- The data item is a single Unicode character -->
<data name="unicodeChar" inType="win:UInt16" outtype="xs:string">
 
<!-- The data item is an IP address that is rendered as a dot separated list of interger values -->
<data name="ipAddress" inType="win:UInt32" outtype="win:IPv4">
 
<!-- The data item is a Boolean value -->
<data name="success" inType="win:boolean">
 
<!-- The data item is a null-terminated ANSI string -->
<data name="string" inType="win:AnsiString"> 

<!-- The data item is a fixed length ANSI string -->
<data name="string" inType="win:AnsiString" length="42"> 
 
<!-- The data item is a fixed length array of null-terminated ANSI strings -->
<data name="strings" inType="win:AnsiString" count="20">
 
<!-- The data item is a fixed length array of fixed length ANSI strings -->
<data name="strings" inType="win:AnsiString" length="42" count="20">
 
<!-- The data item is a variable length array of same sized ANSI strings -->
<data name="stringLength" inType="win:UInt16">
<data name="arrayCount" inType="win:Uint16">
<data name="strings" inType="win:AnsiString" length="stringLength" count="arrayCount"> 
 
<!-- For binary data, you must specify the size.
<!-- The data item is a fixed length array of fixed length binary blobs -->
<data name="blobs" inType="win:Binary" length="42" count="20">

<!-- The data item is a fixed length binary blob -->
<data name="blob" inType="win:Binary" length="42">

<!-- The following are illegal binary data definitions -->
<!-- This definition is illegal because no length is specified -->
<data name="blob" inType="win:Binary"> 
 
<!-- This definition is illegal because you cannot determine the length of each binary blob -->
<data name="blob" inType="win:Binary" count="20"> 
 
<!-- The data item is a variable length array of structures. Each structure -->
<!-- contains an array of same sized ANSI strings --> 
<data name="arrayStructCount" inType="win:UInt16">
<struct name="countedStrings" count="arrayStructCount">
      <data name="stringLength" inType="win:UInt16">
      <data name="string" inType="win:AnsiString" length="stringLength">
</struct>
 
<!-- The data item is a time stamp that is rendered in 100ns units -->
<data name="timestamp" inType="win:UInt32" outType="win:ETWTIME">

<!-- The data item is a fixed length array of integers --> 
<data name="integers" inType="win:UInt32" count="20">

<!-- The data item is a variable length array of integers -->
<data name="arrayCount" inType="win:UInt16"> 
<data name="integers" inType="win:UInt32" count="arrayCount"> 

<!-- The following is illegal because you cannot assign a length value to a data type of a known size -->
<data name="integer" inType="win:UInt32" length="42">
```



## <a name="requirements"></a><span data-ttu-id="b00ee-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b00ee-149">Requirements</span></span>



| <span data-ttu-id="b00ee-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="b00ee-150">Requirement</span></span> | <span data-ttu-id="b00ee-151">Valor</span><span class="sxs-lookup"><span data-stu-id="b00ee-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b00ee-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b00ee-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b00ee-153">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b00ee-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b00ee-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b00ee-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b00ee-155">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b00ee-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





