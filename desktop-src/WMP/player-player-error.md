---
title: Evento Player. Error
description: O evento de erro ocorre quando há uma condição de erro.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Evento de erro do Windows Media Player
- Evento de erro Windows Media Player, classe Player
- Classe de Player Windows Media Player, evento de erro
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773073"
---
# <a name="playererror-event"></a><span data-ttu-id="744fd-106">Evento Player. Error</span><span class="sxs-lookup"><span data-stu-id="744fd-106">Player.Error event</span></span>

<span data-ttu-id="744fd-107">O evento de **erro** ocorre quando há uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="744fd-107">The **Error** event occurs when there is an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="744fd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="744fd-108">Syntax</span></span>


```JScript
Player.Error()
```



## <a name="parameters"></a><span data-ttu-id="744fd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="744fd-109">Parameters</span></span>

<span data-ttu-id="744fd-110">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="744fd-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="744fd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="744fd-111">Return value</span></span>

<span data-ttu-id="744fd-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="744fd-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="744fd-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="744fd-113">Examples</span></span>

<span data-ttu-id="744fd-114">O exemplo de JScript a seguir cria um manipulador de eventos para exibir o texto de descrição do primeiro erro na fila de erros.</span><span class="sxs-lookup"><span data-stu-id="744fd-114">The following JScript example creates an event handler to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="744fd-115">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="744fd-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="744fd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="744fd-116">Requirements</span></span>



| <span data-ttu-id="744fd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="744fd-117">Requirement</span></span> | <span data-ttu-id="744fd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="744fd-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="744fd-119">Versão</span><span class="sxs-lookup"><span data-stu-id="744fd-119">Version</span></span><br/> | <span data-ttu-id="744fd-120">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="744fd-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="744fd-121">DLL</span><span class="sxs-lookup"><span data-stu-id="744fd-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="744fd-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="744fd-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="744fd-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="744fd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="744fd-124">**ErrorItem. errorDescription**</span><span class="sxs-lookup"><span data-stu-id="744fd-124">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> <dt>

[<span data-ttu-id="744fd-125">**Erro. Item**</span><span class="sxs-lookup"><span data-stu-id="744fd-125">**Error.item**</span></span>](error-item.md)
</dt> <dt>

[<span data-ttu-id="744fd-126">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="744fd-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





