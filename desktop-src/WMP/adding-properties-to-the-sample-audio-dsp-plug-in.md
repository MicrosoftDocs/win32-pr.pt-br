---
title: Adicionando propriedades ao plug-in do DSP de áudio de exemplo
description: Adicionando propriedades ao plug-in do DSP de áudio de exemplo
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- Plug-ins do Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, propriedades de áudio
- Plug-ins do DSP, propriedades de áudio
- plug-ins do DSP de áudio, propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ab1054631b09997ac986529a641e6ff05ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813391"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a>Adicionando propriedades ao plug-in do DSP de áudio de exemplo

O código de exemplo do DSP de áudio que o assistente de plug-in do Windows Media Player gera usa uma única propriedade que representa o fator de escala para o volume de áudio. Seu plug-in pode exigir mais de uma propriedade. Você pode adicionar propriedades facilmente ao seu plug-in do DSP no Visual Studio usando as seguintes etapas:

-   Defina os métodos no código de definição de interface no arquivo IDL que faz parte do projeto de stub de proxy.
    -   Adicione as implementações do método ao arquivo CPP principal do projeto:

    ```C++
    STDMETHODIMP CYourProject::get_color(COLORREF *pColor)
    {
        if ( NULL == pColor )
        {
            return E_POINTER;
        }

        *pColor = m_Color;

        return S_OK;
    }

    STDMETHODIMP CYourProject::put_color(COLORREF newColor)
    {
        m_Color = newColor;
        
        return S_OK;
    }
    
    ```

    

Por fim, para tornar as propriedades acessíveis ao usuário, você desejará fazer alterações na implementação da página de propriedades.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando um plug-in do DSP de áudio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




