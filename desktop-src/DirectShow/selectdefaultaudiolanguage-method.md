---
description: O método SelectDefaultAudioLanguage define o idioma de áudio padrão atual no objeto MSWebDVD.
ms.assetid: 7d63b7ef-2b03-4929-822a-c4d11fb7a825
title: Método SelectDefaultAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 126de6daf4f5e0337058495a3ee7898594bfd704
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500356"
---
# <a name="selectdefaultaudiolanguage-method"></a><span data-ttu-id="b2a84-103">Método SelectDefaultAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="b2a84-103">SelectDefaultAudioLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="b2a84-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b2a84-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b2a84-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b2a84-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b2a84-106">O `SelectDefaultAudioLanguage` método define o idioma de áudio padrão atual no objeto mswebdvd.</span><span class="sxs-lookup"><span data-stu-id="b2a84-106">The `SelectDefaultAudioLanguage` method sets the current default audio language in the MSWebDVD object.</span></span>

``` syntax
MSWebDVD.SelectDefaultAudioLanguage(iLang, iExt)
```

## <a name="parameters"></a><span data-ttu-id="b2a84-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2a84-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2a84-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span><span class="sxs-lookup"><span data-stu-id="b2a84-108"><span id="iLang"></span><span id="ilang"></span><span id="ILANG"></span>*iLang*</span></span>
</dt> <dd>

<span data-ttu-id="b2a84-109">Especifica o idioma como um valor LCID inteiro.</span><span class="sxs-lookup"><span data-stu-id="b2a84-109">Specifies the language as an Integer LCID value.</span></span>

</dd> <dt>

<span data-ttu-id="b2a84-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span><span class="sxs-lookup"><span data-stu-id="b2a84-110"><span id="iExt"></span><span id="iext"></span><span id="IEXT"></span>*iExt*</span></span>
</dt> <dd>

<span data-ttu-id="b2a84-111">Especifica a extensão do idioma de áudio do DVD como um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="b2a84-111">Specifies the DVD audio language extension as an integer value.</span></span>



| <span data-ttu-id="b2a84-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b2a84-112">Value</span></span> | <span data-ttu-id="b2a84-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2a84-113">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="b2a84-114">0</span><span class="sxs-lookup"><span data-stu-id="b2a84-114">0</span></span>     | <span data-ttu-id="b2a84-115">NotSpecified</span><span class="sxs-lookup"><span data-stu-id="b2a84-115">NotSpecified</span></span>      |
| <span data-ttu-id="b2a84-116">1</span><span class="sxs-lookup"><span data-stu-id="b2a84-116">1</span></span>     | <span data-ttu-id="b2a84-117">Legendas</span><span class="sxs-lookup"><span data-stu-id="b2a84-117">Captions</span></span>          |
| <span data-ttu-id="b2a84-118">2</span><span class="sxs-lookup"><span data-stu-id="b2a84-118">2</span></span>     | <span data-ttu-id="b2a84-119">VisuallyImpaired</span><span class="sxs-lookup"><span data-stu-id="b2a84-119">VisuallyImpaired</span></span>  |
| <span data-ttu-id="b2a84-120">3</span><span class="sxs-lookup"><span data-stu-id="b2a84-120">3</span></span>     | <span data-ttu-id="b2a84-121">DirectorComments1</span><span class="sxs-lookup"><span data-stu-id="b2a84-121">DirectorComments1</span></span> |
| <span data-ttu-id="b2a84-122">4</span><span class="sxs-lookup"><span data-stu-id="b2a84-122">4</span></span>     | <span data-ttu-id="b2a84-123">DirectorComments2</span><span class="sxs-lookup"><span data-stu-id="b2a84-123">DirectorComments2</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2a84-124">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b2a84-124">Return Value</span></span>

<span data-ttu-id="b2a84-125">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b2a84-125">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2a84-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2a84-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2a84-127">Objeto MSWebDVD</span><span class="sxs-lookup"><span data-stu-id="b2a84-127">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



