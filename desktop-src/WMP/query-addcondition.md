---
title: Método Query. addcondition
description: O método addcondition adiciona uma condição ao objeto de consulta usando a lógica AND.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- método addcondition do Windows Media Player
- método addcondition Windows Media Player, classe de consulta
- Classe de consulta Windows Media Player, método addcondition
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793271"
---
# <a name="queryaddcondition-method"></a><span data-ttu-id="be95a-106">Método Query. addcondition</span><span class="sxs-lookup"><span data-stu-id="be95a-106">Query.addCondition method</span></span>

<span data-ttu-id="be95a-107">O método **addcondition** adiciona uma condição ao objeto de **consulta** usando a lógica and.</span><span class="sxs-lookup"><span data-stu-id="be95a-107">The **addCondition** method adds a condition to the **Query** object using AND logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="be95a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be95a-108">Syntax</span></span>


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="be95a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be95a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be95a-110">*atributo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be95a-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be95a-111">**Cadeia de caracteres** que contém o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="be95a-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="be95a-112">*operador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be95a-112">*operator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be95a-113">**Cadeia de caracteres** que contém o operador.</span><span class="sxs-lookup"><span data-stu-id="be95a-113">**String** containing the operator.</span></span> <span data-ttu-id="be95a-114">Consulte comentários para obter os valores com suporte.</span><span class="sxs-lookup"><span data-stu-id="be95a-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="be95a-115">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="be95a-115">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be95a-116">**Cadeia de caracteres** que contém o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="be95a-116">**String** containing the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be95a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be95a-117">Return value</span></span>

<span data-ttu-id="be95a-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="be95a-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be95a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="be95a-119">Remarks</span></span>

<span data-ttu-id="be95a-120">Consultas compostas usando a **consulta** não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="be95a-120">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="be95a-121">Uma lista de valores para o parâmetro de *atributo* pode ser encontrada na seção [referência de atributo alfabética](alphabetical-attribute-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="be95a-121">A list of values for the *attribute* parameter can be found in the [Alphabetical Attribute Reference](alphabetical-attribute-reference.md) section.</span></span>

<span data-ttu-id="be95a-122">As condições contidas em um objeto de **consulta** são organizadas em grupos de condição.</span><span class="sxs-lookup"><span data-stu-id="be95a-122">Conditions contained in a **Query** object are organized into condition groups.</span></span> <span data-ttu-id="be95a-123">Várias condições dentro de um grupo de condições sempre são concatenadas usando AND Logic.</span><span class="sxs-lookup"><span data-stu-id="be95a-123">Multiple conditions within a condition group are always concatenated using AND logic.</span></span> <span data-ttu-id="be95a-124">Os grupos de condição sempre são concatenados entre si usando ou lógica.</span><span class="sxs-lookup"><span data-stu-id="be95a-124">Condition groups are always concatenated to each other using OR logic.</span></span> <span data-ttu-id="be95a-125">Para iniciar um novo grupo de condição, chame **Query. beginNextGroup**.</span><span class="sxs-lookup"><span data-stu-id="be95a-125">To start a new condition group, call **Query.beginNextGroup**.</span></span>

<span data-ttu-id="be95a-126">A tabela a seguir lista os valores com suporte para o *operador*.</span><span class="sxs-lookup"><span data-stu-id="be95a-126">The following table lists the supported values for *operator*.</span></span>



| <span data-ttu-id="be95a-127">Operador</span><span class="sxs-lookup"><span data-stu-id="be95a-127">Operator</span></span>            | <span data-ttu-id="be95a-128">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="be95a-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="be95a-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="be95a-129">BeginsWith</span></span>          | <span data-ttu-id="be95a-130">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="be95a-130">Strings</span></span>        |
| <span data-ttu-id="be95a-131">Contém</span><span class="sxs-lookup"><span data-stu-id="be95a-131">Contains</span></span>            | <span data-ttu-id="be95a-132">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="be95a-132">Strings</span></span>        |
| <span data-ttu-id="be95a-133">É igual a</span><span class="sxs-lookup"><span data-stu-id="be95a-133">Equals</span></span>              | <span data-ttu-id="be95a-134">Todos os tipos</span><span class="sxs-lookup"><span data-stu-id="be95a-134">All types</span></span>      |
| <span data-ttu-id="be95a-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="be95a-135">GreaterThan</span></span>         | <span data-ttu-id="be95a-136">Números, datas</span><span class="sxs-lookup"><span data-stu-id="be95a-136">Numbers, Dates</span></span> |
| <span data-ttu-id="be95a-137">GreaterThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="be95a-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="be95a-138">Números, datas</span><span class="sxs-lookup"><span data-stu-id="be95a-138">Numbers, Dates</span></span> |
| <span data-ttu-id="be95a-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="be95a-139">LessThan</span></span>            | <span data-ttu-id="be95a-140">Números, datas</span><span class="sxs-lookup"><span data-stu-id="be95a-140">Numbers, Dates</span></span> |
| <span data-ttu-id="be95a-141">LessThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="be95a-141">LessThanOrEquals</span></span>    | <span data-ttu-id="be95a-142">Números, datas</span><span class="sxs-lookup"><span data-stu-id="be95a-142">Numbers, Dates</span></span> |
| <span data-ttu-id="be95a-143">NotBeginsWith</span><span class="sxs-lookup"><span data-stu-id="be95a-143">NotBeginsWith</span></span>       | <span data-ttu-id="be95a-144">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="be95a-144">Strings</span></span>        |
| <span data-ttu-id="be95a-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="be95a-145">NotContains</span></span>         | <span data-ttu-id="be95a-146">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="be95a-146">Strings</span></span>        |
| <span data-ttu-id="be95a-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="be95a-147">NotEquals</span></span>           | <span data-ttu-id="be95a-148">Todos os tipos</span><span class="sxs-lookup"><span data-stu-id="be95a-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="be95a-149">Exemplos</span><span class="sxs-lookup"><span data-stu-id="be95a-149">Examples</span></span>

<span data-ttu-id="be95a-150">O exemplo de JScript a seguir usa **Query. addcondition** e **Query. beginNextGroup** para executar uma consulta de exemplo.</span><span class="sxs-lookup"><span data-stu-id="be95a-150">The following JScript example uses **Query.addCondition** and **Query.beginNextGroup** to perform an example query.</span></span>


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a><span data-ttu-id="be95a-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be95a-151">Requirements</span></span>



| <span data-ttu-id="be95a-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="be95a-152">Requirement</span></span> | <span data-ttu-id="be95a-153">Valor</span><span class="sxs-lookup"><span data-stu-id="be95a-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be95a-154">Versão</span><span class="sxs-lookup"><span data-stu-id="be95a-154">Version</span></span><br/> | <span data-ttu-id="be95a-155">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="be95a-155">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="be95a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="be95a-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="be95a-157"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be95a-157"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be95a-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="be95a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be95a-159">**Mediacollection. createQuery**</span><span class="sxs-lookup"><span data-stu-id="be95a-159">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="be95a-160">**Mediacollection. getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="be95a-160">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="be95a-161">**Mediacollection. getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="be95a-161">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="be95a-162">**Objeto de consulta**</span><span class="sxs-lookup"><span data-stu-id="be95a-162">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="be95a-163">**Query. beginNextGroup**</span><span class="sxs-lookup"><span data-stu-id="be95a-163">**Query.beginNextGroup**</span></span>](query-beginnextgroup.md)
</dt> </dl>

 

 





