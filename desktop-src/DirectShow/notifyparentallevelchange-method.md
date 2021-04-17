---
description: O método NotifyParentalLevelChange habilita ou desabilita a manipulação de eventos para comandos temporários de nível de gerenciamento pai.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Método NotifyParentalLevelChange (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759433"
---
# <a name="notifyparentallevelchange-method"></a><span data-ttu-id="cf7f3-103">Método NotifyParentalLevelChange</span><span class="sxs-lookup"><span data-stu-id="cf7f3-103">NotifyParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="cf7f3-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cf7f3-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cf7f3-106">O `NotifyParentalLevelChange` método habilita ou desabilita a manipulação de eventos para comandos temporários de nível de gerenciamento pai.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-106">The `NotifyParentalLevelChange` method enables or disables the event handling for temporary parental management level commands.</span></span>

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a><span data-ttu-id="cf7f3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf7f3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf7f3-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span><span class="sxs-lookup"><span data-stu-id="cf7f3-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span></span>
</dt> <dd>

<span data-ttu-id="cf7f3-109">Especifica um valor booliano que indica se o aplicativo será notificado quando o objeto MSWebDVD encontrar segmentos de vídeo com uma classificação mais restritiva do que a classificação geral do disco.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-109">Specifies a Boolean value indicating whether or not the application is notified when the MSWebDVD object encounters video segments with a rating more restrictive than the overall rating for the disc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf7f3-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cf7f3-110">Return Value</span></span>

<span data-ttu-id="cf7f3-111">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf7f3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf7f3-112">Remarks</span></span>

<span data-ttu-id="cf7f3-113">As notificações de gerenciamento de pais são desabilitadas por padrão.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-113">Parental management notifications are disabled by default.</span></span> <span data-ttu-id="cf7f3-114">Isso significa que os comandos temporários dos pais do disco são permitidos, mas ignorados e o disco será reproduzido sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-114">This means that temporary parental commands from the disc are allowed but ignored and disc will play without interruption.</span></span> <span data-ttu-id="cf7f3-115">Chame esse método durante a inicialização do seu aplicativo se você precisar manipular comandos temporários no nível de gerenciamento pai do disco. Para desabilitar o gerenciamento de pais depois que ele estiver habilitado, chame esse método com um argumento de false.</span><span class="sxs-lookup"><span data-stu-id="cf7f3-115">Call this method during initialization of your application if you need to handle temporary parental management level commands from the disc. To disable parental management after it is enabled, call this method with an argument of false.</span></span> <span data-ttu-id="cf7f3-116">Para obter mais detalhes sobre o gerenciamento de pais, consulte [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).</span><span class="sxs-lookup"><span data-stu-id="cf7f3-116">For more details on parental management, see [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf7f3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf7f3-117">Requirements</span></span>



| <span data-ttu-id="cf7f3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf7f3-118">Requirement</span></span> | <span data-ttu-id="cf7f3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cf7f3-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7f3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf7f3-120">Header</span></span><br/> | <dl> <span data-ttu-id="cf7f3-121"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf7f3-121"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf7f3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf7f3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf7f3-123">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-123">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-124">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-125">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-125">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-126">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-126">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="cf7f3-127">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="cf7f3-127">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 




