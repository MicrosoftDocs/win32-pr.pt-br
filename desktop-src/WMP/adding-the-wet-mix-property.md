---
title: Adicionando a propriedade de combinação úmida
description: Adicionando a propriedade de combinação úmida
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Plug-ins do Windows Media Player, propriedades de exemplo de eco
- plug-ins, propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, propriedades de exemplo de eco
- Plug-ins do DSP, propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, propriedades
- Exemplo de plug-in do eco DSP, Propriedade Mix úmida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292213"
---
# <a name="adding-the-wet-mix-property"></a><span data-ttu-id="a981c-109">Adicionando a propriedade de combinação úmida</span><span class="sxs-lookup"><span data-stu-id="a981c-109">Adding the Wet Mix Property</span></span>

<span data-ttu-id="a981c-110">Você deve adicionar o código para fornecer a propriedade adicional para o nível de efeito.</span><span class="sxs-lookup"><span data-stu-id="a981c-110">You must add the code to provide the additional property for the effect level.</span></span>

<span data-ttu-id="a981c-111">A seção [adicionando Propriedades ao plug-in de DSP de áudio de exemplo](adding-properties-to-the-sample-audio-dsp-plug-in.md) fornece detalhes sobre como adicionar uma nova propriedade usando Visual C++.</span><span class="sxs-lookup"><span data-stu-id="a981c-111">The section [Adding Properties to the Sample Audio DSP Plug-in](adding-properties-to-the-sample-audio-dsp-plug-in.md) provides details about how to add a new property using Visual C++.</span></span> <span data-ttu-id="a981c-112">Esta seção mostra como adicionar o código manualmente.</span><span class="sxs-lookup"><span data-stu-id="a981c-112">This section shows you how to add the code manually.</span></span> <span data-ttu-id="a981c-113">Isso envolve a adição de código nos mesmos três locais em que você modificou o código da propriedade tempo de atraso.</span><span class="sxs-lookup"><span data-stu-id="a981c-113">This entails adding code in the same three places where you modified the code for the delay time property.</span></span>

<span data-ttu-id="a981c-114">Adicione os protótipos para os \_ métodos get WETMIX e Put \_ WETMIX imediatamente seguindo os outros protótipos de método de propriedade em Echo. h.</span><span class="sxs-lookup"><span data-stu-id="a981c-114">Add the prototypes for the get\_wetmix and put\_wetmix methods immediately following the other property method prototypes in Echo.h.</span></span> <span data-ttu-id="a981c-115">Use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="a981c-115">Use the following syntax:</span></span>


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



<span data-ttu-id="a981c-116">Agora, adicione a implementação para cada método imediatamente seguindo as outras implementações de propriedade em Echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="a981c-116">Now, add the implementation for each method immediately following the other property implementations in Echo.cpp.</span></span> <span data-ttu-id="a981c-117">O exemplo a seguir mostra o código para ambos os métodos:</span><span class="sxs-lookup"><span data-stu-id="a981c-117">The following example shows the code for both methods:</span></span>


```C++
// Property get to retrieve the wet mix value by using the public interface.
STDMETHODIMP CEcho::get_wetmix(double *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_fWetMix;

    return S_OK;
}

// Property put to store the wet mix value by using the public interface.
STDMETHODIMP CEcho::put_wetmix(double newVal)
{
    m_fWetMix = newVal;

    // Calculate m_fDryMix
    m_fDryMix = 1.0 - m_fWetMix;
    
    return S_OK;
}

```



<span data-ttu-id="a981c-118">Observe que a implementação de Put \_ WETMIX inclui o código para calcular o valor correto para m \_ fDryMix.</span><span class="sxs-lookup"><span data-stu-id="a981c-118">Notice that the implementation of put\_wetmix includes the code to calculate the correct value for m\_fDryMix.</span></span> <span data-ttu-id="a981c-119">Cada vez que um novo valor é especificado para m \_ fWetMix, esse cálculo é necessário.</span><span class="sxs-lookup"><span data-stu-id="a981c-119">Each time a new value is specified for m\_fWetMix, this calculation is required.</span></span>

<span data-ttu-id="a981c-120">Adicione o seguinte código à definição de interface logo após o código para os métodos de atraso em Echo. idl:</span><span class="sxs-lookup"><span data-stu-id="a981c-120">Add the following code in the interface definition just after the code for the delay methods in Echo.idl:</span></span>


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a><span data-ttu-id="a981c-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a981c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a981c-122">**Propriedades de exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="a981c-122">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




