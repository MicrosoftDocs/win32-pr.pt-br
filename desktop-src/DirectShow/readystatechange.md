---
description: O evento ReadyStateChange é enviado quando a propriedade ReadyState do controle MSWebDVD é alterada.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500549"
---
# <a name="readystatechange"></a><span data-ttu-id="00758-103">ReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="00758-103">ReadyStateChange</span></span>

> [!Note]  
> <span data-ttu-id="00758-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="00758-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="00758-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="00758-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="00758-106">O `ReadyStateChange` evento é enviado quando a propriedade **ReadyState** do controle MSWebDVD é alterada.</span><span class="sxs-lookup"><span data-stu-id="00758-106">The `ReadyStateChange` event is sent when the **ReadyState** property of the MSWebDVD control has changed.</span></span>

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a><span data-ttu-id="00758-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00758-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00758-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*Ready*</span><span class="sxs-lookup"><span data-stu-id="00758-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span></span>
</dt> <dd>

<span data-ttu-id="00758-109">Especifica o novo valor da propriedade [**ReadyState**](readystate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="00758-109">Specifies the new value of the [**ReadyState**](readystate-property.md) property.</span></span>



| <span data-ttu-id="00758-110">Valor</span><span class="sxs-lookup"><span data-stu-id="00758-110">Value</span></span> | <span data-ttu-id="00758-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="00758-111">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="00758-112">0</span><span class="sxs-lookup"><span data-stu-id="00758-112">0</span></span>     | <span data-ttu-id="00758-113">READYstate não \_ inicializado</span><span class="sxs-lookup"><span data-stu-id="00758-113">READYSTATE\_UNINITIALIZED</span></span> |
| <span data-ttu-id="00758-114">1</span><span class="sxs-lookup"><span data-stu-id="00758-114">1</span></span>     | <span data-ttu-id="00758-115">carregamento de READYstate \_</span><span class="sxs-lookup"><span data-stu-id="00758-115">READYSTATE\_LOADING</span></span>       |
| <span data-ttu-id="00758-116">2</span><span class="sxs-lookup"><span data-stu-id="00758-116">2</span></span>     | <span data-ttu-id="00758-117">READYstate \_ carregado</span><span class="sxs-lookup"><span data-stu-id="00758-117">READYSTATE\_LOADED</span></span>        |
| <span data-ttu-id="00758-118">3</span><span class="sxs-lookup"><span data-stu-id="00758-118">3</span></span>     | <span data-ttu-id="00758-119">READYstate \_ interativo</span><span class="sxs-lookup"><span data-stu-id="00758-119">READYSTATE\_INTERACTIVE</span></span>   |
| <span data-ttu-id="00758-120">4</span><span class="sxs-lookup"><span data-stu-id="00758-120">4</span></span>     | <span data-ttu-id="00758-121">READYstate \_ concluído</span><span class="sxs-lookup"><span data-stu-id="00758-121">READYSTATE\_COMPLETE</span></span>      |



 

</dd> </dl>

 

 



