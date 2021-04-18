---
title: Propriedade AxWindowsMediaPlayer. openState
description: A propriedade OpenState Obtém um valor de enumeração que indica o estado da fonte de conteúdo.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- Propriedade OpenState Windows Media Player
- Propriedade OpenState Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade openState
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784914"
---
# <a name="axwindowsmediaplayeropenstate-property"></a><span data-ttu-id="74007-106">Propriedade AxWindowsMediaPlayer. openState</span><span class="sxs-lookup"><span data-stu-id="74007-106">AxWindowsMediaPlayer.openState property</span></span>

<span data-ttu-id="74007-107">A propriedade OpenState Obtém um valor de enumeração que indica o estado da fonte de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="74007-107">The openState property gets an enumeration value indicating the state of the content source.</span></span>

<span data-ttu-id="74007-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="74007-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="74007-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74007-109">Syntax</span></span>


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a><span data-ttu-id="74007-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="74007-110">Property value</span></span>

<span data-ttu-id="74007-111">O valor de enumeração WMPLib. WMPOpenState.</span><span class="sxs-lookup"><span data-stu-id="74007-111">The WMPLib.WMPOpenState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74007-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="74007-112">Remarks</span></span>

<span data-ttu-id="74007-113">Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="74007-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="74007-114">Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos.</span><span class="sxs-lookup"><span data-stu-id="74007-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="74007-115">Você não deve escrever código que dependa da ordem de estado.</span><span class="sxs-lookup"><span data-stu-id="74007-115">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="74007-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74007-116">Requirements</span></span>



| <span data-ttu-id="74007-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="74007-117">Requirement</span></span> | <span data-ttu-id="74007-118">Valor</span><span class="sxs-lookup"><span data-stu-id="74007-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74007-119">Versão</span><span class="sxs-lookup"><span data-stu-id="74007-119">Version</span></span><br/>   | <span data-ttu-id="74007-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="74007-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="74007-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="74007-121">Namespace</span></span><br/> | <span data-ttu-id="74007-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="74007-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="74007-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="74007-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="74007-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="74007-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74007-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="74007-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74007-126">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="74007-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="74007-127">**Evento AxWindowsMediaPlayer. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="74007-127">**AxWindowsMediaPlayer.OpenStateChange Event**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="74007-128">**WMPLib.WMPOpenState**</span><span class="sxs-lookup"><span data-stu-id="74007-128">**WMPLib.WMPOpenState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





