---
description: O método ActivateAtPosition ativa o botão de menu na posição especificada.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Método ActivateAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a83e7fcbc00990c7be7d1a99638a1b4a3de14b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087875"
---
# <a name="activateatposition-method"></a><span data-ttu-id="b32cf-103">Método ActivateAtPosition</span><span class="sxs-lookup"><span data-stu-id="b32cf-103">ActivateAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="b32cf-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b32cf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b32cf-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b32cf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b32cf-106">O método ActivateAtPosition ativa o botão de menu na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="b32cf-106">The ActivateAtPosition method activates the menu button at the specified position.</span></span>

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="b32cf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b32cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b32cf-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="b32cf-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="b32cf-109">Especifica a coordenada x como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="b32cf-109">Specifies x-coordinate as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="b32cf-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="b32cf-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="b32cf-111">Especifica a coordenada y como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="b32cf-111">Specifies the y-coordinate as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b32cf-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b32cf-112">Return Value</span></span>

<span data-ttu-id="b32cf-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b32cf-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b32cf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b32cf-114">Remarks</span></span>

<span data-ttu-id="b32cf-115">Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="b32cf-115">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b32cf-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="b32cf-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b32cf-117">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="b32cf-117">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="b32cf-118">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="b32cf-118">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="b32cf-119">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="b32cf-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="b32cf-120">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="b32cf-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="b32cf-121">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="b32cf-121">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="b32cf-122">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="b32cf-122">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



