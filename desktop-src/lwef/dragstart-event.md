---
title: Evento DragStart
description: Evento DragStart
ms.assetid: fef0ae05-1958-45c6-8260-107c47b5fa92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e382e77c87848226568755c06d2541ebb4db14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005495"
---
# <a name="dragstart-event"></a><span data-ttu-id="9a636-103">Evento DragStart</span><span class="sxs-lookup"><span data-stu-id="9a636-103">DragStart Event</span></span>

<span data-ttu-id="9a636-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9a636-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9a636-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="9a636-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9a636-106">Ocorre quando o usuário começa a arrastar um caractere.</span><span class="sxs-lookup"><span data-stu-id="9a636-106">Occurs when the user begins dragging a character.</span></span>

</dd> <dt>

<span data-ttu-id="9a636-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="9a636-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9a636-108">**Sub** *Agent \* \* \* \_ DragStart* \*  **(ByVal** *characterid*, **(** *botão* ByVal, **(ByVal** *Shift*, **(ByVal** *X*, **(ByVal** *Y \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="9a636-108">**Sub** *agent\*\*\*\_DragStart*\* **(ByVal** *CharacterID*, **(ByVal** *Button*, **(ByVal** *Shift*, **(ByVal** *X*, **(ByVal** *Y\*\*\*)*\*</span></span>



| <span data-ttu-id="9a636-109">Parte</span><span class="sxs-lookup"><span data-stu-id="9a636-109">Part</span></span>          | <span data-ttu-id="9a636-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a636-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a636-111">*Caractere de caracteres*</span><span class="sxs-lookup"><span data-stu-id="9a636-111">*CharacterID*</span></span> | <span data-ttu-id="9a636-112">Retorna a ID do caractere clicado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9a636-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9a636-113">*Botão*</span><span class="sxs-lookup"><span data-stu-id="9a636-113">*Button*</span></span>      | <span data-ttu-id="9a636-114">Retorna um inteiro que identifica o botão que foi pressionado e liberado para causar o evento.</span><span class="sxs-lookup"><span data-stu-id="9a636-114">Returns an integer that identifies the button that was pressed and released to cause the event.</span></span> <span data-ttu-id="9a636-115">O argumento do botão é um campo de bits que corresponde ao botão esquerdo (bit 0), ao botão direito (bit 1) e ao botão do meio (bit 2).</span><span class="sxs-lookup"><span data-stu-id="9a636-115">The button argument is a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="9a636-116">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9a636-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="9a636-117">Apenas um dos bits é definido, indicando o botão que causou o evento.</span><span class="sxs-lookup"><span data-stu-id="9a636-117">Only one of the bits is set, indicating the button that caused the event.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="9a636-118">*Alternância*</span><span class="sxs-lookup"><span data-stu-id="9a636-118">*Shift*</span></span>       | <span data-ttu-id="9a636-119">Retorna um inteiro que corresponde ao estado das teclas SHIFT, CTRL e ALT quando o botão especificado no argumento Button é pressionado ou liberado.</span><span class="sxs-lookup"><span data-stu-id="9a636-119">Returns an integer that corresponds to the state of the SHIFT, CTRL, and ALT keys when the button specified in the button argument is pressed or released.</span></span> <span data-ttu-id="9a636-120">Um bit será definido se a chave estiver inoperante.</span><span class="sxs-lookup"><span data-stu-id="9a636-120">A bit is set if the key is down.</span></span> <span data-ttu-id="9a636-121">O argumento Shift é um campo de campo com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="9a636-121">The shift argument is a bitfield with the least-significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="9a636-122">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9a636-122">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="9a636-123">O argumento Shift indica o estado dessas chaves.</span><span class="sxs-lookup"><span data-stu-id="9a636-123">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="9a636-124">Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.</span><span class="sxs-lookup"><span data-stu-id="9a636-124">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span> <span data-ttu-id="9a636-125">Por exemplo, se CTRL e ALT forem pressionadas, o valor de Shift seria 6.</span><span class="sxs-lookup"><span data-stu-id="9a636-125">For example, if both CTRL and ALT were pressed, the value of shift would be 6.</span></span> |
| <span data-ttu-id="9a636-126">*X, Y*</span><span class="sxs-lookup"><span data-stu-id="9a636-126">*X,Y*</span></span>         | <span data-ttu-id="9a636-127">Retorna um inteiro que especifica o local atual do ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="9a636-127">Returns an integer that specifies the current location of the mouse pointer.</span></span> <span data-ttu-id="9a636-128">Os valores X e Y são sempre expressos em pixels, em relação ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="9a636-128">The X and Y values are always expressed in pixels, relative to the upper left corner of the screen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="9a636-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a636-129">Remarks</span></span>

<span data-ttu-id="9a636-130">Esse evento é enviado somente para o cliente de entrada-ativo de um caractere.</span><span class="sxs-lookup"><span data-stu-id="9a636-130">This event is sent only to the input-active client of a character.</span></span> <span data-ttu-id="9a636-131">Quando o usuário arrasta um caractere sem entrada-cliente ativo, o servidor define seu último cliente de entrada-ativo como o cliente de entrada-ativo atual, enviando o evento [**ActivateInput**](activateinput-event.md) para esse cliente e, em seguida, enviando o evento **DragStart** .</span><span class="sxs-lookup"><span data-stu-id="9a636-131">When the user drags a character with no input-active client, the server sets its last input-active client as the current input-active client, sending the [**ActivateInput**](activateinput-event.md) event to that client, and then sending the **DragStart** event.</span></span>

### <a name="see-also"></a><span data-ttu-id="9a636-132">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9a636-132">See Also</span></span>

[<span data-ttu-id="9a636-133">**Evento DragComplete**</span><span class="sxs-lookup"><span data-stu-id="9a636-133">**DragComplete event**</span></span>](dragcomplete-event.md)


 

 




