---
description: O controle InkEdit fornece uma maneira fácil de capturar, reconhecer e exibir tinta.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: Controle InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d5441506ee791eefddba05b9b1f3ddb8a8ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828899"
---
# <a name="inkedit-control"></a><span data-ttu-id="b01e9-103">Controle InkEdit</span><span class="sxs-lookup"><span data-stu-id="b01e9-103">InkEdit Control</span></span>

<span data-ttu-id="b01e9-104">O controle [InkEdit](inkedit-control-reference.md) fornece uma maneira fácil de capturar, reconhecer e exibir tinta.</span><span class="sxs-lookup"><span data-stu-id="b01e9-104">The [InkEdit](inkedit-control-reference.md) control provides an easy way to capture, recognize, and display ink.</span></span>

<span data-ttu-id="b01e9-105">Essa implementação do controle [InkEdit](inkedit-control-reference.md) é baseada no controle [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="b01e9-105">This implementation of the [InkEdit](inkedit-control-reference.md) control is based on the [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) control.</span></span> <span data-ttu-id="b01e9-106">A implementação gerenciada (.NET Framework) de [InkEdit](/previous-versions/ms835842(v=msdn.10)) é baseada no controle [**RichTextBox**](/previous-versions/windows/) .</span><span class="sxs-lookup"><span data-stu-id="b01e9-106">The managed (.NET Framework) implementation of [InkEdit](/previous-versions/ms835842(v=msdn.10)) is based on the [**RichTextBox**](/previous-versions/windows/) control.</span></span>

<span data-ttu-id="b01e9-107">A principal finalidade do controle [InkEdit](inkedit-control-reference.md) é coletar tinta, reconhecê-la e exibi-la em formato de texto.</span><span class="sxs-lookup"><span data-stu-id="b01e9-107">The primary purpose of the [InkEdit](inkedit-control-reference.md) control is to collect ink, recognize it, and display it in text form.</span></span> <span data-ttu-id="b01e9-108">Além disso, ele dá suporte à exibição de tinta como um objeto incorporado com recursos de formatação de texto, como negrito e sublinhado.</span><span class="sxs-lookup"><span data-stu-id="b01e9-108">Additionally, it supports displaying ink as an embedded object with text formatting capabilities, such as bold and underline.</span></span>

## <a name="gestures-and-correction"></a><span data-ttu-id="b01e9-109">Gestos e correção</span><span class="sxs-lookup"><span data-stu-id="b01e9-109">Gestures and Correction</span></span>

<span data-ttu-id="b01e9-110">[InkEdit](inkedit-control-reference.md) dá suporte aos seguintes gestos.</span><span class="sxs-lookup"><span data-stu-id="b01e9-110">[InkEdit](inkedit-control-reference.md) supports the following gestures.</span></span>



| <span data-ttu-id="b01e9-111">Gesto</span><span class="sxs-lookup"><span data-stu-id="b01e9-111">Gesture</span></span>                                                                    | <span data-ttu-id="b01e9-112">Nome do gesto</span><span class="sxs-lookup"><span data-stu-id="b01e9-112">Gesture Name</span></span>              | <span data-ttu-id="b01e9-113">Ação</span><span class="sxs-lookup"><span data-stu-id="b01e9-113">Action</span></span>               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![gesto para baixo à esquerda](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | <span data-ttu-id="b01e9-115">Para baixo à esquerda</span><span class="sxs-lookup"><span data-stu-id="b01e9-115">Down-left</span></span><br/>      | <span data-ttu-id="b01e9-116">Digite</span><span class="sxs-lookup"><span data-stu-id="b01e9-116">Enter</span></span><br/>     |
| ![gesto para baixo-esquerdo-longo](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | <span data-ttu-id="b01e9-118">Para baixo à esquerda-longa</span><span class="sxs-lookup"><span data-stu-id="b01e9-118">Down-left-long</span></span><br/> | <span data-ttu-id="b01e9-119">Digite</span><span class="sxs-lookup"><span data-stu-id="b01e9-119">Enter</span></span><br/>     |
| ![gesto para cima para a direita](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | <span data-ttu-id="b01e9-121">Para cima à direita</span><span class="sxs-lookup"><span data-stu-id="b01e9-121">Up-right</span></span><br/>       | <span data-ttu-id="b01e9-122">Tab</span><span class="sxs-lookup"><span data-stu-id="b01e9-122">Tab</span></span><br/>       |
| ![gesto de cima para a direita.](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | <span data-ttu-id="b01e9-124">Para cima à direita</span><span class="sxs-lookup"><span data-stu-id="b01e9-124">Up-right-long</span></span><br/>  | <span data-ttu-id="b01e9-125">Tab</span><span class="sxs-lookup"><span data-stu-id="b01e9-125">Tab</span></span><br/>       |
| ![gesto direito](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | <span data-ttu-id="b01e9-127">Direita</span><span class="sxs-lookup"><span data-stu-id="b01e9-127">Right</span></span><br/>          | <span data-ttu-id="b01e9-128">Space</span><span class="sxs-lookup"><span data-stu-id="b01e9-128">Space</span></span><br/>     |
| ![gesto esquerdo](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | <span data-ttu-id="b01e9-130">Esquerda</span><span class="sxs-lookup"><span data-stu-id="b01e9-130">Left</span></span><br/>           | <span data-ttu-id="b01e9-131">Backspace</span><span class="sxs-lookup"><span data-stu-id="b01e9-131">Backspace</span></span><br/> |



 

<span data-ttu-id="b01e9-132">Os eventos de gesto que você pode manipular contêm informações de gesto, traço e cursor que podem ser usadas para enviar texto para [InkEdit](inkedit-control-reference.md) ou inserir dados na área de transferência.</span><span class="sxs-lookup"><span data-stu-id="b01e9-132">Gesture events that you can handle contain gesture, stroke, and cursor information you can use to send text to [InkEdit](inkedit-control-reference.md) or place data on the clipboard.</span></span>

<span data-ttu-id="b01e9-133">[InkEdit](inkedit-control-reference.md) também fornece uma interface do usuário de correção que permite que os usuários exibam e selecionem alternativas, usem o teclado na tela e os reconhecedores de caractere/letra/bloco.</span><span class="sxs-lookup"><span data-stu-id="b01e9-133">[InkEdit](inkedit-control-reference.md) also provides a correction user interface that enables users to view and select from alternates, use the on-screen keyboard, and character/letter/block recognizers.</span></span>

## <a name="other-details"></a><span data-ttu-id="b01e9-134">Outros detalhes</span><span class="sxs-lookup"><span data-stu-id="b01e9-134">Other Details</span></span>

<span data-ttu-id="b01e9-135">[InkEdit](inkedit-control-reference.md) foi projetado para funcionar bem em um cenário de formulário para uma única linha, bem como entrada e edição de texto multilinha.</span><span class="sxs-lookup"><span data-stu-id="b01e9-135">[InkEdit](inkedit-control-reference.md) is designed to work well in a form scenario for single line as well as multiline text entry and editing.</span></span> <span data-ttu-id="b01e9-136">O uso pretendido principal para InkEdit é obter entrada de texto de um usuário na forma de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="b01e9-136">The primary intended use for InkEdit is to get text input from a user in the form of handwriting.</span></span> <span data-ttu-id="b01e9-137">Por padrão, a entrada de tinta é reconhecida e o texto é inserido em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="b01e9-137">By default, ink input is recognized and text is inserted in its place.</span></span> <span data-ttu-id="b01e9-138">A interface do usuário padrão para InkEdit é semelhante à do controle [**RichTextBox**](/previous-versions/windows/) , exceto quando o usuário está fazendo o layout da tinta.</span><span class="sxs-lookup"><span data-stu-id="b01e9-138">The default user interface for InkEdit resembles that of the [**RichTextBox**](/previous-versions/windows/) control, except when the user is laying down ink.</span></span> <span data-ttu-id="b01e9-139">Você pode exibir a tinta original em vez de texto; no entanto, a tinta é dimensionada para o tamanho da fonte de entrada atual do controle InkEdit e é exibida embutida com outro texto.</span><span class="sxs-lookup"><span data-stu-id="b01e9-139">You can display original ink rather than text; however, the ink is scaled to the current input font size of the InkEdit control and is displayed inline with other text.</span></span>

> [!Note]  
> <span data-ttu-id="b01e9-140">Por motivos de segurança, você deve usar os procedimentos padrão para abrir ou fechar um arquivo, transmitir a entrada/saída e definir a propriedade [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) ou [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) .</span><span class="sxs-lookup"><span data-stu-id="b01e9-140">For security reasons, you must use standard procedures to open or close a file, stream the input/output, and set the [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) or [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) property.</span></span>

 

<span data-ttu-id="b01e9-141">O controle [InkEdit](inkedit-control-reference.md) é definido para reconhecer tinta como texto por padrão.</span><span class="sxs-lookup"><span data-stu-id="b01e9-141">The [InkEdit](inkedit-control-reference.md) control is set to recognize ink as text by default.</span></span> <span data-ttu-id="b01e9-142">Para permitir que os usuários adicionem tinta como tinta, defina a propriedade [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) como **InsertAsInk**.</span><span class="sxs-lookup"><span data-stu-id="b01e9-142">To enable users to add ink as ink, set the [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) property to **InsertAsInk**.</span></span>

<span data-ttu-id="b01e9-143">Para obter informações de referência detalhadas sobre o controle [InkEdit](inkedit-control-reference.md) , consulte InkEdit.</span><span class="sxs-lookup"><span data-stu-id="b01e9-143">For detailed reference information about the [InkEdit](inkedit-control-reference.md) control, see InkEdit.</span></span>

> [!Note]  
> <span data-ttu-id="b01e9-144">Se você usar o controle do Win32 [InkEdit](inkedit-control-reference.md) e colocá-lo dentro de uma caixa de grupo, verifique se a caixa tem um estilo transparente; caso contrário, InkEdit não será capaz de coletar tinta.</span><span class="sxs-lookup"><span data-stu-id="b01e9-144">If you use the Win32 [InkEdit](inkedit-control-reference.md) control and place it inside a group box, make sure the box has a transparent style; otherwise, InkEdit is not able to collect ink.</span></span>

 

> [!Note]  
> <span data-ttu-id="b01e9-145">Para garantir que a tinta seja exibida corretamente, chame o método de [**atualização**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) de controle [InkEdit](inkedit-control-reference.md) quando receber um evento [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) ou [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="b01e9-145">To ensure ink is displayed properly, call the [InkEdit](inkedit-control-reference.md) control [**Refresh**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) method when it receives an [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) or [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) event.</span></span>

 

<span data-ttu-id="b01e9-146">As seções a seguir detalham o uso do controle [InkEdit](inkedit-control-reference.md) :</span><span class="sxs-lookup"><span data-stu-id="b01e9-146">The following sections detail the use of the [InkEdit](inkedit-control-reference.md) control:</span></span>

-   [<span data-ttu-id="b01e9-147">Instanciando InkEdit</span><span class="sxs-lookup"><span data-stu-id="b01e9-147">Instantiating InkEdit</span></span>](instantiating-inkedit.md)
-   [<span data-ttu-id="b01e9-148">Reconhecimento de palavra versus caractere</span><span class="sxs-lookup"><span data-stu-id="b01e9-148">Word vs. Character Recognition</span></span>](word-vs--character-recognition.md)
-   [<span data-ttu-id="b01e9-149">Exibindo tinta como tinta</span><span class="sxs-lookup"><span data-stu-id="b01e9-149">Displaying Ink as Ink</span></span>](displaying-ink-as-ink.md)
-   [<span data-ttu-id="b01e9-150">Usando InkEdit em versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="b01e9-150">Using InkEdit on Earlier Versions of Windows</span></span>](using-inkedit-on-earlier-versions-of-windows.md)
-   [<span data-ttu-id="b01e9-151">Usando um dicionário de aplicativo com InkEdit</span><span class="sxs-lookup"><span data-stu-id="b01e9-151">Using an Application Dictionary with InkEdit</span></span>](using-an-application-dictionary-with-inkedit.md)

 

