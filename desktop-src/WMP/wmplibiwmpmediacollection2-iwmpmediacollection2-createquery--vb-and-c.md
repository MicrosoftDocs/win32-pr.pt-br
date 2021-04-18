---
title: Método IWMPMediaCollection2 createQuery
description: O método createQuery retorna uma interface IWMPQuery que representa uma nova consulta.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- método createQuery Windows Media Player
- método createQuery Windows Media Player, interface IWMPMediaCollection2
- Interface IWMPMediaCollection2 Windows Media Player, método createQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318b27a20ba801e1fbed58ff79c5bed7841f8c29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781240"
---
# <a name="iwmpmediacollection2createquery-method"></a><span data-ttu-id="e9bb9-106">Método IWMPMediaCollection2:: createQuery</span><span class="sxs-lookup"><span data-stu-id="e9bb9-106">IWMPMediaCollection2::createQuery method</span></span>

<span data-ttu-id="e9bb9-107">O `createQuery` método retorna uma interface **IWMPQuery** que representa uma nova consulta.</span><span class="sxs-lookup"><span data-stu-id="e9bb9-107">The `createQuery` method returns an **IWMPQuery** interface that represents a new query.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9bb9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9bb9-108">Syntax</span></span>


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a><span data-ttu-id="e9bb9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9bb9-109">Parameters</span></span>

<span data-ttu-id="e9bb9-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e9bb9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9bb9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9bb9-111">Return value</span></span>

<span data-ttu-id="e9bb9-112">Uma interface **WMPLib. IWMPQuery** que representa uma nova consulta vazia.</span><span class="sxs-lookup"><span data-stu-id="e9bb9-112">A **WMPLib.IWMPQuery** interface that represents a new, empty query.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9bb9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9bb9-113">Remarks</span></span>

<span data-ttu-id="e9bb9-114">A criação de uma nova consulta é a primeira etapa para criar uma consulta composta.</span><span class="sxs-lookup"><span data-stu-id="e9bb9-114">Creating a new query is the first step toward creating a compound query.</span></span>

## <a name="examples"></a><span data-ttu-id="e9bb9-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e9bb9-115">Examples</span></span>

<span data-ttu-id="e9bb9-116">O exemplo a seguir usa `createQuery` para obter uma interface **IWMPQuery** que é inicializada como nula.</span><span class="sxs-lookup"><span data-stu-id="e9bb9-116">The following example uses `createQuery` to get an **IWMPQuery** interface that is initialized to null.</span></span> <span data-ttu-id="e9bb9-117">Como essa consulta não tem condições adicionadas a ela, quando ela é usada como um argumento no método **getStringCollectionByQuery** , o método retornará uma coleção de cadeias de caracteres que contém todos os itens de mídia do tipo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="e9bb9-117">Because this query has no conditions added to it, when it is used as an argument in the **getStringCollectionByQuery** method, the method will return a string collection that contains all of the media items of the specified media type.</span></span> <span data-ttu-id="e9bb9-118">A coleção de cadeia de caracteres é exibida em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="e9bb9-118">The string collection is then displayed in a list box.</span></span>


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="e9bb9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9bb9-119">Requirements</span></span>



| <span data-ttu-id="e9bb9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9bb9-120">Requirement</span></span> | <span data-ttu-id="e9bb9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e9bb9-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bb9-122">Versão</span><span class="sxs-lookup"><span data-stu-id="e9bb9-122">Version</span></span><br/>   | <span data-ttu-id="e9bb9-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="e9bb9-123">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="e9bb9-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9bb9-124">Namespace</span></span><br/> | <span data-ttu-id="e9bb9-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e9bb9-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e9bb9-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="e9bb9-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e9bb9-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e9bb9-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9bb9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9bb9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9bb9-129">**Interface IWMPMediaCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e9bb9-129">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e9bb9-130">**Interface IWMPQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e9bb9-130">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





