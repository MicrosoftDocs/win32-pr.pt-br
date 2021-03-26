---
title: Sombreadores de software
description: Os sombreadores de software são implementados para permitir o desenvolvimento de sombreadores sem suporte de hardware subjacente. Eles dão suporte ao conjunto de recursos completo. Como eles são implementados no software, eles não produzirão o melhor desempenho.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df101edd0362321847fb9c0baf7feb3cc865e2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006190"
---
# <a name="software-shaders"></a><span data-ttu-id="c902e-105">Sombreadores de software</span><span class="sxs-lookup"><span data-stu-id="c902e-105">Software Shaders</span></span>

<span data-ttu-id="c902e-106">Os sombreadores de software são implementados para permitir o desenvolvimento de sombreadores sem suporte de hardware subjacente.</span><span class="sxs-lookup"><span data-stu-id="c902e-106">Software shaders are implemented to allow development of shaders without underlying hardware support.</span></span> <span data-ttu-id="c902e-107">Eles dão suporte ao conjunto de recursos completo.</span><span class="sxs-lookup"><span data-stu-id="c902e-107">They support the full feature set.</span></span> <span data-ttu-id="c902e-108">Como eles são implementados no software, eles não produzirão o melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="c902e-108">Because they are implemented in software, they will not produce the best performance.</span></span>



| <span data-ttu-id="c902e-109">Versão</span><span class="sxs-lookup"><span data-stu-id="c902e-109">Version</span></span>   | <span data-ttu-id="c902e-110">Conjunto de recursos</span><span class="sxs-lookup"><span data-stu-id="c902e-110">Feature Set</span></span>                  | <span data-ttu-id="c902e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c902e-111">Requirements</span></span>                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="c902e-112">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c902e-112">vs\_2\_sw</span></span> | <span data-ttu-id="c902e-113">Todos os recursos do vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c902e-113">All the features of vs\_2\_x</span></span> | <span data-ttu-id="c902e-114">Compatível apenas com o processamento de vértice de software e um dispositivo de referência.</span><span class="sxs-lookup"><span data-stu-id="c902e-114">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="c902e-115">vs \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c902e-115">vs\_3\_sw</span></span> | <span data-ttu-id="c902e-116">Todos os recursos do vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c902e-116">All the features of vs\_3\_0</span></span> | <span data-ttu-id="c902e-117">Compatível apenas com o processamento de vértice de software e um dispositivo de referência.</span><span class="sxs-lookup"><span data-stu-id="c902e-117">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="c902e-118">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c902e-118">ps\_2\_sw</span></span> | <span data-ttu-id="c902e-119">Todos os recursos do PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c902e-119">All the features of ps\_2\_x</span></span> | <span data-ttu-id="c902e-120">Somente com suporte em um dispositivo de referência.</span><span class="sxs-lookup"><span data-stu-id="c902e-120">Only supported by a reference device.</span></span>                                |
| <span data-ttu-id="c902e-121">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c902e-121">ps\_3\_sw</span></span> | <span data-ttu-id="c902e-122">Todos os recursos do PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c902e-122">All the features of ps\_3\_0</span></span> | <span data-ttu-id="c902e-123">Somente com suporte em um dispositivo de referência.</span><span class="sxs-lookup"><span data-stu-id="c902e-123">Only supported by a reference device.</span></span>                                |



 

<span data-ttu-id="c902e-124">Algumas validações são relaxadas para os sombreadores de software.</span><span class="sxs-lookup"><span data-stu-id="c902e-124">Some validations are relaxed for software shaders.</span></span> <span data-ttu-id="c902e-125">Isso é útil para fins de depuração e protótipos.</span><span class="sxs-lookup"><span data-stu-id="c902e-125">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="c902e-126">As validações a seguir são relaxadas: (todas as outras validações permanecem as mesmas)</span><span class="sxs-lookup"><span data-stu-id="c902e-126">The following validations are relaxed: (all other validations remain the same)</span></span>



