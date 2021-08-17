---
title: Implementando o exemplo de renderização
description: Implementando o exemplo de renderização
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- visualizações, exemplo de Brilho
- visualizações personalizadas, amostra de Brilho
- guia de programação, visualizações
- exemplos, visualização do Brilho
- Exemplo de visualização de brilho
- visualizações, função Renderizar
- visualizações personalizadas, função Renderizar
- Função renderizar, exemplo de Brilho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c00b57f15655468e5bd0000ccc3b5120e19c2af58d5a1ad6b5493b535c7253f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135569"
---
# <a name="implementing-render-sample"></a>Implementando o exemplo de renderização

O código a seguir é usado para implementar a **função Renderizar:**


```C++
STDMETHODIMP CGlow::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    COLORREF mycolor;
    int mylevel = pLevels->waveform[0][0];
    
    switch (m_nPreset)
    {
    case PRESET_RED:
        {
        mycolor = RGB( mylevel, 0, 0);    
        }
        break;
    case PRESET_GREEN:
        {
        mycolor = RGB( 0, mylevel, 0);        
        }
        break;
    case PRESET_BLUE:
        {
        mycolor = RGB( 0, 0, mylevel);        
        }
        break;
    }

     HBRUSH hNewBrush = ::CreateSolidBrush( mycolor );
    ::FillRect( hdc, prc, hNewBrush );

    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }

    return S_OK;
}

```



Aqui está uma explicação do código:

Uma variável *chamada mycolor* é usada para a cor do brilho e é declarada com **COLORREF**. Todas as cores devem usar o **tipo de dados COLORREF.**

Uma variável chamada *mylevel* é usada para o instantâneo de nível de forma de onda de áudio. Esse valor dependerá do nível de energia real no momento do instantâneo.

A **instrução** switch é definida pela predefinição que o usuário escolheu Windows Media Player. A opção definirá *mycolor* como a cor desejada (vermelho, verde ou azul). No entanto, a cor exata será determinada pelo nível de energia de áudio. Por exemplo, se a predefinição vermelha for escolhida, a cor será um vermelho sólido, mas será mais clara ou mais escura, dependendo da forma de onda de áudio no momento do instantâneo. Use a macro **RBG** para criar sua cor.

Um pincel é criado chamado *hNewBrush* e é usado para preencher o retângulo *prc* fornecido por Windows Media Player. A superfície de desenho é o contexto do dispositivo *hdc* fornecido pelo Windows Media Player.

O pincel é excluído por **DeleteObject.** Sempre exclua as canetas ou pincéis que você criar.

Depois que **o código** renderizar for concluído, Windows Media Player exibirá os elementos gráficos *hdc* em uma janela determinada pela capa que está sendo usada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**O exemplo de brilho**](the-glow-sample.md)
</dt> </dl>

 

 




