---
description: O método PlayForwards começa a enviar a reprodução do local atual na velocidade especificada.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Método PlayForwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645973"
---
# <a name="playforwards-method"></a><span data-ttu-id="d6812-103">Método PlayForwards</span><span class="sxs-lookup"><span data-stu-id="d6812-103">PlayForwards Method</span></span>

> [!Note]  
> <span data-ttu-id="d6812-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d6812-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d6812-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d6812-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d6812-106">O `PlayForwards` método começa a redirecionar a reprodução do local atual na velocidade especificada.</span><span class="sxs-lookup"><span data-stu-id="d6812-106">The `PlayForwards` method starts forward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="d6812-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6812-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6812-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span><span class="sxs-lookup"><span data-stu-id="d6812-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="d6812-109">Especifica a velocidade na qual reproduzir como um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="d6812-109">Specifies the speed at which to play as an Integer value.</span></span> <span data-ttu-id="d6812-110">Esse valor é um multiplicador — 1,0 é a velocidade de reprodução normal; 2,0 é a velocidade dupla, 0,5 é meia velocidade e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d6812-110">This value is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="d6812-111">Quando **nSpeed** não for igual a 1,0, o áudio ficará mudo e a subimagem será desativada.</span><span class="sxs-lookup"><span data-stu-id="d6812-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6812-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d6812-112">Return Value</span></span>

<span data-ttu-id="d6812-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d6812-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6812-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6812-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6812-115">**PlayBackwards**</span><span class="sxs-lookup"><span data-stu-id="d6812-115">**PlayBackwards**</span></span>](playbackwards-method.md)
</dt> </dl>

 

 



