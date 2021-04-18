---
title: Método removeItem IWMPPlaylist
description: O método removeItem remove o item de mídia especificado da lista de reprodução.
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- método removeItem Windows Media Player
- método removeItem Windows Media Player, interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player, método removeItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec845b7657e04f17c47119dd169032ebe5815786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786240"
---
# <a name="iwmpplaylistremoveitem-method"></a><span data-ttu-id="9b418-106">Método IWMPPlaylist:: removeItem</span><span class="sxs-lookup"><span data-stu-id="9b418-106">IWMPPlaylist::removeItem method</span></span>

<span data-ttu-id="9b418-107">O método **RemoveItem** remove o item de mídia especificado da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="9b418-107">The **removeItem** method removes the specified media item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b418-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b418-108">Syntax</span></span>


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a><span data-ttu-id="9b418-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b418-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b418-110">*pIWMPMedia* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b418-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b418-111">Uma interface **WMPLib. IWMPMedia** que representa o item de mídia a ser removido da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="9b418-111">A **WMPLib.IWMPMedia** interface that represents the media item to remove from the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b418-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b418-112">Return value</span></span>

<span data-ttu-id="9b418-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9b418-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b418-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b418-114">Remarks</span></span>

<span data-ttu-id="9b418-115">Se o item removido for o roteiro em execução no momento, a reprodução será interrompida e o próximo item na playlist se tornará o atual.</span><span class="sxs-lookup"><span data-stu-id="9b418-115">If the item removed is the currently playing track, playback stops and the next item in the playlist becomes the current one.</span></span>

<span data-ttu-id="9b418-116">Se não houver nenhum item seguinte, o item anterior será usado.</span><span class="sxs-lookup"><span data-stu-id="9b418-116">If there is no next item, the previous item is used.</span></span> <span data-ttu-id="9b418-117">Se não houver nenhum outro item, a propriedade **AxWindowsMediaPlayer. currentMedia** retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9b418-117">If there are no other items, then the **AxWindowsMediaPlayer.currentMedia** property will return **NULL**.</span></span>

<span data-ttu-id="9b418-118">Antes de chamar esse método, você deve ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9b418-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="9b418-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9b418-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b418-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b418-120">Requirements</span></span>



| <span data-ttu-id="9b418-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b418-121">Requirement</span></span> | <span data-ttu-id="9b418-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9b418-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b418-123">Versão</span><span class="sxs-lookup"><span data-stu-id="9b418-123">Version</span></span><br/>   | <span data-ttu-id="9b418-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="9b418-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9b418-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b418-125">Namespace</span></span><br/> | <span data-ttu-id="9b418-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9b418-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9b418-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="9b418-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9b418-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9b418-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b418-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b418-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b418-130">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9b418-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b418-131">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9b418-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b418-132">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9b418-132">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b418-133">**IWMPPlaylist. insertItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9b418-133">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b418-134">**IWMPPlaylist. Item (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9b418-134">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b418-135">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9b418-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b418-136">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9b418-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





