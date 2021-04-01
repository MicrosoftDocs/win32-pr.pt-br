---
title: Variáveis para armazenar propriedades
description: Variáveis para armazenar propriedades
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Plug-ins do Windows Media Player, propriedades de exemplo de eco
- plug-ins, propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, propriedades de exemplo de eco
- Plug-ins do DSP, propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, propriedades
- Exemplo de plug-in do eco DSP, variáveis para armazenar propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159978"
---
# <a name="variables-to-store-properties"></a><span data-ttu-id="64aa1-109">Variáveis para armazenar propriedades</span><span class="sxs-lookup"><span data-stu-id="64aa1-109">Variables to Store Properties</span></span>

<span data-ttu-id="64aa1-110">Primeiro, você precisará de uma variável para armazenar o tempo de atraso.</span><span class="sxs-lookup"><span data-stu-id="64aa1-110">First, you will need a variable to store the delay time.</span></span> <span data-ttu-id="64aa1-111">O exemplo padrão criado pelo assistente de plug-in do Windows Media Player fornece uma variável chamada m \_ fScaleFactor para armazenar o multiplicador de dimensionamento usado para processamento.</span><span class="sxs-lookup"><span data-stu-id="64aa1-111">The default sample created by the Windows Media Player Plug-in Wizard provides a variable named m\_fScaleFactor to store the scaling multiplier it uses for processing.</span></span> <span data-ttu-id="64aa1-112">Este exemplo não precisa mais dessa variável, portanto, você pode alterar seu nome e tipo para armazenar o valor do tempo de atraso.</span><span class="sxs-lookup"><span data-stu-id="64aa1-112">This sample no longer needs this variable, so you can change its name and type to store the delay time value.</span></span>

1.  <span data-ttu-id="64aa1-113">Substitua cada instância de m \_ fScaleFactor em Echo. h e Echo. cpp por m \_ dwDelayTime.</span><span class="sxs-lookup"><span data-stu-id="64aa1-113">Replace each instance of m\_fScaleFactor in Echo.h and Echo.cpp with m\_dwDelayTime.</span></span>
2.  <span data-ttu-id="64aa1-114">Altere o tipo de dados para m \_ fScaleFactor (agora m \_ dwDelayTime) de Double para DWORD em Echo. h.</span><span class="sxs-lookup"><span data-stu-id="64aa1-114">Change the data type for m\_fScaleFactor (now m\_dwDelayTime) from double to DWORD in Echo.h.</span></span>
3.  <span data-ttu-id="64aa1-115">No construtor para CEcho, altere o valor de tempo de atraso padrão para 1000.</span><span class="sxs-lookup"><span data-stu-id="64aa1-115">In the constructor for CEcho, change the default delay time value to 1000.</span></span>
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

<span data-ttu-id="64aa1-116">Em seguida, declare duas novas variáveis de membro para armazenar a porcentagem de sinal de efeito e a porcentagem de sinal de origem a ser misturada no buffer de saída final.</span><span class="sxs-lookup"><span data-stu-id="64aa1-116">Next, declare two new member variables to store the percentage of effect signal and the percentage of source signal to be mixed in the final output buffer.</span></span> <span data-ttu-id="64aa1-117">O termo "úmida" refere-se ao efeito, e o termo "seca" refere-se ao sinal de origem.</span><span class="sxs-lookup"><span data-stu-id="64aa1-117">The term "wet" refers to the effect, and the term "dry" refers to the source signal.</span></span> <span data-ttu-id="64aa1-118">Adicione as seguintes declarações a Echo. h:</span><span class="sxs-lookup"><span data-stu-id="64aa1-118">Add the following declarations to Echo.h:</span></span>


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



<span data-ttu-id="64aa1-119">Esses valores são armazenados como representações decimais de percentuais para que possam ser facilmente usados como fatores de escala.</span><span class="sxs-lookup"><span data-stu-id="64aa1-119">These values are stored as decimal representations of percentages so they can easily be used as scale factors.</span></span> <span data-ttu-id="64aa1-120">Por exemplo, uma mistura de 50% de efeito de porcentagem e de 50% de sinal de origem seria representada como um valor de 0,50 para cada variável.</span><span class="sxs-lookup"><span data-stu-id="64aa1-120">For instance, a mixture of 50 percent effect and 50 percent source signal would be represented as a value of 0.50 for each variable.</span></span> <span data-ttu-id="64aa1-121">A soma dos valores para m \_ fWetMix e m \_ fDryMix não deve ser maior que 1,0 (100 por cento).</span><span class="sxs-lookup"><span data-stu-id="64aa1-121">The sum of the values for m\_fWetMix and m\_fDryMix must not be more than 1.0 (100 percent).</span></span> <span data-ttu-id="64aa1-122">Eventualmente, esses valores estarão acessíveis como propriedades.</span><span class="sxs-lookup"><span data-stu-id="64aa1-122">Eventually, these values will be accessible as properties.</span></span>

<span data-ttu-id="64aa1-123">Adicione o seguinte código ao Construtor CEcho para definir os valores padrão como 50% a cada:</span><span class="sxs-lookup"><span data-stu-id="64aa1-123">Add the following code to the CEcho constructor to set the default values to 50 percent each:</span></span>


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a><span data-ttu-id="64aa1-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64aa1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64aa1-125">**Propriedades de exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="64aa1-125">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




