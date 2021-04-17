---
title: Propriedade IWMPClosedCaption2 SAMILangCount
description: A propriedade SAMILangCount Obtém o número de idiomas com suporte pelo arquivo SAMI atual.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Propriedade SAMILangCount Windows Media Player
- Propriedade SAMILangCount Windows Media Player, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 Windows Media Player, Propriedade SAMILangCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea01357de508dea319389cd14ab85ebafe0329e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780090"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a><span data-ttu-id="a2932-106">Propriedade IWMPClosedCaption2:: SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="a2932-106">IWMPClosedCaption2::SAMILangCount property</span></span>

<span data-ttu-id="a2932-107">A propriedade **SAMILangCount** Obtém o número de idiomas com suporte pelo arquivo Sami atual.</span><span class="sxs-lookup"><span data-stu-id="a2932-107">The **SAMILangCount** property gets the number of languages supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2932-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2932-108">Syntax</span></span>


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="a2932-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a2932-109">Property value</span></span>

<span data-ttu-id="a2932-110">Um **System. Int32** que é o número de idiomas com suporte.</span><span class="sxs-lookup"><span data-stu-id="a2932-110">A **System.Int32** that is the number of languages supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2932-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2932-111">Remarks</span></span>

<span data-ttu-id="a2932-112">Essa propriedade retorna 0, a menos que um arquivo de mídia digital esteja aberto (AxWindowsMediaPlayer. OpenState é igual a 13).</span><span class="sxs-lookup"><span data-stu-id="a2932-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2932-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2932-113">Requirements</span></span>



| <span data-ttu-id="a2932-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2932-114">Requirement</span></span> | <span data-ttu-id="a2932-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a2932-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2932-116">Versão</span><span class="sxs-lookup"><span data-stu-id="a2932-116">Version</span></span><br/>   | <span data-ttu-id="a2932-117">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="a2932-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a2932-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2932-118">Namespace</span></span><br/> | <span data-ttu-id="a2932-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a2932-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a2932-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="a2932-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a2932-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a2932-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2932-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2932-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2932-123">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="a2932-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="a2932-124">**Interface IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a2932-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a2932-125">**IWMPClosedCaption. SAMILang (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a2932-125">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a2932-126">**Interface IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a2932-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a2932-127">**IWMPClosedCaption2. getSAMILangName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a2932-127">**IWMPClosedCaption2.getSAMILangName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





