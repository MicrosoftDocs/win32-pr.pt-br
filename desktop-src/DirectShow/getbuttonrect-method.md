---
description: O método GetButtonRect recupera o retângulo para o botão especificado, em coordenadas de janela.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Método GetButtonRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087277"
---
# <a name="getbuttonrect-method"></a><span data-ttu-id="c8952-103">Método GetButtonRect</span><span class="sxs-lookup"><span data-stu-id="c8952-103">GetButtonRect Method</span></span>

> [!Note]  
> <span data-ttu-id="c8952-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c8952-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c8952-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c8952-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c8952-106">O `GetButtonRect` método recupera o retângulo para o botão especificado, em coordenadas de janela.</span><span class="sxs-lookup"><span data-stu-id="c8952-106">The `GetButtonRect` method retrieves the rectangle for the specified button, in window coordinates.</span></span>

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a><span data-ttu-id="c8952-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8952-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8952-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span><span class="sxs-lookup"><span data-stu-id="c8952-108"><span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*</span></span>
</dt> <dd>

<span data-ttu-id="c8952-109">Especifica o número do botão como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="c8952-109">Specifies the button number as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8952-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c8952-110">Return Value</span></span>

<span data-ttu-id="c8952-111">Retorna um objeto [DVDRect](dvdrect-object.md) que define o retângulo.</span><span class="sxs-lookup"><span data-stu-id="c8952-111">Returns a [DVDRect](dvdrect-object.md) object that defines the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8952-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8952-112">Remarks</span></span>

<span data-ttu-id="c8952-113">Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="c8952-113">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8952-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8952-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8952-115">**ButtonsAvailable**</span><span class="sxs-lookup"><span data-stu-id="c8952-115">**ButtonsAvailable**</span></span>](buttonsavailable-property.md)
</dt> <dt>

[<span data-ttu-id="c8952-116">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="c8952-116">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="c8952-117">**ActivateButton**</span><span class="sxs-lookup"><span data-stu-id="c8952-117">**ActivateButton**</span></span>](activatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="c8952-118">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="c8952-118">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="c8952-119">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="c8952-119">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



