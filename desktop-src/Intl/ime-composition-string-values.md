---
description: Esses valores são usados com a composição do IME do ImmGetCompositionString e do WM \_ \_ .
ms.assetid: 14087598-8041-4e02-a168-f5538a437be0
title: Valores da cadeia de caracteres de composição do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5b3935329e56f015cdb08a764e1660142a067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827289"
---
# <a name="ime-composition-string-values"></a><span data-ttu-id="f3c77-103">Valores da cadeia de caracteres de composição do IME</span><span class="sxs-lookup"><span data-stu-id="f3c77-103">IME Composition String Values</span></span>

<span data-ttu-id="f3c77-104">Esses valores são usados com a [**composição do \_ IME \_**](wm-ime-composition.md)do [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) e do WM.</span><span class="sxs-lookup"><span data-stu-id="f3c77-104">These values are used with [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) and [**WM\_IME\_COMPOSITION**](wm-ime-composition.md).</span></span>



| <span data-ttu-id="f3c77-105">Valor</span><span class="sxs-lookup"><span data-stu-id="f3c77-105">Value</span></span>                 | <span data-ttu-id="f3c77-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3c77-106">Description</span></span>                                                                                |
|-----------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c77-107">GCS \_ COMPATTR</span><span class="sxs-lookup"><span data-stu-id="f3c77-107">GCS\_COMPATTR</span></span>         | <span data-ttu-id="f3c77-108">Recupere ou atualize o atributo da cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="f3c77-108">Retrieve or update the attribute of the composition string.</span></span>                                |
| <span data-ttu-id="f3c77-109">GCS \_ COMPCLAUSE</span><span class="sxs-lookup"><span data-stu-id="f3c77-109">GCS\_COMPCLAUSE</span></span>       | <span data-ttu-id="f3c77-110">Recupere ou atualize as informações de cláusula da cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="f3c77-110">Retrieve or update clause information of the composition string.</span></span>                           |
| <span data-ttu-id="f3c77-111">GCS \_ COMPREADATTR</span><span class="sxs-lookup"><span data-stu-id="f3c77-111">GCS\_COMPREADATTR</span></span>     | <span data-ttu-id="f3c77-112">Recupere ou atualize os atributos da cadeia de caracteres de leitura da composição atual.</span><span class="sxs-lookup"><span data-stu-id="f3c77-112">Retrieve or update the attributes of the reading string of the current composition.</span></span>        |
| <span data-ttu-id="f3c77-113">GCS \_ COMPREADCLAUSE</span><span class="sxs-lookup"><span data-stu-id="f3c77-113">GCS\_COMPREADCLAUSE</span></span>   | <span data-ttu-id="f3c77-114">Recupere ou atualize as informações de cláusula da cadeia de caracteres de leitura da cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="f3c77-114">Retrieve or update the clause information of the reading string of the composition string.</span></span> |
| <span data-ttu-id="f3c77-115">GCS \_ COMPREADSTR</span><span class="sxs-lookup"><span data-stu-id="f3c77-115">GCS\_COMPREADSTR</span></span>      | <span data-ttu-id="f3c77-116">Recupere ou atualize a cadeia de caracteres de leitura da composição atual.</span><span class="sxs-lookup"><span data-stu-id="f3c77-116">Retrieve or update the reading string of the current composition.</span></span>                          |
| <span data-ttu-id="f3c77-117">GCS \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="f3c77-117">GCS\_COMPSTR</span></span>          | <span data-ttu-id="f3c77-118">Recuperar ou atualizar a cadeia de caracteres de composição atual.</span><span class="sxs-lookup"><span data-stu-id="f3c77-118">Retrieve or update the current composition string.</span></span>                                         |
| <span data-ttu-id="f3c77-119">GCS \_ CURSORPOS</span><span class="sxs-lookup"><span data-stu-id="f3c77-119">GCS\_CURSORPOS</span></span>        | <span data-ttu-id="f3c77-120">Recupere ou atualize a posição do cursor na cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="f3c77-120">Retrieve or update the cursor position in composition string.</span></span>                              |
| <span data-ttu-id="f3c77-121">GCS \_ DELTASTART</span><span class="sxs-lookup"><span data-stu-id="f3c77-121">GCS\_DELTASTART</span></span>       | <span data-ttu-id="f3c77-122">Recupere ou atualize a posição inicial de quaisquer alterações na cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="f3c77-122">Retrieve or update the starting position of any changes in composition string.</span></span>             |
| <span data-ttu-id="f3c77-123">GCS \_ RESULTCLAUSE</span><span class="sxs-lookup"><span data-stu-id="f3c77-123">GCS\_RESULTCLAUSE</span></span>     | <span data-ttu-id="f3c77-124">Recupere ou atualize as informações de cláusula da cadeia de caracteres de resultado.</span><span class="sxs-lookup"><span data-stu-id="f3c77-124">Retrieve or update clause information of the result string.</span></span>                                |
| <span data-ttu-id="f3c77-125">GCS \_ RESULTREADCLAUSE</span><span class="sxs-lookup"><span data-stu-id="f3c77-125">GCS\_RESULTREADCLAUSE</span></span> | <span data-ttu-id="f3c77-126">Recupere ou atualize as informações de cláusula da cadeia de caracteres de leitura.</span><span class="sxs-lookup"><span data-stu-id="f3c77-126">Retrieve or update clause information of the reading string.</span></span>                               |
| <span data-ttu-id="f3c77-127">GCS \_ RESULTREADSTR</span><span class="sxs-lookup"><span data-stu-id="f3c77-127">GCS\_RESULTREADSTR</span></span>    | <span data-ttu-id="f3c77-128">Recupere ou atualize a cadeia de caracteres de leitura.</span><span class="sxs-lookup"><span data-stu-id="f3c77-128">Retrieve or update the reading string.</span></span>                                                     |
| <span data-ttu-id="f3c77-129">GCS \_ RESULTSTR</span><span class="sxs-lookup"><span data-stu-id="f3c77-129">GCS\_RESULTSTR</span></span>        | <span data-ttu-id="f3c77-130">Recupere ou atualize a cadeia de caracteres do resultado da composição.</span><span class="sxs-lookup"><span data-stu-id="f3c77-130">Retrieve or update the string of the composition result.</span></span>                                   |



 

 

 



