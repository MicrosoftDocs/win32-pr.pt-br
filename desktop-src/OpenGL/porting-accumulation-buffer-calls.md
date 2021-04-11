---
title: Portando chamadas de buffer de acumulação
description: Você deve alocar seu buffer de acumulação solicitando o formato de pixel apropriado com a função OpenGL auxInitDisplayMode ou ChoosePixelFormat.
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- Portabilidade do íris GL, buffers de acumulação
- portando do íris GL, buffers de acumulação
- portando para OpenGL do íris GL, buffers de acumulação
- Portabilidade OpenGL do íris GL, buffers de acumulação
- buffers de acumulação OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160465"
---
# <a name="porting-accumulation-buffer-calls"></a><span data-ttu-id="9d016-108">Portando chamadas de buffer de acumulação</span><span class="sxs-lookup"><span data-stu-id="9d016-108">Porting Accumulation Buffer Calls</span></span>

<span data-ttu-id="9d016-109">Você deve alocar seu buffer de acumulação solicitando o formato de pixel apropriado com a função OpenGL **auxInitDisplayMode** ou [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) .</span><span class="sxs-lookup"><span data-stu-id="9d016-109">You must allocate your accumulation buffer by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function.</span></span> <span data-ttu-id="9d016-110">A tabela a seguir lista as funções do íris GL que afetam o buffer de acumulação e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="9d016-110">The following table lists IRIS GL functions that affect the accumulation buffer and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="9d016-111">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="9d016-111">IRIS GL function</span></span>       | <span data-ttu-id="9d016-112">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="9d016-112">OpenGL function</span></span>                                       | <span data-ttu-id="9d016-113">Significado</span><span class="sxs-lookup"><span data-stu-id="9d016-113">Meaning</span></span>                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="9d016-114">**acsize**</span><span class="sxs-lookup"><span data-stu-id="9d016-114">**acsize**</span></span>             | <span data-ttu-id="9d016-115">**auxInitDisplayMode** ou **ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="9d016-115">**auxInitDisplayMode** or **ChoosePixelFormat**</span></span>       | <span data-ttu-id="9d016-116">Especifica o número de bitplanes por componente de cor no buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="9d016-116">Specifies number of bitplanes per color component in the accumulation buffer.</span></span> |
| <span data-ttu-id="9d016-117">**acbuf**</span><span class="sxs-lookup"><span data-stu-id="9d016-117">**acbuf**</span></span>              | [<span data-ttu-id="9d016-118">**glAccum**</span><span class="sxs-lookup"><span data-stu-id="9d016-118">**glAccum**</span></span>](glaccum.md)                            | <span data-ttu-id="9d016-119">Opera no buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="9d016-119">Operates on the accumulation buffer.</span></span>                                          |
|                        | [<span data-ttu-id="9d016-120">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="9d016-120">**glClearAccum**</span></span>](glclearaccum.md)                  | <span data-ttu-id="9d016-121">Define valores claros para o buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="9d016-121">Sets clear values for accumulation buffer.</span></span>                                    |
| <span data-ttu-id="9d016-122">**acbuf**(AC \_ limpa)</span><span class="sxs-lookup"><span data-stu-id="9d016-122">**acbuf**( AC\_CLEAR )</span></span> | <span data-ttu-id="9d016-123">[**glClear**](glclear.md) (bit de buffer do GL \_ Accum \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="9d016-123">[**glClear**](glclear.md) ( GL\_ACCUM\_BUFFER\_BIT )</span></span> | <span data-ttu-id="9d016-124">Limpa o buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="9d016-124">Clears the accumulation buffer.</span></span>                                               |



 

<span data-ttu-id="9d016-125">A tabela a seguir lista os parâmetros **acbuf** do íris GL juntamente com os parâmetros equivalentes do OpenGL [**glAccum**](glaccum.md) .</span><span class="sxs-lookup"><span data-stu-id="9d016-125">The following table lists the IRIS GL **acbuf** parameters along with the equivalent OpenGL [**glAccum**](glaccum.md) parameters.</span></span>



| <span data-ttu-id="9d016-126">Parâmetro do íris GL</span><span class="sxs-lookup"><span data-stu-id="9d016-126">IRIS GL parameter</span></span>     | <span data-ttu-id="9d016-127">Parâmetro OpenGL</span><span class="sxs-lookup"><span data-stu-id="9d016-127">OpenGL parameter</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="9d016-128">\_acumulação de AC</span><span class="sxs-lookup"><span data-stu-id="9d016-128">AC\_ACCUMULATE</span></span>        | <span data-ttu-id="9d016-129">GL \_ Accum</span><span class="sxs-lookup"><span data-stu-id="9d016-129">GL\_ACCUM</span></span>        |
| <span data-ttu-id="9d016-130">\_desacumular AC limpar \_</span><span class="sxs-lookup"><span data-stu-id="9d016-130">AC\_CLEAR\_ACCUMULATE</span></span> | <span data-ttu-id="9d016-131">\_carga GL</span><span class="sxs-lookup"><span data-stu-id="9d016-131">GL\_LOAD</span></span>         |
| <span data-ttu-id="9d016-132">retorno de AC \_</span><span class="sxs-lookup"><span data-stu-id="9d016-132">AC\_RETURN</span></span>            | <span data-ttu-id="9d016-133">retorno do GL \_</span><span class="sxs-lookup"><span data-stu-id="9d016-133">GL\_RETURN</span></span>       |
| <span data-ttu-id="9d016-134">\_mult AC</span><span class="sxs-lookup"><span data-stu-id="9d016-134">AC\_MULT</span></span>              | <span data-ttu-id="9d016-135">\_mult GL</span><span class="sxs-lookup"><span data-stu-id="9d016-135">GL\_MULT</span></span>         |
| <span data-ttu-id="9d016-136">adição de AC \_</span><span class="sxs-lookup"><span data-stu-id="9d016-136">AC\_ADD</span></span>               | <span data-ttu-id="9d016-137">adição de GL \_</span><span class="sxs-lookup"><span data-stu-id="9d016-137">GL\_ADD</span></span>          |



 

 

 