| <span data-ttu-id="c902e-127">Tipo de validação</span><span class="sxs-lookup"><span data-stu-id="c902e-127">Validation type</span></span>                                 | <span data-ttu-id="c902e-128">Relaxamento</span><span class="sxs-lookup"><span data-stu-id="c902e-128">Relaxation</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c902e-129">Contagens de instrução:</span><span class="sxs-lookup"><span data-stu-id="c902e-129">Instruction Counts:</span></span>                             | <span data-ttu-id="c902e-130">Isso é relaxado para vs \_ 2 SW \_ , vs \_ 3 SW \_ e PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="c902e-130">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="c902e-131">Instruções ilimitadas são permitidas.</span><span class="sxs-lookup"><span data-stu-id="c902e-131">Unlimited instructions are allowed.</span></span>                                                                                                              |
| <span data-ttu-id="c902e-132">Contagens de constantes flutuantes:</span><span class="sxs-lookup"><span data-stu-id="c902e-132">Float Constant Counts:</span></span>                          | <span data-ttu-id="c902e-133">Isso é relaxado para vs \_ 2 SW \_ , vs \_ 3 SW \_ e PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="c902e-133">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="c902e-134">São permitidas até 8192 constantes.</span><span class="sxs-lookup"><span data-stu-id="c902e-134">Up to 8192 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="c902e-135">Contagens de constantes inteiras:</span><span class="sxs-lookup"><span data-stu-id="c902e-135">Integer Constant Counts:</span></span>                        | <span data-ttu-id="c902e-136">Isso é relaxado para vs \_ 2 SW \_ , vs \_ 3 SW \_ e PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="c902e-136">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="c902e-137">São permitidas até 2048 constantes.</span><span class="sxs-lookup"><span data-stu-id="c902e-137">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="c902e-138">Contagens de constantes boolianas:</span><span class="sxs-lookup"><span data-stu-id="c902e-138">Boolean Constant Counts:</span></span>                        | <span data-ttu-id="c902e-139">Isso é relaxado para vs \_ 2 SW \_ , vs \_ 3 SW \_ e PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="c902e-139">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="c902e-140">São permitidas até 2048 constantes.</span><span class="sxs-lookup"><span data-stu-id="c902e-140">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="c902e-141">Dependente-ler profundidade:</span><span class="sxs-lookup"><span data-stu-id="c902e-141">Dependent-read depth:</span></span>                           | <span data-ttu-id="c902e-142">Isso é relaxado para \_ o \_ software PS 2.</span><span class="sxs-lookup"><span data-stu-id="c902e-142">This is relaxed for ps\_2\_sw.</span></span> <span data-ttu-id="c902e-143">Como no vs \_ 3 \_ 0 e no PS \_ 3 \_ 0, leituras dependentes ilimitadas são permitidas.</span><span class="sxs-lookup"><span data-stu-id="c902e-143">Like in vs\_3\_0 and ps\_3\_0, unlimited dependent reads are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="c902e-144">Número de instruções e rótulos de controle de fluxo:</span><span class="sxs-lookup"><span data-stu-id="c902e-144">Number of flow control instructions and labels:</span></span> | <span data-ttu-id="c902e-145">Isso é relaxado para o vs \_ 2 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="c902e-145">This is relaxed for vs\_2\_sw.</span></span> <span data-ttu-id="c902e-146">São permitidas instruções de controle de fluxo ilimitadas e até 2048 rótulos.</span><span class="sxs-lookup"><span data-stu-id="c902e-146">Unlimited flow control instructions and upto 2048 labels are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="c902e-147">Contagem de loops/início/etapa:</span><span class="sxs-lookup"><span data-stu-id="c902e-147">Loop count/start/step:</span></span>                          | <span data-ttu-id="c902e-148">Eles são relaxados para o vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW e PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="c902e-148">These are relaxed for vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw.</span></span> <span data-ttu-id="c902e-149">O tamanho da etapa de início e de interseção de iteração para instruções de rep e loop são intergers assinadas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c902e-149">Iteration start and interation step size for rep and loop instructions are 32-bit signed intergers.</span></span> <span data-ttu-id="c902e-150">A contagem de interativação pode ser até o máximo \_ int/64.</span><span class="sxs-lookup"><span data-stu-id="c902e-150">Interation count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="c902e-151">Limites de porta de leitura:</span><span class="sxs-lookup"><span data-stu-id="c902e-151">Read-port limits:</span></span>                               | <span data-ttu-id="c902e-152">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW e PS \_ 3 \_ SW não têm nenhum limite de porta de leitura.</span><span class="sxs-lookup"><span data-stu-id="c902e-152">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw have no read-port limit.</span></span>                                                                                                                                              |
| <span data-ttu-id="c902e-153">Número de interpoladores:</span><span class="sxs-lookup"><span data-stu-id="c902e-153">Number of interpolators:</span></span>                        | <span data-ttu-id="c902e-154">Há 16 [registros-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) em vs \_ 3 \_ SW e 10 [PS \_ 3 \_ 0 registros](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) para o PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="c902e-154">There are 16 [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) in vs\_3\_sw and 10 [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#) for ps\_3\_sw.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="c902e-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c902e-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c902e-156">Referência do sombreador ASM</span><span class="sxs-lookup"><span data-stu-id="c902e-156">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




