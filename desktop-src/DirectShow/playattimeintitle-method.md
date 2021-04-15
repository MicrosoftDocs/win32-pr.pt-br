---
description: O método PlayAtTimeInTitle inicia a reprodução na hora especificada dentro do título especificado.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: Método PlayAtTimeInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c40373b4327b6df5fc341ca392c223d464a70a8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456344"
---
# <a name="playattimeintitle-method"></a><span data-ttu-id="21254-103">Método PlayAtTimeInTitle</span><span class="sxs-lookup"><span data-stu-id="21254-103">PlayAtTimeInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="21254-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="21254-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="21254-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="21254-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="21254-106">O `PlayAtTimeInTitle` método inicia a reprodução na hora especificada dentro do título especificado.</span><span class="sxs-lookup"><span data-stu-id="21254-106">The `PlayAtTimeInTitle` method starts playback at the specified time within the specified title.</span></span>

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a><span data-ttu-id="21254-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21254-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21254-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span><span class="sxs-lookup"><span data-stu-id="21254-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span></span>
</dt> <dd>

<span data-ttu-id="21254-109">Especifica a hora na qual iniciar a reprodução como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="21254-109">Specifies the time at which to start playback as a string.</span></span> <span data-ttu-id="21254-110">A cadeia de caracteres deve estar no formato "hh: mm: SS: FF" (especificando horas, minutos, segundos, quadros).</span><span class="sxs-lookup"><span data-stu-id="21254-110">The string must be in the format "hh:mm:ss:ff" (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="21254-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="21254-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="21254-112">Especifica o índice do título como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="21254-112">Specifies the index of the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21254-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="21254-113">Return Value</span></span>

<span data-ttu-id="21254-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="21254-114">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="21254-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="21254-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21254-116">**CurrentTitle**</span><span class="sxs-lookup"><span data-stu-id="21254-116">**CurrentTitle**</span></span>](currenttitle-property.md)
</dt> <dt>

[<span data-ttu-id="21254-117">**PlayAtTime**</span><span class="sxs-lookup"><span data-stu-id="21254-117">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="21254-118">**TitlesAvailable**</span><span class="sxs-lookup"><span data-stu-id="21254-118">**TitlesAvailable**</span></span>](titlesavailable-property.md)
</dt> </dl>

 

 



