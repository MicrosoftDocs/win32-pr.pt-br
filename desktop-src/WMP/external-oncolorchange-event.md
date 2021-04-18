---
title: Evento external. OnColorChange
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnColorChange
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Evento external. OnColorChange do Windows Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029c8bb860443ed026737c7413be2bed8862c6d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788162"
---
# <a name="externaloncolorchange-event"></a><span data-ttu-id="02dfc-105">Evento external. OnColorChange</span><span class="sxs-lookup"><span data-stu-id="02dfc-105">External.OnColorChange Event</span></span>

> [!Note]  
> <span data-ttu-id="02dfc-106">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="02dfc-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="02dfc-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="02dfc-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="02dfc-108">O evento **OnColorChange** ocorre quando a cor da interface do usuário do Windows Media Player é alterada.</span><span class="sxs-lookup"><span data-stu-id="02dfc-108">The **OnColorChange** event occurs when the color of the Windows Media Player user interface changes.</span></span>

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="02dfc-109">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="02dfc-109">Possible Values</span></span>

<span data-ttu-id="02dfc-110">Essa é uma propriedade somente gravação que especifica o nome da função no script que o Windows Media Player chama quando o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="02dfc-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="02dfc-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02dfc-111">Parameters</span></span>

<span data-ttu-id="02dfc-112">A função que manipula esse evento não usa parâmetros.</span><span class="sxs-lookup"><span data-stu-id="02dfc-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="02dfc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="02dfc-113">Remarks</span></span>

<span data-ttu-id="02dfc-114">Os usuários podem alterar a cor da interface do usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="02dfc-114">Users can change the color of the Windows Media Player user interface.</span></span> <span data-ttu-id="02dfc-115">Você pode usar esse evento para personalizar a aparência da página da web hospedada para corresponder ao Player.</span><span class="sxs-lookup"><span data-stu-id="02dfc-115">You can use this event to customize the appearance of your hosted webpage to match the Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="02dfc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02dfc-116">Requirements</span></span>



| <span data-ttu-id="02dfc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="02dfc-117">Requirement</span></span> | <span data-ttu-id="02dfc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="02dfc-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02dfc-119">Versão</span><span class="sxs-lookup"><span data-stu-id="02dfc-119">Version</span></span><br/> | <span data-ttu-id="02dfc-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="02dfc-120">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="02dfc-121">DLL</span><span class="sxs-lookup"><span data-stu-id="02dfc-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="02dfc-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02dfc-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02dfc-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="02dfc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02dfc-124">**Objeto externo para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="02dfc-124">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





