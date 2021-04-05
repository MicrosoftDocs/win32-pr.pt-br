---
description: A propriedade PreferredSubpictureStream recupera o fluxo de subimagem preferencial para a sessão de exibição atual.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Propriedade PreferredSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23377d74d3632c665b001ae415dc151ca73bd148
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825766"
---
# <a name="preferredsubpicturestream-property"></a><span data-ttu-id="12316-103">Propriedade PreferredSubpictureStream</span><span class="sxs-lookup"><span data-stu-id="12316-103">PreferredSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="12316-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="12316-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="12316-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="12316-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="12316-106">A `PreferredSubpictureStream` propriedade recupera o fluxo de subimagem preferencial para a sessão de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="12316-106">The `PreferredSubpictureStream` property retrieves the preferred subpicture stream for the current viewing session.</span></span>

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="12316-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="12316-107">Return Value</span></span>

<span data-ttu-id="12316-108">Retorna um valor inteiro que representa o fluxo de subimagem preferencial atual no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="12316-108">Returns an Integer value representing the current preferred subpicture stream in the system registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="12316-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="12316-109">Remarks</span></span>

<span data-ttu-id="12316-110">O fluxo de subimagem preferencial é definido com [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)do objeto [MSDVDAdm](msdvdadm-object.md) .</span><span class="sxs-lookup"><span data-stu-id="12316-110">The preferred subpicture stream is set with [MSDVDAdm](msdvdadm-object.md) object's [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md).</span></span>

 

 



