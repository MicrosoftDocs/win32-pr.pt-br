---
title: Propriedade AutoStart do IWMPSettings
description: A propriedade AutoStart Obtém ou define um valor que indica se o item de mídia atual começa a ser reproduzido automaticamente.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- Propriedade AutoStart do Windows Media Player
- Propriedade AutoStart do Windows Media Player, interface IWMPSettings
- Interface IWMPSettings do Windows Media Player, Propriedade AutoStart
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765359"
---
# <a name="iwmpsettingsautostart-property"></a><span data-ttu-id="b0ece-106">Propriedade IWMPSettings:: AutoStart</span><span class="sxs-lookup"><span data-stu-id="b0ece-106">IWMPSettings::autoStart property</span></span>

<span data-ttu-id="b0ece-107">A propriedade **AutoStart** Obtém ou define um valor que indica se o item de mídia atual começa a ser reproduzido automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b0ece-107">The **autoStart** property gets or sets a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0ece-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0ece-108">Syntax</span></span>


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="b0ece-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b0ece-109">Property value</span></span>

<span data-ttu-id="b0ece-110">Um valor **System. Boolean** que indica se o item de mídia atual começa a ser reproduzido automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b0ece-110">A **System.Boolean** value that indicates whether the current media item begins playing automatically.</span></span> <span data-ttu-id="b0ece-111">O padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="b0ece-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0ece-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0ece-112">Remarks</span></span>

<span data-ttu-id="b0ece-113">Se **AutoStart** for definido como **true**, o item de mídia começará a ser reproduzido quando **AxWindowsMediaPlayer. URL**, **AxWindowsMediaPlayer. currentPlaylist** ou **AxWindowsMediaPlayer. currentMedia** for definido.</span><span class="sxs-lookup"><span data-stu-id="b0ece-113">If **autoStart** is set to **true**, the media item will begin playing when **AxWindowsMediaPlayer.URL**, **AxWindowsMediaPlayer.currentPlaylist**, or **AxWindowsMediaPlayer.currentMedia** is set.</span></span> <span data-ttu-id="b0ece-114">Caso contrário, o item de mídia não começará a ser reproduzido até que o método **IWMPControls. Play** seja chamado.</span><span class="sxs-lookup"><span data-stu-id="b0ece-114">Otherwise, the media item will not start playing until the **IWMPControls.play** method is called.</span></span>

<span data-ttu-id="b0ece-115">A menos que você defina **AutoStart** como **true** imediatamente antes de especificar um item de mídia, você não deve confiar nessa configuração como um substituto para usar o método **IWMPControls. Play** .</span><span class="sxs-lookup"><span data-stu-id="b0ece-115">Unless you set **autoStart** to **true** immediately before specifying a media item, you should not rely on this setting as a substitute for using the **IWMPControls.play** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0ece-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0ece-116">Requirements</span></span>



| <span data-ttu-id="b0ece-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0ece-117">Requirement</span></span> | <span data-ttu-id="b0ece-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b0ece-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ece-119">Versão</span><span class="sxs-lookup"><span data-stu-id="b0ece-119">Version</span></span><br/>   | <span data-ttu-id="b0ece-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b0ece-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b0ece-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0ece-121">Namespace</span></span><br/> | <span data-ttu-id="b0ece-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b0ece-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b0ece-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="b0ece-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b0ece-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b0ece-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0ece-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0ece-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0ece-126">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b0ece-126">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b0ece-127">**AxWindowsMediaPlayer. currentPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b0ece-127">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b0ece-128">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b0ece-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b0ece-129">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b0ece-129">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b0ece-130">**Interface IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b0ece-130">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





