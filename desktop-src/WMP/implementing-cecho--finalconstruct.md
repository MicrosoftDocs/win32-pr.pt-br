---
title: Implementando CEcho FinalConstruct
description: Implementando CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
- Exemplo de plug-in do eco DSP, método CEcho FinalConstruct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876db9f2479644800c42354a041ad3b1909b526b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084067"
---
# <a name="implementing-cechofinalconstruct"></a><span data-ttu-id="e2ede-109">Implementando CEcho:: FinalConstruct</span><span class="sxs-lookup"><span data-stu-id="e2ede-109">Implementing CEcho::FinalConstruct</span></span>

<span data-ttu-id="e2ede-110">O método CEcho:: FinalConstruct é implementado em Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="e2ede-110">The CEcho::FinalConstruct method is implemented in Echo.cpp.</span></span> <span data-ttu-id="e2ede-111">Ele contém o código para ler os valores de Propriedade do registro quando o Windows Media Player instancia o objeto de plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="e2ede-111">It contains code to read the property values from the registry when Windows Media Player instantiates the DSP plug-in object.</span></span> <span data-ttu-id="e2ede-112">Isso é importante porque permite que as configurações do usuário persistam entre instâncias do objeto, bem como entre sessões.</span><span class="sxs-lookup"><span data-stu-id="e2ede-112">This is important because it allows the user settings to persist between instances of the object, as well as between sessions.</span></span> <span data-ttu-id="e2ede-113">O código de exemplo do assistente de plug-in fornece implementação para ler uma única propriedade do registro.</span><span class="sxs-lookup"><span data-stu-id="e2ede-113">The plug-in wizard sample code provides implementation to read a single property from the registry.</span></span> <span data-ttu-id="e2ede-114">Você pode modificar esse código para manipular a propriedade de tempo de atraso e, em seguida, adicionar código para ler o valor da propriedade de combinação úmida.</span><span class="sxs-lookup"><span data-stu-id="e2ede-114">You can modify this code to handle the delay time property, and then add code to read the wet mix property value.</span></span>

<span data-ttu-id="e2ede-115">O código de exemplo a seguir lê cada valor de Propriedade do registro e armazena cada um na variável de membro correta:</span><span class="sxs-lookup"><span data-stu-id="e2ede-115">The following example code reads each property value from the registry and stores each in the correct member variable:</span></span>


```CSharp
CRegKey key;
LONG    lResult;
DWORD   dwValue;

lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
if (ERROR_SUCCESS == lResult)
{
    // Read the delay time from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
    if (ERROR_SUCCESS == lResult)
    {
        m_dwDelayTime = dwValue;
    }

    // Read the wet mix value from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsWetmix );
    if (ERROR_SUCCESS == lResult)
    {
        // Convert the DWORD to a double.
        m_fWetMix = (double)dwValue / 100;
        // Calculate the dry mix value.
        m_fDryMix = 1.0 - m_fWetMix;
    }

}

return S_OK;
```



<span data-ttu-id="e2ede-116">Observe que o valor DWORD para a combinação úmida é convertido em um valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="e2ede-116">Notice that the DWORD value for the wet mix is converted to a floating-point value.</span></span> <span data-ttu-id="e2ede-117">Observe também que o código calcula o valor correto para m \_ fDryMix.</span><span class="sxs-lookup"><span data-stu-id="e2ede-117">Also note that the code calculates the correct value for m\_fDryMix.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2ede-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2ede-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2ede-119">**Modificando a página de propriedades de exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="e2ede-119">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




