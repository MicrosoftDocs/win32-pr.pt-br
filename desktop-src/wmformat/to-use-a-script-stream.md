---
title: Para usar um fluxo de script
description: Para usar um fluxo de script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK, fluxos de script
- FORMATO DE SISTEMAS Avançados (ASF), fluxos de script
- ASF (Formato de Sistemas Avançados), fluxos de script
- fluxos de script, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444727"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="c888e-107">Para usar um fluxo de script</span><span class="sxs-lookup"><span data-stu-id="c888e-107">To Use a Script Stream</span></span>

<span data-ttu-id="c888e-108">Esta seção descreve como enviar dados de script para o autor para inclusão em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c888e-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="c888e-109">Para obter informações sobre como incluir fluxos de script em perfis, consulte [Configurando tipos de fluxo arbitrários](configuring-arbitrary-stream-types.md).</span><span class="sxs-lookup"><span data-stu-id="c888e-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="c888e-110">Cada script consiste em duas cadeias de caracteres, uma cadeia de caracteres *de* tipo e uma cadeia *de caracteres de* argumento.</span><span class="sxs-lookup"><span data-stu-id="c888e-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="c888e-111">Os dados de script devem ser formatados antes de serem enviados ao autor.</span><span class="sxs-lookup"><span data-stu-id="c888e-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="c888e-112">As cadeias de caracteres devem ser concatenadas, separadas por um **caractere NULL** e terminadas com um **caractere NULL.**</span><span class="sxs-lookup"><span data-stu-id="c888e-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="c888e-113">O exemplo a seguir mostra um script legítimo:</span><span class="sxs-lookup"><span data-stu-id="c888e-113">The following example shows a legitimate script:</span></span>



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="c888e-114">U</span><span class="sxs-lookup"><span data-stu-id="c888e-114">U</span></span>   | <span data-ttu-id="c888e-115">R</span><span class="sxs-lookup"><span data-stu-id="c888e-115">R</span></span>   | <span data-ttu-id="c888e-116">L</span><span class="sxs-lookup"><span data-stu-id="c888e-116">L</span></span>   | &nbsp; | <span data-ttu-id="c888e-117">h</span><span class="sxs-lookup"><span data-stu-id="c888e-117">h</span></span>   | <span data-ttu-id="c888e-118">t</span><span class="sxs-lookup"><span data-stu-id="c888e-118">t</span></span>   | <span data-ttu-id="c888e-119">t</span><span class="sxs-lookup"><span data-stu-id="c888e-119">t</span></span>   | <span data-ttu-id="c888e-120">p</span><span class="sxs-lookup"><span data-stu-id="c888e-120">p</span></span>   | <span data-ttu-id="c888e-121">:</span><span class="sxs-lookup"><span data-stu-id="c888e-121">:</span></span>   | /   | /   | <span data-ttu-id="c888e-122">w</span><span class="sxs-lookup"><span data-stu-id="c888e-122">w</span></span>   | <span data-ttu-id="c888e-123">w</span><span class="sxs-lookup"><span data-stu-id="c888e-123">w</span></span>   | <span data-ttu-id="c888e-124">w</span><span class="sxs-lookup"><span data-stu-id="c888e-124">w</span></span>   | <span data-ttu-id="c888e-125">.</span><span class="sxs-lookup"><span data-stu-id="c888e-125">.</span></span>   | <span data-ttu-id="c888e-126">um</span><span class="sxs-lookup"><span data-stu-id="c888e-126">a</span></span>   | <span data-ttu-id="c888e-127">d</span><span class="sxs-lookup"><span data-stu-id="c888e-127">d</span></span>   | <span data-ttu-id="c888e-128">um</span><span class="sxs-lookup"><span data-stu-id="c888e-128">a</span></span>   | <span data-ttu-id="c888e-129">t</span><span class="sxs-lookup"><span data-stu-id="c888e-129">t</span></span>   | <span data-ttu-id="c888e-130">u</span><span class="sxs-lookup"><span data-stu-id="c888e-130">u</span></span>   | <span data-ttu-id="c888e-131">m</span><span class="sxs-lookup"><span data-stu-id="c888e-131">m</span></span>   | <span data-ttu-id="c888e-132">.</span><span class="sxs-lookup"><span data-stu-id="c888e-132">.</span></span>   | <span data-ttu-id="c888e-133">c</span><span class="sxs-lookup"><span data-stu-id="c888e-133">c</span></span>   | <span data-ttu-id="c888e-134">o</span><span class="sxs-lookup"><span data-stu-id="c888e-134">o</span></span>   | <span data-ttu-id="c888e-135">m</span><span class="sxs-lookup"><span data-stu-id="c888e-135">m</span></span>   | &nbsp; |



 

<span data-ttu-id="c888e-136">Cada par de comandos de script deve ser gravado como um exemplo para o autor.</span><span class="sxs-lookup"><span data-stu-id="c888e-136">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="c888e-137">Para obter mais informações sobre como escrever exemplos, consulte [To Write Samples](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="c888e-137">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="c888e-138">Quando o arquivo ASF for tocado, os comandos de script serão entregues pelo leitor (ou leitor síncrono) na ordem de tempo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="c888e-138">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="c888e-139">É responsabilidade do aplicativo analisar as duas cadeias de caracteres e responder ao comando de script.</span><span class="sxs-lookup"><span data-stu-id="c888e-139">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="c888e-140">Ao usar o DRM para criptografar um arquivo, nenhum comando de script pode ter um tempo de apresentação de 0.</span><span class="sxs-lookup"><span data-stu-id="c888e-140">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c888e-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c888e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c888e-142">**Usando comandos de script**</span><span class="sxs-lookup"><span data-stu-id="c888e-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




