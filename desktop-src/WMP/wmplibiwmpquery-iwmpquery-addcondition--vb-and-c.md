---
title: Método addcondition IWMPQuery
description: O método addcondition adiciona uma condição à consulta composta usando AND Logic.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- método addcondition do Windows Media Player
- método addcondition Windows Media Player, interface IWMPQuery
- Interface IWMPQuery Windows Media Player, método addcondition
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764170"
---
# <a name="iwmpqueryaddcondition-method"></a><span data-ttu-id="ebd89-106">Método IWMPQuery:: addcondition</span><span class="sxs-lookup"><span data-stu-id="ebd89-106">IWMPQuery::addCondition method</span></span>

<span data-ttu-id="ebd89-107">O método **addcondition** adiciona uma condição à consulta composta usando **and** Logic.</span><span class="sxs-lookup"><span data-stu-id="ebd89-107">The **addCondition** method adds a condition to the compound query using **AND** logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd89-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ebd89-108">Syntax</span></span>


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a><span data-ttu-id="ebd89-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebd89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd89-110">*bstrattribute* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ebd89-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd89-111">Um **System. String** que é o nome do atributo a ser adicionado à consulta.</span><span class="sxs-lookup"><span data-stu-id="ebd89-111">A **System.String** that is the name of the attribute to be added to the query.</span></span>

</dd> <dt>

<span data-ttu-id="ebd89-112">*bstrOperator* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ebd89-112">*bstrOperator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd89-113">Um **System. String** que é o operador.</span><span class="sxs-lookup"><span data-stu-id="ebd89-113">A **System.String** that is the operator.</span></span> <span data-ttu-id="ebd89-114">Consulte comentários para obter os valores com suporte.</span><span class="sxs-lookup"><span data-stu-id="ebd89-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="ebd89-115">*bstrvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ebd89-115">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd89-116">Um **System. String** que é o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="ebd89-116">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebd89-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebd89-117">Return value</span></span>

<span data-ttu-id="ebd89-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ebd89-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebd89-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebd89-119">Remarks</span></span>

