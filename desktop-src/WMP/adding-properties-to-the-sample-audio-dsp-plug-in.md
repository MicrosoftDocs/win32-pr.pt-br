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
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="2f2c4-108">Adicionando propriedades ao plug-in do DSP de áudio de exemplo</span><span class="sxs-lookup"><span data-stu-id="2f2c4-108">Adding Properties to the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="2f2c4-109">O código de exemplo do DSP de áudio que o assistente de plug-in do Windows Media Player gera usa uma única propriedade que representa o fator de escala para o volume de áudio.</span><span class="sxs-lookup"><span data-stu-id="2f2c4-109">The audio DSP sample code that the Windows Media Player Plug-in Wizard generates uses a single property that represents the scale factor for the audio volume.</span></span> <span data-ttu-id="2f2c4-110">Seu plug-in pode exigir mais de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="2f2c4-110">Your plug-in may require more than one property.</span></span> <span data-ttu-id="2f2c4-111">Você pode adicionar propriedades facilmente ao seu plug-in do DSP no Visual Studio usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="2f2c4-111">You can easily add properties to your DSP plug-in in Visual Studio using the following steps:</span></span>

-   <span data-ttu-id="2f2c4-112">Defina os métodos no código de definição de interface no arquivo IDL que faz parte do projeto de stub de proxy.</span><span class="sxs-lookup"><span data-stu-id="2f2c4-112">Define the methods in the interface definition code in the IDL file that is part of the proxy-stub project.</span></span>
    -   <span data-ttu-id="2f2c4-113">Adicione as implementações do método ao arquivo CPP principal do projeto:</span><span class="sxs-lookup"><span data-stu-id="2f2c4-113">Add the method implementations to the project's main CPP file:</span></span>

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

    

<span data-ttu-id="2f2c4-114">Por fim, para tornar as propriedades acessíveis ao usuário, você desejará fazer alterações na implementação da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="2f2c4-114">Finally, to make the properties accessible to the user, you'll want to make changes to the property page implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f2c4-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f2c4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f2c4-116">**Implementando um plug-in do DSP de áudio**</span><span class="sxs-lookup"><span data-stu-id="2f2c4-116">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




