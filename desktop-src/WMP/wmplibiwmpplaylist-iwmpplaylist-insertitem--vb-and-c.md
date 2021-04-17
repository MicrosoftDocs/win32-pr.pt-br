---
title: Método IWMPPlaylist insertItem
description: O método insertItem insere um item de mídia em um local especificado em uma lista de reprodução.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- método insertItem Windows Media Player
- método insertItem Windows Media Player, interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player, método insertItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ef167a5f3931f34d4cd6fb91b3d044affb9484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797951"
---
# <a name="iwmpplaylistinsertitem-method"></a><span data-ttu-id="98b43-106">Método IWMPPlaylist:: insertItem</span><span class="sxs-lookup"><span data-stu-id="98b43-106">IWMPPlaylist::insertItem method</span></span>

<span data-ttu-id="98b43-107">O método **insertItem** insere um item de mídia em um local especificado em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="98b43-107">The **insertItem** method inserts a media item at a specified location in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b43-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98b43-108">Syntax</span></span>


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a><span data-ttu-id="98b43-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98b43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98b43-110">*Lindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98b43-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98b43-111">Um **System. Int32** que é o índice de base zero no qual o item de mídia será inserido na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="98b43-111">A **System.Int32** that is the zero-based index at which the media item will be inserted in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="98b43-112">*pIWMPMedia* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="98b43-112">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98b43-113">Uma interface **WMPLib. IWMPMedia** que representa o item de mídia a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="98b43-113">A **WMPLib.IWMPMedia** interface that represents the media item to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98b43-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98b43-114">Return value</span></span>

<span data-ttu-id="98b43-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="98b43-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98b43-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="98b43-116">Remarks</span></span>

<span data-ttu-id="98b43-117">Todos os itens de mídia após o item inserido terão seus índices aumentados em um.</span><span class="sxs-lookup"><span data-stu-id="98b43-117">All media items after the inserted item will have their indexes increased by one.</span></span>

<span data-ttu-id="98b43-118">Antes de chamar esse método, você deve ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="98b43-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="98b43-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="98b43-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98b43-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98b43-120">Requirements</span></span>



| <span data-ttu-id="98b43-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="98b43-121">Requirement</span></span> | <span data-ttu-id="98b43-122">Valor</span><span class="sxs-lookup"><span data-stu-id="98b43-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98b43-123">Versão</span><span class="sxs-lookup"><span data-stu-id="98b43-123">Version</span></span><br/>   | <span data-ttu-id="98b43-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="98b43-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="98b43-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="98b43-125">Namespace</span></span><br/> | <span data-ttu-id="98b43-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="98b43-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="98b43-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="98b43-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="98b43-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="98b43-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98b43-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="98b43-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b43-130">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="98b43-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98b43-131">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="98b43-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98b43-132">**IWMPPlaylist. removeItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="98b43-132">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