<span data-ttu-id="ebd89-120">As condições contidas em uma consulta composta são organizadas em grupos de condição.</span><span class="sxs-lookup"><span data-stu-id="ebd89-120">Conditions contained in a compound query are organized into condition groups.</span></span> <span data-ttu-id="ebd89-121">Várias condições dentro de um grupo de condição são sempre concatenadas usando **and** lógica.</span><span class="sxs-lookup"><span data-stu-id="ebd89-121">Multiple conditions within a condition group are always concatenated by using **AND** logic.</span></span> <span data-ttu-id="ebd89-122">Os grupos de condição sempre são concatenados entre si usando **ou** lógica.</span><span class="sxs-lookup"><span data-stu-id="ebd89-122">Condition groups are always concatenated to each other by using **OR** logic.</span></span> <span data-ttu-id="ebd89-123">Para iniciar um novo grupo de condição, chame [IWMPQuery. beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="ebd89-123">To start a new condition group, call [IWMPQuery.beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span></span>

<span data-ttu-id="ebd89-124">As consultas compostas usando **IWMPQuery** não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ebd89-124">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="ebd89-125">Uma lista de valores para o parâmetro *bstrattribute* pode ser encontrada em [referência de atributo alfabética](alphabetical-attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ebd89-125">A list of values for the *bstrAttribute* parameter can be found in [Alphabetical Attribute Reference](alphabetical-attribute-reference.md).</span></span>

<span data-ttu-id="ebd89-126">A tabela a seguir lista os valores com suporte para *bstrOperator*.</span><span class="sxs-lookup"><span data-stu-id="ebd89-126">The following table lists the supported values for *bstrOperator*.</span></span>



| <span data-ttu-id="ebd89-127">String</span><span class="sxs-lookup"><span data-stu-id="ebd89-127">String</span></span>              | <span data-ttu-id="ebd89-128">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="ebd89-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="ebd89-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="ebd89-129">BeginsWith</span></span>          | <span data-ttu-id="ebd89-130">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="ebd89-130">Strings</span></span>        |
| <span data-ttu-id="ebd89-131">Contém</span><span class="sxs-lookup"><span data-stu-id="ebd89-131">Contains</span></span>            | <span data-ttu-id="ebd89-132">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="ebd89-132">Strings</span></span>        |
| <span data-ttu-id="ebd89-133">É igual a</span><span class="sxs-lookup"><span data-stu-id="ebd89-133">Equals</span></span>              | <span data-ttu-id="ebd89-134">Todos os tipos</span><span class="sxs-lookup"><span data-stu-id="ebd89-134">All types</span></span>      |
| <span data-ttu-id="ebd89-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="ebd89-135">GreaterThan</span></span>         | <span data-ttu-id="ebd89-136">Números, datas</span><span class="sxs-lookup"><span data-stu-id="ebd89-136">Numbers, Dates</span></span> |
| <span data-ttu-id="ebd89-137">GreaterThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="ebd89-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="ebd89-138">Números, datas</span><span class="sxs-lookup"><span data-stu-id="ebd89-138">Numbers, Dates</span></span> |
| <span data-ttu-id="ebd89-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="ebd89-139">LessThan</span></span>            | <span data-ttu-id="ebd89-140">Números, datas</span><span class="sxs-lookup"><span data-stu-id="ebd89-140">Numbers, Dates</span></span> |
| <span data-ttu-id="ebd89-141">LessThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="ebd89-141">LessThanOrEquals</span></span>    | <span data-ttu-id="ebd89-142">Números, datas</span><span class="sxs-lookup"><span data-stu-id="ebd89-142">Numbers, Dates</span></span> |
| <span data-ttu-id="ebd89-143">NotBeginsWith</span><span class="sxs-lookup"><span data-stu-id="ebd89-143">NotBeginsWith</span></span>       | <span data-ttu-id="ebd89-144">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="ebd89-144">Strings</span></span>        |
| <span data-ttu-id="ebd89-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="ebd89-145">NotContains</span></span>         | <span data-ttu-id="ebd89-146">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="ebd89-146">Strings</span></span>        |
| <span data-ttu-id="ebd89-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="ebd89-147">NotEquals</span></span>           | <span data-ttu-id="ebd89-148">Todos os tipos</span><span class="sxs-lookup"><span data-stu-id="ebd89-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="ebd89-149">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ebd89-149">Examples</span></span>

<span data-ttu-id="ebd89-150">O exemplo a seguir cria uma consulta, adiciona duas condições a ela e usa essa consulta para extrair os resultados da consulta como uma coleção de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ebd89-150">The following example creates a query, adds two conditions to it, and uses that query to extract the results of the query as a string collection.</span></span> <span data-ttu-id="ebd89-151">Os resultados são exibidos em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="ebd89-151">The results are then displayed in a list box.</span></span> <span data-ttu-id="ebd89-152">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="ebd89-152">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="ebd89-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebd89-153">Requirements</span></span>



| <span data-ttu-id="ebd89-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebd89-154">Requirement</span></span> | <span data-ttu-id="ebd89-155">Valor</span><span class="sxs-lookup"><span data-stu-id="ebd89-155">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd89-156">Versão</span><span class="sxs-lookup"><span data-stu-id="ebd89-156">Version</span></span><br/>   | <span data-ttu-id="ebd89-157">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ebd89-157">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="ebd89-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebd89-158">Namespace</span></span><br/> | <span data-ttu-id="ebd89-159">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ebd89-159">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ebd89-160">Assembly</span><span class="sxs-lookup"><span data-stu-id="ebd89-160">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ebd89-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ebd89-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd89-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebd89-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd89-163">**Referência de atributo alfabético**</span><span class="sxs-lookup"><span data-stu-id="ebd89-163">**Alphabetical Attribute Reference**</span></span>](alphabetical-attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="ebd89-164">**IWMPMediaCollection2. createQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ebd89-164">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ebd89-165">**IWMPMediaCollection2. getPlaylistByQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ebd89-165">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ebd89-166">**IWMPMediaCollection2. getStringCollectionByQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ebd89-166">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ebd89-167">**Interface IWMPQuery**</span><span class="sxs-lookup"><span data-stu-id="ebd89-167">**IWMPQuery Interface**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





