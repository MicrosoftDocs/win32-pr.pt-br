---
title: Player. tela inteira
description: A propriedade fullScreen especifica ou recupera um valor que indica se o conteúdo do vídeo é reproduzido no modo de tela inteira.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player. tela inteira do Windows Media Player
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781356"
---
# <a name="playerfullscreen"></a><span data-ttu-id="08b09-104">Player. tela inteira</span><span class="sxs-lookup"><span data-stu-id="08b09-104">Player.fullScreen</span></span>

<span data-ttu-id="08b09-105">A propriedade **fullscreen** especifica ou recupera um valor que indica se o conteúdo do vídeo é reproduzido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="08b09-105">The **fullScreen** property specifies or retrieves a value indicating whether video content is played back in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="08b09-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="08b09-106">Syntax</span></span>

<span data-ttu-id="08b09-107">*Player* . **tela inteira**</span><span class="sxs-lookup"><span data-stu-id="08b09-107">*player* .**fullScreen**</span></span>

## <a name="possible-values"></a><span data-ttu-id="08b09-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="08b09-108">Possible Values</span></span>

<span data-ttu-id="08b09-109">Esta propriedade é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="08b09-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="08b09-110">Valor</span><span class="sxs-lookup"><span data-stu-id="08b09-110">Value</span></span> | <span data-ttu-id="08b09-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="08b09-111">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="08b09-112">true</span><span class="sxs-lookup"><span data-stu-id="08b09-112">true</span></span>  | <span data-ttu-id="08b09-113">O conteúdo de vídeo é reproduzido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="08b09-113">Video content is played back in full-screen mode.</span></span>              |
| <span data-ttu-id="08b09-114">false</span><span class="sxs-lookup"><span data-stu-id="08b09-114">false</span></span> | <span data-ttu-id="08b09-115">Padrão.</span><span class="sxs-lookup"><span data-stu-id="08b09-115">Default.</span></span> <span data-ttu-id="08b09-116">O conteúdo de vídeo não é reproduzido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="08b09-116">Video content is not played back in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="08b09-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="08b09-117">Remarks</span></span>

<span data-ttu-id="08b09-118">Para que o modo de tela inteira funcione corretamente ao inserir o controle do Windows Media Player, a área de exibição de vídeo deve ter uma altura e largura de pelo menos um pixel.</span><span class="sxs-lookup"><span data-stu-id="08b09-118">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="08b09-119">Se **UIMODE** for definido como "mini" ou "Full", a altura do controle em si deverá ser 65 ou maior para acomodar a área de exibição do vídeo além da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="08b09-119">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="08b09-120">Se **UIMODE** for definido como "invisível", a configuração dessa propriedade como true gerará um erro e não afetará o comportamento do controle.</span><span class="sxs-lookup"><span data-stu-id="08b09-120">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="08b09-121">Durante a reprodução de tela inteira, o Windows Media Player oculta o cursor do mouse quando **enableContextMenu** é igual a false e **UIMODE** é igual a "None".</span><span class="sxs-lookup"><span data-stu-id="08b09-121">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="08b09-122">Se **UIMODE** for definido como "Full" ou "mini", o Windows Media Player exibirá controles de transporte no modo de tela inteira quando o cursor do mouse se mover.</span><span class="sxs-lookup"><span data-stu-id="08b09-122">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="08b09-123">Após um breve intervalo de sem movimento do mouse, os controles de transporte ficam ocultos.</span><span class="sxs-lookup"><span data-stu-id="08b09-123">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="08b09-124">Se **UIMODE** for definido como "None", nenhum controle será exibido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="08b09-124">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="08b09-125">**Observação**</span><span class="sxs-lookup"><span data-stu-id="08b09-125">**Note**</span></span>

<span data-ttu-id="08b09-126">A exibição de controles de transporte no modo de tela inteira requer o sistema operacional Windows XP.</span><span class="sxs-lookup"><span data-stu-id="08b09-126">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

<span data-ttu-id="08b09-127">Se os controles de transporte não forem exibidos no modo de tela inteira, o Windows Media Player sairá automaticamente do modo de tela inteira quando a reprodução for interrompida.</span><span class="sxs-lookup"><span data-stu-id="08b09-127">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

<span data-ttu-id="08b09-128">**Observação**</span><span class="sxs-lookup"><span data-stu-id="08b09-128">**Note**</span></span>

<span data-ttu-id="08b09-129">Sempre certifique-se de informar ao usuário como retornar do modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="08b09-129">Always be sure to inform the user how to return from full-screen mode.</span></span>

## <a name="examples"></a><span data-ttu-id="08b09-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="08b09-130">Examples</span></span>

<span data-ttu-id="08b09-131">O exemplo a seguir cria um botão de entrada HTML que usa o *Player*. **tela inteira** para alternar um objeto de player incorporado para o modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="08b09-131">The following example creates an HTML input button that uses *Player*.**fullScreen** to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="08b09-132">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="08b09-132">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a><span data-ttu-id="08b09-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08b09-133">Requirements</span></span>



| <span data-ttu-id="08b09-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="08b09-134">Requirement</span></span> | <span data-ttu-id="08b09-135">Valor</span><span class="sxs-lookup"><span data-stu-id="08b09-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08b09-136">Versão</span><span class="sxs-lookup"><span data-stu-id="08b09-136">Version</span></span><br/> | <span data-ttu-id="08b09-137">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="08b09-137">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="08b09-138">DLL</span><span class="sxs-lookup"><span data-stu-id="08b09-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="08b09-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08b09-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08b09-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="08b09-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b09-141">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="08b09-141">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





