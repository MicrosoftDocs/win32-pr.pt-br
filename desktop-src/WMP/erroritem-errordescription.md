---
title: ErrorItem. errorDescription
description: A propriedade errorDescription recupera uma descrição do erro.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- ErrorItem. errorDescription Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0de19bb67a5846a82e87d091f95a18cd12c5c2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759713"
---
# <a name="erroritemerrordescription"></a><span data-ttu-id="cbdfc-104">ErrorItem. errorDescription</span><span class="sxs-lookup"><span data-stu-id="cbdfc-104">ErrorItem.errorDescription</span></span>

<span data-ttu-id="cbdfc-105">A propriedade **errorDescription** recupera uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-105">The **errorDescription** property retrieves a description of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a><span data-ttu-id="cbdfc-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="cbdfc-106">Possible Values</span></span>

<span data-ttu-id="cbdfc-107">Esta propriedade é uma **cadeia de caracteres** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbdfc-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbdfc-108">Remarks</span></span>

<span data-ttu-id="cbdfc-109">Você deve definir *as configurações*. **enableErrorDialogs** como false se você optar por exibir mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="cbdfc-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cbdfc-110">Examples</span></span>

<span data-ttu-id="cbdfc-111">O exemplo de JScript a seguir usa *ErrorItem*. **errorDescription** em um manipulador de eventos para exibir a mensagem de erro para o usuário.</span><span class="sxs-lookup"><span data-stu-id="cbdfc-111">The following JScript example uses *ErrorItem*.**errorDescription** in an event handler to display the error message to the user.</span></span> <span data-ttu-id="cbdfc-112">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="cbdfc-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="cbdfc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbdfc-113">Requirements</span></span>



| <span data-ttu-id="cbdfc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbdfc-114">Requirement</span></span> | <span data-ttu-id="cbdfc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cbdfc-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cbdfc-116">Versão</span><span class="sxs-lookup"><span data-stu-id="cbdfc-116">Version</span></span><br/> | <span data-ttu-id="cbdfc-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cbdfc-117">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="cbdfc-118">DLL</span><span class="sxs-lookup"><span data-stu-id="cbdfc-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="cbdfc-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbdfc-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbdfc-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbdfc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbdfc-121">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="cbdfc-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





