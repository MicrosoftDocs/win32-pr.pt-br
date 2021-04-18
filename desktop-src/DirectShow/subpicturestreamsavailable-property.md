---
description: A propriedade SubpictureStreamsAvailable recupera o número de fluxos de subimagem disponíveis no título atual.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Propriedade SubpictureStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758827"
---
# <a name="subpicturestreamsavailable-property"></a><span data-ttu-id="0c827-103">Propriedade SubpictureStreamsAvailable</span><span class="sxs-lookup"><span data-stu-id="0c827-103">SubpictureStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="0c827-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0c827-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0c827-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0c827-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0c827-106">A `SubpictureStreamsAvailable` propriedade recupera o número de fluxos de subimagem disponíveis no título atual.</span><span class="sxs-lookup"><span data-stu-id="0c827-106">The `SubpictureStreamsAvailable` property retrieves the number of subpicture streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="0c827-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0c827-107">Return Value</span></span>

<span data-ttu-id="0c827-108">Retorna o número de fluxos disponíveis como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="0c827-108">Returns the number of available streams as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c827-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c827-109">Remarks</span></span>

<span data-ttu-id="0c827-110">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="0c827-110">This property is read-only with no default value.</span></span> <span data-ttu-id="0c827-111">Para consultar cada fluxo para seu atributo de idioma, primeiro chame esse método para obter o limite superior.</span><span class="sxs-lookup"><span data-stu-id="0c827-111">To query each stream for its language attribute, first call this method to get the upper bound.</span></span>

<span data-ttu-id="0c827-112">A numeração de fluxo é baseada em zero.</span><span class="sxs-lookup"><span data-stu-id="0c827-112">Stream numbering is zero-based.</span></span>

 

 



