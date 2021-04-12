---
title: Implementando exemplo de renderização
description: Implementando exemplo de renderização
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- visualizações, exemplo de brilho
- visualizações personalizadas, exemplo de brilho
- Guia de programação, visualizações
- amostras, visualização de brilho
- Exemplo de visualização de brilho
- visualizações, função render
- visualizações personalizadas, função render
- Função render, exemplo de brilho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabc816283113a82c1d5d677dfc0ca8e8887d344
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499225"
---
# <a name="implementing-render-sample"></a>Implementando exemplo de renderização

O código a seguir é usado para implementar a função **render** :


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

Uma variável chamada *MyColor* é usada para a cor do brilho e é declarada com **COLORREF**. Todas as cores devem usar o tipo de dados **COLORREF** .

Uma variável chamada *MyLevel* é usada para o instantâneo do nível de onda de áudio. Esse valor dependerá do nível de energia real no momento do instantâneo.

A instrução **switch** é definida pela predefinição que o usuário escolheu no Windows Media Player. A opção definirá *MyColor* como a cor desejada (vermelho, verde ou azul). No entanto, a cor exata será determinada pelo nível de energia de áudio. Por exemplo, se a predefinição vermelha for escolhida, a cor será um vermelho sólido, mas será mais clara ou mais escura dependendo da forma de onda de áudio no momento do instantâneo. Certifique-se de usar a macro **RGB** para criar sua cor.

Um pincel é criado chamado *hNewBrush* e é usado para preencher o retângulo *prc* fornecido pelo Windows Media Player. A superfície de desenho é o contexto de dispositivo *HDC* fornecido pelo Windows Media Player.

O pincel é excluído por **ExcluirObjeto**. Sempre certifique-se de excluir as canetas ou os pincéis que você criar.

Depois que o código de **renderização** for concluído, o Windows Media Player exibirá os gráficos *HDC* em uma janela determinada pela capa que está sendo usada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**O exemplo de brilho**](the-glow-sample.md)
</dt> </dl>

 

 




