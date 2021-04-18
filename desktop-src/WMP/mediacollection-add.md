---
title: Método mediacollection. Add
description: O método add adiciona um novo item de mídia ou lista de reprodução à biblioteca. | Método mediacollection. Add
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Adicionar método Windows Media Player
- Adicionar método Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, Adicionar método
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788152"
---
# <a name="mediacollectionadd-method"></a><span data-ttu-id="9eb5d-107">Método mediacollection. Add</span><span class="sxs-lookup"><span data-stu-id="9eb5d-107">MediaCollection.add method</span></span>

<span data-ttu-id="9eb5d-108">O método **Add** adiciona um novo item de mídia ou lista de reprodução à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9eb5d-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb5d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9eb5d-109">Syntax</span></span>


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a><span data-ttu-id="9eb5d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eb5d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb5d-111">*caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9eb5d-111">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb5d-112">**Cadeia de caracteres** que contém o caminho.</span><span class="sxs-lookup"><span data-stu-id="9eb5d-112">**String** containing the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb5d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9eb5d-113">Return value</span></span>

<span data-ttu-id="9eb5d-114">Esse método retorna um objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="9eb5d-114">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb5d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9eb5d-115">Remarks</span></span>

<span data-ttu-id="9eb5d-116">Esse método carrega um item de mídia existente ou uma lista de reprodução na biblioteca, dado um caminho para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="9eb5d-116">This method loads an existing media item or playlist into the library, given a path to a file.</span></span> <span data-ttu-id="9eb5d-117">Esse método não move nem altera o arquivo.</span><span class="sxs-lookup"><span data-stu-id="9eb5d-117">This method does not move or change the file.</span></span> <span data-ttu-id="9eb5d-118">Esse método falhará se um caminho local inválido for fornecido, mas os arquivos de mídia digital não serão verificados quanto à validade antes de serem adicionados à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9eb5d-118">This method fails if given an invalid local path, but digital media files are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="9eb5d-119">Esse método aceita arquivos de lista de reprodução estáticos e automáticos.</span><span class="sxs-lookup"><span data-stu-id="9eb5d-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="9eb5d-120">A *playlistcollection*. o método **importPlaylist** também pode ser usado para adicionar uma lista de reprodução estática à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9eb5d-120">The *PlaylistCollection*.**importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="9eb5d-121">Para usar esse método, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9eb5d-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="9eb5d-122">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9eb5d-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9eb5d-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9eb5d-123">Examples</span></span>

<span data-ttu-id="9eb5d-124">O exemplo do Microsoft JScript a seguir adiciona três objetos de mídia à coleção de mídia do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9eb5d-124">The following Microsoft JScript example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="9eb5d-125">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9eb5d-125">The **Player** object was created with ID="Player".</span></span>


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a><span data-ttu-id="9eb5d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eb5d-126">Requirements</span></span>



| <span data-ttu-id="9eb5d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb5d-127">Requirement</span></span> | <span data-ttu-id="9eb5d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9eb5d-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb5d-129">Versão</span><span class="sxs-lookup"><span data-stu-id="9eb5d-129">Version</span></span><br/> | <span data-ttu-id="9eb5d-130">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9eb5d-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9eb5d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9eb5d-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="9eb5d-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb5d-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eb5d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="9eb5d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb5d-134">**Gerenciando listas de reprodução**</span><span class="sxs-lookup"><span data-stu-id="9eb5d-134">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="9eb5d-135">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="9eb5d-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="9eb5d-136">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="9eb5d-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="9eb5d-137">**Mediacollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="9eb5d-137">**MediaCollection.remove**</span></span>](mediacollection-remove.md)
</dt> <dt>

[<span data-ttu-id="9eb5d-138">**Playlistcollection. importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="9eb5d-138">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="9eb5d-139">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="9eb5d-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="9eb5d-140">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="9eb5d-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





