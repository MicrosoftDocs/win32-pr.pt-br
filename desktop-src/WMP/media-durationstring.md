---
title: Media. durationstring
description: A propriedade durationstring recupera um valor de cadeia de caracteres que indica a duração do item de mídia atual no formato HH MM SS.
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- Media. durationstring Windows Media Player
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763334"
---
# <a name="mediadurationstring"></a><span data-ttu-id="f6deb-104">Media. durationstring</span><span class="sxs-lookup"><span data-stu-id="f6deb-104">Media.durationString</span></span>

<span data-ttu-id="f6deb-105">A propriedade **durationstring** recupera um valor de **cadeia de caracteres** que indica a duração do item de mídia atual no formato hh: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="f6deb-105">The **durationString** property retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6deb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6deb-106">Syntax</span></span>

<span data-ttu-id="f6deb-107">*Player*. *currentMedia*. **duraçãostring**</span><span class="sxs-lookup"><span data-stu-id="f6deb-107">*player*.*currentMedia*.**durationString**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f6deb-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="f6deb-108">Possible Values</span></span>

<span data-ttu-id="f6deb-109">Esta propriedade é uma **cadeia de caracteres** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f6deb-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6deb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6deb-110">Remarks</span></span>

<span data-ttu-id="f6deb-111">Se essa propriedade for usada com um item de mídia diferente daquele especificado no *Player*. **currentMedia**, ele não pode conter um valor válido.</span><span class="sxs-lookup"><span data-stu-id="f6deb-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span> <span data-ttu-id="f6deb-112">Se o item de mídia for menor que uma hora, a parte HH: do valor de retorno será omitida.</span><span class="sxs-lookup"><span data-stu-id="f6deb-112">If the media item is less than an hour long, the HH: portion of the return value is omitted.</span></span>

<span data-ttu-id="f6deb-113">Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f6deb-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="f6deb-114">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f6deb-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f6deb-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6deb-115">Examples</span></span>

<span data-ttu-id="f6deb-116">O exemplo de JScript a seguir usa *mídia*. **durationstring** para exibir a duração do item de mídia atual como texto formatado.</span><span class="sxs-lookup"><span data-stu-id="f6deb-116">The following JScript example uses *Media*.**durationString** to display the duration of the current media item as formatted text.</span></span> <span data-ttu-id="f6deb-117">Um elemento HTML DIV chamado MediaInfo exibe as informações de duração.</span><span class="sxs-lookup"><span data-stu-id="f6deb-117">An HTML DIV element named MediaInfo displays the duration information.</span></span> <span data-ttu-id="f6deb-118">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f6deb-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="f6deb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6deb-119">Requirements</span></span>



| <span data-ttu-id="f6deb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6deb-120">Requirement</span></span> | <span data-ttu-id="f6deb-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f6deb-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6deb-122">Versão</span><span class="sxs-lookup"><span data-stu-id="f6deb-122">Version</span></span><br/> | <span data-ttu-id="f6deb-123">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f6deb-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f6deb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f6deb-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="f6deb-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6deb-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6deb-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6deb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6deb-127">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="f6deb-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f6deb-128">**Duração da mídia**</span><span class="sxs-lookup"><span data-stu-id="f6deb-128">**Media.duration**</span></span>](media-duration.md)
</dt> <dt>

[<span data-ttu-id="f6deb-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="f6deb-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="f6deb-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f6deb-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f6deb-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f6deb-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





