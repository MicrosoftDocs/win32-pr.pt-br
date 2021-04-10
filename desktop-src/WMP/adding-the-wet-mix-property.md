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
# <a name="adding-the-wet-mix-property"></a>Adicionando a propriedade de combinação úmida

Você deve adicionar o código para fornecer a propriedade adicional para o nível de efeito.

A seção [adicionando Propriedades ao plug-in de DSP de áudio de exemplo](adding-properties-to-the-sample-audio-dsp-plug-in.md) fornece detalhes sobre como adicionar uma nova propriedade usando Visual C++. Esta seção mostra como adicionar o código manualmente. Isso envolve a adição de código nos mesmos três locais em que você modificou o código da propriedade tempo de atraso.

Adicione os protótipos para os \_ métodos get WETMIX e Put \_ WETMIX imediatamente seguindo os outros protótipos de método de propriedade em Echo. h. Use a seguinte sintaxe:


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



Agora, adicione a implementação para cada método imediatamente seguindo as outras implementações de propriedade em Echo. cpp. O exemplo a seguir mostra o código para ambos os métodos:


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



Observe que a implementação de Put \_ WETMIX inclui o código para calcular o valor correto para m \_ fDryMix. Cada vez que um novo valor é especificado para m \_ fWetMix, esse cálculo é necessário.

Adicione o seguinte código à definição de interface logo após o código para os métodos de atraso em Echo. idl:


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedades de exemplo de eco**](echo-sample-properties.md)
</dt> </dl>

 

 




