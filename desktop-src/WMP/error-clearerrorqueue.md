---
title: Erro. método clearErrorQueue
description: O método clearErrorQueue limpa os erros da fila de erros. | Erro. método clearErrorQueue
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- método clearErrorQueue Windows Media Player
- método clearErrorQueue Windows Media Player, classe Error
- Classe de erro do Windows Media Player, método clearErrorQueue
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789551"
---
# <a name="errorclearerrorqueue-method"></a><span data-ttu-id="43ce7-107">Erro. método clearErrorQueue</span><span class="sxs-lookup"><span data-stu-id="43ce7-107">Error.clearErrorQueue method</span></span>

<span data-ttu-id="43ce7-108">O método **clearErrorQueue** limpa os erros da fila de erros.</span><span class="sxs-lookup"><span data-stu-id="43ce7-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ce7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43ce7-109">Syntax</span></span>


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a><span data-ttu-id="43ce7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43ce7-110">Parameters</span></span>

<span data-ttu-id="43ce7-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="43ce7-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43ce7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43ce7-112">Return value</span></span>

<span data-ttu-id="43ce7-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="43ce7-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43ce7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="43ce7-114">Remarks</span></span>

<span data-ttu-id="43ce7-115">Esse método é útil para limpar a fila de erros depois que uma série de erros é processada.</span><span class="sxs-lookup"><span data-stu-id="43ce7-115">This method is useful to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="43ce7-116">Você deve definir *as configurações*. **enableErrorDialogs** como false se você optar por exibir mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="43ce7-116">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="43ce7-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="43ce7-117">Examples</span></span>

<span data-ttu-id="43ce7-118">O exemplo de JScript a seguir usa *erro*. **clearErrorQueue** em um manipulador de eventos para esvaziar a fila de erros após a exibição de todas as descrições de erro.</span><span class="sxs-lookup"><span data-stu-id="43ce7-118">The following JScript example uses *Error*.**clearErrorQueue** in an event handler to empty the error queue after all error descriptions are displayed.</span></span> <span data-ttu-id="43ce7-119">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="43ce7-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="43ce7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43ce7-120">Requirements</span></span>



| <span data-ttu-id="43ce7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="43ce7-121">Requirement</span></span> | <span data-ttu-id="43ce7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="43ce7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43ce7-123">Versão</span><span class="sxs-lookup"><span data-stu-id="43ce7-123">Version</span></span><br/> | <span data-ttu-id="43ce7-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="43ce7-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="43ce7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="43ce7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="43ce7-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43ce7-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43ce7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="43ce7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ce7-128">**Objeto Error**</span><span class="sxs-lookup"><span data-stu-id="43ce7-128">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





