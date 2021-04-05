---
description: O método SelectDefaultSubpictureLanguage define a linguagem de subimagem padrão atual no objeto MSWebDVD.
ms.assetid: e83980d1-c7cd-4755-9a27-3b0c2548009e
title: Método SelectDefaultSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d7dd4d66ae9d0580bf863ede9fff1e51d373e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645836"
---
# <a name="selectdefaultsubpicturelanguage-method"></a><span data-ttu-id="bfec2-103">Método SelectDefaultSubpictureLanguage</span><span class="sxs-lookup"><span data-stu-id="bfec2-103">SelectDefaultSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="bfec2-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bfec2-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="bfec2-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="bfec2-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="bfec2-106">O `SelectDefaultSubpictureLanguage` método define a linguagem de subimagem padrão atual no objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="bfec2-106">The `SelectDefaultSubpictureLanguage` method sets the current default subpicture language in the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a><span data-ttu-id="bfec2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfec2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfec2-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span><span class="sxs-lookup"><span data-stu-id="bfec2-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="bfec2-109">Especifica o idioma como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="bfec2-109">Specifies the language as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="bfec2-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span><span class="sxs-lookup"><span data-stu-id="bfec2-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="bfec2-111">Especifica a extensão de linguagem da subimagem como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="bfec2-111">Specifies the subpicture language extension as an Integer.</span></span>



| <span data-ttu-id="bfec2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="bfec2-112">Value</span></span> | <span data-ttu-id="bfec2-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfec2-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="bfec2-114">0</span><span class="sxs-lookup"><span data-stu-id="bfec2-114">0</span></span>     | <span data-ttu-id="bfec2-115">Extensão não especificada</span><span class="sxs-lookup"><span data-stu-id="bfec2-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="bfec2-116">1</span><span class="sxs-lookup"><span data-stu-id="bfec2-116">1</span></span>     | <span data-ttu-id="bfec2-117">Legendas normais</span><span class="sxs-lookup"><span data-stu-id="bfec2-117">Normal Captions</span></span>                |
| <span data-ttu-id="bfec2-118">2</span><span class="sxs-lookup"><span data-stu-id="bfec2-118">2</span></span>     | <span data-ttu-id="bfec2-119">Legendas grandes</span><span class="sxs-lookup"><span data-stu-id="bfec2-119">Big Captions</span></span>                   |
| <span data-ttu-id="bfec2-120">3</span><span class="sxs-lookup"><span data-stu-id="bfec2-120">3</span></span>     | <span data-ttu-id="bfec2-121">Legendas das crianças</span><span class="sxs-lookup"><span data-stu-id="bfec2-121">Children's Captions</span></span>            |
| <span data-ttu-id="bfec2-122">5</span><span class="sxs-lookup"><span data-stu-id="bfec2-122">5</span></span>     | <span data-ttu-id="bfec2-123">Legendas normais ocultas</span><span class="sxs-lookup"><span data-stu-id="bfec2-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="bfec2-124">6</span><span class="sxs-lookup"><span data-stu-id="bfec2-124">6</span></span>     | <span data-ttu-id="bfec2-125">Legendas grandes ocultas</span><span class="sxs-lookup"><span data-stu-id="bfec2-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="bfec2-126">7</span><span class="sxs-lookup"><span data-stu-id="bfec2-126">7</span></span>     | <span data-ttu-id="bfec2-127">Legendas ocultas de filhos</span><span class="sxs-lookup"><span data-stu-id="bfec2-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="bfec2-128">9</span><span class="sxs-lookup"><span data-stu-id="bfec2-128">9</span></span>     | <span data-ttu-id="bfec2-129">Forced (forçado)</span><span class="sxs-lookup"><span data-stu-id="bfec2-129">Forced</span></span>                         |
| <span data-ttu-id="bfec2-130">13</span><span class="sxs-lookup"><span data-stu-id="bfec2-130">13</span></span>    | <span data-ttu-id="bfec2-131">Comentários do diretor normal</span><span class="sxs-lookup"><span data-stu-id="bfec2-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="bfec2-132">14</span><span class="sxs-lookup"><span data-stu-id="bfec2-132">14</span></span>    | <span data-ttu-id="bfec2-133">Comentários do Big Director</span><span class="sxs-lookup"><span data-stu-id="bfec2-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="bfec2-134">15</span><span class="sxs-lookup"><span data-stu-id="bfec2-134">15</span></span>    | <span data-ttu-id="bfec2-135">Comentários de Director's dos filhos</span><span class="sxs-lookup"><span data-stu-id="bfec2-135">Children's Director's Comments</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfec2-136">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bfec2-136">Return Value</span></span>

<span data-ttu-id="bfec2-137">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="bfec2-137">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfec2-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfec2-138">Remarks</span></span>

<span data-ttu-id="bfec2-139">A extensão de linguagem de subimagem fornece mais informações sobre a subimagem.</span><span class="sxs-lookup"><span data-stu-id="bfec2-139">The subpicture language extension provides further information about the subpicture.</span></span>

 

 



