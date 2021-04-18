---
title: Propriedade IWMPClosedCaption captioningId
description: A propriedade IWMPClosedCaption Obtém ou define o nome do elemento HTML que exibe a legenda.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- Propriedade captioningId Windows Media Player
- Propriedade captioningId Windows Media Player, interface IWMPClosedCaption
- Interface IWMPClosedCaption Windows Media Player, Propriedade captioningId
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748669"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a><span data-ttu-id="fd0bd-106">Propriedade IWMPClosedCaption:: captioningId</span><span class="sxs-lookup"><span data-stu-id="fd0bd-106">IWMPClosedCaption::captioningId property</span></span>

<span data-ttu-id="fd0bd-107">A propriedade **IWMPClosedCaption** Obtém ou define o nome do elemento HTML que exibe a legenda.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-107">The **IWMPClosedCaption** property gets or sets the name of the HTML element displaying the captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0bd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd0bd-108">Syntax</span></span>


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a><span data-ttu-id="fd0bd-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fd0bd-109">Property value</span></span>

<span data-ttu-id="fd0bd-110">O **System. String** que é a ID do elemento HTML.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-110">The **System.String** that is the ID of the HTML element.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd0bd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd0bd-111">Remarks</span></span>

<span data-ttu-id="fd0bd-112">O nome do elemento especificado pode ser qualquer elemento HTML na página da Web, contanto que dê suporte ao atributo **InnerHtml** .</span><span class="sxs-lookup"><span data-stu-id="fd0bd-112">The element name specified can be any HTML element in the webpage as long as it supports the **innerHTML** attribute.</span></span> <span data-ttu-id="fd0bd-113">Se a página da Web contiver vários quadros, o nome do elemento só poderá fazer referência a um elemento no mesmo quadro que o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-113">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Windows Media Player control.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd0bd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd0bd-114">Requirements</span></span>



| <span data-ttu-id="fd0bd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd0bd-115">Requirement</span></span> | <span data-ttu-id="fd0bd-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fd0bd-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0bd-117">Versão</span><span class="sxs-lookup"><span data-stu-id="fd0bd-117">Version</span></span><br/>   | <span data-ttu-id="fd0bd-118">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="fd0bd-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fd0bd-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd0bd-119">Namespace</span></span><br/> | <span data-ttu-id="fd0bd-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fd0bd-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fd0bd-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="fd0bd-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fd0bd-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fd0bd-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd0bd-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd0bd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0bd-124">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="fd0bd-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="fd0bd-125">**Interface IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fd0bd-125">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fd0bd-126">**Interface IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fd0bd-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





