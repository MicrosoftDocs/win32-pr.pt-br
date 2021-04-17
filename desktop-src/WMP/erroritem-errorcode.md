---
title: ErrorItem. errorCode
description: A propriedade errorCode recupera o código de erro atual.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- ErrorItem. errorCode Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c934b83b28e510f29b84a45b48bde700968c97b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759714"
---
# <a name="erroritemerrorcode"></a><span data-ttu-id="6b56b-104">ErrorItem. errorCode</span><span class="sxs-lookup"><span data-stu-id="6b56b-104">ErrorItem.errorCode</span></span>

<span data-ttu-id="6b56b-105">A propriedade **ErrorCode** recupera o código de erro atual.</span><span class="sxs-lookup"><span data-stu-id="6b56b-105">The **errorCode** property retrieves the current error code.</span></span>

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a><span data-ttu-id="6b56b-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6b56b-106">Possible Values</span></span>

<span data-ttu-id="6b56b-107">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="6b56b-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b56b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b56b-108">Remarks</span></span>

<span data-ttu-id="6b56b-109">Você deve definir *as configurações*. **enableErrorDialogs** como false se você optar por exibir mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6b56b-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="6b56b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6b56b-110">Examples</span></span>

<span data-ttu-id="6b56b-111">O exemplo de JScript a seguir usa *ErrorItem*. **ErrorCode** em um manipulador de eventos para exibir o código de erro para o usuário.</span><span class="sxs-lookup"><span data-stu-id="6b56b-111">The following JScript example uses *ErrorItem*.**errorCode** in an event handler to display the error code to the user.</span></span> <span data-ttu-id="6b56b-112">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6b56b-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="6b56b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b56b-113">Requirements</span></span>



| <span data-ttu-id="6b56b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b56b-114">Requirement</span></span> | <span data-ttu-id="6b56b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6b56b-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b56b-116">Versão</span><span class="sxs-lookup"><span data-stu-id="6b56b-116">Version</span></span><br/> | <span data-ttu-id="6b56b-117">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6b56b-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6b56b-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6b56b-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b56b-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b56b-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b56b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b56b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b56b-121">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="6b56b-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="6b56b-122">**ErrorItem. errorDescription**</span><span class="sxs-lookup"><span data-stu-id="6b56b-122">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> </dl>

 

 





