---
description: O método SelectAtPosition seleciona o botão de menu nas coordenadas do ponteiro do mouse especificado.
ms.assetid: 005ec550-e04c-4dae-aa5d-d79afefe48ed
title: Método SelectAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97bc9feaa4855baac75fca0e776a26a6975b235a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645837"
---
# <a name="selectatposition-method"></a><span data-ttu-id="79382-103">Método SelectAtPosition</span><span class="sxs-lookup"><span data-stu-id="79382-103">SelectAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="79382-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="79382-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="79382-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="79382-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="79382-106">O `SelectAtPosition` método seleciona o botão de menu nas coordenadas do ponteiro do mouse especificado.</span><span class="sxs-lookup"><span data-stu-id="79382-106">The `SelectAtPosition` method selects the menu button at the specified mouse pointer coordinates.</span></span>

``` syntax
MSWebDVD.SelectAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="79382-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79382-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79382-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="79382-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="79382-109">Especifica a coordenada x como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="79382-109">Specifies the x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="79382-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="79382-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="79382-111">Especifica a coordenada y como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="79382-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79382-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="79382-112">Return Value</span></span>

<span data-ttu-id="79382-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="79382-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79382-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="79382-114">Remarks</span></span>

<span data-ttu-id="79382-115">Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="79382-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="79382-116">Selecionar meramente realça o botão.</span><span class="sxs-lookup"><span data-stu-id="79382-116">Selecting merely highlights the button.</span></span> <span data-ttu-id="79382-117">Para enviar o comando associado a um botão que foi selecionado, chame [**ActivateButton**](activatebutton-method.md).</span><span class="sxs-lookup"><span data-stu-id="79382-117">To send the command associated with a button that has been selected, call [**ActivateButton**](activatebutton-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="79382-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="79382-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79382-119">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="79382-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="79382-120">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="79382-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="79382-121">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="79382-121">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="79382-122">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="79382-122">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="79382-123">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="79382-123">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> </dl>

 

 



