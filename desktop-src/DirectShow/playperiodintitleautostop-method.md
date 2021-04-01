---
description: O método PlayPeriodInTitleAutoStop inicia a reprodução na hora especificada no título especificado até a hora de parada especificada.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Método PlayPeriodInTitleAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825694"
---
# <a name="playperiodintitleautostop-method"></a><span data-ttu-id="60f05-103">Método PlayPeriodInTitleAutoStop</span><span class="sxs-lookup"><span data-stu-id="60f05-103">PlayPeriodInTitleAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="60f05-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="60f05-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="60f05-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="60f05-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="60f05-106">O `PlayPeriodInTitleAutoStop` método inicia a reprodução na hora especificada no título especificado até a hora de parada especificada.</span><span class="sxs-lookup"><span data-stu-id="60f05-106">The `PlayPeriodInTitleAutoStop` method starts playback at the specified time in the specified title until the specified stop time.</span></span>

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a><span data-ttu-id="60f05-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60f05-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f05-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="60f05-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="60f05-109">Especifica o título como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="60f05-109">Specifies the title as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="60f05-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span><span class="sxs-lookup"><span data-stu-id="60f05-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span></span>
</dt> <dd>

<span data-ttu-id="60f05-111">Especifica a hora de início como uma cadeia de caracteres no formato "hh: mm: SS: FF" (especificando horas, minutos, segundos, quadros).</span><span class="sxs-lookup"><span data-stu-id="60f05-111">Specifies the start time as a string in "hh:mm:ss:ff" format (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="60f05-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*Enviartime*</span><span class="sxs-lookup"><span data-stu-id="60f05-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*</span></span>
</dt> <dd>

<span data-ttu-id="60f05-113">Especifica a hora de término como uma cadeia de caracteres no formato "hh: mm: SS: FF".</span><span class="sxs-lookup"><span data-stu-id="60f05-113">Specifies the end time as a String in "hh:mm:ss:ff" format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f05-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="60f05-114">Return Value</span></span>

<span data-ttu-id="60f05-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="60f05-115">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="60f05-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="60f05-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f05-117">**PlayChaptersAutoStop**</span><span class="sxs-lookup"><span data-stu-id="60f05-117">**PlayChaptersAutoStop**</span></span>](playchaptersautostop-method.md)
</dt> </dl>

 

 



