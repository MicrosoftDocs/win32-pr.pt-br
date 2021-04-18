---
title: Evento Player. PlayStateChange
description: O evento PlayStateChange ocorre quando há uma alteração na propriedade PlayState.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Evento PlayStateChange do Windows Media Player
- Evento PlayStateChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento PlayStateChange
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790592"
---
# <a name="playerplaystatechange-event"></a><span data-ttu-id="38f70-106">Evento Player. PlayStateChange</span><span class="sxs-lookup"><span data-stu-id="38f70-106">Player.PlayStateChange event</span></span>

<span data-ttu-id="38f70-107">O evento **PlayStateChange** ocorre quando há uma alteração na propriedade **PlayState** .</span><span class="sxs-lookup"><span data-stu-id="38f70-107">The **PlayStateChange** event occurs when there is a change in the **playState** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f70-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38f70-108">Syntax</span></span>


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="38f70-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38f70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f70-110">*NewState*</span><span class="sxs-lookup"><span data-stu-id="38f70-110">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="38f70-111">Número (**longo**) que especifica o novo **PlayState**.</span><span class="sxs-lookup"><span data-stu-id="38f70-111">Number (**long**) which specifies the new **playState**.</span></span> <span data-ttu-id="38f70-112">Consulte [PlayState](player-playstate.md) para obter uma tabela de valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="38f70-112">See [playState](player-playstate.md) for a table of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f70-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38f70-113">Return value</span></span>

<span data-ttu-id="38f70-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="38f70-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38f70-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="38f70-115">Remarks</span></span>

<span data-ttu-id="38f70-116">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="38f70-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="38f70-117">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="38f70-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="38f70-118">Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="38f70-118">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="38f70-119">Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos.</span><span class="sxs-lookup"><span data-stu-id="38f70-119">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="38f70-120">Você não deve escrever código que dependa da ordem de estado.</span><span class="sxs-lookup"><span data-stu-id="38f70-120">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="38f70-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="38f70-121">Examples</span></span>

<span data-ttu-id="38f70-122">O exemplo a seguir demonstra um manipulador de eventos para o *Player*. evento **playStateChange** .</span><span class="sxs-lookup"><span data-stu-id="38f70-122">The following example demonstrates an event handler for the *Player*.**playStateChange** event.</span></span> <span data-ttu-id="38f70-123">Um elemento de texto HTML, chamado "MyText", exibe o novo estado de reprodução.</span><span class="sxs-lookup"><span data-stu-id="38f70-123">An HTML text element, named "myText", displays the new play state.</span></span> <span data-ttu-id="38f70-124">O objeto de jogador foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="38f70-124">The player object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="38f70-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38f70-125">Requirements</span></span>



| <span data-ttu-id="38f70-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="38f70-126">Requirement</span></span> | <span data-ttu-id="38f70-127">Valor</span><span class="sxs-lookup"><span data-stu-id="38f70-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="38f70-128">Versão</span><span class="sxs-lookup"><span data-stu-id="38f70-128">Version</span></span><br/> | <span data-ttu-id="38f70-129">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="38f70-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="38f70-130">DLL</span><span class="sxs-lookup"><span data-stu-id="38f70-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="38f70-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38f70-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38f70-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="38f70-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f70-133">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="38f70-133">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="38f70-134">**Player. PlayState**</span><span class="sxs-lookup"><span data-stu-id="38f70-134">**Player.playState**</span></span>](player-playstate.md)
</dt> </dl>

 

 





