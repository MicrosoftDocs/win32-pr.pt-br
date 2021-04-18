---
title: Método IWMPMediaCollection Add
description: O método add adiciona um novo item de mídia ou lista de reprodução à biblioteca. | Método IWMPMediaCollection Add
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Adicionar método Windows Media Player
- Adicionar método Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, Adicionar método
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7953067281e394df71a1a53c874cb80837a5f35d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753383"
---
# <a name="iwmpmediacollectionadd-method"></a><span data-ttu-id="3a0e7-107">Método IWMPMediaCollection:: Add</span><span class="sxs-lookup"><span data-stu-id="3a0e7-107">IWMPMediaCollection::add method</span></span>

<span data-ttu-id="3a0e7-108">O método **Add** adiciona um novo item de mídia ou lista de reprodução à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3a0e7-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a0e7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a0e7-109">Syntax</span></span>


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a><span data-ttu-id="3a0e7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a0e7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a0e7-111">*bstrURL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a0e7-111">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0e7-112">Um **System. String** que é a URL que especifica o local do item de mídia ou da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="3a0e7-112">A **System.String** that is the URL that specifies the location of the media item or playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a0e7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a0e7-113">Return value</span></span>

<span data-ttu-id="3a0e7-114">A interface **WMPLib. IWMPMedia** para o item adicionado ou a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="3a0e7-114">The **WMPLib.IWMPMedia** interface for the added item or playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a0e7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a0e7-115">Remarks</span></span>

<span data-ttu-id="3a0e7-116">Esse método carrega um item de mídia existente ou uma lista de reprodução na biblioteca, dado um caminho.</span><span class="sxs-lookup"><span data-stu-id="3a0e7-116">This method loads an existing media item or playlist into the library, given a path.</span></span> <span data-ttu-id="3a0e7-117">Esse método não move nem altera o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3a0e7-117">This method does not move or change the file.</span></span> <span data-ttu-id="3a0e7-118">Esse método falhará se um caminho local inválido for fornecido, mas os próprios itens de mídia não serão verificados quanto à validade antes de serem adicionados à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3a0e7-118">This method fails if given an invalid local path, but media items themselves are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="3a0e7-119">Esse método aceita arquivos de lista de reprodução estáticos e automáticos.</span><span class="sxs-lookup"><span data-stu-id="3a0e7-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="3a0e7-120">O método **IWMPPlaylistCollection. importPlaylist** também pode ser usado para adicionar uma lista de reprodução estática à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3a0e7-120">The **IWMPPlaylistCollection.importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="3a0e7-121">Antes de chamar esse método, você deve ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3a0e7-121">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="3a0e7-122">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3a0e7-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3a0e7-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3a0e7-123">Examples</span></span>

<span data-ttu-id="3a0e7-124">O exemplo a seguir adiciona três objetos de mídia à coleção de mídia do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3a0e7-124">The following example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="3a0e7-125">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="3a0e7-125">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
```





## <a name="requirements"></a><span data-ttu-id="3a0e7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a0e7-126">Requirements</span></span>



| <span data-ttu-id="3a0e7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a0e7-127">Requirement</span></span> | <span data-ttu-id="3a0e7-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3a0e7-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0e7-129">Versão</span><span class="sxs-lookup"><span data-stu-id="3a0e7-129">Version</span></span><br/>   | <span data-ttu-id="3a0e7-130">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="3a0e7-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3a0e7-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a0e7-131">Namespace</span></span><br/> | <span data-ttu-id="3a0e7-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3a0e7-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3a0e7-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="3a0e7-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3a0e7-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3a0e7-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a0e7-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a0e7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a0e7-136">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3a0e7-136">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a0e7-137">**IWMPMediaCollection. Remove (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3a0e7-137">**IWMPMediaCollection.remove (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a0e7-138">**IWMPPlaylistCollection. importPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3a0e7-138">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





