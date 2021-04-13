---
description: O método PlayBackwards inicia a reprodução regressiva do local atual na velocidade especificada.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Método PlayBackwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b396c3829569d3f3ad25f0c0e8718dfd23f268
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456343"
---
# <a name="playbackwards-method"></a><span data-ttu-id="7716c-103">Método PlayBackwards</span><span class="sxs-lookup"><span data-stu-id="7716c-103">PlayBackwards Method</span></span>

> [!Note]  
> <span data-ttu-id="7716c-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7716c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7716c-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7716c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7716c-106">O `PlayBackwards` método inicia a reprodução regressiva do local atual na velocidade especificada.</span><span class="sxs-lookup"><span data-stu-id="7716c-106">The `PlayBackwards` method starts backward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="7716c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7716c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7716c-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span><span class="sxs-lookup"><span data-stu-id="7716c-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="7716c-109">Especifica a velocidade na qual reproduzir como um número.</span><span class="sxs-lookup"><span data-stu-id="7716c-109">Specifies the speed at which to play as a number.</span></span> <span data-ttu-id="7716c-110">Esse número é um multiplicador – 1.0 é a velocidade de reprodução normal; 2,0 é a velocidade dupla, 0,5 é meia velocidade e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7716c-110">This number is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="7716c-111">Quando **nSpeed** não for igual a 1,0, o áudio ficará mudo e a subimagem será desativada.</span><span class="sxs-lookup"><span data-stu-id="7716c-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7716c-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7716c-112">Return Value</span></span>

<span data-ttu-id="7716c-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="7716c-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="7716c-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="7716c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7716c-115">**PlayForwards**</span><span class="sxs-lookup"><span data-stu-id="7716c-115">**PlayForwards**</span></span>](playforwards-method.md)
</dt> </dl>

 

 



