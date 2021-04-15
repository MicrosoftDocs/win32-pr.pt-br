---
title: Duração da mídia
description: A Propriedade Duration recupera a duração do item de mídia atual em segundos.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media. Duration Windows Media Player
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71586f6aa37401d56a9e9537bfbea6c5af23f318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761281"
---
# <a name="mediaduration"></a><span data-ttu-id="85e34-104">Duração da mídia</span><span class="sxs-lookup"><span data-stu-id="85e34-104">Media.duration</span></span>

<span data-ttu-id="85e34-105">A propriedade **Duration** recupera a duração do item de mídia atual em segundos.</span><span class="sxs-lookup"><span data-stu-id="85e34-105">The **duration** property retrieves the duration of the current media item in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e34-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="85e34-106">Syntax</span></span>

<span data-ttu-id="85e34-107">*Player*. *currentMedia*. **duração**</span><span class="sxs-lookup"><span data-stu-id="85e34-107">*player*.*currentMedia*.**duration**</span></span>

## <a name="possible-values"></a><span data-ttu-id="85e34-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="85e34-108">Possible Values</span></span>

<span data-ttu-id="85e34-109">Essa propriedade é um **número** somente leitura ( **duplo**).</span><span class="sxs-lookup"><span data-stu-id="85e34-109">This property is a read-only **Number** ( **double**).</span></span>

## <a name="remarks"></a><span data-ttu-id="85e34-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="85e34-110">Remarks</span></span>

<span data-ttu-id="85e34-111">Se essa propriedade for usada com um item de mídia diferente daquele especificado no *Player*. **currentMedia**, ele não pode conter um valor válido.</span><span class="sxs-lookup"><span data-stu-id="85e34-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span>

<span data-ttu-id="85e34-112">Para recuperar a duração de arquivos que não estão na biblioteca do usuário, você deve aguardar que o Windows Media Player Abra o arquivo; ou seja, o OpenState atual deve ser igual a MediaOpen.</span><span class="sxs-lookup"><span data-stu-id="85e34-112">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current OpenState must equal MediaOpen.</span></span> <span data-ttu-id="85e34-113">Você pode verificar isso manipulando o *Player*. Evento **OpenStateChange** ou verificando periodicamente o valor do *Player*. **OpenState**.</span><span class="sxs-lookup"><span data-stu-id="85e34-113">You can verify this by handling the *Player*.**OpenStateChange** event or by periodically checking the value of *Player*.**openState**.</span></span>

<span data-ttu-id="85e34-114">Para listas de reprodução, a duração de cada item de mídia pode ser recuperada quando o item de mídia individual é aberto, em vez de quando a playlist é aberta.</span><span class="sxs-lookup"><span data-stu-id="85e34-114">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="85e34-115">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="85e34-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="85e34-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="85e34-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="85e34-117">O exemplo de JScript a seguir usa *mídia*. **duração** para exibir o tempo restante no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="85e34-117">The following JScript example uses *Media*.**duration** to display the time remaining in the current media item.</span></span> <span data-ttu-id="85e34-118">Um elemento HTML DIV chamado RemTime exibe as informações.</span><span class="sxs-lookup"><span data-stu-id="85e34-118">An HTML DIV element named RemTime displays the information.</span></span> <span data-ttu-id="85e34-119">Um temporizador HTML atualiza o texto no elemento DIV a cada segundo.</span><span class="sxs-lookup"><span data-stu-id="85e34-119">An HTML timer updates the text in the DIV element every second.</span></span>

<span data-ttu-id="85e34-120">O código JScript a seguir inicia o temporizador:</span><span class="sxs-lookup"><span data-stu-id="85e34-120">The following JScript code starts the timer:</span></span>


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



<span data-ttu-id="85e34-121">O seguinte código JScript interrompe o temporizador:</span><span class="sxs-lookup"><span data-stu-id="85e34-121">The following JScript code stops the timer:</span></span>


```JScript
window.clearInterval(idTmr);
```



<span data-ttu-id="85e34-122">Use o *Player*. Evento **PlayStateChange** com uma instrução **switch** para determinar quando iniciar e parar o temporizador.</span><span class="sxs-lookup"><span data-stu-id="85e34-122">Use the *Player*.**PlayStateChange** event with a **switch** statement to determine when to start and stop the timer.</span></span>

<span data-ttu-id="85e34-123">O seguinte código JScript é executado cada vez que o temporizador chama a função Update:</span><span class="sxs-lookup"><span data-stu-id="85e34-123">The following JScript code executes each time the timer calls the update function:</span></span>


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
```



## <a name="requirements"></a><span data-ttu-id="85e34-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85e34-124">Requirements</span></span>



| <span data-ttu-id="85e34-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="85e34-125">Requirement</span></span> | <span data-ttu-id="85e34-126">Valor</span><span class="sxs-lookup"><span data-stu-id="85e34-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85e34-127">Versão</span><span class="sxs-lookup"><span data-stu-id="85e34-127">Version</span></span><br/> | <span data-ttu-id="85e34-128">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="85e34-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="85e34-129">DLL</span><span class="sxs-lookup"><span data-stu-id="85e34-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="85e34-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85e34-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85e34-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="85e34-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e34-132">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="85e34-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="85e34-133">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="85e34-133">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="85e34-134">**Evento Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="85e34-134">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="85e34-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="85e34-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="85e34-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="85e34-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





