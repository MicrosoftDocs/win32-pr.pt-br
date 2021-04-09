---
description: O método GetButtonAtPosition recupera o número do botão nas coordenadas especificadas sem selecioná-lo ou ativá-lo.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Método GetButtonAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087278"
---
# <a name="getbuttonatposition-method"></a><span data-ttu-id="4491e-103">Método GetButtonAtPosition</span><span class="sxs-lookup"><span data-stu-id="4491e-103">GetButtonAtPosition Method</span></span>

> [!Note]  
> <span data-ttu-id="4491e-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4491e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4491e-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="4491e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4491e-106">O `GetButtonAtPosition` método recupera o número do botão nas coordenadas especificadas sem selecioná-lo ou ativá-lo.</span><span class="sxs-lookup"><span data-stu-id="4491e-106">The `GetButtonAtPosition` method retrieves the number of the button at the specified coordinates without selecting or activating it.</span></span>

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a><span data-ttu-id="4491e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4491e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4491e-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="4491e-108"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="4491e-109">Especifica a coordenada x do ponteiro do mouse como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="4491e-109">Specifies the x-coordinate of the mouse pointer as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="4491e-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="4491e-110"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="4491e-111">Especifica a coordenada y do ponteiro do mouse como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="4491e-111">Specifies the y-coordinate of the mouse pointer as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4491e-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4491e-112">Return Value</span></span>

<span data-ttu-id="4491e-113">Retorna um valor inteiro especificando o botão, se houver, na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="4491e-113">Returns an integer value specifying the button, if any, at the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="4491e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4491e-114">Remarks</span></span>

<span data-ttu-id="4491e-115">Esse método retornará zero se nenhum botão estiver presente nas coordenadas fornecidas.</span><span class="sxs-lookup"><span data-stu-id="4491e-115">This method returns zero if no button is present at the given coordinates.</span></span> <span data-ttu-id="4491e-116">Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="4491e-116">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="4491e-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="4491e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4491e-118">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="4491e-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="4491e-119">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="4491e-119">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="4491e-120">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="4491e-120">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="4491e-121">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="4491e-121">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="4491e-122">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="4491e-122">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="4491e-123">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="4491e-123">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



