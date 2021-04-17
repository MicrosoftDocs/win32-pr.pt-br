---
title: Método IWMPPlaylistCollection getAll
description: O método getAll retorna uma interface IWMPPlaylistArray que fornece acesso a todas as listas de reprodução na biblioteca.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- método getAll Windows Media Player
- método getAll Windows Media Player, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection Windows Media Player, método getAll
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4260f5c960650cf6c04a1dd8b39d887f711fb8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762436"
---
# <a name="iwmpplaylistcollectiongetall-method"></a><span data-ttu-id="c27d5-106">Método IWMPPlaylistCollection:: getAll</span><span class="sxs-lookup"><span data-stu-id="c27d5-106">IWMPPlaylistCollection::getAll method</span></span>

<span data-ttu-id="c27d5-107">O método **getAll** retorna uma interface **IWMPPlaylistArray** que fornece acesso a todas as listas de reprodução na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c27d5-107">The **getAll** method returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="c27d5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c27d5-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="c27d5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c27d5-109">Parameters</span></span>

<span data-ttu-id="c27d5-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c27d5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c27d5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c27d5-111">Return value</span></span>

<span data-ttu-id="c27d5-112">Uma interface **WMPLib. IWMPPlaylistArray** para a matriz de listas de reprodução recuperada.</span><span class="sxs-lookup"><span data-stu-id="c27d5-112">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="c27d5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c27d5-113">Remarks</span></span>

<span data-ttu-id="c27d5-114">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c27d5-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="c27d5-115">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c27d5-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c27d5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c27d5-116">Requirements</span></span>



| <span data-ttu-id="c27d5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c27d5-117">Requirement</span></span> | <span data-ttu-id="c27d5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c27d5-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c27d5-119">Versão</span><span class="sxs-lookup"><span data-stu-id="c27d5-119">Version</span></span><br/>   | <span data-ttu-id="c27d5-120">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c27d5-120">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="c27d5-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="c27d5-121">Namespace</span></span><br/> | <span data-ttu-id="c27d5-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c27d5-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c27d5-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="c27d5-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c27d5-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c27d5-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c27d5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c27d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c27d5-126">**Interface IWMPPlaylistArray (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c27d5-126">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c27d5-127">**Interface IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c27d5-127">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





