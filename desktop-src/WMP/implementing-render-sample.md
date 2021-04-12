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
# <a name="implementing-render-sample"></a><span data-ttu-id="8b15b-111">Implementando exemplo de renderização</span><span class="sxs-lookup"><span data-stu-id="8b15b-111">Implementing Render Sample</span></span>

<span data-ttu-id="8b15b-112">O código a seguir é usado para implementar a função **render** :</span><span class="sxs-lookup"><span data-stu-id="8b15b-112">The following code is used to implement the **Render** function:</span></span>


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



<span data-ttu-id="8b15b-113">Aqui está uma explicação do código:</span><span class="sxs-lookup"><span data-stu-id="8b15b-113">Here is an explanation of the code:</span></span>

<span data-ttu-id="8b15b-114">Uma variável chamada *MyColor* é usada para a cor do brilho e é declarada com **COLORREF**.</span><span class="sxs-lookup"><span data-stu-id="8b15b-114">A variable named *mycolor* is used for the color of the glow and is declared with **COLORREF**.</span></span> <span data-ttu-id="8b15b-115">Todas as cores devem usar o tipo de dados **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="8b15b-115">All colors should use the **COLORREF** data type.</span></span>

<span data-ttu-id="8b15b-116">Uma variável chamada *MyLevel* é usada para o instantâneo do nível de onda de áudio.</span><span class="sxs-lookup"><span data-stu-id="8b15b-116">A variable named *mylevel* is used for the audio waveform level snapshot.</span></span> <span data-ttu-id="8b15b-117">Esse valor dependerá do nível de energia real no momento do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="8b15b-117">This value will depend on the actual power level at the moment of the snapshot.</span></span>

<span data-ttu-id="8b15b-118">A instrução **switch** é definida pela predefinição que o usuário escolheu no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8b15b-118">The **switch** statement is set by the preset that the user has chosen on Windows Media Player.</span></span> <span data-ttu-id="8b15b-119">A opção definirá *MyColor* como a cor desejada (vermelho, verde ou azul).</span><span class="sxs-lookup"><span data-stu-id="8b15b-119">The choice will set *mycolor* to the desired color (red, green, or blue).</span></span> <span data-ttu-id="8b15b-120">No entanto, a cor exata será determinada pelo nível de energia de áudio.</span><span class="sxs-lookup"><span data-stu-id="8b15b-120">However, the exact color will be determined by the audio power level.</span></span> <span data-ttu-id="8b15b-121">Por exemplo, se a predefinição vermelha for escolhida, a cor será um vermelho sólido, mas será mais clara ou mais escura dependendo da forma de onda de áudio no momento do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="8b15b-121">For example, if the red preset is chosen, the color will be a solid red, but it will be lighter or darker depending on the audio waveform at the moment of the snapshot.</span></span> <span data-ttu-id="8b15b-122">Certifique-se de usar a macro **RGB** para criar sua cor.</span><span class="sxs-lookup"><span data-stu-id="8b15b-122">Be sure to use the **RBG** macro to create your color.</span></span>

<span data-ttu-id="8b15b-123">Um pincel é criado chamado *hNewBrush* e é usado para preencher o retângulo *prc* fornecido pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8b15b-123">A brush is created called *hNewBrush*, and it is used to fill the *prc* rectangle provided by Windows Media Player.</span></span> <span data-ttu-id="8b15b-124">A superfície de desenho é o contexto de dispositivo *HDC* fornecido pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8b15b-124">The drawing surface is the *hdc* device context provided by Windows Media Player.</span></span>

<span data-ttu-id="8b15b-125">O pincel é excluído por **ExcluirObjeto**.</span><span class="sxs-lookup"><span data-stu-id="8b15b-125">The brush is deleted by **DeleteObject**.</span></span> <span data-ttu-id="8b15b-126">Sempre certifique-se de excluir as canetas ou os pincéis que você criar.</span><span class="sxs-lookup"><span data-stu-id="8b15b-126">Always be sure to delete any pens or brushes you create.</span></span>

<span data-ttu-id="8b15b-127">Depois que o código de **renderização** for concluído, o Windows Media Player exibirá os gráficos *HDC* em uma janela determinada pela capa que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="8b15b-127">Once the **Render** code is finished, Windows Media Player will display the *hdc* graphics in a window determined by the skin being used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b15b-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b15b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b15b-129">**O exemplo de brilho**</span><span class="sxs-lookup"><span data-stu-id="8b15b-129">**The Glow Sample**</span></span>](the-glow-sample.md)
</dt> </dl>

 

 




