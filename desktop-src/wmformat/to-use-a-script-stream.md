---
title: Para usar um fluxo de script
description: Para usar um fluxo de script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- SDK do Windows Media Format, fluxos de script
- ASF (Advanced Systems Format), fluxos de script
- ASF (formato de sistemas avançados), fluxos de script
- fluxos de script, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dee2c4a9789406c21b18c58a5f281a768fc713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292828"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="da0f4-107">Para usar um fluxo de script</span><span class="sxs-lookup"><span data-stu-id="da0f4-107">To Use a Script Stream</span></span>

<span data-ttu-id="da0f4-108">Esta seção descreve como enviar dados de script para o gravador para inclusão em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="da0f4-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="da0f4-109">Para obter informações sobre como incluir fluxos de script em perfis, consulte [Configurando tipos de fluxo arbitrários](configuring-arbitrary-stream-types.md).</span><span class="sxs-lookup"><span data-stu-id="da0f4-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="da0f4-110">Cada script consiste em duas cadeias de caracteres, um *tipo* String e uma cadeia de caracteres de *argumento* .</span><span class="sxs-lookup"><span data-stu-id="da0f4-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="da0f4-111">Os dados de script devem ser formatados antes de serem enviados ao gravador.</span><span class="sxs-lookup"><span data-stu-id="da0f4-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="da0f4-112">As cadeias de caracteres devem ser concatenadas, separadas por um caractere **nulo** e terminadas com um caractere **nulo** .</span><span class="sxs-lookup"><span data-stu-id="da0f4-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="da0f4-113">O exemplo a seguir mostra um script legítimo:</span><span class="sxs-lookup"><span data-stu-id="da0f4-113">The following example shows a legitimate script:</span></span>



|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="da0f4-114">U</span><span class="sxs-lookup"><span data-stu-id="da0f4-114">U</span></span>   | <span data-ttu-id="da0f4-115">R</span><span class="sxs-lookup"><span data-stu-id="da0f4-115">R</span></span>   | <span data-ttu-id="da0f4-116">L</span><span class="sxs-lookup"><span data-stu-id="da0f4-116">L</span></span>   | <span data-ttu-id="da0f4-117">\\0</span><span class="sxs-lookup"><span data-stu-id="da0f4-117">\\0</span></span> | <span data-ttu-id="da0f4-118">h</span><span class="sxs-lookup"><span data-stu-id="da0f4-118">h</span></span>   | <span data-ttu-id="da0f4-119">t</span><span class="sxs-lookup"><span data-stu-id="da0f4-119">t</span></span>   | <span data-ttu-id="da0f4-120">t</span><span class="sxs-lookup"><span data-stu-id="da0f4-120">t</span></span>   | <span data-ttu-id="da0f4-121">p</span><span class="sxs-lookup"><span data-stu-id="da0f4-121">p</span></span>   | <span data-ttu-id="da0f4-122">:</span><span class="sxs-lookup"><span data-stu-id="da0f4-122">:</span></span>   | /   | /   | <span data-ttu-id="da0f4-123">w</span><span class="sxs-lookup"><span data-stu-id="da0f4-123">w</span></span>   | <span data-ttu-id="da0f4-124">w</span><span class="sxs-lookup"><span data-stu-id="da0f4-124">w</span></span>   | <span data-ttu-id="da0f4-125">w</span><span class="sxs-lookup"><span data-stu-id="da0f4-125">w</span></span>   | <span data-ttu-id="da0f4-126">.</span><span class="sxs-lookup"><span data-stu-id="da0f4-126">.</span></span>   | <span data-ttu-id="da0f4-127">um</span><span class="sxs-lookup"><span data-stu-id="da0f4-127">a</span></span>   | <span data-ttu-id="da0f4-128">d</span><span class="sxs-lookup"><span data-stu-id="da0f4-128">d</span></span>   | <span data-ttu-id="da0f4-129">um</span><span class="sxs-lookup"><span data-stu-id="da0f4-129">a</span></span>   | <span data-ttu-id="da0f4-130">t</span><span class="sxs-lookup"><span data-stu-id="da0f4-130">t</span></span>   | <span data-ttu-id="da0f4-131">u</span><span class="sxs-lookup"><span data-stu-id="da0f4-131">u</span></span>   | <span data-ttu-id="da0f4-132">m</span><span class="sxs-lookup"><span data-stu-id="da0f4-132">m</span></span>   | <span data-ttu-id="da0f4-133">.</span><span class="sxs-lookup"><span data-stu-id="da0f4-133">.</span></span>   | <span data-ttu-id="da0f4-134">c</span><span class="sxs-lookup"><span data-stu-id="da0f4-134">c</span></span>   | <span data-ttu-id="da0f4-135">o</span><span class="sxs-lookup"><span data-stu-id="da0f4-135">o</span></span>   | <span data-ttu-id="da0f4-136">m</span><span class="sxs-lookup"><span data-stu-id="da0f4-136">m</span></span>   | <span data-ttu-id="da0f4-137">\\0</span><span class="sxs-lookup"><span data-stu-id="da0f4-137">\\0</span></span> |



 

<span data-ttu-id="da0f4-138">Cada par de comandos de script deve ser escrito como um exemplo para o gravador.</span><span class="sxs-lookup"><span data-stu-id="da0f4-138">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="da0f4-139">Para obter mais informações sobre como escrever exemplos, consulte [para escrever exemplos](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="da0f4-139">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="da0f4-140">Quando o arquivo ASF for reproduzido, os comandos de script serão entregues pelo leitor (ou leitor síncrono) na ordem de tempo da apresentação.</span><span class="sxs-lookup"><span data-stu-id="da0f4-140">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="da0f4-141">É responsabilidade do aplicativo analisar as duas cadeias de caracteres e responder ao comando de script.</span><span class="sxs-lookup"><span data-stu-id="da0f4-141">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="da0f4-142">Ao usar o DRM para criptografar um arquivo, nenhum comando de script pode ter um horário de apresentação de 0.</span><span class="sxs-lookup"><span data-stu-id="da0f4-142">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="da0f4-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da0f4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da0f4-144">**Usando comandos de script**</span><span class="sxs-lookup"><span data-stu-id="da0f4-144">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




