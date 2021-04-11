---
description: A propriedade CurrentButton recupera o número do botão de menu selecionado.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Propriedade CurrentButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c12def9f9a73c9538781bde6940b03bfb376fcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296021"
---
# <a name="currentbutton-property"></a><span data-ttu-id="e1b80-103">Propriedade CurrentButton</span><span class="sxs-lookup"><span data-stu-id="e1b80-103">CurrentButton Property</span></span>

> [!Note]  
> <span data-ttu-id="e1b80-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e1b80-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e1b80-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e1b80-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e1b80-106">A `CurrentButton` propriedade recupera o número do botão de menu selecionado.</span><span class="sxs-lookup"><span data-stu-id="e1b80-106">The `CurrentButton` property retrieves the number of the selected menu button.</span></span>

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a><span data-ttu-id="e1b80-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e1b80-107">Return Value</span></span>

<span data-ttu-id="e1b80-108">Retorna um valor inteiro que representa o botão.</span><span class="sxs-lookup"><span data-stu-id="e1b80-108">Returns an integer value representing the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b80-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1b80-109">Remarks</span></span>

<span data-ttu-id="e1b80-110">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="e1b80-110">This property is read-only with no default value.</span></span> <span data-ttu-id="e1b80-111">Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="e1b80-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1b80-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1b80-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b80-113">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="e1b80-113">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="e1b80-114">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="e1b80-114">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="e1b80-115">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="e1b80-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="e1b80-116">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="e1b80-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="e1b80-117">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="e1b80-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="e1b80-118">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="e1b80-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



