---
title: Adicionando a propriedade De mistura de umidade
description: Adicionando a propriedade De mistura de umidade
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Windows Media Player plug-ins, propriedades de exemplo de eco
- plug-ins, propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, propriedades de exemplo de eco
- Plug-ins DSP, propriedades de exemplo de eco
- Exemplo de plug-in do DSP de eco, propriedades
- Exemplo de plug-in do DSP de eco, propriedade de combinação de umidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f743cc25ce25aed1e7ff5695c022d65e30c1680eee4121eb3952698d6f0da94f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055414"
---
# <a name="adding-the-wet-mix-property"></a>Adicionando a propriedade De mistura de umidade

Você deve adicionar o código para fornecer a propriedade adicional para o nível de efeito.

A seção [Adicionando propriedades ao plug-in DSP](adding-properties-to-the-sample-audio-dsp-plug-in.md) de áudio de exemplo fornece detalhes sobre como adicionar uma nova propriedade usando Visual C++. Esta seção mostra como adicionar o código manualmente. Isso envolve a adição de código nos mesmos três locais em que você modificou o código para a propriedade de tempo de atraso.

Adicione os protótipos para os métodos get wetmix e put wetmix imediatamente após os outros protótipos de método de propriedade \_ \_ em Echo.h. Use a seguinte sintaxe:


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



Agora, adicione a implementação para cada método imediatamente após as outras implementações de propriedade em Echo.cpp. O exemplo a seguir mostra o código para ambos os métodos:


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



Observe que a implementação de put wetmix inclui o código para calcular o \_ valor correto para m \_ fDryMix. Sempre que um novo valor for especificado para m \_ fWetMix, esse cálculo será necessário.

Adicione o seguinte código na definição da interface logo após o código para os métodos de atraso em Echo.idl:


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedades de exemplo de eco**](echo-sample-properties.md)
</dt> </dl>

 

 




