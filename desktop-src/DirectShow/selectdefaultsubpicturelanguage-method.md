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
# <a name="selectdefaultsubpicturelanguage-method"></a><span data-ttu-id="8c01f-103">Método SelectDefaultSubpictureLanguage</span><span class="sxs-lookup"><span data-stu-id="8c01f-103">SelectDefaultSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="8c01f-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8c01f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8c01f-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="8c01f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8c01f-106">O `SelectDefaultSubpictureLanguage` método define a linguagem de subimagem padrão atual no objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="8c01f-106">The `SelectDefaultSubpictureLanguage` method sets the current default subpicture language in the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SelectDefaultSubpictureLanguage(iLang,iExt)
```

## <a name="parameters"></a><span data-ttu-id="8c01f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c01f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c01f-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span><span class="sxs-lookup"><span data-stu-id="8c01f-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="8c01f-109">Especifica o idioma como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="8c01f-109">Specifies the language as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="8c01f-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span><span class="sxs-lookup"><span data-stu-id="8c01f-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="8c01f-111">Especifica a extensão de linguagem da subimagem como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="8c01f-111">Specifies the subpicture language extension as an Integer.</span></span>



| <span data-ttu-id="8c01f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="8c01f-112">Value</span></span> | <span data-ttu-id="8c01f-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c01f-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="8c01f-114">0</span><span class="sxs-lookup"><span data-stu-id="8c01f-114">0</span></span>     | <span data-ttu-id="8c01f-115">Extensão não especificada</span><span class="sxs-lookup"><span data-stu-id="8c01f-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="8c01f-116">1</span><span class="sxs-lookup"><span data-stu-id="8c01f-116">1</span></span>     | <span data-ttu-id="8c01f-117">Legendas normais</span><span class="sxs-lookup"><span data-stu-id="8c01f-117">Normal Captions</span></span>                |
| <span data-ttu-id="8c01f-118">2</span><span class="sxs-lookup"><span data-stu-id="8c01f-118">2</span></span>     | <span data-ttu-id="8c01f-119">Legendas grandes</span><span class="sxs-lookup"><span data-stu-id="8c01f-119">Big Captions</span></span>                   |
| <span data-ttu-id="8c01f-120">3</span><span class="sxs-lookup"><span data-stu-id="8c01f-120">3</span></span>     | <span data-ttu-id="8c01f-121">Legendas das crianças</span><span class="sxs-lookup"><span data-stu-id="8c01f-121">Children's Captions</span></span>            |
| <span data-ttu-id="8c01f-122">5</span><span class="sxs-lookup"><span data-stu-id="8c01f-122">5</span></span>     | <span data-ttu-id="8c01f-123">Legendas normais ocultas</span><span class="sxs-lookup"><span data-stu-id="8c01f-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="8c01f-124">6</span><span class="sxs-lookup"><span data-stu-id="8c01f-124">6</span></span>     | <span data-ttu-id="8c01f-125">Legendas grandes ocultas</span><span class="sxs-lookup"><span data-stu-id="8c01f-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="8c01f-126">7</span><span class="sxs-lookup"><span data-stu-id="8c01f-126">7</span></span>     | <span data-ttu-id="8c01f-127">Legendas ocultas de filhos</span><span class="sxs-lookup"><span data-stu-id="8c01f-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="8c01f-128">9</span><span class="sxs-lookup"><span data-stu-id="8c01f-128">9</span></span>     | <span data-ttu-id="8c01f-129">Forced (forçado)</span><span class="sxs-lookup"><span data-stu-id="8c01f-129">Forced</span></span>                         |
| <span data-ttu-id="8c01f-130">13</span><span class="sxs-lookup"><span data-stu-id="8c01f-130">13</span></span>    | <span data-ttu-id="8c01f-131">Comentários do diretor normal</span><span class="sxs-lookup"><span data-stu-id="8c01f-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="8c01f-132">14</span><span class="sxs-lookup"><span data-stu-id="8c01f-132">14</span></span>    | <span data-ttu-id="8c01f-133">Comentários do Big Director</span><span class="sxs-lookup"><span data-stu-id="8c01f-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="8c01f-134">15</span><span class="sxs-lookup"><span data-stu-id="8c01f-134">15</span></span>    | <span data-ttu-id="8c01f-135">Comentários de Director's dos filhos</span><span class="sxs-lookup"><span data-stu-id="8c01f-135">Children's Director's Comments</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c01f-136">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8c01f-136">Return Value</span></span>

<span data-ttu-id="8c01f-137">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="8c01f-137">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c01f-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c01f-138">Remarks</span></span>

<span data-ttu-id="8c01f-139">A extensão de linguagem de subimagem fornece mais informações sobre a subimagem.</span><span class="sxs-lookup"><span data-stu-id="8c01f-139">The subpicture language extension provides further information about the subpicture.</span></span>

 

 



