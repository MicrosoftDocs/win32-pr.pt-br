---
description: A propriedade CurrentCCService define ou recupera o serviço de legendagem oculta atual.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Propriedade CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825860"
---
# <a name="currentccservice-property"></a><span data-ttu-id="839dc-103">Propriedade CurrentCCService</span><span class="sxs-lookup"><span data-stu-id="839dc-103">CurrentCCService Property</span></span>

> [!Note]  
> <span data-ttu-id="839dc-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="839dc-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="839dc-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="839dc-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="839dc-106">A `CurrentCCService` propriedade define ou recupera o serviço de legendagem oculta atual.</span><span class="sxs-lookup"><span data-stu-id="839dc-106">The `CurrentCCService` property sets or retrieves the current closed captioning service.</span></span>

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a><span data-ttu-id="839dc-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="839dc-107">Return Value</span></span>

<span data-ttu-id="839dc-108">Retorna um valor inteiro que indica o tipo de serviço de legendagem oculta habilitado.</span><span class="sxs-lookup"><span data-stu-id="839dc-108">Returns an integer value indicating the type of closed captioning service enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="839dc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="839dc-109">Remarks</span></span>

<span data-ttu-id="839dc-110">Os valores possíveis dessa propriedade são:</span><span class="sxs-lookup"><span data-stu-id="839dc-110">The possible values of this property are:</span></span>



| <span data-ttu-id="839dc-111">Valor</span><span class="sxs-lookup"><span data-stu-id="839dc-111">Value</span></span> | <span data-ttu-id="839dc-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="839dc-112">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="839dc-113">0x0</span><span class="sxs-lookup"><span data-stu-id="839dc-113">0x0</span></span>   | <span data-ttu-id="839dc-114">Nenhum serviço atual.</span><span class="sxs-lookup"><span data-stu-id="839dc-114">No current service.</span></span> <span data-ttu-id="839dc-115">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="839dc-115">This is the default value.</span></span>                       |
| <span data-ttu-id="839dc-116">0x1</span><span class="sxs-lookup"><span data-stu-id="839dc-116">0x1</span></span>   | <span data-ttu-id="839dc-117">Legenda verdadeira, primeiro campo.</span><span class="sxs-lookup"><span data-stu-id="839dc-117">True captioning, first field.</span></span> <span data-ttu-id="839dc-118">Serviço padrão.</span><span class="sxs-lookup"><span data-stu-id="839dc-118">Default service.</span></span>                       |
| <span data-ttu-id="839dc-119">0x2</span><span class="sxs-lookup"><span data-stu-id="839dc-119">0x2</span></span>   | <span data-ttu-id="839dc-120">Legenda do idioma secundário, segundo campo.</span><span class="sxs-lookup"><span data-stu-id="839dc-120">Captioning for secondary language, second field.</span></span> <span data-ttu-id="839dc-121">Geralmente não usado.</span><span class="sxs-lookup"><span data-stu-id="839dc-121">Generally not used.</span></span> |



 

<span data-ttu-id="839dc-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="839dc-122">This property is read/write.</span></span>

## <a name="see-also"></a><span data-ttu-id="839dc-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="839dc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="839dc-124">**CCActive**</span><span class="sxs-lookup"><span data-stu-id="839dc-124">**CCActive**</span></span>](ccactive-property.md)
</dt> </dl>

 

 



