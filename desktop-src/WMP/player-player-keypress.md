---
title: Evento Player. KeyPress
description: O evento KeyPress ocorre quando uma tecla é pressionada e liberada. | Evento Player. KeyPress
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- Evento KeyPress Windows Media Player
- Evento KeyPress Windows Media Player, classe Player
- Classe Player Windows Media Player, evento KeyPress
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791512"
---
# <a name="playerkeypress-event"></a><span data-ttu-id="28759-107">Evento Player. KeyPress</span><span class="sxs-lookup"><span data-stu-id="28759-107">Player.KeyPress event</span></span>

<span data-ttu-id="28759-108">O evento **KeyPress** ocorre quando uma tecla é pressionada e liberada.</span><span class="sxs-lookup"><span data-stu-id="28759-108">The **KeyPress** event occurs when a key is pressed and released.</span></span>

## <a name="syntax"></a><span data-ttu-id="28759-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28759-109">Syntax</span></span>


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a><span data-ttu-id="28759-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28759-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28759-111">*nKeyAscii*</span><span class="sxs-lookup"><span data-stu-id="28759-111">*nKeyAscii*</span></span> 
</dt> <dd>

<span data-ttu-id="28759-112">**Número** (**int**) especificando o código ANSI numérico padrão para o caractere.</span><span class="sxs-lookup"><span data-stu-id="28759-112">**Number** (**int**) specifying the standard numeric ANSI code for the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28759-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28759-113">Return value</span></span>

<span data-ttu-id="28759-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="28759-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28759-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="28759-115">Remarks</span></span>

<span data-ttu-id="28759-116">Esse evento ocorre quando o pressionamento de tecla resulta em qualquer caractere de teclado imprimível, a tecla CTRL combinada com um caractere do alfabeto padrão ou um de alguns caracteres especiais e a tecla ENTER ou Backspace.</span><span class="sxs-lookup"><span data-stu-id="28759-116">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

<span data-ttu-id="28759-117">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="28759-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="28759-118">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="28759-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="28759-119">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="28759-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="28759-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28759-120">Requirements</span></span>



| <span data-ttu-id="28759-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="28759-121">Requirement</span></span> | <span data-ttu-id="28759-122">Valor</span><span class="sxs-lookup"><span data-stu-id="28759-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28759-123">Versão</span><span class="sxs-lookup"><span data-stu-id="28759-123">Version</span></span><br/> | <span data-ttu-id="28759-124">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="28759-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="28759-125">DLL</span><span class="sxs-lookup"><span data-stu-id="28759-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="28759-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28759-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28759-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="28759-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28759-128">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="28759-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





