---
title: Evento Player. CurrentPlaylistChange
description: O evento CurrentPlaylistChange ocorre quando algo é alterado na playlist atual. | Evento Player. CurrentPlaylistChange
ms.assetid: 5270373e-e401-40c6-bf8c-ef0557610372
keywords:
- Evento CurrentPlaylistChange do Windows Media Player
- Evento CurrentPlaylistChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento CurrentPlaylistChange
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4722db224285587198e3ddb021022ec5d8f2cea6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773048"
---
# <a name="playercurrentplaylistchange-event"></a><span data-ttu-id="0e3e5-107">Evento Player. CurrentPlaylistChange</span><span class="sxs-lookup"><span data-stu-id="0e3e5-107">Player.CurrentPlaylistChange event</span></span>

<span data-ttu-id="0e3e5-108">O evento **CurrentPlaylistChange** ocorre quando algo é alterado na playlist atual.</span><span class="sxs-lookup"><span data-stu-id="0e3e5-108">The **CurrentPlaylistChange** event occurs when something changes within the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e3e5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e3e5-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistChange(
  change
)
```



## <a name="parameters"></a><span data-ttu-id="0e3e5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e3e5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e3e5-111">*change*</span><span class="sxs-lookup"><span data-stu-id="0e3e5-111">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="0e3e5-112">**Número** (**longo**) indicando que tipo de alteração ocorreu na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0e3e5-112">**Number** (**long**) indicating what type of change occurred to the playlist.</span></span> <span data-ttu-id="0e3e5-113">Consulte o *Player*. Evento **PlaylistChange** para uma tabela de valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="0e3e5-113">See the *Player*.**PlaylistChange** event for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e3e5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e3e5-114">Return value</span></span>

<span data-ttu-id="0e3e5-115">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0e3e5-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e3e5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e3e5-116">Remarks</span></span>

<span data-ttu-id="0e3e5-117">Esse evento não ocorre quando uma playlist diferente se torna a playlist atual.</span><span class="sxs-lookup"><span data-stu-id="0e3e5-117">This event does not occur when a different playlist becomes the current playlist.</span></span> <span data-ttu-id="0e3e5-118">Isso ocorre apenas quando uma alteração acontece na playlist atual, como um item de mídia que está sendo anexado à playlist.</span><span class="sxs-lookup"><span data-stu-id="0e3e5-118">It only occurs when a change happens within the current playlist, such as a media item being appended to the playlist.</span></span>

<span data-ttu-id="0e3e5-119">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="0e3e5-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="0e3e5-120">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="0e3e5-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="examples"></a><span data-ttu-id="0e3e5-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e3e5-121">Examples</span></span>

<span data-ttu-id="0e3e5-122">O exemplo de JScript a seguir atualiza o texto em um elemento HTML DIV, chamado PlItems, para exibir os nomes dos itens de mídia na playlist atual.</span><span class="sxs-lookup"><span data-stu-id="0e3e5-122">The following JScript example updates the text in an HTML DIV element, named PlItems, to display the names of the media items in the current playlist.</span></span> <span data-ttu-id="0e3e5-123">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="0e3e5-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for current playlist change. -->
<SCRIPT FOR = "Player" EVENT = "currentPlaylistChange(change)">
   switch (change){
      // Only update for move, delete, insert, and append events.
      case 3, 4, 5, 6:

         // Clear the contents of the DIV.
         PlItems.innerHTML = "";

         // Loop through the playlist and display each item name.
         for (var i = 0; i < Player.currentPlaylist.count; i++){
            PlItems.innerHTML += Player.currentPlaylist.item(i).name;
            PlItems.innerHTML += "<br>";
         }
         break;
      
      default:
   } 
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="0e3e5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e3e5-124">Requirements</span></span>



| <span data-ttu-id="0e3e5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e3e5-125">Requirement</span></span> | <span data-ttu-id="0e3e5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0e3e5-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e3e5-127">Versão</span><span class="sxs-lookup"><span data-stu-id="0e3e5-127">Version</span></span><br/> | <span data-ttu-id="0e3e5-128">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="0e3e5-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0e3e5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0e3e5-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="0e3e5-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e3e5-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e3e5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e3e5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e3e5-132">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="0e3e5-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="0e3e5-133">**Player. currentPlaylist**</span><span class="sxs-lookup"><span data-stu-id="0e3e5-133">**Player.currentPlaylist**</span></span>](player-currentplaylist.md)
</dt> <dt>

[<span data-ttu-id="0e3e5-134">**Player. PlaylistChange**</span><span class="sxs-lookup"><span data-stu-id="0e3e5-134">**Player.PlaylistChange**</span></span>](player-player-playlistchange.md)
</dt> </dl>

 

 





