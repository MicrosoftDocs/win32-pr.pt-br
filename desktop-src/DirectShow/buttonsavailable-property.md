---
description: A propriedade ButtonsAvailable recupera o número total de botões no menu atual.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Propriedade ButtonsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370266"
---
# <a name="buttonsavailable-property"></a><span data-ttu-id="c37ef-103">Propriedade ButtonsAvailable</span><span class="sxs-lookup"><span data-stu-id="c37ef-103">ButtonsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="c37ef-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c37ef-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c37ef-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c37ef-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c37ef-106">A `ButtonsAvailable` propriedade recupera o número total de botões no menu atual.</span><span class="sxs-lookup"><span data-stu-id="c37ef-106">The `ButtonsAvailable` property retrieves the total number of buttons on the current menu.</span></span>

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a><span data-ttu-id="c37ef-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c37ef-107">Return Value</span></span>

<span data-ttu-id="c37ef-108">Retorna um valor inteiro que representa o número de botões.</span><span class="sxs-lookup"><span data-stu-id="c37ef-108">Returns an integer value representing the number of buttons.</span></span>

## <a name="remarks"></a><span data-ttu-id="c37ef-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c37ef-109">Remarks</span></span>

<span data-ttu-id="c37ef-110">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="c37ef-110">This property is read-only with no default value.</span></span> <span data-ttu-id="c37ef-111">Use esse método ao implementar a manipulação de mouse personalizada depois de definir [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="c37ef-111">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="c37ef-112">Chame esse método para recuperar o limite superior do intervalo de números de botões válidos.</span><span class="sxs-lookup"><span data-stu-id="c37ef-112">Call this method to retrieve the upper limit for the range of valid button numbers.</span></span>

## <a name="see-also"></a><span data-ttu-id="c37ef-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="c37ef-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c37ef-114">**CurrentButton**</span><span class="sxs-lookup"><span data-stu-id="c37ef-114">**CurrentButton**</span></span>](currentbutton-property.md)
</dt> <dt>

[<span data-ttu-id="c37ef-115">**GetButtonAtPosition**</span><span class="sxs-lookup"><span data-stu-id="c37ef-115">**GetButtonAtPosition**</span></span>](getbuttonatposition-method.md)
</dt> <dt>

[<span data-ttu-id="c37ef-116">**GetButtonRect**</span><span class="sxs-lookup"><span data-stu-id="c37ef-116">**GetButtonRect**</span></span>](getbuttonrect-method.md)
</dt> <dt>

[<span data-ttu-id="c37ef-117">**SelectAndActivateButton**</span><span class="sxs-lookup"><span data-stu-id="c37ef-117">**SelectAndActivateButton**</span></span>](selectandactivatebutton-method.md)
</dt> <dt>

[<span data-ttu-id="c37ef-118">**SelectAtPosition**</span><span class="sxs-lookup"><span data-stu-id="c37ef-118">**SelectAtPosition**</span></span>](selectatposition-method.md)
</dt> </dl>

 

 



