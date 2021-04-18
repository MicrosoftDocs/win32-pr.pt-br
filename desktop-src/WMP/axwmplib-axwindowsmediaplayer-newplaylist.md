---
title: Método AxWindowsMediaPlayer. newPlaylist
description: O método newPlaylist retorna uma interface IWMPPlaylist para uma nova lista de reprodução.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- método newPlaylist Windows Media Player
- método newPlaylist Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, método newPlaylist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760467"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a><span data-ttu-id="f19db-106">Método AxWindowsMediaPlayer. newPlaylist</span><span class="sxs-lookup"><span data-stu-id="f19db-106">AxWindowsMediaPlayer.newPlaylist method</span></span>

<span data-ttu-id="f19db-107">O método newPlaylist retorna uma interface IWMPPlaylist para uma nova lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f19db-107">The newPlaylist method returns an IWMPPlaylist interface for a new playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="f19db-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f19db-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a><span data-ttu-id="f19db-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f19db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f19db-110">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="f19db-110">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="f19db-111">O **System. String** que é o nome da nova lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f19db-111">The **System.String** that is the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="f19db-112">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="f19db-112">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="f19db-113">O **System. String** que é a URL da playlist do metarquivo do Windows Media que é usada para inicializar a nova lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f19db-113">The **System.String** that is the URL of the Windows Media metafile playlist that is used to initialize the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f19db-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f19db-114">Return value</span></span>

<span data-ttu-id="f19db-115">Uma interface WMPLib. IWMPPlaylist que representa a lista de reprodução recém-criada.</span><span class="sxs-lookup"><span data-stu-id="f19db-115">A WMPLib.IWMPPlaylist interface that represents the newly created playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="f19db-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f19db-116">Remarks</span></span>

<span data-ttu-id="f19db-117">Se o parâmetro *bstrURL* for uma cadeia de caracteres nula ou de comprimento zero (""), esse método criará uma **lista de reprodução** vazia.</span><span class="sxs-lookup"><span data-stu-id="f19db-117">If the *bstrURL* parameter is a null or zero-length string (""), this method creates an empty **playlist**.</span></span> <span data-ttu-id="f19db-118">Se o parâmetro *bstrname* for uma cadeia de caracteres de comprimento zero (""), esse método aplicará o nome do metarquivo atual.</span><span class="sxs-lookup"><span data-stu-id="f19db-118">If the *bstrName* parameter is a zero-length string (""), this method applies the current metafile name.</span></span>

<span data-ttu-id="f19db-119">A nova lista de reprodução criada com esse método não é adicionada à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f19db-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="f19db-120">Para adicionar uma nova lista de reprodução à biblioteca, use IWMPPlaylistCollection. **importPlaylist** ou IWMPPlaylistCollection. **newPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="f19db-120">To add a new playlist to the library, use IWMPPlaylistCollection.**importPlaylist** or IWMPPlaylistCollection.**newPlaylist**.</span></span> <span data-ttu-id="f19db-121">Os espaços à esquerda ou à direita no nome da playlist são removidos automaticamente quando adicionados à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f19db-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="f19db-122">Como a biblioteca permite várias listas de reprodução com o mesmo nome, talvez você queira verificar a presença de uma lista de reprodução com um nome específico antes de adicionar uma nova.</span><span class="sxs-lookup"><span data-stu-id="f19db-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="f19db-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f19db-123">Requirements</span></span>



| <span data-ttu-id="f19db-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f19db-124">Requirement</span></span> | <span data-ttu-id="f19db-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f19db-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f19db-126">Versão</span><span class="sxs-lookup"><span data-stu-id="f19db-126">Version</span></span><br/>   | <span data-ttu-id="f19db-127">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f19db-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f19db-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="f19db-128">Namespace</span></span><br/> | <span data-ttu-id="f19db-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f19db-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f19db-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="f19db-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f19db-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f19db-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f19db-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f19db-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f19db-133">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f19db-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f19db-134">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f19db-134">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f19db-135">**IWMPPlaylistCollection. importPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f19db-135">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f19db-136">**IWMPPlaylistCollection. newPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f19db-136">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





