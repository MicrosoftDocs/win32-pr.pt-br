---
title: Propriedade AxWindowsMediaPlayer. mediacollection
description: A propriedade mediacollection Obtém uma interface IWMPMediaCollection que fornece uma maneira de organizar uma grande coleção de itens de mídia.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- Propriedade mediacollection Windows Media Player
- Propriedade mediacollection Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade mediacollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6501dd5dda8e60b8ba1a5f2667f6b581cbdfd90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762101"
---
# <a name="axwindowsmediaplayermediacollection-property"></a><span data-ttu-id="b02bf-106">Propriedade AxWindowsMediaPlayer. mediacollection</span><span class="sxs-lookup"><span data-stu-id="b02bf-106">AxWindowsMediaPlayer.mediaCollection property</span></span>

<span data-ttu-id="b02bf-107">A propriedade mediacollection Obtém uma interface **IWMPMediaCollection** que fornece uma maneira de organizar uma grande coleção de itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="b02bf-107">The mediaCollection property gets an **IWMPMediaCollection** interface that provides a way to organize a large collection of media items.</span></span>

<span data-ttu-id="b02bf-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b02bf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b02bf-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b02bf-109">Syntax</span></span>


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a><span data-ttu-id="b02bf-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b02bf-110">Property value</span></span>

<span data-ttu-id="b02bf-111">A interface WMPLib. IWMPMediaCollection para uma coleção de itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="b02bf-111">The WMPLib.IWMPMediaCollection interface to a collection of media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="b02bf-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b02bf-112">Remarks</span></span>

<span data-ttu-id="b02bf-113">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b02bf-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="b02bf-114">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b02bf-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b02bf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b02bf-115">Requirements</span></span>



| <span data-ttu-id="b02bf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b02bf-116">Requirement</span></span> | <span data-ttu-id="b02bf-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b02bf-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b02bf-118">Versão</span><span class="sxs-lookup"><span data-stu-id="b02bf-118">Version</span></span><br/>   | <span data-ttu-id="b02bf-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b02bf-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b02bf-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="b02bf-120">Namespace</span></span><br/> | <span data-ttu-id="b02bf-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b02bf-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b02bf-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="b02bf-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b02bf-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b02bf-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b02bf-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b02bf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b02bf-125">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b02bf-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b02bf-126">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b02bf-126">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b02bf-127">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b02bf-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b02bf-128">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b02bf-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





