---
title: Propriedade AxWindowsMediaPlayer. currentMedia
description: A propriedade currentMedia Obtém ou define a interface IWMPMedia que corresponde ao item de mídia atual.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- Propriedade currentMedia Windows Media Player
- Propriedade currentMedia Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade currentMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3720a36d2a1969c652ed757f31301cf6a9ead706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813196"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a><span data-ttu-id="c3a33-106">Propriedade AxWindowsMediaPlayer. currentMedia</span><span class="sxs-lookup"><span data-stu-id="c3a33-106">AxWindowsMediaPlayer.currentMedia property</span></span>

<span data-ttu-id="c3a33-107">A propriedade currentMedia Obtém ou define a interface IWMPMedia que corresponde ao item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="c3a33-107">The currentMedia property gets or sets the IWMPMedia interface that corresponds to the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a33-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3a33-108">Syntax</span></span>


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="c3a33-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c3a33-109">Property value</span></span>

<span data-ttu-id="c3a33-110">A interface WMPLib. IWMPMedia que fornece acesso ao item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="c3a33-110">The WMPLib.IWMPMedia interface that provides access to the current media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a33-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3a33-111">Remarks</span></span>

<span data-ttu-id="c3a33-112">Se AxWindowsMediaPlayer. Settings. a propriedade **AutoStart** é true, a reprodução é iniciada automaticamente sempre que você definir **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="c3a33-112">If the AxWindowsMediaPlayer.settings.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="c3a33-113">Você pode recuperar uma interface IWMPMedia para um determinado item de mídia por meio da propriedade IWMPPlaylist. Item (o método IWMPPlaylist. get \_ item em C#).</span><span class="sxs-lookup"><span data-stu-id="c3a33-113">You can retrieve an IWMPMedia interface for a given media item through the IWMPPlaylist.Item property (the IWMPPlaylist.get\_Item method in C#).</span></span> <span data-ttu-id="c3a33-114">Para carregar um item de mídia usando um nome de arquivo, defina a propriedade URL ou use newMedia.</span><span class="sxs-lookup"><span data-stu-id="c3a33-114">To load a media item using a file name, set the URL property or use newMedia.</span></span>

## <a name="examples"></a><span data-ttu-id="c3a33-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c3a33-115">Examples</span></span>

<span data-ttu-id="c3a33-116">O exemplo a seguir recupera o primeiro item de mídia na biblioteca e usa a propriedade currentMedia para definir o item de mídia recuperado como o item de mídia atual e exibir seu nome.</span><span class="sxs-lookup"><span data-stu-id="c3a33-116">The following example retrieves the first media item in the library and uses the currentMedia property to set the retrieved media item as the current media item and display its name.</span></span> <span data-ttu-id="c3a33-117">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="c3a33-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
```





## <a name="requirements"></a><span data-ttu-id="c3a33-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3a33-118">Requirements</span></span>



| <span data-ttu-id="c3a33-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3a33-119">Requirement</span></span> | <span data-ttu-id="c3a33-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c3a33-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a33-121">Versão</span><span class="sxs-lookup"><span data-stu-id="c3a33-121">Version</span></span><br/>   | <span data-ttu-id="c3a33-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="c3a33-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c3a33-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3a33-123">Namespace</span></span><br/> | <span data-ttu-id="c3a33-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c3a33-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c3a33-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="c3a33-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c3a33-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c3a33-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3a33-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3a33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a33-128">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3a33-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3a33-129">**AxWindowsMediaPlayer. newMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3a33-129">**AxWindowsMediaPlayer.newMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[<span data-ttu-id="c3a33-130">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3a33-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3a33-131">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3a33-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3a33-132">**IWMPPlaylist. Item (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3a33-132">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3a33-133">**IWMPSettings. AutoStart (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3a33-133">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





