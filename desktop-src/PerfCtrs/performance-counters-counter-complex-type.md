---
description: Define um contador.
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: Tipo complexo do contador
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d591d4c23b626eaf2e2bfb10b528ff7c054507df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766840"
---
# <a name="counter-complex-type"></a><span data-ttu-id="062a4-103">Tipo complexo do contador</span><span class="sxs-lookup"><span data-stu-id="062a4-103">counter Complex Type</span></span>

<span data-ttu-id="062a4-104">Define um contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-104">Defines a counter.</span></span>

``` syntax
<xs:complexType name="counter">
    <xs:choice
        minOccurs="0"
        maxOccurs="1"
    >
        <xs:element name="counterAttributes"
            type="man:counterAttributes"
        >
            <xs:key name="uniqueCounterAttributeName">
                <xs:selector
                    xpath="./man:counterAttribute"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="id"
        type="man:UInt32Type"
        use="required"
     />
    <xs:attribute name="uri"
        type="xs:anyURI"
        use="required"
     />
    <xs:attribute name="name"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:maxLength
                    value="1023"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="description"
        type="xs:string"
        use="optional"
     />
    <xs:attribute name="type"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="perf_counter_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer"
                 />
                <xs:enumeration
                    value="perf_counter_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_large_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_100ns_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_obj_time_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_bulk_count"
                 />
                <xs:enumeration
                    value="perf_counter_text"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_sample_fraction"
                 />
                <xs:enumeration
                    value="perf_sample_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer_inv"
                 />
                <xs:enumeration
                    value="perf_sample_base"
                 />
                <xs:enumeration
                    value="perf_average_timer"
                 />
                <xs:enumeration
                    value="perf_average_base"
                 />
                <xs:enumeration
                    value="perf_average_bulk"
                 />
                <xs:enumeration
                    value="perf_obj_time_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_base"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_large_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_raw_base"
                 />
                <xs:enumeration
                    value="perf_large_raw_base"
                 />
                <xs:enumeration
                    value="perf_elapsed_time"
                 />
                <xs:enumeration
                    value="perf_counter_delta"
                 />
                <xs:enumeration
                    value="perf_counter_large_delta"
                 />
                <xs:enumeration
                    value="perf_precision_system_timer"
                 />
                <xs:enumeration
                    value="perf_precision_100ns_timer"
                 />
                <xs:enumeration
                    value="perf_precision_object_timer"
                 />
                <xs:enumeration
                    value="perf_counter_composite"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="baseID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="detailLevel"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="standard"
                 />
                <xs:enumeration
                    value="advanced"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="defaultScale"
        use="optional"
        default="0"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:integer"
            >
                <xs:minInclusive
                    value="-10"
                 />
                <xs:maxInclusive
                    value="10"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="aggregate"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="sum"
                 />
                <xs:enumeration
                    value="avg"
                 />
                <xs:enumeration
                    value="max"
                 />
                <xs:enumeration
                    value="min"
                 />
                <xs:enumeration
                    value="undefined"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="perfTimeID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="perfFreqID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="multiCounterID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="struct"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="field"
        type="man:CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="062a4-105">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="062a4-105">Child elements</span></span>



| <span data-ttu-id="062a4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="062a4-106">Element</span></span>               | <span data-ttu-id="062a4-107">Type</span><span class="sxs-lookup"><span data-stu-id="062a4-107">Type</span></span>                                                                                 | <span data-ttu-id="062a4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="062a4-108">Description</span></span>                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="062a4-109">**metaatributos**</span><span class="sxs-lookup"><span data-stu-id="062a4-109">**counterAttributes**</span></span> | [<span data-ttu-id="062a4-110">**Man: metaatributos**</span><span class="sxs-lookup"><span data-stu-id="062a4-110">**man:counterAttributes**</span></span>](performance-counters-counterattributes-complex-type.md) | <span data-ttu-id="062a4-111">Lista os atributos exclusivos que especificam como os dados do contador são exibidos em um aplicativo de consumidor.</span><span class="sxs-lookup"><span data-stu-id="062a4-111">Lists the unique attributes that specify how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="062a4-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="062a4-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="062a4-113">Nome</span><span class="sxs-lookup"><span data-stu-id="062a4-113">Name</span></span></th>
<th><span data-ttu-id="062a4-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="062a4-114">Type</span></span></th>
<th><span data-ttu-id="062a4-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="062a4-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="062a4-116">aggregate</span><span class="sxs-lookup"><span data-stu-id="062a4-116">aggregate</span></span></td>

<td><span data-ttu-id="062a4-117">A função de agregação a ser aplicada se o atributo <strong>Instances</strong> de <a href="performance-counters-counterset-complex-type.md"><strong>CounterSet</strong></a> for GlobalAggregate, multipleAggregate ou globalAggregateHistory.</span><span class="sxs-lookup"><span data-stu-id="062a4-117">The aggregation function to apply if the <strong>instances</strong> attribute of <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> is globalAggregate, multipleAggregate, or globalAggregateHistory.</span></span> <span data-ttu-id="062a4-118">A seguir estão as funções de agregação possíveis que você pode aplicar:</span><span class="sxs-lookup"><span data-stu-id="062a4-118">The following are the possible aggregation functions that you can apply:</span></span><br/> <dl> <span data-ttu-id="062a4-119"><dt><span id="max"></span><span id="MAX"></span>maximizar</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-119"><dt><span id="max"></span><span id="MAX"></span>max</dt> </span></span><dd> <span data-ttu-id="062a4-120">O valor máximo do contador é retornado.</span><span class="sxs-lookup"><span data-stu-id="062a4-120">The maximum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="062a4-121"><dt><span id="min"></span><span id="MIN"></span>min</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-121"><dt><span id="min"></span><span id="MIN"></span>min</dt> </span></span><dd> <span data-ttu-id="062a4-122">O valor mínimo do contador é retornado.</span><span class="sxs-lookup"><span data-stu-id="062a4-122">The minimum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="062a4-123"><dt><span id="avg"></span><span id="AVG"></span>média</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-123"><dt><span id="avg"></span><span id="AVG"></span>avg</dt> </span></span><dd> <span data-ttu-id="062a4-124">O valor médio do contador é retornado.</span><span class="sxs-lookup"><span data-stu-id="062a4-124">The average counter value is returned.</span></span><br/> </dd> <span data-ttu-id="062a4-125"><dt><span id="sum"></span><span id="SUM"></span>quantia</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-125"><dt><span id="sum"></span><span id="SUM"></span>sum</dt> </span></span><dd> <span data-ttu-id="062a4-126">A soma dos valores do contador é retornada.</span><span class="sxs-lookup"><span data-stu-id="062a4-126">The sum of the counter values is returned.</span></span><br/> </dd> <span data-ttu-id="062a4-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>indefinido</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>undefined</dt> </span></span><dd> <span data-ttu-id="062a4-128">Não agregue este contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-128">Do not aggregate this counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062a4-129">BaseId</span><span class="sxs-lookup"><span data-stu-id="062a4-129">baseID</span></span></td>
<td><span data-ttu-id="062a4-130"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32type</strong></a></span><span class="sxs-lookup"><span data-stu-id="062a4-130"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="062a4-131">O identificador de outro contador dentro do mesmo conjunto de contadores cujo valor é usado para calcular o valor desse contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-131">The identifier of another counter within the same counter set, whose value is used to calculate this counter's value.</span></span> <span data-ttu-id="062a4-132">Os seguintes tipos de contadores exigem um contador base:</span><span class="sxs-lookup"><span data-stu-id="062a4-132">The following counter types require a base counter:</span></span><br/> <dl> <span data-ttu-id="062a4-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span></span><dd> <span data-ttu-id="062a4-134">Requer o contador base PERF_AVERAGE_BASE.</span><span class="sxs-lookup"><span data-stu-id="062a4-134">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="062a4-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span></span><dd> <span data-ttu-id="062a4-136">Requer o contador base PERF_AVERAGE_BASE.</span><span class="sxs-lookup"><span data-stu-id="062a4-136">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="062a4-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span></span><dd> <span data-ttu-id="062a4-138">Requer o contador base PERF_COUNTER_MULTI_BASE.</span><span class="sxs-lookup"><span data-stu-id="062a4-138">Requires the PERF_COUNTER_MULTI_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="062a4-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="062a4-140">Requer o contador base PERF_LARGE_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="062a4-140">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="062a4-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span></span><dd> <span data-ttu-id="062a4-142">Requer o contador base PERF_LARGE_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="062a4-142">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="062a4-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="062a4-144">Requer o contador base PERF_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="062a4-144">Requires the PERF_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="062a4-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span></span><dd> <span data-ttu-id="062a4-146">Requer o contador base PERF_SAMPLE_BASE.</span><span class="sxs-lookup"><span data-stu-id="062a4-146">Requires the PERF_SAMPLE_BASE base counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062a4-147">DefaultScale</span><span class="sxs-lookup"><span data-stu-id="062a4-147">defaultScale</span></span></td>

<td><span data-ttu-id="062a4-148">O fator de escala a ser aplicado ao valor do contador (fator \* valor do contador).</span><span class="sxs-lookup"><span data-stu-id="062a4-148">The scale factor to apply to the counter value (factor \* counter value).</span></span> <span data-ttu-id="062a4-149">O padrão será zero se nenhuma escala for aplicada.</span><span class="sxs-lookup"><span data-stu-id="062a4-149">The default is zero if no scale is applied.</span></span> <span data-ttu-id="062a4-150">Os valores válidos variam de 10 a 10 (0, 1 a 1000000000).</span><span class="sxs-lookup"><span data-stu-id="062a4-150">Valid values range from  10 to 10 (0.0000000001 to 1000000000).</span></span> <span data-ttu-id="062a4-151">Se esse valor for zero, o valor de escala será 1; Se esse valor for 1, o valor de escala será 10; Se esse valor for 1, o valor de escala será. 10; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="062a4-151">If this value is zero, the scale value is 1; if this value is 1, the scale value is 10; if this value is  1, the scale value is .10; and so on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062a4-152">descrição</span><span class="sxs-lookup"><span data-stu-id="062a4-152">description</span></span></td>
<td><span data-ttu-id="062a4-153"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="062a4-153"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="062a4-154">Uma breve descrição do contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-154">A short description of the counter.</span></span> <span data-ttu-id="062a4-155">Você não precisa especificar esse atributo se o contador incluir o atributo <a href="performance-counters-counterattribute-complex-type.md"><strong>NoDisplay</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="062a4-155">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062a4-156">detailLevel</span><span class="sxs-lookup"><span data-stu-id="062a4-156">detailLevel</span></span></td>

<td><span data-ttu-id="062a4-157">Especifica o público-alvo para os detalhes do contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-157">Specifies the target audience for the counter details.</span></span> <span data-ttu-id="062a4-158">O valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="062a4-158">The following are the possible values:</span></span><br/> <dl> <span data-ttu-id="062a4-159"><dt><span id="standard"></span><span id="STANDARD"></span>Standardization</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-159"><dt><span id="standard"></span><span id="STANDARD"></span>standard</dt> </span></span><dd> <span data-ttu-id="062a4-160">Exibir detalhes sobre o contador que um usuário típico entenderia.</span><span class="sxs-lookup"><span data-stu-id="062a4-160">Display details about the counter that a typical user would understand.</span></span><br/> </dd> <span data-ttu-id="062a4-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>avançadas</dt> </span><span class="sxs-lookup"><span data-stu-id="062a4-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>advanced</dt> </span></span><dd> <span data-ttu-id="062a4-162">Exibir detalhes sobre o contador que apenas um usuário avançado deve entender.</span><span class="sxs-lookup"><span data-stu-id="062a4-162">Display details about the counter that only an advanced user would understand.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062a4-163">field</span><span class="sxs-lookup"><span data-stu-id="062a4-163">field</span></span></td>
<td><span data-ttu-id="062a4-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>homem: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="062a4-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="062a4-165">O nome de um campo dentro da estrutura que contém o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-165">The name of a field within the struct that contains the counter value.</span></span> <span data-ttu-id="062a4-166">Esse atributo não é permitido para provedores de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="062a4-166">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062a4-167">id</span><span class="sxs-lookup"><span data-stu-id="062a4-167">id</span></span></td>
<td><span data-ttu-id="062a4-168"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32type</strong></a></span><span class="sxs-lookup"><span data-stu-id="062a4-168"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="062a4-169">Um número exclusivo que identifica o contador dentro do conjunto de contadores.</span><span class="sxs-lookup"><span data-stu-id="062a4-169">A unique number that identifies the counter within the counter set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062a4-170">multicounterid</span><span class="sxs-lookup"><span data-stu-id="062a4-170">multiCounterID</span></span></td>
<td><span data-ttu-id="062a4-171"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32type</strong></a></span><span class="sxs-lookup"><span data-stu-id="062a4-171"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="062a4-172">O identificador de outro contador dentro do mesmo conjunto de contadores, cujo valor de multiplicador é usado para calcular o valor desse contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-172">The identifier of another counter within the same counter set, whose multiplier value is used to calculate this counter's value.</span></span> <span data-ttu-id="062a4-173">Os tipos de contador a seguir exigem um valor de multiplicador.</span><span class="sxs-lookup"><span data-stu-id="062a4-173">The following counter types require a multiplier value.</span></span> <span data-ttu-id="062a4-174">O contador referenciado deve ser do tipo PERF_COUNTER_RAWCOUNT.</span><span class="sxs-lookup"><span data-stu-id="062a4-174">The referenced counter must be of type PERF_COUNTER_RAWCOUNT.</span></span><br/>
<ul>
<li><span data-ttu-id="062a4-175">PERF_COUNTER_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="062a4-175">PERF_COUNTER_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="062a4-176">PERF_COUNTER_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="062a4-176">PERF_COUNTER_MULTI_TIMER_INV</span></span></li>
<li><span data-ttu-id="062a4-177">PERF_100NSEC_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="062a4-177">PERF_100NSEC_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="062a4-178">PERF_100NSEC_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="062a4-178">PERF_100NSEC_MULTI_TIMER_INV</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062a4-179">name</span><span class="sxs-lookup"><span data-stu-id="062a4-179">name</span></span></td>

<td><span data-ttu-id="062a4-180">O nome do contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-180">The name of the counter.</span></span> <span data-ttu-id="062a4-181">O nome deve ser exclusivo e menor que 1.024 caracteres.</span><span class="sxs-lookup"><span data-stu-id="062a4-181">The name must be unique and less than 1,024 characters.</span></span> <span data-ttu-id="062a4-182">O nome diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="062a4-182">The name is case-sensitive.</span></span> <span data-ttu-id="062a4-183">Você não precisa especificar esse atributo se o contador incluir o atributo <a href="performance-counters-counterattribute-complex-type.md"><strong>NoDisplay</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="062a4-183">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062a4-184">perfFreqID</span><span class="sxs-lookup"><span data-stu-id="062a4-184">perfFreqID</span></span></td>
<td><span data-ttu-id="062a4-185"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32type</strong></a></span><span class="sxs-lookup"><span data-stu-id="062a4-185"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="062a4-186">O identificador de outro contador dentro do mesmo conjunto de contadores, cujo valor de Frequency é usado para calcular o valor desse contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-186">The identifier of another counter within the same counter set, whose frequency value is used to calculate this counter's value.</span></span> <span data-ttu-id="062a4-187">Os tipos de contador a seguir exigem uma frequência.</span><span class="sxs-lookup"><span data-stu-id="062a4-187">The following counter types require a frequency.</span></span> <span data-ttu-id="062a4-188">O tipo de contador de PERF_COUNTER_LARGE_RAWCOUNT contém o valor de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="062a4-188">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="062a4-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="062a4-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="062a4-190">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="062a4-190">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="062a4-191">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="062a4-191">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="062a4-192">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="062a4-192">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062a4-193">perfTimeID</span><span class="sxs-lookup"><span data-stu-id="062a4-193">perfTimeID</span></span></td>
<td><span data-ttu-id="062a4-194"><a href="performance-counters-uint32type-simple-type.md"><strong>Man: UInt32type</strong></a></span><span class="sxs-lookup"><span data-stu-id="062a4-194"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="062a4-195">O identificador de outro contador dentro do mesmo conjunto de contadores, cujo valor de carimbo de data/hora é usado para calcular o valor desse contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-195">The identifier of another counter within the same counter set, whose time stamp value is used to calculate this counter's value.</span></span> <span data-ttu-id="062a4-196">Os tipos de contador a seguir exigem um carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="062a4-196">The following counter types require a time stamp.</span></span> <span data-ttu-id="062a4-197">O tipo de contador de PERF_COUNTER_LARGE_RAWCOUNT contém o valor de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="062a4-197">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="062a4-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="062a4-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="062a4-199">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="062a4-199">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="062a4-200">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="062a4-200">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="062a4-201">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="062a4-201">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062a4-202">struct</span><span class="sxs-lookup"><span data-stu-id="062a4-202">struct</span></span></td>
<td><span data-ttu-id="062a4-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>homem: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="062a4-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="062a4-204">O nome de um elemento de struct que contém esse valor de contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-204">The name of a struct element that contains this counter value.</span></span> <span data-ttu-id="062a4-205">Esse atributo não é permitido para provedores de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="062a4-205">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062a4-206">símbolo</span><span class="sxs-lookup"><span data-stu-id="062a4-206">symbol</span></span></td>
<td><span data-ttu-id="062a4-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>homem: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="062a4-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="062a4-208">Um nome simbólico que identifica o contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-208">A symbolic name that identifies the counter.</span></span> <span data-ttu-id="062a4-209">A ferramenta <a href="ctrpp.md">ctrpp</a> cria uma constante que você pode usar ao chamar funções que exigem um identificador de contador (por exemplo, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="062a4-209">The <a href="ctrpp.md">CTRPP</a> tool creates a constant that you can use when calling functions that require a counter identifier (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>).</span></span> <span data-ttu-id="062a4-210">O nome da constante é o nome simbólico.</span><span class="sxs-lookup"><span data-stu-id="062a4-210">The name of the constant is the symbolic name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="062a4-211">tipo</span><span class="sxs-lookup"><span data-stu-id="062a4-211">type</span></span></td>

<td><span data-ttu-id="062a4-212">O nome do tipo de contador.</span><span class="sxs-lookup"><span data-stu-id="062a4-212">The name of the counter type.</span></span> <span data-ttu-id="062a4-213">Para obter os valores possíveis, consulte o bloco de sintaxe acima.</span><span class="sxs-lookup"><span data-stu-id="062a4-213">For possible values, see the above syntax block.</span></span> <span data-ttu-id="062a4-214">Para obter detalhes de cada tipo, consulte <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">tipos de contadores</a> no guia de implantação do Windows 2003.</span><span class="sxs-lookup"><span data-stu-id="062a4-214">For details of each type, see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Counter Types</a> in the Windows 2003 Deployment Guide.</span></span> <span data-ttu-id="062a4-215">O nome diferencia maiúsculas de minúsculas e usa letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="062a4-215">The name is case-sensitive use lowercase.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="062a4-216">uri</span><span class="sxs-lookup"><span data-stu-id="062a4-216">uri</span></span></td>
<td><span data-ttu-id="062a4-217"><strong>xs: anyURI</strong></span><span class="sxs-lookup"><span data-stu-id="062a4-217"><strong>xs:anyURI</strong></span></span></td>
<td><span data-ttu-id="062a4-218">Um identificador de recurso uniforme exclusivo que permite aos usuários recuperar valores de contador de qualquer local.</span><span class="sxs-lookup"><span data-stu-id="062a4-218">A unique uniform resource identifier that lets users retrieve counter values from any location.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="062a4-219">Comentários</span><span class="sxs-lookup"><span data-stu-id="062a4-219">Remarks</span></span>

<span data-ttu-id="062a4-220">Para fornecer compatibilidade com versões anteriores, cada contador no conjunto de contadores deve especificar os mesmos valores de **perfFreqID** e **perfTimeID** .</span><span class="sxs-lookup"><span data-stu-id="062a4-220">To provide backwards-compatibility, each counter in the counter set should specify the same **perfFreqID** and **perfTimeID** values.</span></span>

## <a name="requirements"></a><span data-ttu-id="062a4-221">Requisitos</span><span class="sxs-lookup"><span data-stu-id="062a4-221">Requirements</span></span>



| <span data-ttu-id="062a4-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="062a4-222">Requirement</span></span> | <span data-ttu-id="062a4-223">Valor</span><span class="sxs-lookup"><span data-stu-id="062a4-223">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="062a4-224">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="062a4-224">Minimum supported client</span></span><br/> | <span data-ttu-id="062a4-225">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="062a4-225">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="062a4-226">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="062a4-226">Minimum supported server</span></span><br/> | <span data-ttu-id="062a4-227">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="062a4-227">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

