---
description: A propriedade DefaultSubpictureLanguageExt recupera a extensão de linguagem de subimagem de DVD padrão.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Propriedade DefaultSubpictureLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500224"
---
# <a name="defaultsubpicturelanguageext-property"></a><span data-ttu-id="79bbe-103">Propriedade DefaultSubpictureLanguageExt</span><span class="sxs-lookup"><span data-stu-id="79bbe-103">DefaultSubpictureLanguageExt Property</span></span>

> [!Note]  
> <span data-ttu-id="79bbe-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="79bbe-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="79bbe-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="79bbe-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="79bbe-106">A `DefaultSubpictureLanguageExt` propriedade recupera a extensão de linguagem de subimagem do DVD padrão.</span><span class="sxs-lookup"><span data-stu-id="79bbe-106">The `DefaultSubpictureLanguageExt` property retrieves the default DVD subpicture language extension.</span></span>

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a><span data-ttu-id="79bbe-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="79bbe-107">Return Value</span></span>

<span data-ttu-id="79bbe-108">Retorna um valor inteiro que indica a extensão de linguagem de subimagem do DVD padrão.</span><span class="sxs-lookup"><span data-stu-id="79bbe-108">Returns an Integer value indicating the default DVD subpicture language extension.</span></span>

## <a name="remarks"></a><span data-ttu-id="79bbe-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="79bbe-109">Remarks</span></span>

<span data-ttu-id="79bbe-110">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="79bbe-110">This property is read-only with no default value.</span></span> <span data-ttu-id="79bbe-111">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="79bbe-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="79bbe-112">Valor</span><span class="sxs-lookup"><span data-stu-id="79bbe-112">Value</span></span> | <span data-ttu-id="79bbe-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="79bbe-113">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="79bbe-114">0</span><span class="sxs-lookup"><span data-stu-id="79bbe-114">0</span></span>     | <span data-ttu-id="79bbe-115">Extensão não especificada</span><span class="sxs-lookup"><span data-stu-id="79bbe-115">Extension Not Specified</span></span>        |
| <span data-ttu-id="79bbe-116">1</span><span class="sxs-lookup"><span data-stu-id="79bbe-116">1</span></span>     | <span data-ttu-id="79bbe-117">Legendas normais</span><span class="sxs-lookup"><span data-stu-id="79bbe-117">Normal Captions</span></span>                |
| <span data-ttu-id="79bbe-118">2</span><span class="sxs-lookup"><span data-stu-id="79bbe-118">2</span></span>     | <span data-ttu-id="79bbe-119">Legendas grandes</span><span class="sxs-lookup"><span data-stu-id="79bbe-119">Big Captions</span></span>                   |
| <span data-ttu-id="79bbe-120">3</span><span class="sxs-lookup"><span data-stu-id="79bbe-120">3</span></span>     | <span data-ttu-id="79bbe-121">Legendas das crianças</span><span class="sxs-lookup"><span data-stu-id="79bbe-121">Children's Captions</span></span>            |
| <span data-ttu-id="79bbe-122">5</span><span class="sxs-lookup"><span data-stu-id="79bbe-122">5</span></span>     | <span data-ttu-id="79bbe-123">Legendas normais ocultas</span><span class="sxs-lookup"><span data-stu-id="79bbe-123">Normal Closed Captions</span></span>         |
| <span data-ttu-id="79bbe-124">6</span><span class="sxs-lookup"><span data-stu-id="79bbe-124">6</span></span>     | <span data-ttu-id="79bbe-125">Legendas grandes ocultas</span><span class="sxs-lookup"><span data-stu-id="79bbe-125">Big Closed Captions</span></span>            |
| <span data-ttu-id="79bbe-126">7</span><span class="sxs-lookup"><span data-stu-id="79bbe-126">7</span></span>     | <span data-ttu-id="79bbe-127">Legendas ocultas de filhos</span><span class="sxs-lookup"><span data-stu-id="79bbe-127">Children's Closed Captions</span></span>     |
| <span data-ttu-id="79bbe-128">9</span><span class="sxs-lookup"><span data-stu-id="79bbe-128">9</span></span>     | <span data-ttu-id="79bbe-129">Forced (forçado)</span><span class="sxs-lookup"><span data-stu-id="79bbe-129">Forced</span></span>                         |
| <span data-ttu-id="79bbe-130">13</span><span class="sxs-lookup"><span data-stu-id="79bbe-130">13</span></span>    | <span data-ttu-id="79bbe-131">Comentários do diretor normal</span><span class="sxs-lookup"><span data-stu-id="79bbe-131">Normal Director's Comments</span></span>     |
| <span data-ttu-id="79bbe-132">14</span><span class="sxs-lookup"><span data-stu-id="79bbe-132">14</span></span>    | <span data-ttu-id="79bbe-133">Comentários do Big Director</span><span class="sxs-lookup"><span data-stu-id="79bbe-133">Big Director's Comments</span></span>        |
| <span data-ttu-id="79bbe-134">15</span><span class="sxs-lookup"><span data-stu-id="79bbe-134">15</span></span>    | <span data-ttu-id="79bbe-135">Comentários de Director's dos filhos</span><span class="sxs-lookup"><span data-stu-id="79bbe-135">Children's Director's Comments</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="79bbe-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="79bbe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79bbe-137">**SelectDefaultSubpictureLanguage**</span><span class="sxs-lookup"><span data-stu-id="79bbe-137">**SelectDefaultSubpictureLanguage**</span></span>](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



