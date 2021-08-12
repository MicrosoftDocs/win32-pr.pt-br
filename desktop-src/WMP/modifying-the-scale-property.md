---
title: Modificando a propriedade Scale
description: Modificando a propriedade Scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Windows Media Player plug-ins, propriedades de exemplo de eco
- plug-ins, propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, propriedades de exemplo de eco
- Plug-ins DSP, propriedades de exemplo de eco
- Exemplo de plug-in do DSP de eco, propriedade de escala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10073e01213469dcb6a85ddffd378421fddb6ae8f2fd432b9822c3a5046fdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574613"
---
# <a name="modifying-the-scale-property"></a>Modificando a propriedade Scale

A implementação padrão do assistente expõe a propriedade de escala. Você pode alterar a implementação existente para expor a propriedade de tempo de atraso.

Primeiro, use o exemplo a seguir para alterar os protótipos de função para obter \_ escala e colocar a escala em \_ Echo.h. Altere o nome dos métodos e os tipos de dados para os parâmetros:


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



Em seguida, altere as implementações da escala get e coloque os métodos \_ \_ de escala em Echo.cpp. Faça o código corresponder aos seguintes exemplos:


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



O código de exemplo anterior altera os nomes de método e os tipos de dados de parâmetro. O nome da variável de membro deve ter sido alterado anteriormente. Lembre-se de alterar os comentários que introduzem cada método também.

Agora, altere a definição da interface. O código a seguir substitui o código na declaração da interface IEcho em Echo.idl:


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedades de exemplo de eco**](echo-sample-properties.md)
</dt> </dl>

 

 




