---
title: Evento Player. CurrentItemChange
description: O evento CurrentItemChange ocorre quando o Controls. currentItem é alterado.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Evento CurrentItemChange do Windows Media Player
- Evento CurrentItemChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento CurrentItemChange
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810879"
---
# <a name="playercurrentitemchange-event"></a><span data-ttu-id="e80d5-106">Evento Player. CurrentItemChange</span><span class="sxs-lookup"><span data-stu-id="e80d5-106">Player.CurrentItemChange event</span></span>

<span data-ttu-id="e80d5-107">O evento **CurrentItemChange** ocorre quando os *controles*. **currentItem** é alterado.</span><span class="sxs-lookup"><span data-stu-id="e80d5-107">The **CurrentItemChange** event occurs when *Controls*.**currentItem** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e80d5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e80d5-108">Syntax</span></span>


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a><span data-ttu-id="e80d5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e80d5-109">Parameters</span></span>

<span data-ttu-id="e80d5-110">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e80d5-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e80d5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e80d5-111">Return value</span></span>

<span data-ttu-id="e80d5-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e80d5-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="e80d5-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e80d5-113">Examples</span></span>

<span data-ttu-id="e80d5-114">O exemplo de JScript a seguir demonstra um manipulador de eventos para o *Player*. evento **currentItemChange** .</span><span class="sxs-lookup"><span data-stu-id="e80d5-114">The following JScript example demonstrates an event handler for the *Player*.**currentItemChange** event.</span></span> <span data-ttu-id="e80d5-115">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="e80d5-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="e80d5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e80d5-116">Requirements</span></span>



| <span data-ttu-id="e80d5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e80d5-117">Requirement</span></span> | <span data-ttu-id="e80d5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e80d5-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e80d5-119">Versão</span><span class="sxs-lookup"><span data-stu-id="e80d5-119">Version</span></span><br/> | <span data-ttu-id="e80d5-120">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e80d5-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e80d5-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e80d5-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="e80d5-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e80d5-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e80d5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e80d5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80d5-124">**Controls. currentItem**</span><span class="sxs-lookup"><span data-stu-id="e80d5-124">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="e80d5-125">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="e80d5-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





