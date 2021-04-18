---
title: Evento Player. OpenStateChange
description: O evento OpenStateChange ocorre quando a propriedade OpenState muda de valor. | Evento Player. OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Evento OpenStateChange do Windows Media Player
- Evento OpenStateChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento OpenStateChange
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762948"
---
# <a name="playeropenstatechange-event"></a><span data-ttu-id="7fc0e-107">Evento Player. OpenStateChange</span><span class="sxs-lookup"><span data-stu-id="7fc0e-107">Player.OpenStateChange event</span></span>

<span data-ttu-id="7fc0e-108">O evento **OpenStateChange** ocorre quando a propriedade **OpenState** muda de valor.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-108">The **OpenStateChange** event occurs when the **openState** property changes value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fc0e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fc0e-109">Syntax</span></span>


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="7fc0e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fc0e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fc0e-111">*NewState*</span><span class="sxs-lookup"><span data-stu-id="7fc0e-111">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="7fc0e-112">**Número** (**longo**) que especifica o novo estado aberto.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-112">**Number** (**long**) specifying the new open state.</span></span> <span data-ttu-id="7fc0e-113">Consulte [OpenState](player-openstate.md) para obter uma tabela de valores.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-113">See [openState](player-openstate.md) for a table of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fc0e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7fc0e-114">Return value</span></span>

<span data-ttu-id="7fc0e-115">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fc0e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fc0e-116">Remarks</span></span>

<span data-ttu-id="7fc0e-117">O Windows Media Player pode passar por vários Estados abertos enquanto tenta abrir um arquivo de rede, como localizar o servidor, conectar-se ao servidor e, finalmente, abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-117">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="7fc0e-118">Esse evento será acionado sempre que o estado aberto for alterado.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-118">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="7fc0e-119">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="7fc0e-120">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="7fc0e-121">Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-121">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="7fc0e-122">Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-122">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="7fc0e-123">Você não deve escrever código que dependa da ordem de estado.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-123">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fc0e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fc0e-124">Requirements</span></span>



| <span data-ttu-id="7fc0e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fc0e-125">Requirement</span></span> | <span data-ttu-id="7fc0e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7fc0e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc0e-127">Versão</span><span class="sxs-lookup"><span data-stu-id="7fc0e-127">Version</span></span><br/> | <span data-ttu-id="7fc0e-128">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7fc0e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7fc0e-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="7fc0e-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fc0e-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fc0e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fc0e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc0e-132">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="7fc0e-133">**Player. openState**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-133">**Player.openState**</span></span>](player-openstate.md)
</dt> </dl>

 

 





