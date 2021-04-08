---
description: A propriedade TotalTitleTime recupera o tempo de reprodução total para o título atual.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Propriedade TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828724"
---
# <a name="totaltitletime-property"></a><span data-ttu-id="3ca42-103">Propriedade TotalTitleTime</span><span class="sxs-lookup"><span data-stu-id="3ca42-103">TotalTitleTime Property</span></span>

> [!Note]  
> <span data-ttu-id="3ca42-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3ca42-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3ca42-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="3ca42-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3ca42-106">A `TotalTitleTime` propriedade recupera o tempo total de reprodução para o título atual.</span><span class="sxs-lookup"><span data-stu-id="3ca42-106">The `TotalTitleTime` property retrieves the total playback time for the current title.</span></span>

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a><span data-ttu-id="3ca42-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3ca42-107">Return Value</span></span>

<span data-ttu-id="3ca42-108">Retorna o tempo de execução total do título atual como uma cadeia de caracteres no formato "hh: mm: SS: FF".</span><span class="sxs-lookup"><span data-stu-id="3ca42-108">Returns the total playing time of the current title as a String in the format "hh:mm:ss:ff".</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca42-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ca42-109">Remarks</span></span>

<span data-ttu-id="3ca42-110">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="3ca42-110">This property is read-only with no default value.</span></span> <span data-ttu-id="3ca42-111">A cadeia de caracteres retornada terá 11 caracteres de comprimento no formato "hh: mm: SS: FF" (horas, minutos, segundos, quadros).</span><span class="sxs-lookup"><span data-stu-id="3ca42-111">The returned string will be 11 characters long in the format "hh:mm:ss:ff" (hours, minutes, seconds, frames).</span></span>

## <a name="see-also"></a><span data-ttu-id="3ca42-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ca42-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ca42-113">**PlayAtTime**</span><span class="sxs-lookup"><span data-stu-id="3ca42-113">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="3ca42-114">**PlayAtTimeInTitle**</span><span class="sxs-lookup"><span data-stu-id="3ca42-114">**PlayAtTimeInTitle**</span></span>](playattimeintitle-method.md)
</dt> </dl>

 

 



