---
description: A propriedade CurrentVolume recupera o número de volume para o diretório raiz atual.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Propriedade CurrentVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789649"
---
# <a name="currentvolume-property"></a><span data-ttu-id="7ff9d-103">Propriedade CurrentVolume</span><span class="sxs-lookup"><span data-stu-id="7ff9d-103">CurrentVolume Property</span></span>

> [!Note]  
> <span data-ttu-id="7ff9d-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7ff9d-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7ff9d-106">A `CurrentVolume` propriedade recupera o número de volume para o diretório raiz atual.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-106">The `CurrentVolume` property retrieves the volume number for the current root directory.</span></span>

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a><span data-ttu-id="7ff9d-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7ff9d-107">Return Value</span></span>

<span data-ttu-id="7ff9d-108">Retorna um valor inteiro que representa o volume de DVD atual.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-108">Returns an integer value representing the current DVD volume.</span></span> <span data-ttu-id="7ff9d-109">Se um disco fizer parte de um conjunto de vários volumes, o valor inteiro deverá ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-109">If a disc is part of a multi-volume set, then the integer value should be greater than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff9d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ff9d-110">Remarks</span></span>

<span data-ttu-id="7ff9d-111">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-111">This property is read-only with no default value.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ff9d-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ff9d-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff9d-113">**VolumesAvailable**</span><span class="sxs-lookup"><span data-stu-id="7ff9d-113">**VolumesAvailable**</span></span>](volumesavailable-property.md)
</dt> </dl>

 

 



