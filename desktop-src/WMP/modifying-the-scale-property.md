---
title: Modificando a propriedade Scale
description: Modificando a propriedade Scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Plug-ins do Windows Media Player, propriedades de exemplo de eco
- plug-ins, propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, propriedades de exemplo de eco
- Plug-ins do DSP, propriedades de exemplo de eco
- Exemplo de plug-in do DSP de eco, Propriedade Scale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763909"
---
# <a name="modifying-the-scale-property"></a>Modificando a propriedade Scale

A implementação do assistente padrão expõe a propriedade Scale. Você pode alterar a implementação existente para expor a propriedade tempo de atraso em vez disso.

Primeiro, use o exemplo a seguir para alterar os protótipos de função para obter \_ escala e colocar \_ escala em Echo. h. Altere o nome dos métodos e os tipos de dados para os parâmetros:


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



Em seguida, altere as implementações dos \_ métodos obter escala e colocar \_ escala em Echo. cpp. Faça com que o código corresponda aos seguintes exemplos:


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

Agora, altere a definição da interface. O código a seguir substitui o código na declaração de interface IEcho em Echo. idl:


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Propriedades de exemplo de eco**](echo-sample-properties.md)
</dt> </dl>

 

 




