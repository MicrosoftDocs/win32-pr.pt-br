---
description: O método SelectAndActivateButton seleciona e ativa o botão especificado.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Método SelectAndActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717af00becd5f00f55b166353246f92ea7dfd1bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105768780"
---
# <a name="selectandactivatebutton-method"></a><span data-ttu-id="e972f-103">Método SelectAndActivateButton</span><span class="sxs-lookup"><span data-stu-id="e972f-103">SelectAndActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="e972f-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e972f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e972f-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e972f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e972f-106">O `SelectAndActivateButton` método seleciona e ativa o botão especificado.</span><span class="sxs-lookup"><span data-stu-id="e972f-106">The `SelectAndActivateButton` method selects and activates the specified button.</span></span>

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a><span data-ttu-id="e972f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e972f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e972f-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="e972f-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="e972f-109">Especifica o botão como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="e972f-109">Specifies the button as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e972f-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e972f-110">Return Value</span></span>

<span data-ttu-id="e972f-111">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e972f-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e972f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e972f-112">Remarks</span></span>

<span data-ttu-id="e972f-113">Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="e972f-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="e972f-114">Esse método realça o botão especificado e o ativa automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e972f-114">This method highlights the specified button and activate it automatically.</span></span>

## <a name="see-also"></a><span data-ttu-id="e972f-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="e972f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e972f-116">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="e972f-116">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="e972f-117">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="e972f-117">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="e972f-118">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="e972f-118">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="e972f-119">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="e972f-119">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="e972f-120">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="e972f-120">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="e972f-121">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="e972f-121">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



