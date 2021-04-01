---
title: Variáveis para executar o processamento
description: Variáveis para executar o processamento
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Plug-ins do Windows Media Player, método Echo DoProcessOutput de exemplo
- plug-ins, exemplo de método Echo DoProcessOutput
- plug-ins de processamento de sinal digital, Echo Sample DoProcessOutput Method
- Plug-ins do DSP, método Echo de exemplo DoProcessOutput
- Exemplo de plug-in do DSP de eco, método DoProcessOutput
- Exemplo de plug-in do eco DSP, variáveis de processamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636104"
---
# <a name="variables-to-perform-processing"></a><span data-ttu-id="45e80-109">Variáveis para executar o processamento</span><span class="sxs-lookup"><span data-stu-id="45e80-109">Variables to Perform Processing</span></span>

<span data-ttu-id="45e80-110">As variáveis de membro para manipular o buffer de atraso lidam com quantidades de **bytes** ; Eles são ponteiros de **bytes** e um inteiro que armazena uma contagem de bytes.</span><span class="sxs-lookup"><span data-stu-id="45e80-110">The member variables for handling the delay buffer deal with **BYTE** quantities; they are **BYTE** pointers and an integer that stores a count of bytes.</span></span> <span data-ttu-id="45e80-111">Isso é ideal para o processamento de áudio de 8 bits, uma vez que um exemplo de 8 bits se encaixa bem em um byte de memória.</span><span class="sxs-lookup"><span data-stu-id="45e80-111">This is ideal for processing 8-bit audio, since an 8-bit sample fits nicely into one byte of memory.</span></span> <span data-ttu-id="45e80-112">No entanto, ao processar o áudio de 16 bits, é mais conveniente convertê-los em ponteiros **curtos** , para que o processamento possa ocorrer dois bytes por vez.</span><span class="sxs-lookup"><span data-stu-id="45e80-112">When processing 16-bit audio, though, it is more convenient to convert these to **short** pointers, so the processing can occur two bytes at a time.</span></span>

<span data-ttu-id="45e80-113">O código de exemplo a seguir aloca os novos ponteiros de 16 bits e adiciona uma variável de ponteiro que armazena o endereço do final do buffer de atraso.</span><span class="sxs-lookup"><span data-stu-id="45e80-113">The following example code allocates the new 16-bit pointers, and adds a pointer variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="45e80-114">Insira-o na seção "Case 16" logo antes do ponto de entrada do loop:</span><span class="sxs-lookup"><span data-stu-id="45e80-114">Insert it in the "case 16" section just before the loop entry point:</span></span>


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



<span data-ttu-id="45e80-115">O código para o processamento de 8 bits também aloca uma variável que armazena o endereço do final do buffer de atraso.</span><span class="sxs-lookup"><span data-stu-id="45e80-115">The code for 8-bit processing also allocates a variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="45e80-116">O armazenamento desse valor torna mais fácil testar se o ponteiro do buffer de atraso móvel atingiu o final do buffer de atraso.</span><span class="sxs-lookup"><span data-stu-id="45e80-116">Storing this value makes it easy to test whether the movable delay buffer pointer has reached the end of the delay buffer.</span></span> <span data-ttu-id="45e80-117">O código de exemplo a seguir calcula o valor:</span><span class="sxs-lookup"><span data-stu-id="45e80-117">The following example code calculates the value:</span></span>


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a><span data-ttu-id="45e80-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45e80-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45e80-119">**Implementando CEcho::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="45e80-119">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




