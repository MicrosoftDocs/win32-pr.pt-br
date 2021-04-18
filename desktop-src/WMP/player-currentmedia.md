---
title: Player. currentMedia
description: A propriedade currentMedia especifica ou recupera o objeto de mídia atual.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Player. currentMedia Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea90b7be72bcb10a8ec0d3c49116f3effceb9a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759834"
---
# <a name="playercurrentmedia"></a><span data-ttu-id="f2cc2-104">Player. currentMedia</span><span class="sxs-lookup"><span data-stu-id="f2cc2-104">Player.currentMedia</span></span>

<span data-ttu-id="f2cc2-105">A propriedade **currentMedia** especifica ou recupera o objeto de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="f2cc2-105">The **currentMedia** property specifies or retrieves the current Media object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2cc2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2cc2-106">Syntax</span></span>

<span data-ttu-id="f2cc2-107">*Player* . **currentMedia**</span><span class="sxs-lookup"><span data-stu-id="f2cc2-107">*player* .**currentMedia**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f2cc2-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="f2cc2-108">Possible Values</span></span>

<span data-ttu-id="f2cc2-109">Esta propriedade é um objeto de mídia de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f2cc2-109">This property is a read/write Media object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2cc2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2cc2-110">Remarks</span></span>

<span data-ttu-id="f2cc2-111">Se as *configurações*. a propriedade **AutoStart** é true, a reprodução é iniciada automaticamente sempre que você definir **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="f2cc2-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="f2cc2-112">Essa propriedade usa um objeto de mídia, que pode ser adquirido usando a *lista de reprodução*. **Item**.</span><span class="sxs-lookup"><span data-stu-id="f2cc2-112">This property takes a Media object, which can be acquired by using *Playlist*.**item**.</span></span> <span data-ttu-id="f2cc2-113">Para carregar um item de **mídia** usando um nome de arquivo, defina a propriedade URL ou use **newMedia**.</span><span class="sxs-lookup"><span data-stu-id="f2cc2-113">To load a **Media** item using a file name, set the URL property or use **newMedia**.</span></span>

## <a name="examples"></a><span data-ttu-id="f2cc2-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2cc2-114">Examples</span></span>

<span data-ttu-id="f2cc2-115">O exemplo de JScript a seguir recupera o primeiro item de mídia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f2cc2-115">The following JScript example retrieves the first media item in the library.</span></span> <span data-ttu-id="f2cc2-116">Em seguida, ele usa **currentMedia** para tornar o item de mídia recuperado o item de mídia atual e, em seguida, exibir o nome do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="f2cc2-116">It then uses **currentMedia** to make the retrieved media item the current media item, and then to display the name of the current media item.</span></span> <span data-ttu-id="f2cc2-117">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f2cc2-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
```



## <a name="requirements"></a><span data-ttu-id="f2cc2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2cc2-118">Requirements</span></span>



| <span data-ttu-id="f2cc2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2cc2-119">Requirement</span></span> | <span data-ttu-id="f2cc2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f2cc2-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2cc2-121">Versão</span><span class="sxs-lookup"><span data-stu-id="f2cc2-121">Version</span></span><br/> | <span data-ttu-id="f2cc2-122">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f2cc2-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f2cc2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f2cc2-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="f2cc2-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2cc2-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2cc2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2cc2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2cc2-126">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="f2cc2-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f2cc2-127">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="f2cc2-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="f2cc2-128">**Player. newMedia**</span><span class="sxs-lookup"><span data-stu-id="f2cc2-128">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="f2cc2-129">**Lista de reprodução. Item**</span><span class="sxs-lookup"><span data-stu-id="f2cc2-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="f2cc2-130">**Settings. AutoStart**</span><span class="sxs-lookup"><span data-stu-id="f2cc2-130">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





