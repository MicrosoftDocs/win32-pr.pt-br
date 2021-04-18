---
description: Visão geral da estrutura de serviços de texto para o Tablet PC.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Estrutura de serviços de texto (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788085"
---
# <a name="text-services-framework-tablet-pc"></a><span data-ttu-id="95c60-103">Estrutura de serviços de texto (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="95c60-103">Text Services Framework (Tablet PC)</span></span>

<span data-ttu-id="95c60-104">Quando a [estrutura de serviços de texto (TSF)](../tsf/text-services-framework.md) é habilitada em um controle com um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) anexado, o objeto PenInputPanel pode inserir texto diretamente.</span><span class="sxs-lookup"><span data-stu-id="95c60-104">When the [Text Services Framework (TSF)](../tsf/text-services-framework.md) is enabled on a control with a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached, the PenInputPanel object can insert text directly.</span></span> <span data-ttu-id="95c60-105">Se o controle não oferecer suporte à TSF (estrutura de serviços de texto), o objeto PenInputPanel deverá recorrer ao uso da [função SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) para inserir texto.</span><span class="sxs-lookup"><span data-stu-id="95c60-105">If the control does not support Text Services Framework (TSF), the PenInputPanel object must resort to using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) to insert text.</span></span>

<span data-ttu-id="95c60-106">A capacidade de inserir texto diretamente se torna muito importante para aqueles que estão inserindo caracteres do leste asiático, em que o uso da [função SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) pode produzir caracteres incorretos.</span><span class="sxs-lookup"><span data-stu-id="95c60-106">The ability to insert text directly becomes very important for those inputting East Asian characters, where using the [SendInput function](/windows/win32/api/winuser/nf-winuser-sendinput) can produce incorrect characters.</span></span>

<span data-ttu-id="95c60-107">O TSF fornece uma interface para corrigir erros de reconhecimento, permitindo que o usuário final corrija, reescreva ou até mesmo dite o texto adequado.</span><span class="sxs-lookup"><span data-stu-id="95c60-107">TSF provides an interface for correcting recognition errors enabling the end user to correct, rewrite, or even dictate the proper text.</span></span>

<span data-ttu-id="95c60-108">O TSF é habilitado chamando o método [EnableTsf](/previous-versions/ms569656(v=vs.100)) com o parâmetro *Enable* definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="95c60-108">TSF is enabled by calling the [EnableTsf](/previous-versions/ms569656(v=vs.100)) method with the *enable* parameter set to **TRUE**.</span></span>

<span data-ttu-id="95c60-109">\[C\#\]</span><span class="sxs-lookup"><span data-stu-id="95c60-109">\[C\#\]</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



<span data-ttu-id="95c60-110">Um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) anexado a um controle [InkEdit](/previous-versions/ms552265(v=vs.100)) fornece uma experiência de usuário robusta, pois INKEDIT dá suporte a TSF.</span><span class="sxs-lookup"><span data-stu-id="95c60-110">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object attached to a [InkEdit](/previous-versions/ms552265(v=vs.100)) control provides a robust user experience because the InkEdit supports TSF.</span></span> <span data-ttu-id="95c60-111">No entanto, certifique-se de definir a propriedade [InkMode](/previous-versions/ms835850(v=msdn.10)) como [Microsoft. Ink. InkMode. Ink](/previous-versions/ms827399(v=msdn.10)) no controle InkEdit conforme mencionado no tópico [práticas recomendadas](best-practices.md) .</span><span class="sxs-lookup"><span data-stu-id="95c60-111">However, be sure to set the [InkMode](/previous-versions/ms835850(v=msdn.10)) property to [Microsoft.Ink.InkMode.Ink](/previous-versions/ms827399(v=msdn.10)) on the InkEdit control as mentioned in the [Best Practices](best-practices.md) topic.</span></span>

<span data-ttu-id="95c60-112">O [exemplo PenInputPanel](peninputpanel-sample.md) fornece um exemplo de como habilitar o TSF.</span><span class="sxs-lookup"><span data-stu-id="95c60-112">The [PenInputPanel Sample](peninputpanel-sample.md) provides an example of enabling TSF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95c60-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="95c60-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95c60-114">Estrutura de serviços de texto</span><span class="sxs-lookup"><span data-stu-id="95c60-114">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
