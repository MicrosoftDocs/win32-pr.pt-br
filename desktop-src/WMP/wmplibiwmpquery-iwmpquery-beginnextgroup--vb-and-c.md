---
title: Método IWMPQuery beginNextGroup
description: O método beginNextGroup inicia um novo grupo de condição. | Método IWMPQuery beginNextGroup
ms.assetid: 15d20c9f-2ce7-4a86-9054-b7317ebe1a0a
keywords:
- método beginNextGroup Windows Media Player
- método beginNextGroup Windows Media Player, interface IWMPQuery
- Interface IWMPQuery Windows Media Player, método beginNextGroup
topic_type:
- apiref
api_name:
- IWMPQuery.beginNextGroup
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866727f821fb40b6bf09f3ee2cf0231c4ffc3005
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812000"
---
# <a name="iwmpquerybeginnextgroup-method"></a><span data-ttu-id="d2de6-107">Método IWMPQuery:: beginNextGroup</span><span class="sxs-lookup"><span data-stu-id="d2de6-107">IWMPQuery::beginNextGroup method</span></span>

<span data-ttu-id="d2de6-108">O método **beginNextGroup** inicia um novo grupo de condição.</span><span class="sxs-lookup"><span data-stu-id="d2de6-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2de6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2de6-109">Syntax</span></span>


```CSharp
public void beginNextGroup();
```


```VB

Public Sub beginNextGroup()
Implements IWMPQuery.beginNextGroup
```





## <a name="parameters"></a><span data-ttu-id="d2de6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2de6-110">Parameters</span></span>

<span data-ttu-id="d2de6-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d2de6-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2de6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2de6-112">Return value</span></span>

<span data-ttu-id="d2de6-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d2de6-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2de6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2de6-114">Remarks</span></span>

<span data-ttu-id="d2de6-115">Iniciar um novo grupo de condição implica que você concluiu o grupo de condições atual.</span><span class="sxs-lookup"><span data-stu-id="d2de6-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="d2de6-116">O novo grupo de condição sempre é concatenado ao grupo de condições anterior usando **ou** lógica.</span><span class="sxs-lookup"><span data-stu-id="d2de6-116">The new condition group is always concatenated to the previous condition group by using **OR** logic.</span></span>

## <a name="examples"></a><span data-ttu-id="d2de6-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d2de6-117">Examples</span></span>

<span data-ttu-id="d2de6-118">O exemplo a seguir cria uma consulta complexa, combinando dois grupos que contêm uma condição.</span><span class="sxs-lookup"><span data-stu-id="d2de6-118">The following example creates a complex query by combing two groups that each contain a condition.</span></span> <span data-ttu-id="d2de6-119">Os resultados da consulta são extraídos como uma coleção de cadeia de caracteres e exibidos em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="d2de6-119">The results of the query are extracted as a string collection and displayed in a list box.</span></span> <span data-ttu-id="d2de6-120">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="d2de6-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");

// Begin another Query group.
q.beginNextGroup();

// Add a condition to the new group understanding that it will be combined with the
// first group using OR logic.
q.addCondition("Title", "Contains", "Capriol");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    complexQueryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

' Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi")

' Begin another Query group.
q.beginNextGroup()

' Add a condition to the new group understanding that it will be combined with the
' first group using OR logic.
q.addCondition("Title", "Contains", "Capriol")

' Query the media collection and get a string collection containing the result.
' In this case, the string collection will contain the titles of all audio items that
' match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery("Title", q, "audio", "", False)

' Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    complexQueryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="d2de6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2de6-121">Requirements</span></span>



| <span data-ttu-id="d2de6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2de6-122">Requirement</span></span> | <span data-ttu-id="d2de6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d2de6-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2de6-124">Versão</span><span class="sxs-lookup"><span data-stu-id="d2de6-124">Version</span></span><br/>   | <span data-ttu-id="d2de6-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="d2de6-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="d2de6-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2de6-126">Namespace</span></span><br/> | <span data-ttu-id="d2de6-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d2de6-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d2de6-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="d2de6-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d2de6-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d2de6-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2de6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2de6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2de6-131">**IWMPMediaCollection2. createQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d2de6-131">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d2de6-132">**IWMPMediaCollection2. getPlaylistByQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d2de6-132">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d2de6-133">**IWMPMediaCollection2. getStringCollectionByQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d2de6-133">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d2de6-134">**Interface IWMPQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d2de6-134">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





