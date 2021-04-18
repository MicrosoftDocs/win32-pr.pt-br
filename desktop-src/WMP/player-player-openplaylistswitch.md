---
title: Evento Player. OpenPlaylistSwitch
description: O evento OpenPlaylistSwitch ocorre quando um título em um DVD começa a ser reproduzido. | Evento Player. OpenPlaylistSwitch
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Evento OpenPlaylistSwitch do Windows Media Player
- Evento OpenPlaylistSwitch Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento OpenPlaylistSwitch
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789011"
---
# <a name="playeropenplaylistswitch-event"></a><span data-ttu-id="58932-107">Evento Player. OpenPlaylistSwitch</span><span class="sxs-lookup"><span data-stu-id="58932-107">Player.OpenPlaylistSwitch event</span></span>

<span data-ttu-id="58932-108">O evento **OpenPlaylistSwitch** ocorre quando um título em um DVD começa a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="58932-108">The **OpenPlaylistSwitch** event occurs when a title on a DVD begins playing.</span></span>

## <a name="syntax"></a><span data-ttu-id="58932-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58932-109">Syntax</span></span>


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a><span data-ttu-id="58932-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58932-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58932-111">*pItem*</span><span class="sxs-lookup"><span data-stu-id="58932-111">*pItem*</span></span> 
</dt> <dd>

<span data-ttu-id="58932-112">Objeto **playlist** que representa o título.</span><span class="sxs-lookup"><span data-stu-id="58932-112">**Playlist** object representing the title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58932-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58932-113">Return value</span></span>

<span data-ttu-id="58932-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="58932-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58932-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="58932-115">Remarks</span></span>

<span data-ttu-id="58932-116">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="58932-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="58932-117">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="58932-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="58932-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58932-118">Requirements</span></span>



| <span data-ttu-id="58932-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="58932-119">Requirement</span></span> | <span data-ttu-id="58932-120">Valor</span><span class="sxs-lookup"><span data-stu-id="58932-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58932-121">Versão</span><span class="sxs-lookup"><span data-stu-id="58932-121">Version</span></span><br/> | <span data-ttu-id="58932-122">Windows Media Player para Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="58932-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="58932-123">DLL</span><span class="sxs-lookup"><span data-stu-id="58932-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="58932-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58932-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58932-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="58932-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58932-126">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="58932-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





