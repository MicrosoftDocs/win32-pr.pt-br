---
description: A propriedade VolumesAvailable recupera o número de volumes em um conjunto de vários volumes.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Propriedade VolumesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccdcf32ba8b7bea3958ef469bc0f90f9d41ecc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759895"
---
# <a name="volumesavailable-property"></a><span data-ttu-id="db8a1-103">Propriedade VolumesAvailable</span><span class="sxs-lookup"><span data-stu-id="db8a1-103">VolumesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="db8a1-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="db8a1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="db8a1-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="db8a1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="db8a1-106">A `VolumesAvailable` propriedade recupera o número de volumes em um conjunto de vários volumes.</span><span class="sxs-lookup"><span data-stu-id="db8a1-106">The `VolumesAvailable` property retrieves the number of volumes in a multivolume set.</span></span>

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a><span data-ttu-id="db8a1-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="db8a1-107">Return Value</span></span>

<span data-ttu-id="db8a1-108">Retorna o número de volumes no conjunto como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="db8a1-108">Returns the number of volumes in the set as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="db8a1-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="db8a1-109">Remarks</span></span>

<span data-ttu-id="db8a1-110">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="db8a1-110">This property is read-only with no default value.</span></span> <span data-ttu-id="db8a1-111">Alguns títulos de DVD podem ser lançados como um conjunto ou série de vários discos.</span><span class="sxs-lookup"><span data-stu-id="db8a1-111">Some DVD titles might be released as a multidisc set or series.</span></span> <span data-ttu-id="db8a1-112">Use esse método para determinar o número de volume do disco atual.</span><span class="sxs-lookup"><span data-stu-id="db8a1-112">Use this method to determine the volume number for the current disc.</span></span>

 

 



