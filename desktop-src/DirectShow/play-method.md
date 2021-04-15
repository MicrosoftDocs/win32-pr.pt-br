---
description: O método Play reproduz o título do DVD atual.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Método play (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500361"
---
# <a name="play-method-directshow"></a><span data-ttu-id="b6ee1-103">Método play (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b6ee1-103">Play Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="b6ee1-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b6ee1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b6ee1-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b6ee1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b6ee1-106">O `Play` método reproduz o título do DVD atual.</span><span class="sxs-lookup"><span data-stu-id="b6ee1-106">The `Play` method plays the current DVD title.</span></span>

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a><span data-ttu-id="b6ee1-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b6ee1-107">Return Value</span></span>

<span data-ttu-id="b6ee1-108">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b6ee1-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6ee1-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6ee1-109">Remarks</span></span>

<span data-ttu-id="b6ee1-110">Se a reprodução for pausada ou interrompida e [**EnableResetOnStop**](enableresetonstop-property.md) for true, chamar **Play** retomará a reprodução em velocidade normal no local atual.</span><span class="sxs-lookup"><span data-stu-id="b6ee1-110">If playback is paused or stopped and [**EnableResetOnStop**](enableresetonstop-property.md) is true, then calling **Play** will resume playback at normal speed at the current location.</span></span> <span data-ttu-id="b6ee1-111">Se a reprodução for interrompida e **EnableResetOnStop** for false, chamar **Play** fará com que o disco comece a ser reproduzido no início do primeiro título.</span><span class="sxs-lookup"><span data-stu-id="b6ee1-111">If playback is stopped and **EnableResetOnStop** is false, then calling **Play** will cause the disc to start playing at the beginning of the first title.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6ee1-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6ee1-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ee1-113">**Retomar**</span><span class="sxs-lookup"><span data-stu-id="b6ee1-113">**Resume**</span></span>](resume-method.md)
</dt> </dl>

 

 



