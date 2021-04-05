---
description: O método IsSubpictureStreamEnabled recupera um valor que indica se o fluxo de subimagem especificado está habilitado no título atual.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Método IsSubpictureStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825942"
---
# <a name="issubpicturestreamenabled-method"></a><span data-ttu-id="9d13a-103">Método IsSubpictureStreamEnabled</span><span class="sxs-lookup"><span data-stu-id="9d13a-103">IsSubpictureStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="9d13a-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9d13a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9d13a-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="9d13a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9d13a-106">O `IsSubpictureStreamEnabled` método recupera um valor que indica se o fluxo de subimagem especificado está habilitado no título atual.</span><span class="sxs-lookup"><span data-stu-id="9d13a-106">The `IsSubpictureStreamEnabled` method retrieves a value indicating whether the specified subpicture stream is enabled in the current title.</span></span>

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="9d13a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d13a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d13a-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="9d13a-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="9d13a-109">Especifica o fluxo de subimagem como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="9d13a-109">Specifies the subpicture stream as an Integer.</span></span>



| <span data-ttu-id="9d13a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9d13a-110">Value</span></span>   | <span data-ttu-id="9d13a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d13a-111">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="9d13a-112">0 a 31</span><span class="sxs-lookup"><span data-stu-id="9d13a-112">0 to 31</span></span> | <span data-ttu-id="9d13a-113">fluxo de subimagem</span><span class="sxs-lookup"><span data-stu-id="9d13a-113">subpicture stream</span></span>        |
| <span data-ttu-id="9d13a-114">63</span><span class="sxs-lookup"><span data-stu-id="9d13a-114">63</span></span>      | <span data-ttu-id="9d13a-115">fluxo de baixa taxa de bits sem áudio</span><span class="sxs-lookup"><span data-stu-id="9d13a-115">muted low-bitrate stream</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d13a-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9d13a-116">Return Value</span></span>

<span data-ttu-id="9d13a-117">Retorna um valor booliano que indica se o fluxo de áudio especificado está disponível no título atual.</span><span class="sxs-lookup"><span data-stu-id="9d13a-117">Returns a Boolean value indicating whether the specified audio stream is available in the current title.</span></span> <span data-ttu-id="9d13a-118">Verdadeiro significa que está disponível.</span><span class="sxs-lookup"><span data-stu-id="9d13a-118">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d13a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d13a-119">Remarks</span></span>

<span data-ttu-id="9d13a-120">Embora um disco possa conter até 32 fluxos de subimagem, cada fluxo não está necessariamente disponível para cada título.</span><span class="sxs-lookup"><span data-stu-id="9d13a-120">Although a disc can contain up to 32 subpicture streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="9d13a-121">Sempre verifique se um fluxo está disponível para um título antes de definir a propriedade [**CurrentSubpictureStream**](currentsubpicturestream-property.md) .</span><span class="sxs-lookup"><span data-stu-id="9d13a-121">Always verify that a stream is available for a title before setting the [**CurrentSubpictureStream**](currentsubpicturestream-property.md) property.</span></span>

 

 



