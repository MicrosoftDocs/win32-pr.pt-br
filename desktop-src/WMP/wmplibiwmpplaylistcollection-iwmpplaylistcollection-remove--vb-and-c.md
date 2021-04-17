---
title: Método de remoção de IWMPPlaylistCollection
description: O método remove remove uma lista de reprodução da biblioteca. | Método de remoção de IWMPPlaylistCollection
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- remover método Windows Media Player
- método de remoção do Windows Media Player, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection Windows Media Player, remover método
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99fbaa2f60c769599bd6173b8e38f4d99e9f42d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812291"
---
# <a name="iwmpplaylistcollectionremove-method"></a><span data-ttu-id="23c8e-107">Método IWMPPlaylistCollection:: Remove</span><span class="sxs-lookup"><span data-stu-id="23c8e-107">IWMPPlaylistCollection::remove method</span></span>

<span data-ttu-id="23c8e-108">O método **Remove** remove uma lista de reprodução da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="23c8e-108">The **remove** method removes a playlist from the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="23c8e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23c8e-109">Syntax</span></span>


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="23c8e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23c8e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23c8e-111">*pItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23c8e-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23c8e-112">Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução que será removida por este método.</span><span class="sxs-lookup"><span data-stu-id="23c8e-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23c8e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23c8e-113">Return value</span></span>

<span data-ttu-id="23c8e-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="23c8e-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23c8e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="23c8e-115">Remarks</span></span>

<span data-ttu-id="23c8e-116">Antes de chamar esse método, você deve ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="23c8e-116">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="23c8e-117">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="23c8e-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="23c8e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23c8e-118">Requirements</span></span>



| <span data-ttu-id="23c8e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="23c8e-119">Requirement</span></span> | <span data-ttu-id="23c8e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="23c8e-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23c8e-121">Versão</span><span class="sxs-lookup"><span data-stu-id="23c8e-121">Version</span></span><br/>   | <span data-ttu-id="23c8e-122">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="23c8e-122">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="23c8e-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="23c8e-123">Namespace</span></span><br/> | <span data-ttu-id="23c8e-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="23c8e-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="23c8e-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="23c8e-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="23c8e-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="23c8e-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23c8e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="23c8e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c8e-128">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="23c8e-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="23c8e-129">**Interface IWMPPlaylistCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="23c8e-129">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





