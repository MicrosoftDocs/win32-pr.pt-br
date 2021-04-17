---
title: Evento Player. MediaChange
description: O evento MediaChange ocorre quando um item de mídia é alterado. | Evento Player. MediaChange
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Evento MediaChange do Windows Media Player
- Evento MediaChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MediaChange
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763333"
---
# <a name="playermediachange-event"></a><span data-ttu-id="6fbb5-107">Evento Player. MediaChange</span><span class="sxs-lookup"><span data-stu-id="6fbb5-107">Player.MediaChange event</span></span>

<span data-ttu-id="6fbb5-108">O evento **MediaChange** ocorre quando um item de mídia é alterado.</span><span class="sxs-lookup"><span data-stu-id="6fbb5-108">The **MediaChange** event occurs when a media item changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fbb5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fbb5-109">Syntax</span></span>


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a><span data-ttu-id="6fbb5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fbb5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fbb5-111">*Item*</span><span class="sxs-lookup"><span data-stu-id="6fbb5-111">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="6fbb5-112">O objeto de **mídia** que representa o item que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="6fbb5-112">**Media** object representing the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fbb5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fbb5-113">Return value</span></span>

<span data-ttu-id="6fbb5-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6fbb5-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fbb5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fbb5-115">Remarks</span></span>

<span data-ttu-id="6fbb5-116">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="6fbb5-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="6fbb5-117">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="6fbb5-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="6fbb5-118">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="6fbb5-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="6fbb5-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6fbb5-119">Examples</span></span>

<span data-ttu-id="6fbb5-120">O exemplo de JScript a seguir usa um elemento HTML DIV, chamado MEDIANAME, para exibir o nome do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="6fbb5-120">The following JScript example uses an HTML DIV element, named MediaName, to display the name of the current media item.</span></span> <span data-ttu-id="6fbb5-121">O código atualiza o texto na DIV com cada ocorrência do evento **mediaChange** .</span><span class="sxs-lookup"><span data-stu-id="6fbb5-121">The code updates the text in the DIV with each occurrence of the **mediaChange** event.</span></span> <span data-ttu-id="6fbb5-122">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6fbb5-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="6fbb5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fbb5-123">Requirements</span></span>



| <span data-ttu-id="6fbb5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fbb5-124">Requirement</span></span> | <span data-ttu-id="6fbb5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6fbb5-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6fbb5-126">Versão</span><span class="sxs-lookup"><span data-stu-id="6fbb5-126">Version</span></span><br/> | <span data-ttu-id="6fbb5-127">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6fbb5-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6fbb5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6fbb5-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="6fbb5-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fbb5-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fbb5-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fbb5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fbb5-131">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="6fbb5-131">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





