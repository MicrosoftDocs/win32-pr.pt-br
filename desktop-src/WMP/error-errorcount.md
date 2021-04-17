---
title: Erro. errorCount
description: A propriedade errorCount recupera o número de erros na fila de erros.
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- Erro. errorCount Windows Media Player
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94848023d2cd331545f97d3bea6d92f2fcd4b49c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762078"
---
# <a name="errorerrorcount"></a><span data-ttu-id="6de77-104">Erro. errorCount</span><span class="sxs-lookup"><span data-stu-id="6de77-104">Error.errorCount</span></span>

<span data-ttu-id="6de77-105">A propriedade **errorCount** recupera o número de erros na fila de erros.</span><span class="sxs-lookup"><span data-stu-id="6de77-105">The **errorCount** property retrieves the number of errors in the error queue.</span></span>

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a><span data-ttu-id="6de77-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6de77-106">Possible Values</span></span>

<span data-ttu-id="6de77-107">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="6de77-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="6de77-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6de77-108">Remarks</span></span>

<span data-ttu-id="6de77-109">Você deve definir *as configurações*. **enableErrorDialogs** como false se você optar por exibir mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6de77-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="6de77-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6de77-110">Examples</span></span>

<span data-ttu-id="6de77-111">O exemplo de JScript a seguir usa *erro*. **errorCount** em um manipulador de eventos para alertar o usuário sobre o erro mais recente na fila de erros.</span><span class="sxs-lookup"><span data-stu-id="6de77-111">The following JScript example uses *Error*.**errorCount** in an event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="6de77-112">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6de77-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="6de77-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6de77-113">Requirements</span></span>



| <span data-ttu-id="6de77-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6de77-114">Requirement</span></span> | <span data-ttu-id="6de77-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6de77-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6de77-116">Versão</span><span class="sxs-lookup"><span data-stu-id="6de77-116">Version</span></span><br/> | <span data-ttu-id="6de77-117">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6de77-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6de77-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6de77-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="6de77-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6de77-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de77-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6de77-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de77-121">**Objeto Error**</span><span class="sxs-lookup"><span data-stu-id="6de77-121">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





