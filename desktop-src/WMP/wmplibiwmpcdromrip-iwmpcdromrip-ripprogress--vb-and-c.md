---
title: Propriedade IWMPCdromRip ripProgress
description: A propriedade ripProgress Obtém o andamento da cópia de CD como porcentagem concluída.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- Propriedade ripProgress Windows Media Player
- Propriedade ripProgress Windows Media Player, interface IWMPCdromRip
- Interface IWMPCdromRip Windows Media Player, Propriedade ripProgress
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812292"
---
# <a name="iwmpcdromripripprogress-property"></a><span data-ttu-id="65442-106">Propriedade IWMPCdromRip:: ripProgress</span><span class="sxs-lookup"><span data-stu-id="65442-106">IWMPCdromRip::ripProgress property</span></span>

<span data-ttu-id="65442-107">A propriedade **ripProgress** Obtém o andamento da cópia de CD como porcentagem concluída.</span><span class="sxs-lookup"><span data-stu-id="65442-107">The **ripProgress** property gets the CD ripping progress as percent complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="65442-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="65442-108">Syntax</span></span>


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="65442-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="65442-109">Property value</span></span>

<span data-ttu-id="65442-110">Um **System. Int32** que é o valor de progresso.</span><span class="sxs-lookup"><span data-stu-id="65442-110">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="65442-111">Os valores de progresso variam de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="65442-111">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="65442-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="65442-112">Remarks</span></span>

<span data-ttu-id="65442-113">O valor de progresso representa a porcentagem completa de todo o processo de cópia de CDs.</span><span class="sxs-lookup"><span data-stu-id="65442-113">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="65442-114">Para determinar o progresso de uma faixa específica, use [IWMPMedia. getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) com **RipProgress** como o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="65442-114">To determine the progress of a specific track, use [IWMPMedia.getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) with **RipProgress** as the attribute name.</span></span> <span data-ttu-id="65442-115">Para obter o índice da faixa que está sendo copiada no momento, chame IWMPPlaylist. getItemInfo com "CurrentRipTrackIndex" como o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="65442-115">To get the index of the track currently being ripped, call IWMPPlaylist.getItemInfo with "CurrentRipTrackIndex" as the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="65442-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65442-116">Requirements</span></span>



| <span data-ttu-id="65442-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="65442-117">Requirement</span></span> | <span data-ttu-id="65442-118">Valor</span><span class="sxs-lookup"><span data-stu-id="65442-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65442-119">Versão</span><span class="sxs-lookup"><span data-stu-id="65442-119">Version</span></span><br/>   | <span data-ttu-id="65442-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="65442-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="65442-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="65442-121">Namespace</span></span><br/> | <span data-ttu-id="65442-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="65442-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="65442-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="65442-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="65442-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="65442-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65442-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="65442-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65442-126">**Interface IWMPCdromRip (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="65442-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="65442-127">**Copiando um CD**</span><span class="sxs-lookup"><span data-stu-id="65442-127">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





