---
title: Usando um editor de método de entrada em um jogo
description: Este artigo explica como você pode implementar um controle de edição IME básico em um aplicativo Microsoft DirectX de tela inteira.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1519f07a4e105ae822bd13fd7acd8b29e5ad8a0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103930522"
---
# <a name="using-an-input-method-editor-in-a-game"></a><span data-ttu-id="1c8c3-103">Usando um editor de método de entrada em um jogo</span><span class="sxs-lookup"><span data-stu-id="1c8c3-103">Using an Input Method Editor in a Game</span></span>

> [!Note]  
> <span data-ttu-id="1c8c3-104">Este artigo fornece detalhes sobre como trabalhar com o IME (editor de método de entrada) do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-104">This article details working with the Windows XP Input Method Editor (IME).</span></span> <span data-ttu-id="1c8c3-105">Foram feitas alterações no IME para Windows Vista que não são totalmente detalhadas neste artigo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-105">Changes were made to the IME for Windows Vista that are not fully detailed in this article.</span></span> <span data-ttu-id="1c8c3-106">Para obter mais informações sobre as alterações no IME para Windows Vista, consulte [Input Method Editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows Vista-uma exibição Ever-Expanding da internacionalização](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) no portal de desenvolvimento e computação global da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-106">For more info about changes to the IME for Windows Vista, see [Input Method Editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows Vista - An Ever-Expanding View of Internationalization](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) on the Microsoft Global Development and Computing Portal.</span></span>

 

<span data-ttu-id="1c8c3-107">Um IME (editor de método de entrada) é um programa que permite uma entrada de texto fácil usando um teclado padrão para idiomas do leste asiático, como chinês, japonês, coreano e outras linguagens com caracteres complexos.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-107">An input method editor (IME) is a program that allows easy text entry using a standard keyboard for East Asian languages such as Chinese, Japanese, Korean, and other languages with complex characters.</span></span> <span data-ttu-id="1c8c3-108">Por exemplo, com IMEs, um usuário pode digitar caracteres complexos em um processador de texto ou um jogador de um jogo online com vários participantes pode bater papo com amigos em caracteres complexos.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-108">For example, with IMEs a user can type complex characters in a word processor, or a player of a massive multiplayer online game can chat with friends in complex characters.</span></span>

<span data-ttu-id="1c8c3-109">Este artigo explica como você pode implementar um controle de edição IME básico em um aplicativo Microsoft DirectX de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-109">This article explains how you can implement a basic IME edit control in a full-screen Microsoft DirectX application.</span></span> <span data-ttu-id="1c8c3-110">Os aplicativos que tiram proveito do DXUT automaticamente obtêm a funcionalidade do IME.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-110">Applications that take advantage of DXUT automatically get IME functionality.</span></span> <span data-ttu-id="1c8c3-111">Para aplicativos que não fazem uso da estrutura, este artigo descreve como adicionar suporte ao IME a um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-111">For applications that do not make use of the framework, this article describes how to add IME support to an edit control.</span></span>

<span data-ttu-id="1c8c3-112">Conteúdo:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-112">Contents:</span></span>

-   [<span data-ttu-id="1c8c3-113">Comportamento padrão do IME</span><span class="sxs-lookup"><span data-stu-id="1c8c3-113">Default IME Behavior</span></span>](#default-ime-behavior)
-   [<span data-ttu-id="1c8c3-114">Usando IMEs com DXUT</span><span class="sxs-lookup"><span data-stu-id="1c8c3-114">Using IMEs with DXUT</span></span>](#using-imes-with-dxut)
-   [<span data-ttu-id="1c8c3-115">Substituindo o comportamento padrão do IME</span><span class="sxs-lookup"><span data-stu-id="1c8c3-115">Overriding the Default IME Behavior</span></span>](#overriding-the-default-ime-behavior)
-   [<span data-ttu-id="1c8c3-116">Funções</span><span class="sxs-lookup"><span data-stu-id="1c8c3-116">Functions</span></span>](#functions)
-   [<span data-ttu-id="1c8c3-117">Mensagens</span><span class="sxs-lookup"><span data-stu-id="1c8c3-117">Messages</span></span>](#ime-messages)
-   [<span data-ttu-id="1c8c3-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1c8c3-118">Examples</span></span>](#examples)
    -   [<span data-ttu-id="1c8c3-119">IME do CHT versão 4,2, 4,3 e 4,4</span><span class="sxs-lookup"><span data-stu-id="1c8c3-119">CHT IME version 4.2, 4.3 and 4.4</span></span>](#cht-ime-version-42-43-and-44)
    -   [<span data-ttu-id="1c8c3-120">IME do CHT versão 5,0</span><span class="sxs-lookup"><span data-stu-id="1c8c3-120">CHT IME version 5.0</span></span>](#cht-ime-version-50)
    -   [<span data-ttu-id="1c8c3-121">Chinês do CHT versão 5,1, 5,2 e CHS IME versão 5,3</span><span class="sxs-lookup"><span data-stu-id="1c8c3-121">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [<span data-ttu-id="1c8c3-122">O IME CHS versão 4,1</span><span class="sxs-lookup"><span data-stu-id="1c8c3-122">CHS IME version 4.1</span></span>](#chs-ime-version-41)
    -   [<span data-ttu-id="1c8c3-123">O IME CHS versão 4,2</span><span class="sxs-lookup"><span data-stu-id="1c8c3-123">CHS IME version 4.2</span></span>](#chs-ime-version-42)
-   [<span data-ttu-id="1c8c3-124">Mensagens do IME</span><span class="sxs-lookup"><span data-stu-id="1c8c3-124">IME Messages</span></span>](#ime-messages)
    -   [<span data-ttu-id="1c8c3-125">INPUTLANGCHANGE do WM \_</span><span class="sxs-lookup"><span data-stu-id="1c8c3-125">WM\_INPUTLANGCHANGE</span></span>](#wm_inputlangchange)
    -   [<span data-ttu-id="1c8c3-126">\_STARTCOMPOSITION IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="1c8c3-126">WM\_IME\_STARTCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="1c8c3-127">\_composição do IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="1c8c3-127">WM\_IME\_COMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="1c8c3-128">\_composição de endime do WM \_</span><span class="sxs-lookup"><span data-stu-id="1c8c3-128">WM\_IME\_ENDCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="1c8c3-129">\_notificação do IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="1c8c3-129">WM\_IME\_NOTIFY</span></span>](/windows)
-   [<span data-ttu-id="1c8c3-130">Renderização</span><span class="sxs-lookup"><span data-stu-id="1c8c3-130">Rendering</span></span>](#rendering)
    -   [<span data-ttu-id="1c8c3-131">Indicador de localidade de entrada</span><span class="sxs-lookup"><span data-stu-id="1c8c3-131">Input Locale Indicator</span></span>](#input-locale-indicator)
    -   [<span data-ttu-id="1c8c3-132">Janela de composição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-132">Composition Window</span></span>](#composition-window)
    -   [<span data-ttu-id="1c8c3-133">Leitura e candidatos do Windows</span><span class="sxs-lookup"><span data-stu-id="1c8c3-133">Reading and Candidate Windows</span></span>](#reading-and-candidate-windows)
-   [<span data-ttu-id="1c8c3-134">Limitações</span><span class="sxs-lookup"><span data-stu-id="1c8c3-134">Limitations</span></span>](#limitations)
-   [<span data-ttu-id="1c8c3-135">Informações do registro</span><span class="sxs-lookup"><span data-stu-id="1c8c3-135">Registry Information</span></span>](#registry-information)
-   [<span data-ttu-id="1c8c3-136">Apêndice A: versões do CHT por sistema operacional</span><span class="sxs-lookup"><span data-stu-id="1c8c3-136">Appendix A: CHT Versions per Operating System</span></span>](#appendix-a-cht-versions-per-operating-system)
-   [<span data-ttu-id="1c8c3-137">Mais informações</span><span class="sxs-lookup"><span data-stu-id="1c8c3-137">Further Information</span></span>](#further-information)
-   [<span data-ttu-id="1c8c3-138">Getreadingstring</span><span class="sxs-lookup"><span data-stu-id="1c8c3-138">GetReadingString</span></span>](#getreadingstring)
-   [<span data-ttu-id="1c8c3-139">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="1c8c3-139">ShowReadingWindow</span></span>](#showreadingwindow)

## <a name="default-ime-behavior"></a><span data-ttu-id="1c8c3-140">Comportamento padrão do IME</span><span class="sxs-lookup"><span data-stu-id="1c8c3-140">Default IME Behavior</span></span>

<span data-ttu-id="1c8c3-141">Os IMEs mapeiam a entrada de teclado para componentes fonéticos ou outros elementos de linguagem específicos para um idioma selecionado.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-141">IMEs map keyboard input to phonetic components or other language elements specific to a selected language.</span></span> <span data-ttu-id="1c8c3-142">Em um cenário típico, o usuário digita chaves que representam a pronúncia de um caractere complexo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-142">In a typical scenario, the user types keys that represent pronunciation of a complex character.</span></span> <span data-ttu-id="1c8c3-143">Se o IME reconhecer a pronúncia como válida, ele apresentará ao usuário uma lista de candidatos a palavras ou frases das quais o usuário pode selecionar uma escolha final.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-143">If the IME recognizes the pronunciation as valid, it presents the user with a list of word or phrase candidates from which the user can select a final choice.</span></span> <span data-ttu-id="1c8c3-144">A palavra escolhida é enviada para o aplicativo por meio de uma série de mensagens do Microsoft Windows [**WM \_ Char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="1c8c3-144">The chosen word is then sent to the application through a series of Microsoft Windows [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span> <span data-ttu-id="1c8c3-145">Como o IME funciona em um nível abaixo do aplicativo interceptando a entrada do teclado, a presença de um IME é transparente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-145">Because the IME works at a level below the application by intercepting keyboard input, the presence of an IME is transparent to the application.</span></span> <span data-ttu-id="1c8c3-146">Quase todos os aplicativos do Windows podem aproveitar prontamente os IMEs sem estar atento à sua existência e sem a necessidade de codificação especial.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-146">Almost all Windows applications can readily take advantage of IMEs without being aware of their existence and without requiring special coding.</span></span>

<span data-ttu-id="1c8c3-147">Um IME típico exibe várias janelas para guiar o usuário por meio de entrada de caracteres, conforme mostrado nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-147">A typical IME displays several windows to guide the user through character entry, as shown in the following examples.</span></span>

![o IME exibe várias janelas](images/ime-elements.png)

| <span data-ttu-id="1c8c3-149">Tipo de janela</span><span class="sxs-lookup"><span data-stu-id="1c8c3-149">Window Type</span></span>                                       | <span data-ttu-id="1c8c3-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-150">Description</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="1c8c3-151">Saída do IME</span><span class="sxs-lookup"><span data-stu-id="1c8c3-151">IME Output</span></span>                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="1c8c3-152">a.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-152">A.</span></span> <span data-ttu-id="1c8c3-153">Janela de leitura</span><span class="sxs-lookup"><span data-stu-id="1c8c3-153">Reading Window</span></span>                                 | <span data-ttu-id="1c8c3-154">Contém pressionamentos de teclas do teclado; Normalmente, muda após cada pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-154">Contains keystrokes from the keyboard; typically changes after each keystroke.</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="1c8c3-155">Cadeia de caracteres de leitura</span><span class="sxs-lookup"><span data-stu-id="1c8c3-155">reading string</span></span>                               |
| <span data-ttu-id="1c8c3-156">B.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-156">B.</span></span> <span data-ttu-id="1c8c3-157">Janela de composição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-157">Composition Window</span></span>                             | <span data-ttu-id="1c8c3-158">Contém a coleção de caracteres que o usuário criou com o IME.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-158">Contains the collection of characters that the user has composed with the IME.</span></span> <span data-ttu-id="1c8c3-159">Esses caracteres são desenhados pelo IME na parte superior do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-159">These characters are drawn by the IME on top of the application.</span></span> <span data-ttu-id="1c8c3-160">Quando o usuário notifica o IME que a cadeia de caracteres de composição é satisfatória, o IME envia a cadeia de caracteres de composição para o aplicativo por meio de uma série de mensagens do WM \_ Char.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-160">When the user notifies the IME that the composition string is satisfactory, the IME then sends the composition string to the application via a series of WM\_CHAR messages.</span></span> | <span data-ttu-id="1c8c3-161">Cadeia de caracteres de composição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-161">composition string</span></span>                           |
| <span data-ttu-id="1c8c3-162">C.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-162">C.</span></span> <span data-ttu-id="1c8c3-163">Janela candidata</span><span class="sxs-lookup"><span data-stu-id="1c8c3-163">Candidate Window</span></span>                               | <span data-ttu-id="1c8c3-164">Quando o usuário insere uma pronúncia válida, o IME exibe uma lista de caracteres candidatos que correspondem à pronúncia determinada.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-164">When the user has entered a valid pronunciation, the IME displays a list of candidate characters that all match the given pronunciation.</span></span> <span data-ttu-id="1c8c3-165">O usuário seleciona o caractere pretendido nessa lista e o IME adiciona esse caractere à janela de composição exibida.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-165">The user then selects the intended character from this list, and the IME adds this character to the Composition Window display.</span></span>                                                    | <span data-ttu-id="1c8c3-166">o próximo caractere na cadeia de caracteres de composição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-166">the next character in the composition string</span></span> |
| <span data-ttu-id="1c8c3-167">D.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-167">D.</span></span> <span data-ttu-id="1c8c3-168">Indicador de [localidade de entrada](/windows/desktop/Intl/nls-terminology)</span><span class="sxs-lookup"><span data-stu-id="1c8c3-168">[Input Locale](/windows/desktop/Intl/nls-terminology) indicator</span></span> | <span data-ttu-id="1c8c3-169">Mostra o idioma que o usuário selecionou para entrada de teclado.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-169">Shows the language the user has selected for keyboard input.</span></span> <span data-ttu-id="1c8c3-170">Esse indicador é inserido na barra de tarefas do Windows.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-170">This indicator is embedded in the Windows taskbar.</span></span> <span data-ttu-id="1c8c3-171">O idioma de entrada pode ser selecionado abrindo o painel de controle opções regionais e de idiomas e clicando em detalhes na guia idiomas.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-171">The input language can be selected by opening the Regional and Language Options Control Panel and then clicking Details on the Languages tab.</span></span>                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a><span data-ttu-id="1c8c3-172">Usando IMEs com DXUT</span><span class="sxs-lookup"><span data-stu-id="1c8c3-172">Using IMEs with DXUT</span></span>

<span data-ttu-id="1c8c3-173">No DXUT, a classe CDXUTIMEEditBox implementa a funcionalidade do IME.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-173">In DXUT, the CDXUTIMEEditBox class implements IME functionality.</span></span> <span data-ttu-id="1c8c3-174">Essa classe é derivada da classe CDXUTEditBox, o controle de edição básico fornecido pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-174">This class is derived from the CDXUTEditBox class, the basic edit control provided by the framework.</span></span> <span data-ttu-id="1c8c3-175">CDXUTIMEEditBox estende esse controle de edição para dar suporte a IMEs, substituindo os métodos CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-175">CDXUTIMEEditBox extends that edit control to support IMEs by overriding the CDXUTIMEEditBox methods.</span></span> <span data-ttu-id="1c8c3-176">As classes são projetadas dessa forma para ajudar os desenvolvedores a aprender o que precisam tomar da estrutura para implementar o suporte do IME em seus próprios controles de edição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-176">The classes are designed this way to help developers learn what they need to take from the framework to implement IME support in their own edit controls.</span></span> <span data-ttu-id="1c8c3-177">O restante deste tópico explica como a estrutura, e CDXUTIMEEditBox em particular, substitui um controle de edição básico para implementar a funcionalidade do IME.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-177">The rest of this topic explains how the framework, and CDXUTIMEEditBox in particular, overrides a basic edit control to implement IME functionality.</span></span>

<span data-ttu-id="1c8c3-178">A maioria das variáveis específicas do IME em CDXUTIMEEditBox são declaradas como estáticas, porque muitos buffers e Estados do IME são específicos para o processo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-178">Most of the IME-specific variables in CDXUTIMEEditBox are declared as static, because many IME buffers and states are specific to the process.</span></span> <span data-ttu-id="1c8c3-179">Por exemplo, um processo tem apenas um buffer para a cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-179">For instance, a process has only one buffer for the composition string.</span></span> <span data-ttu-id="1c8c3-180">Mesmo que o processo tenha dez controles de edição, todos eles estarão compartilhando o mesmo buffer de cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-180">Even if the process has ten edit controls, they will all be sharing the same composition string buffer.</span></span> <span data-ttu-id="1c8c3-181">O buffer da cadeia de caracteres de composição para CDXUTIMEEditBox é, portanto, estático, impedindo o aplicativo de ocupar espaço de memória desnecessário.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-181">The composition string buffer for CDXUTIMEEditBox is therefore static, preventing the application from taking up unnecessary memory space.</span></span>

<span data-ttu-id="1c8c3-182">CDXUTIMEEditBox é implementado no seguinte código de DXUT:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-182">CDXUTIMEEditBox is implemented in the following DXUT code:</span></span>

<span data-ttu-id="1c8c3-183">(Raiz do SDK) \\ Exemplos do \\ C++ \\ Common \\ DXUTgui. cpp</span><span class="sxs-lookup"><span data-stu-id="1c8c3-183">(SDK root)\\Samples\\C++\\Common\\DXUTgui.cpp</span></span>

## <a name="overriding-the-default-ime-behavior"></a><span data-ttu-id="1c8c3-184">Substituindo o comportamento padrão do IME</span><span class="sxs-lookup"><span data-stu-id="1c8c3-184">Overriding the Default IME Behavior</span></span>

<span data-ttu-id="1c8c3-185">Normalmente, um IME usa procedimentos padrão do Windows para criar uma janela (consulte [usando o Windows](/windows/desktop/winmsg/using-windows)).</span><span class="sxs-lookup"><span data-stu-id="1c8c3-185">Normally an IME uses standard Windows procedures to create a window (see [Using Windows](/windows/desktop/winmsg/using-windows)).</span></span> <span data-ttu-id="1c8c3-186">Em circunstâncias normais, isso produz resultados satisfatórios.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-186">Under normal circumstances, this produces satisfactory results.</span></span> <span data-ttu-id="1c8c3-187">No entanto, quando o aplicativo apresenta o modo de tela inteira, como é comum para jogos, as janelas padrão não funcionam mais e podem não ser exibidas na parte superior do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-187">However, when the application presents in full-screen mode, as is common for games, standard windows no longer work and may not display on top of the application.</span></span> <span data-ttu-id="1c8c3-188">Para superar esse problema, o aplicativo deve desenhar o próprio Windows do IME em vez de depender do Windows para executar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-188">To overcome this issue, the application must draw the IME windows itself instead of relying on Windows to perform this task.</span></span>

<span data-ttu-id="1c8c3-189">Quando o comportamento de criação da janela do IME padrão não fornece o que um aplicativo requer, o aplicativo pode substituir a manipulação da janela do IME.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-189">When the default IME window creation behavior does not provide what an application requires, the application can override the IME window handling.</span></span> <span data-ttu-id="1c8c3-190">Um aplicativo pode conseguir isso processando mensagens relacionadas ao IME e chamando a API do IMM ( [Input Method Manager](/windows/desktop/Intl/input-method-manager) ).</span><span class="sxs-lookup"><span data-stu-id="1c8c3-190">An application can achieve this by processing IME-related messages and calling the [Input Method Manager](/windows/desktop/Intl/input-method-manager) (IMM) API.</span></span>

<span data-ttu-id="1c8c3-191">Quando um usuário interage com um IME para inserir caracteres complexos, o IMM envia mensagens ao aplicativo para notificá-lo de eventos importantes, como iniciar uma composição ou mostrar a janela candidata.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-191">When a user interacts with an IME to input complex characters, the IMM sends messages to the application to notify it of important events, such as starting a composition or showing the candidate window.</span></span> <span data-ttu-id="1c8c3-192">Um aplicativo normalmente ignora essas mensagens e as passa para o manipulador de mensagens padrão, o que faz com que o IME as manipule.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-192">An application typically ignores these messages and passes them to the default message handler, which causes the IME to handle them.</span></span> <span data-ttu-id="1c8c3-193">Quando o aplicativo, em vez do manipulador padrão, manipula as mensagens, ele controla exatamente o que acontece em cada um dos eventos do IME.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-193">When the application, instead of the default handler, handles the messages, it controls exactly what happens at each of the IME events.</span></span> <span data-ttu-id="1c8c3-194">Geralmente, o manipulador de mensagens recupera o conteúdo das várias janelas do IME chamando a API do IMM.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-194">Often the message handler retrieves the content of the various IME windows by calling the IMM API.</span></span> <span data-ttu-id="1c8c3-195">Depois que o aplicativo tiver essas informações, ele poderá desenhar corretamente o próprio Windows do IME quando precisar renderizar para a exibição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-195">Once the application has this information, it can properly draw the IME windows itself when it needs to render to the display.</span></span>

## <a name="functions"></a><span data-ttu-id="1c8c3-196">Funções</span><span class="sxs-lookup"><span data-stu-id="1c8c3-196">Functions</span></span>

<span data-ttu-id="1c8c3-197">Um IME precisa obter a cadeia de caracteres de leitura, ocultar a janela de leitura e obter a orientação da janela de leitura.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-197">An IME needs to get the reading string, hide the reading window, and get the orientation of reading window.</span></span> <span data-ttu-id="1c8c3-198">Esta tabela mostra as funcionalidades por versão do IME:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-198">This table shows the functionalities per IME version:</span></span>



|                    | <span data-ttu-id="1c8c3-199">Obtendo cadeia de caracteres de leitura</span><span class="sxs-lookup"><span data-stu-id="1c8c3-199">Getting reading string</span></span>                                                | <span data-ttu-id="1c8c3-200">Ocultando janela de leitura</span><span class="sxs-lookup"><span data-stu-id="1c8c3-200">Hiding reading window</span></span>                       | <span data-ttu-id="1c8c3-201">Orientação da janela de leitura</span><span class="sxs-lookup"><span data-stu-id="1c8c3-201">Orientation of reading window</span></span>                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1c8c3-202">Antes da versão 6,0</span><span class="sxs-lookup"><span data-stu-id="1c8c3-202">Before version 6.0</span></span> | <span data-ttu-id="1c8c3-203">a.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-203">A.</span></span> <span data-ttu-id="1c8c3-204">Lendo o acesso à janela dados privados do IME diretamente.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-204">Reading Window Access IME private data directly.</span></span> <span data-ttu-id="1c8c3-205">Consulte "4 estrutura"</span><span class="sxs-lookup"><span data-stu-id="1c8c3-205">See "4 Structure"</span></span> | <span data-ttu-id="1c8c3-206">Interceptar mensagens privadas do IME.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-206">Trap IME private messages.</span></span> <span data-ttu-id="1c8c3-207">Consulte "3 mensagens"</span><span class="sxs-lookup"><span data-stu-id="1c8c3-207">See "3 Messages"</span></span> | <span data-ttu-id="1c8c3-208">Examine as informações do registro.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-208">Examine registry information.</span></span> <span data-ttu-id="1c8c3-209">Consulte "5 informações do registro"</span><span class="sxs-lookup"><span data-stu-id="1c8c3-209">See "5 Registry Information"</span></span> |
| <span data-ttu-id="1c8c3-210">Após a versão 6,0</span><span class="sxs-lookup"><span data-stu-id="1c8c3-210">After version 6.0</span></span>  | [<span data-ttu-id="1c8c3-211">Getreadingstring</span><span class="sxs-lookup"><span data-stu-id="1c8c3-211">GetReadingString</span></span>](#getreadingstring)                                 | [<span data-ttu-id="1c8c3-212">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="1c8c3-212">ShowReadingWindow</span></span>](#showreadingwindow)     | [<span data-ttu-id="1c8c3-213">Getreadingstring</span><span class="sxs-lookup"><span data-stu-id="1c8c3-213">GetReadingString</span></span>](#getreadingstring)                      |



 

## <a name="messages"></a><span data-ttu-id="1c8c3-214">Mensagens</span><span class="sxs-lookup"><span data-stu-id="1c8c3-214">Messages</span></span>

<span data-ttu-id="1c8c3-215">As mensagens a seguir não precisam ser processadas para o IME mais recente que implementa [ShowReadingWindow](#showreadingwindow)().</span><span class="sxs-lookup"><span data-stu-id="1c8c3-215">The following messages don't have to be processed for newer IME that implements [ShowReadingWindow](#showreadingwindow)().</span></span>

<span data-ttu-id="1c8c3-216">As mensagens a seguir são interceptadas pelo manipulador de mensagens do aplicativo (ou seja, elas não são passadas para DefWindowProc) para impedir que a janela de leitura seja exibida.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-216">The following messages are trapped by application message handler (i.e. they are not passed to DefWindowProc) to prevent the reading window from showing up.</span></span>

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a><span data-ttu-id="1c8c3-217">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1c8c3-217">Examples</span></span>

<span data-ttu-id="1c8c3-218">Os exemplos a seguir ilustram como obter informações de cadeia de caracteres de leitura do IME mais antigo que não tem getreadingstring ().</span><span class="sxs-lookup"><span data-stu-id="1c8c3-218">The following examples illustrate how to get reading string information from older IME that doesn't have GetReadingString().</span></span> <span data-ttu-id="1c8c3-219">O código gera as seguintes saídas:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-219">The code generates the following outputs:</span></span>



|              |                                                                                       |
|--------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c8c3-220">DwLen DWORD</span><span class="sxs-lookup"><span data-stu-id="1c8c3-220">DWORD dwlen</span></span>  | <span data-ttu-id="1c8c3-221">Comprimento da cadeia de caracteres de leitura</span><span class="sxs-lookup"><span data-stu-id="1c8c3-221">Length of the reading string</span></span>                                                          |
| <span data-ttu-id="1c8c3-222">Dwerr DWORD</span><span class="sxs-lookup"><span data-stu-id="1c8c3-222">DWORD dwerr</span></span>  | <span data-ttu-id="1c8c3-223">Índice do caractere de erro</span><span class="sxs-lookup"><span data-stu-id="1c8c3-223">Index of error char</span></span>                                                                   |
| <span data-ttu-id="1c8c3-224">WSTR de LPWSTR</span><span class="sxs-lookup"><span data-stu-id="1c8c3-224">LPWSTR wstr</span></span>  | <span data-ttu-id="1c8c3-225">Ponteiro para a cadeia de caracteres de leitura</span><span class="sxs-lookup"><span data-stu-id="1c8c3-225">Pointer to the reading string</span></span>                                                         |
| <span data-ttu-id="1c8c3-226">BOOLIANo Unicode</span><span class="sxs-lookup"><span data-stu-id="1c8c3-226">BOOL unicode</span></span> | <span data-ttu-id="1c8c3-227">Se for true, a cadeia de caracteres de leitura estará no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-227">If true, the reading string is in Unicode format.</span></span> <span data-ttu-id="1c8c3-228">Caso contrário, ele estará em formato multibyte.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-228">Otherwise it's in multibyte format.</span></span> |



 

### <a name="cht-ime-version-42-43-and-44"></a><span data-ttu-id="1c8c3-229">IME do CHT versão 4,2, 4,3 e 4,4</span><span class="sxs-lookup"><span data-stu-id="1c8c3-229">CHT IME version 4.2, 4.3 and 4.4</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a><span data-ttu-id="1c8c3-230">IME do CHT versão 5,0</span><span class="sxs-lookup"><span data-stu-id="1c8c3-230">CHT IME version 5.0</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 3*4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4 + 4*2 );
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 + 1*4);
wstr = (WCHAR *)(p + 1*4 + (16*2+2*4) + 5*4);
unicode = FALSE;
```

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a><span data-ttu-id="1c8c3-231">Chinês do CHT versão 5,1, 5,2 e CHS IME versão 5,3</span><span class="sxs-lookup"><span data-stu-id="1c8c3-231">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4); 
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2 + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = TRUE;
```

### <a name="chs-ime-version-41"></a><span data-ttu-id="1c8c3-232">O IME CHS versão 4,1</span><span class="sxs-lookup"><span data-stu-id="1c8c3-232">CHS IME version 4.1</span></span>

``` syntax
// GetImeId(1) returns VS_FIXEDFILEINFO:: dwProductVersionLS of IME file
int offset = ( GetImeId( 1 ) >= 0x00000002 ) ? 8 : 7;
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + offset * 4);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 16*2*4);
dwerr = *(DWORD *)(p + 8*4 + 16*2*4);
dwerr = min(dwerr, dwlen);
wstr = (WCHAR *)(p + 6*4 + 16*2*1);
unicode = TRUE;
```

### <a name="chs-ime-version-42"></a><span data-ttu-id="1c8c3-233">O IME CHS versão 4,2</span><span class="sxs-lookup"><span data-stu-id="1c8c3-233">CHS IME version 4.2</span></span>

``` syntax
int nTcharSize = IsNT() ? sizeof(WCHAR) : sizeof(char);
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 1*4 + 1*4 + 6*4);
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = IsNT() ? TRUE : FALSE;
```

## <a name="ime-messages"></a><span data-ttu-id="1c8c3-234">Mensagens do IME</span><span class="sxs-lookup"><span data-stu-id="1c8c3-234">IME Messages</span></span>

<span data-ttu-id="1c8c3-235">Um aplicativo de tela inteira deve lidar corretamente com as seguintes mensagens relacionadas ao IME:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-235">A full-screen application must properly handle the following IME-related messages:</span></span>

### <a name="wm_inputlangchange"></a><span data-ttu-id="1c8c3-236">INPUTLANGCHANGE do WM \_</span><span class="sxs-lookup"><span data-stu-id="1c8c3-236">WM\_INPUTLANGCHANGE</span></span>

<span data-ttu-id="1c8c3-237">O IMM envia uma \_ mensagem de INPUTLANGCHANGE do WM para a janela ativa de um aplicativo após a localidade de entrada ter sido alterada pelo usuário com uma combinação de teclas (geralmente Alt + Shift) ou com o indicador de localidade de entrada na barra de tarefas ou no idioma.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-237">The IMM sends a WM\_INPUTLANGCHANGE message to the active window of an application after the input locale has been changed by the user with a key combination (usually ALT+SHIFT), or with the input locale indicator on the taskbar or language bar.</span></span> <span data-ttu-id="1c8c3-238">A barra de idiomas é um controle na tela com o qual o usuário pode configurar um serviço de texto.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-238">The language bar is an on-screen control with which the user can configure a text service.</span></span> <span data-ttu-id="1c8c3-239">(Consulte [como mostrar a barra de idiomas](/windows/desktop/TSF/how-to-set-up-tsf).) A captura de tela a seguir mostra uma lista de seleção de idioma que é exibida quando o usuário clica no indicador de localidade.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-239">(See [How to show the language bar](/windows/desktop/TSF/how-to-set-up-tsf).) The following screen shot shows a language selection list that is displayed when the user clicks on the locale indicator.</span></span>

![lista de seleção de idioma exibida quando o usuário clica no indicador de localidade](images/ime-langselection.png)

<span data-ttu-id="1c8c3-241">Quando o IMM envia uma mensagem de INPUTLANGCHANGE do WM \_ , o CDXUTIMEEditBox deve executar várias tarefas importantes:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-241">When the IMM sends a WM\_INPUTLANGCHANGE message, CDXUTIMEEditBox must perform several important tasks:</span></span>

1.  <span data-ttu-id="1c8c3-242">O método GetKeyboardLayout é chamado para retornar o identificador de localidade de entrada (ID) para o thread do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-242">The GetKeyboardLayout method is called to return the input locale identifier (ID) for the application thread.</span></span> <span data-ttu-id="1c8c3-243">A classe CDXUTIMEEditBox salva essa ID em sua variável de membro estática s \_ hklCurrent para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-243">The CDXUTIMEEditBox class saves this ID in its static member variable s\_hklCurrent for later use.</span></span> <span data-ttu-id="1c8c3-244">É importante que o aplicativo conheça a localidade de entrada atual, porque o IME para cada idioma tem seu próprio comportamento distinto.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-244">It is important for the application to know the current input locale, because the IME for each language has its own distinct behavior.</span></span> <span data-ttu-id="1c8c3-245">O desenvolvedor pode precisar fornecer código diferente para diferentes localidades de entrada.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-245">The developer may need to provide different code for different input locales.</span></span>
2.  <span data-ttu-id="1c8c3-246">CDXUTIMEEditBox Inicializa uma cadeia de caracteres para exibição no indicador de idioma da caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-246">CDXUTIMEEditBox initializes a string to display in the edit box language indicator.</span></span> <span data-ttu-id="1c8c3-247">Esse indicador pode exibir o idioma de entrada ativo quando o aplicativo está sendo executado no modo de tela inteira e nem a barra de tarefas nem a barra de idiomas é visível.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-247">This indicator can display the active input language when the application is running in full-screen mode and neither the taskbar nor language bar is visible.</span></span>
3.  <span data-ttu-id="1c8c3-248">O método ImmGetConversionStatus é chamado para indicar se a localidade de entrada está no modo de conversão nativo ou não nativo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-248">The ImmGetConversionStatus method is called to indicate whether the input locale is in native or non-native conversion mode.</span></span> <span data-ttu-id="1c8c3-249">O modo de conversão nativo permite que o usuário insira texto na linguagem escolhida.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-249">Native conversion mode lets the user enter text in the chosen language.</span></span> <span data-ttu-id="1c8c3-250">O modo de conversão não nativo faz com que o teclado atue como um teclado padrão em inglês.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-250">Non-native conversion mode makes the keyboard act as a standard English keyboard.</span></span> <span data-ttu-id="1c8c3-251">É importante dar ao usuário uma indicação visual sobre o tipo de modo de conversão em que o IME está, para que o usuário possa saber facilmente quais caracteres devem ser esperados ao atingir uma chave.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-251">It is important to give the user a visual cue as to what type of conversion mode the IME is in, so that the user can easily know what characters to expect when hitting a key.</span></span> <span data-ttu-id="1c8c3-252">CDXUTIMEEditBox fornece essa indicação visual com uma cor de indicador de idioma.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-252">CDXUTIMEEditBox provides this visual cue with a language indicator color.</span></span> <span data-ttu-id="1c8c3-253">Quando a localidade de entrada usa um IME com o modo de conversão nativo, a classe CDXUTIMEEditBox desenha o texto do indicador com a cor definida pelo \_ parâmetro m IndicatorImeColor.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-253">When the input locale uses an IME with native conversion mode, the CDXUTIMEEditBox class draws the indicator text with the color defined by the m\_IndicatorImeColor parameter.</span></span> <span data-ttu-id="1c8c3-254">Quando o IME está no modo de conversão não nativa ou nenhum IME é usado, a classe desenha o texto do indicador com a cor definida pelo \_ parâmetro m IndicatorEngColor.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-254">When the IME is in non-native conversion mode, or no IME is used at all, the class draws the indicator text with the color defined by the m\_IndicatorEngColor parameter.</span></span>
4.  <span data-ttu-id="1c8c3-255">CDXUTIMEEditBox verifica a localidade de entrada e define a variável de membro estático s \_ bInsertOnType como true para coreano e false para todas as outras linguagens.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-255">CDXUTIMEEditBox checks the input locale and sets the static member variable s\_bInsertOnType to TRUE for Korean and FALSE for all other languages.</span></span> <span data-ttu-id="1c8c3-256">Esse sinalizador é necessário devido aos diferentes comportamentos de IMEs do coreano e de todos os outros IMEs.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-256">This flag is required because of the different behaviors of Korean IMEs and all other IMEs.</span></span> <span data-ttu-id="1c8c3-257">Ao inserir caracteres em idiomas diferentes de coreano, o texto inserido pelo usuário é exibido na janela de composição e o usuário pode alterar livremente o conteúdo da cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-257">When entering characters in languages other than Korean, the user-entered text is displayed in the composition window, and the user can freely change the content of the composition string.</span></span> <span data-ttu-id="1c8c3-258">O usuário pressiona a tecla ENTER quando estiver satisfeito com a cadeia de caracteres de composição e a cadeia de caracteres de composição será enviada ao aplicativo como uma série de mensagens do WM \_ Char.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-258">The user presses the ENTER key when satisfied with the composition string, and the composition string is sent to the application as a series of WM\_CHAR messages.</span></span> <span data-ttu-id="1c8c3-259">No caso de IMEs do coreano, no entanto, quando um usuário pressiona uma tecla para inserir texto, um caractere é enviado imediatamente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-259">In Korean IMEs, however, when a user presses a key to enter text, a character is immediately sent to the application.</span></span> <span data-ttu-id="1c8c3-260">Quando o usuário pressiona subseqüentemente mais chaves para modificar esse caractere inicial, o caractere na caixa de edição é alterado para refletir a entrada adicional do usuário.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-260">When the user subsequently presses more keys to modify that initial character, the character in the edit box changes to reflect additional input from the user.</span></span> <span data-ttu-id="1c8c3-261">Essencialmente, o usuário está compondo caracteres na caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-261">Essentially, the user is composing characters in the edit box.</span></span> <span data-ttu-id="1c8c3-262">Esses dois comportamentos são diferentes o suficiente para que o CDXUTIMEEditBox precise codificar cada um especificamente.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-262">These two behaviors are different enough that CDXUTIMEEditBox must code for each of them specifically.</span></span>
5.  <span data-ttu-id="1c8c3-263">O método de membro estático SetupImeApi é chamado para recuperar endereços de duas funções do módulo IME: getreadingstring e ShowReadingWindow.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-263">The static member method SetupImeApi is called to retrieve addresses of two functions from the IME module: GetReadingString and ShowReadingWindow.</span></span> <span data-ttu-id="1c8c3-264">Se essas funções existirem, ShowReadingWindow será chamado para ocultar a janela de leitura padrão para este IME.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-264">If these functions exist, ShowReadingWindow is called to hide the default reading window for this IME.</span></span> <span data-ttu-id="1c8c3-265">Como o aplicativo renderiza a janela de leitura em si, ele notifica o IME para desabilitar o desenho da janela de leitura padrão para que ela não interfira na renderização de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-265">Because the application renders the reading window itself, it notifies the IME to disable drawing the default reading window so that it will not interfere with full-screen rendering.</span></span>

<span data-ttu-id="1c8c3-266">O IMM envia uma \_ \_ mensagem SetContext do WM IME quando uma janela do aplicativo é ativada.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-266">The IMM sends a WM\_IME\_SETCONTEXT message when a window of the application is activated.</span></span> <span data-ttu-id="1c8c3-267">O parâmetro lParam desta mensagem contém um sinalizador que indica para o IME quais janelas devem ser desenhadas e quais não devem.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-267">The lParam parameter of this message contains a flag that indicates to the IME which windows should get drawn and which should not.</span></span> <span data-ttu-id="1c8c3-268">Como o aplicativo está lidando com todo o desenho, ele não precisa do IME para desenhar nenhuma das janelas do IME.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-268">Because the application is handling all of the drawing, it does not need the IME to draw any of the IME windows.</span></span> <span data-ttu-id="1c8c3-269">Portanto, o manipulador de mensagens do aplicativo simplesmente define lParam como 0 e retorna.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-269">Therefore, the application's message handler simply sets lParam to 0 and returns.</span></span>

<span data-ttu-id="1c8c3-270">Para que os aplicativos ofereçam suporte ao IME, o processamento especial é necessário para a mensagem relacionada ao IME do WM \_ IME \_ SetContext.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-270">In order for applications to support IME, special processing is needed for the IME-related message WM\_IME\_SETCONTEXT.</span></span> <span data-ttu-id="1c8c3-271">Como o Windows normalmente envia essa mensagem para o aplicativo antes de chamar o método PanoramaInitialize (), o panorama não tem a oportunidade de processar a interface do usuário para mostrar as janelas de lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-271">Since Windows typically sends this message to the application prior to calling the PanoramaInitialize() method, Panorama doesn't have a chance to process the UI for showing candidate list windows.</span></span>

<span data-ttu-id="1c8c3-272">O trecho de código a seguir especifica a aplicativos do Windows para não exibir nenhuma interface do usuário associada à janela lista de candidatos, permitindo que o panorama manipule especificamente essa interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-272">The following code snippet specifies to Windows applications not to display any UI associated with the candidate list window, allowing Panorama to specifically handle this UI.</span></span>

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a><span data-ttu-id="1c8c3-273">\_STARTCOMPOSITION IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="1c8c3-273">WM\_IME\_STARTCOMPOSITION</span></span>

<span data-ttu-id="1c8c3-274">O IMM envia uma \_ \_ mensagem STARTCOMPOSITION do WM IME para o aplicativo quando uma composição do IME está prestes a começar como resultado de pressionamentos de teclas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-274">The IMM sends a WM\_IME\_STARTCOMPOSITION message to the application when an IME composition is about to begin as a result of keystrokes by the user.</span></span> <span data-ttu-id="1c8c3-275">Se o IME usar a janela de composição, ele exibirá a cadeia de caracteres de composição atual em uma janela de composição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-275">If the IME uses the composition window, it displays the current composition string in a composition window.</span></span> <span data-ttu-id="1c8c3-276">O CDXUTIMEEditBox lida com essa mensagem executando duas tarefas:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-276">CDXUTIMEEditBox handles this message by performing two tasks:</span></span>

1.  <span data-ttu-id="1c8c3-277">CDXUTIMEEditBox limpa o buffer da cadeia de caracteres de composição e o buffer do atributo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-277">CDXUTIMEEditBox clears the composition string buffer and attribute buffer.</span></span> <span data-ttu-id="1c8c3-278">Esses buffers são membros estáticos de CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-278">These buffers are static members of CDXUTIMEEditBox.</span></span>
2.  <span data-ttu-id="1c8c3-279">CDXUTIMEEditBox define a \_ variável de membro estático s bHideCaret como true.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-279">CDXUTIMEEditBox sets the s\_bHideCaret static member variable to TRUE.</span></span> <span data-ttu-id="1c8c3-280">Esse membro, definido na classe CDXUTEditBox base, controla se o cursor na caixa de edição deve ser desenhado quando a caixa de edição é renderizada.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-280">This member, defined in the base CDXUTEditBox class, controls whether the cursor in the edit box should be drawn when the edit box is rendered.</span></span> <span data-ttu-id="1c8c3-281">A janela composição funciona de forma semelhante a uma caixa de edição com texto e cursor.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-281">The composition window functions similarly to an edit box with text and cursor.</span></span> <span data-ttu-id="1c8c3-282">Para evitar confusão quando a janela de composição estiver visível, a caixa de edição ocultará o cursor para que apenas um cursor fique visível por vez.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-282">To avoid confusion when the composition window is visible, the edit box hides its cursor so that only one cursor is visible at a time.</span></span>

### <a name="wm_ime_composition"></a><span data-ttu-id="1c8c3-283">\_composição do IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="1c8c3-283">WM\_IME\_COMPOSITION</span></span>

<span data-ttu-id="1c8c3-284">O IMM envia uma \_ mensagem de \_ composição IME do WM para o aplicativo quando o usuário insere um pressionamento de tecla para alterar a cadeia de caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-284">The IMM sends a WM\_IME\_COMPOSITION message to the application when the user enters a keystroke to change the composition string.</span></span> <span data-ttu-id="1c8c3-285">O valor de lParam indica que tipo de informações o aplicativo pode recuperar do IMM (Input Method Manager).</span><span class="sxs-lookup"><span data-stu-id="1c8c3-285">The value of lParam indicates what type of information the application can retrieve from the Input Method Manager (IMM).</span></span> <span data-ttu-id="1c8c3-286">O aplicativo deve recuperar as informações disponíveis chamando [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) e, em seguida, deve salvar as informações em seu buffer privado para que possa renderizar os elementos do IME posteriormente.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-286">The application should retrieve the available information by calling [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) and then should save the information in its private buffer so that it can render the IME elements later.</span></span>

<span data-ttu-id="1c8c3-287">O CDXUTIMEEditBox verifica e recupera os seguintes dados de cadeia de caracteres de composição:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-287">CDXUTIMEEditBox checks for and retrieves the following composition string data:</span></span>



| <span data-ttu-id="1c8c3-288">[**WM \_ Valor \_**](/windows/desktop/Intl/wm-ime-composition) do sinalizador lParam de composição do IME</span><span class="sxs-lookup"><span data-stu-id="1c8c3-288">[**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam Flag Value</span></span> | <span data-ttu-id="1c8c3-289">Dados</span><span class="sxs-lookup"><span data-stu-id="1c8c3-289">Data</span></span>                           | <span data-ttu-id="1c8c3-290">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-290">Description</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c8c3-291">GCS \_ COMPATTR</span><span class="sxs-lookup"><span data-stu-id="1c8c3-291">GCS\_COMPATTR</span></span>                                                         | <span data-ttu-id="1c8c3-292">Atributo de composição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-292">Composition Attribute</span></span>          | <span data-ttu-id="1c8c3-293">Esse atributo contém informações como o status de cada caractere na cadeia de caracteres de composição (por exemplo, convertido ou não convertido).</span><span class="sxs-lookup"><span data-stu-id="1c8c3-293">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="1c8c3-294">Essas informações são necessárias porque o CDXUTIMEEditBox colore a cadeia de caracteres de composição de forma diferente com base em seus atributos.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-294">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span>                                                                                   |
| <span data-ttu-id="1c8c3-295">GCS \_ COMPCLAUSE</span><span class="sxs-lookup"><span data-stu-id="1c8c3-295">GCS\_COMPCLAUSE</span></span>                                                       | <span data-ttu-id="1c8c3-296">Informações da cláusula de composição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-296">Composition Clause Information</span></span> | <span data-ttu-id="1c8c3-297">Essas informações de cláusula são usadas quando o IME do japonês está ativo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-297">This clause information is used when the Japanese IME is active.</span></span> <span data-ttu-id="1c8c3-298">Quando uma cadeia de caracteres de composição em Japonês é convertida, os caracteres podem ser agrupados como uma cláusula que é convertida em uma única entidade.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-298">When a Japanese composition string is converted, characters may be grouped together as a clause that gets converted to a single entity.</span></span> <span data-ttu-id="1c8c3-299">Quando o usuário move o cursor, CDXUTIMEEditBox usa essas informações para realçar a cláusula inteira, em vez de apenas um único caractere dentro da cláusula.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-299">When the user moves the cursor, CDXUTIMEEditBox uses this information to highlight the entire clause, instead of just a single character within the clause.</span></span> |
| <span data-ttu-id="1c8c3-300">GCS \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="1c8c3-300">GCS\_COMPSTR</span></span>                                                          | <span data-ttu-id="1c8c3-301">Cadeia de caracteres de composição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-301">Composition String</span></span>             | <span data-ttu-id="1c8c3-302">Essa cadeia de caracteres é a cadeia de caracteres atualizada que está sendo composta pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-302">This string is the up-to-date string being composed by the user.</span></span> <span data-ttu-id="1c8c3-303">Essa também é a cadeia de caracteres exibida na janela de composição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-303">This is also the string displayed in the composition window.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="1c8c3-304">GCS \_ CURSORPOS</span><span class="sxs-lookup"><span data-stu-id="1c8c3-304">GCS\_CURSORPOS</span></span>                                                        | <span data-ttu-id="1c8c3-305">Posição do cursor de composição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-305">Composition Cursor Position</span></span>    | <span data-ttu-id="1c8c3-306">A janela composição implementa um cursor, semelhante ao cursor em uma caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-306">The composition window implements a cursor, similar to the cursor in an edit box.</span></span> <span data-ttu-id="1c8c3-307">O aplicativo pode recuperar a posição do cursor ao processar a \_ mensagem de composição do IME do WM \_ para desenhar o cursor corretamente.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-307">The application can retrieve the cursor position when processing the WM\_IME\_COMPOSITION message in order to draw the cursor properly.</span></span>                                                                                                                                            |
| <span data-ttu-id="1c8c3-308">GCS \_ RESULTSTR</span><span class="sxs-lookup"><span data-stu-id="1c8c3-308">GCS\_RESULTSTR</span></span>                                                        | <span data-ttu-id="1c8c3-309">Cadeia de caracteres de resultado</span><span class="sxs-lookup"><span data-stu-id="1c8c3-309">Result String</span></span>                  | <span data-ttu-id="1c8c3-310">A cadeia de caracteres de resultado está disponível quando o usuário está prestes a concluir o processo de composição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-310">The result string is available when the user is about to complete the composition process.</span></span> <span data-ttu-id="1c8c3-311">Essa cadeia de caracteres deve ser recuperada e os caracteres devem ser enviados para a caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-311">This string should be retrieved and the characters should be sent to the edit box.</span></span>                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a><span data-ttu-id="1c8c3-312">\_composição de endime do WM \_</span><span class="sxs-lookup"><span data-stu-id="1c8c3-312">WM\_IME\_ENDCOMPOSITION</span></span>

<span data-ttu-id="1c8c3-313">O IMM envia uma \_ mensagem de ENDcomposição do WM IME \_ para o aplicativo quando a operação de composição do IME está terminando.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-313">The IMM sends a WM\_IME\_ENDCOMPOSITION message to the application when the IME composition operation is ending.</span></span> <span data-ttu-id="1c8c3-314">Isso pode ocorrer quando o usuário pressiona a tecla ENTER para aprovar a cadeia de caracteres de composição ou a tecla ESC para cancelar a composição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-314">This can occur when the user presses the ENTER key to approve the composition string, or the ESC key to cancel the composition.</span></span> <span data-ttu-id="1c8c3-315">CDXUTIMEEditBox manipula essa mensagem definindo o buffer da cadeia de caracteres de composição como vazio.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-315">CDXUTIMEEditBox handles this message by setting the composition string buffer to be empty.</span></span> <span data-ttu-id="1c8c3-316">Em seguida, ele define s \_ bHideCaret como false porque a janela de composição é fechada e o cursor na caixa de edição deve estar visível novamente.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-316">It then sets s\_bHideCaret to FALSE because the composition window is closed and the cursor in the edit box should again be visible.</span></span>

<span data-ttu-id="1c8c3-317">O manipulador de mensagens CDXUTIMEEditBox também define s \_ bShowReadingWindow como false.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-317">The CDXUTIMEEditBox message handler also sets s\_bShowReadingWindow to FALSE.</span></span> <span data-ttu-id="1c8c3-318">Esse sinalizador controla se a classe desenha a janela de leitura quando a caixa de edição é processada, portanto, ela deve ser definida como FALSE quando uma composição termina.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-318">This flag controls whether the class draws the reading window when the edit box renders itself, so it must be set to FALSE when a composition ends.</span></span>

### <a name="wm_ime_notify"></a><span data-ttu-id="1c8c3-319">\_notificação do IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="1c8c3-319">WM\_IME\_NOTIFY</span></span>

<span data-ttu-id="1c8c3-320">O IMM envia uma \_ mensagem de \_ notificação do WM IME para o aplicativo sempre que uma janela do IME é alterada.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-320">The IMM sends a WM\_IME\_NOTIFY message to the application whenever an IME window changes.</span></span> <span data-ttu-id="1c8c3-321">Um aplicativo que manipula o desenho das janelas do IME deve processar essa mensagem para que esteja ciente de qualquer atualização para o conteúdo da janela.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-321">An application that handles the drawing of the IME windows should process this message so that it is aware of any update to the content of the window.</span></span> <span data-ttu-id="1c8c3-322">WParam indica o comando ou a alteração que está ocorrendo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-322">The wParam indicates the command or the change that is taking place.</span></span> <span data-ttu-id="1c8c3-323">CDXUTIMEEditBox manipula os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-323">CDXUTIMEEditBox handles the following commands:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c8c3-324">Comando do IME</span><span class="sxs-lookup"><span data-stu-id="1c8c3-324">IME Command</span></span></th>
<th><span data-ttu-id="1c8c3-325">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-325">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c8c3-326"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="1c8c3-326"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span></span></td>
<td><span data-ttu-id="1c8c3-327">Esse atributo contém informações como o status de cada caractere na cadeia de caracteres de composição (por exemplo, convertido ou não convertido).</span><span class="sxs-lookup"><span data-stu-id="1c8c3-327">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="1c8c3-328">Essas informações são necessárias porque o CDXUTIMEEditBox colore a cadeia de caracteres de composição de forma diferente com base em seus atributos.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-328">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c8c3-329"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="1c8c3-329"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a> / <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span></span></td>
<td><span data-ttu-id="1c8c3-330">Enviado ao aplicativo quando a janela candidata estiver prestes a ser aberta ou atualizada, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-330">Sent to the application when the candidate window is about to be opened or updated, respectively.</span></span> <span data-ttu-id="1c8c3-331">A janela candidato é aberta quando um usuário deseja alterar a opção de texto convertido.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-331">The candidate window opens when a user wishes to change the converted text choice.</span></span> <span data-ttu-id="1c8c3-332">A janela é atualizada quando um usuário move o indicador de seleção ou altera a página.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-332">The window is updated when a user moves the selection indicator or changes the page.</span></span> <span data-ttu-id="1c8c3-333">O CDXUTIMEEditBox usa um manipulador de mensagens para ambos os comandos porque as tarefas necessárias são exatamente as mesmas:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-333">CDXUTIMEEditBox uses one message handler for both of these commands because the tasks required are exactly the same:</span></span><br/>
<ol>
<li><span data-ttu-id="1c8c3-334">CDXUTIMEEditBox define o membro bShowWindow da estrutura da lista de candidatos s_CandList como TRUE para indicar que a janela candidata precisa ser desenhada durante a renderização do quadro.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-334">CDXUTIMEEditBox sets the bShowWindow member of the candidate list structure s_CandList to TRUE to indicate that the candidate window needs to be drawn during frame rendering.</span></span></li>
<li><span data-ttu-id="1c8c3-335">CDXUTIMEEditBox recupera a lista de candidatos chamando <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, primeiro para obter o tamanho de buffer necessário e, em seguida, para obter os dados reais.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-335">CDXUTIMEEditBox retrieves the candidate list by calling <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, first to get the required buffer size, and then again to get the actual data.</span></span></li>
<li><span data-ttu-id="1c8c3-336">A estrutura de lista de candidatos particular s_CandList é inicializada com os dados candidatos recuperados.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-336">The private candidate list structure s_CandList is initialized with the retrieved candidate data.</span></span></li>
<li><span data-ttu-id="1c8c3-337">As cadeias de caracteres candidatas são armazenadas como uma matriz de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-337">The candidate strings are stored as an array of strings.</span></span></li>
<li><span data-ttu-id="1c8c3-338">O índice da entrada selecionada, bem como o índice de página, é salvo.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-338">The index of the selected entry, as well as the page index, is saved.</span></span></li>
<li><span data-ttu-id="1c8c3-339">CDXUTIMEEditBox verifica se o estilo da janela candidata é vertical ou horizontal.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-339">CDXUTIMEEditBox checks whether the candidate window style is vertical or horizontal.</span></span> <span data-ttu-id="1c8c3-340">Se o estilo da janela for horizontal, um buffer de cadeia de caracteres adicional, o membro HoriCand de s_CandList, deverá ser inicializado com todas as cadeias de caracteres candidatas, com espaços de espaço inseridos entre todas as seqüências adjacentes.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-340">If the window style is horizontal, an additional string buffer, the HoriCand member of s_CandList, must be initialized with all of the candidate strings, with space characters inserted between all adjacent strings.</span></span> <span data-ttu-id="1c8c3-341">Ao renderizar uma janela de candidato vertical, as cadeias de caracteres candidatas individuais são desenhadas uma de cada vez, com as coordenadas y incrementadas para cada cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-341">When rendering a vertical candidate window, the individual candidate strings are drawn one at a time, with the y coordinates incremented for each string.</span></span> <span data-ttu-id="1c8c3-342">No entanto, essa cadeia de caracteres HoriCand deve ser usada ao renderizar uma janela de candidato horizontal, porque o caractere de espaço é a melhor maneira de separar duas cadeias de caracteres adjacentes na mesma linha.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-342">However, this HoriCand string should be used when rendering a horizontal candidate window, because the space character is the best way to separate two adjacent strings on the same line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c8c3-343"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="1c8c3-343"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span></span></td>
<td><span data-ttu-id="1c8c3-344">Enviado ao aplicativo quando uma janela candidata está prestes a ser fechada.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-344">Sent to the application when a candidate window is about to close.</span></span> <span data-ttu-id="1c8c3-345">Isso acontece quando um usuário fez uma seleção na lista de candidatos.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-345">This happens when a user has made a selection from the candidate list.</span></span> <span data-ttu-id="1c8c3-346">CDXUTIMEEditBox manipula esse comando definindo o sinalizador visível da janela candidata como FALSE e, em seguida, limpando o buffer da cadeia de caracteres candidata.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-346">CDXUTIMEEditBox handles this command by setting the visible flag of the candidate window to FALSE and then clearing the candidate string buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c8c3-347">IMN_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="1c8c3-347">IMN_PRIVATE</span></span></td>
<td><span data-ttu-id="1c8c3-348">Enviado ao aplicativo quando o IME atualizou sua cadeia de caracteres de leitura como resultado do usuário digitando ou removendo caracteres.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-348">Sent to the application when the IME has updated its reading string as a result of the user typing or removing characters.</span></span> <span data-ttu-id="1c8c3-349">O aplicativo deve recuperar a cadeia de caracteres de leitura e salvá-la para renderização.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-349">The application should retrieve the reading string and save it for rendering.</span></span> <span data-ttu-id="1c8c3-350">CDXUTIMEEditBox tem dois métodos para recuperar a cadeia de caracteres de leitura, com base em como há suporte para as cadeias de leitura no IME:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-350">CDXUTIMEEditBox has two methods to retrieve the reading string, based upon how reading strings are supported in the IME:</span></span> <br/>
<ul>
<li><span data-ttu-id="1c8c3-351">Se o IME der suporte para a função getreadingstring, getreadingstring será chamado para recuperar a cadeia de caracteres de leitura.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-351">If the IME supports the GetReadingString function, GetReadingString is called to retrieve the reading string.</span></span></li>
<li><span data-ttu-id="1c8c3-352">Se o IME não implementar getreadingstring, CDXUTIMEEditBox recuperará a cadeia de caracteres de leitura do conteúdo do contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-352">If the IME does not implement GetReadingString, CDXUTIMEEditBox retrieves the reading string from the input context content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a><span data-ttu-id="1c8c3-353">Renderização</span><span class="sxs-lookup"><span data-stu-id="1c8c3-353">Rendering</span></span>

<span data-ttu-id="1c8c3-354">A renderização dos elementos do IME e do Windows é simples.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-354">Rendering of the IME elements and windows is straightforward.</span></span> <span data-ttu-id="1c8c3-355">CDXUTIMEEditBox permite que a classe base renderize primeiro porque as janelas do IME devem aparecer na parte superior do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-355">CDXUTIMEEditBox lets the base class render first because IME windows should appear on top of the edit control.</span></span> <span data-ttu-id="1c8c3-356">Depois que a caixa de edição base é renderizada, o CDXUTIMEEditBox verifica o sinalizador de visibilidade de cada janela do IME (indicador, composição, candidato e janela de leitura) e desenha a janela se ela deve estar visível.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-356">After the base edit box is rendered, CDXUTIMEEditBox checks the visibility flag of each IME window (indicator, composition, candidate, and reading window) and draws the window if it should be visible.</span></span> <span data-ttu-id="1c8c3-357">Consulte comportamento padrão do IME para obter descrições dos diferentes tipos de janela do IME.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-357">See Default IME Behavior for descriptions of the different IME window types.</span></span>

### <a name="input-locale-indicator"></a><span data-ttu-id="1c8c3-358">Indicador de localidade de entrada</span><span class="sxs-lookup"><span data-stu-id="1c8c3-358">Input Locale Indicator</span></span>

<span data-ttu-id="1c8c3-359">O indicador de localidade de entrada é processado antes de qualquer outra janela do IME, pois é um elemento que é sempre exibido.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-359">The input locale indicator is rendered before any other IME windows because it is an element that is always displayed.</span></span> <span data-ttu-id="1c8c3-360">Portanto, ele deve aparecer abaixo de outras janelas do IME.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-360">It should therefore appear below other IME windows.</span></span> <span data-ttu-id="1c8c3-361">CDXUTIMEEditBox renderiza o indicador chamando o método RenderIndicator, no qual a cor da fonte do indicador é determinada examinando a \_ variável estática de is outimóvel, que reflete o modo de conversão do IME atual.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-361">CDXUTIMEEditBox renders the indicator by calling the RenderIndicator method, in which the indicator font color is determined by examining the s\_ImeState static variable, which reflects the current IME conversion mode.</span></span> <span data-ttu-id="1c8c3-362">Quando o IME está habilitado e a conversão nativa está ativa, o método usa m \_ IndicatorImeColor como a cor do indicador.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-362">When the IME is enabled and native conversion is active, the method uses m\_IndicatorImeColor as the indicator color.</span></span> <span data-ttu-id="1c8c3-363">Se o IME estiver desabilitado ou estiver no modo de conversão não nativa, m \_ IndicatorImeColor será usado para desenhar o texto do indicador.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-363">If the IME is disabled or is in non-native conversion mode, m\_IndicatorImeColor is used to draw the indicator text.</span></span> <span data-ttu-id="1c8c3-364">Por padrão, a própria janela do indicador é desenhada à direita da caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-364">By default, the indicator window itself is drawn to the right of the edit box.</span></span> <span data-ttu-id="1c8c3-365">Os aplicativos podem alterar esse comportamento substituindo o método RenderIndicator.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-365">Applications can change this behavior by overriding the RenderIndicator method.</span></span>

<span data-ttu-id="1c8c3-366">A figura a seguir mostra as diferentes aparências de um indicador de localidade de entrada para inglês, japonês no modo de conversão alfanumérica e japonês no modo de conversão nativa:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-366">The following figure shows the different appearances of an input locale indicator for English, Japanese in alphanumeric conversion mode, and Japanese in native conversion mode:</span></span>

![aparências diferentes de um indicador de localidade de entrada para inglês e japonês](images/ime-indicator.png)

### <a name="composition-window"></a><span data-ttu-id="1c8c3-368">Janela de composição</span><span class="sxs-lookup"><span data-stu-id="1c8c3-368">Composition Window</span></span>

<span data-ttu-id="1c8c3-369">O desenho da janela de composição é tratado no método RenderComposition de CDXUTIMEEditBox.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-369">The drawing of the composition window is handled in the RenderComposition method of CDXUTIMEEditBox.</span></span> <span data-ttu-id="1c8c3-370">A janela de composição flutua acima da caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-370">The composition window floats above the edit box.</span></span> <span data-ttu-id="1c8c3-371">Ele deve ser desenhado na posição do cursor do controle de edição subjacente.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-371">It should be drawn at the cursor position of the underlying edit control.</span></span> <span data-ttu-id="1c8c3-372">O CDXUTIMEEditBox lida com a renderização da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-372">CDXUTIMEEditBox handles the rendering as follows:</span></span>

1.  <span data-ttu-id="1c8c3-373">A cadeia de caracteres de composição inteira é desenhada usando as cores de cadeia de caracteres de composição padrão</span><span class="sxs-lookup"><span data-stu-id="1c8c3-373">The entire composition string is drawn using the default composition string colors.</span></span>
2.  <span data-ttu-id="1c8c3-374">Caracteres com determinados atributos especiais devem ser desenhados em cores diferentes, portanto, o CDXUTIMEEditBox revisa os caracteres da cadeia de caracteres de composição e inspeciona o atributo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-374">Characters with certain special attributes should be drawn in different colors, so CDXUTIMEEditBox reviews the characters of the composition string and inspects the string attribute.</span></span> <span data-ttu-id="1c8c3-375">Se o atributo chamar cores diferentes, o caractere será desenhado novamente com as cores apropriadas.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-375">If the attribute calls for different colors, the character is drawn again with the appropriate colors.</span></span>
3.  <span data-ttu-id="1c8c3-376">O cursor da janela de composição é desenhado para concluir a renderização.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-376">The cursor of the composition window is drawn to complete the rendering.</span></span>

<span data-ttu-id="1c8c3-377">O cursor deve piscar para IMEs do coreano, mas não deve ser para outros IMEs.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-377">The cursor should blink for Korean IMEs, but it should not for other IMEs.</span></span> <span data-ttu-id="1c8c3-378">RenderComposition determina se o cursor deve ser visível com base nos valores do temporizador quando o IME coreano é usado.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-378">RenderComposition determines whether the cursor should be visible based upon timer values when the Korean IME is used.</span></span>

### <a name="reading-and-candidate-windows"></a><span data-ttu-id="1c8c3-379">Leitura e candidatos do Windows</span><span class="sxs-lookup"><span data-stu-id="1c8c3-379">Reading and Candidate Windows</span></span>

<span data-ttu-id="1c8c3-380">As janelas de leitura e candidatas são renderizadas pelo mesmo método CDXUTIMEEditBox, RenderCandidateReadingWindow.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-380">The reading and candidate windows are rendered by the same CDXUTIMEEditBox method, RenderCandidateReadingWindow.</span></span> <span data-ttu-id="1c8c3-381">Ambas as janelas contêm uma matriz de cadeias de caracteres para layout vertical ou uma única cadeia de caracteres no caso do layout horizontal.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-381">Both windows contain an array of strings for vertical layout, or a single string in the case of horizontal layout.</span></span> <span data-ttu-id="1c8c3-382">A massa do código em RenderCandidateReadingWindow é usada para posicionar a janela de modo que nenhuma parte da janela fique fora da janela do aplicativo e seja recortada.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-382">The bulk of the code in RenderCandidateReadingWindow is used to position the window so that no part of the window falls outside the application window and gets clipped.</span></span>

## <a name="limitations"></a><span data-ttu-id="1c8c3-383">Limitações</span><span class="sxs-lookup"><span data-stu-id="1c8c3-383">Limitations</span></span>

<span data-ttu-id="1c8c3-384">Os IMEs às vezes contêm recursos avançados para melhorar a facilidade de inserir texto.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-384">IMEs sometimes contain advanced features to improve the ease of inputting text.</span></span> <span data-ttu-id="1c8c3-385">Alguns dos recursos encontrados em IMEs mais recentes são mostrados nas figuras a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-385">Some of the features found in newer IMEs are shown in the following figures.</span></span> <span data-ttu-id="1c8c3-386">Esses recursos avançados não estão presentes no DXUT.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-386">These advanced features are not present in DXUT.</span></span> <span data-ttu-id="1c8c3-387">A implementação de suporte para esses recursos avançados pode ser desafiadora porque não há nenhuma interface definida para obter as informações necessárias dos IMEs.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-387">Implementing support for these advanced features can be challenging because there is no interface defined to obtain the necessary information from the IMEs.</span></span>

<span data-ttu-id="1c8c3-388">IME chinês tradicional avançado com lista de candidatos expandida:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-388">Advanced Traditional Chinese IME with expanded candidate list:</span></span>

![IME chinês tradicional avançado com lista de candidatos expandida](images/ime-advanced1.png)

<span data-ttu-id="1c8c3-390">IME japonês avançado com algumas entradas candidatas que contêm texto adicional para descrever seus significados:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-390">Advanced Japanese IME with some candidate entries that contain additional text to describe their meanings:</span></span>

![IME japonês avançado com algumas entradas candidatas que contêm texto adicional para descrever seus significados](images/ime-advanced2.png)

<span data-ttu-id="1c8c3-392">IME coreano avançado que inclui um sistema de reconhecimento de manuscrito:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-392">Advanced Korean IME that includes a handwriting recognition system:</span></span>

![IME coreano avançado que inclui um sistema de reconhecimento de manuscrito](images/ime-advanced3.png)

## <a name="registry-information"></a><span data-ttu-id="1c8c3-394">Informações do registro</span><span class="sxs-lookup"><span data-stu-id="1c8c3-394">Registry Information</span></span>

<span data-ttu-id="1c8c3-395">As informações de registro a seguir são verificadas para determinar a orientação da janela de leitura, quando o IME atual é uma nova fonética do CHT mais antiga que não implementa getreadingstring ().</span><span class="sxs-lookup"><span data-stu-id="1c8c3-395">The following registry information is checked to determine the orientation of the reading window, when the current IME is older CHT New Phonetic that doesn't implement GetReadingString().</span></span>



| <span data-ttu-id="1c8c3-396">Chave</span><span class="sxs-lookup"><span data-stu-id="1c8c3-396">Key</span></span>                                                           | <span data-ttu-id="1c8c3-397">Valor</span><span class="sxs-lookup"><span data-stu-id="1c8c3-397">Value</span></span>            |
|---------------------------------------------------------------|------------------|
| <span data-ttu-id="1c8c3-398">\\ \\ Nome do IME do Microsoft \\ Windows \\ CurrentVersion \\ \_ software</span><span class="sxs-lookup"><span data-stu-id="1c8c3-398">HKCU\\software\\microsoft\\windows\\currentversion\\IME\_Name</span></span> | <span data-ttu-id="1c8c3-399">mapeamento de teclado</span><span class="sxs-lookup"><span data-stu-id="1c8c3-399">keyboard mapping</span></span> |



 

<span data-ttu-id="1c8c3-400">Em que: \_ o nome do IME será MSTCIPH se a versão do arquivo IME for 5,1 ou posterior; caso contrário, o nome do IME \_ será TINTLGNT.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-400">Where: IME\_Name is MSTCIPH if the IME file version is 5.1 or later; otherwise IME\_Name is TINTLGNT.</span></span>

<span data-ttu-id="1c8c3-401">A orientação da janela de leitura será horizontal se:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-401">The orientation of reading window is horizontal if either:</span></span>

-   <span data-ttu-id="1c8c3-402">O IME é a versão 5,0 e o valor de mapeamento de teclado é 0x22 ou 0x23</span><span class="sxs-lookup"><span data-stu-id="1c8c3-402">The IME is version 5.0 and keyboard mapping value is 0x22 or 0x23</span></span>
-   <span data-ttu-id="1c8c3-403">O IME é a versão 5,1 ou a versão 5,2 e o valor de mapeamento de teclado é 0x22, 0x23 ou 0x24.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-403">The IME is version 5.1 or version 5.2 and keyboard mapping value is 0x22, 0x23 or 0x24.</span></span>

<span data-ttu-id="1c8c3-404">Se nenhuma das condições for atendida, a janela de leitura será vertical.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-404">If neither condition is met, the reading window is vertical.</span></span>

## <a name="appendix-a-cht-versions-per-operating-system"></a><span data-ttu-id="1c8c3-405">Apêndice A: versões do CHT por sistema operacional</span><span class="sxs-lookup"><span data-stu-id="1c8c3-405">Appendix A: CHT Versions per Operating System</span></span>



| <span data-ttu-id="1c8c3-406">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="1c8c3-406">Operating System</span></span>           | <span data-ttu-id="1c8c3-407">Versão do IME do CHT</span><span class="sxs-lookup"><span data-stu-id="1c8c3-407">CHT IME Version</span></span> |
|----------------------------|-----------------|
| <span data-ttu-id="1c8c3-408">Windows 98</span><span class="sxs-lookup"><span data-stu-id="1c8c3-408">Windows 98</span></span>                 | <span data-ttu-id="1c8c3-409">4.2</span><span class="sxs-lookup"><span data-stu-id="1c8c3-409">4.2</span></span>             |
| <span data-ttu-id="1c8c3-410">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="1c8c3-410">Windows 2000</span></span>               | <span data-ttu-id="1c8c3-411">4.3</span><span class="sxs-lookup"><span data-stu-id="1c8c3-411">4.3</span></span>             |
| <span data-ttu-id="1c8c3-412">unknown</span><span class="sxs-lookup"><span data-stu-id="1c8c3-412">unknown</span></span>                    | <span data-ttu-id="1c8c3-413">4.4</span><span class="sxs-lookup"><span data-stu-id="1c8c3-413">4.4</span></span>             |
| <span data-ttu-id="1c8c3-414">Windows ME</span><span class="sxs-lookup"><span data-stu-id="1c8c3-414">Windows ME</span></span>                 | <span data-ttu-id="1c8c3-415">5.0</span><span class="sxs-lookup"><span data-stu-id="1c8c3-415">5.0</span></span>             |
| <span data-ttu-id="1c8c3-416">Office XP</span><span class="sxs-lookup"><span data-stu-id="1c8c3-416">Office XP</span></span>                  | <span data-ttu-id="1c8c3-417">5.1</span><span class="sxs-lookup"><span data-stu-id="1c8c3-417">5.1</span></span>             |
| <span data-ttu-id="1c8c3-418">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c8c3-418">Windows XP</span></span>                 | <span data-ttu-id="1c8c3-419">5.2</span><span class="sxs-lookup"><span data-stu-id="1c8c3-419">5.2</span></span>             |
| <span data-ttu-id="1c8c3-420">Downloadble Web autônomos</span><span class="sxs-lookup"><span data-stu-id="1c8c3-420">Standalone web downloadble</span></span> | <span data-ttu-id="1c8c3-421">6.0</span><span class="sxs-lookup"><span data-stu-id="1c8c3-421">6.0</span></span>             |



 

## <a name="further-information"></a><span data-ttu-id="1c8c3-422">Mais informações</span><span class="sxs-lookup"><span data-stu-id="1c8c3-422">Further Information</span></span>

<span data-ttu-id="1c8c3-423">Para obter informações adicionais, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1c8c3-423">For additional information, see the following:</span></span>

-   [<span data-ttu-id="1c8c3-424">Instalar e usar editores de método de entrada</span><span class="sxs-lookup"><span data-stu-id="1c8c3-424">Installing and Using Input Method Editors</span></span>](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [<span data-ttu-id="1c8c3-425">Exibição de texto internacional</span><span class="sxs-lookup"><span data-stu-id="1c8c3-425">International Text Display</span></span>](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [<span data-ttu-id="1c8c3-426">O consórcio Unicode</span><span class="sxs-lookup"><span data-stu-id="1c8c3-426">The Unicode Consortium</span></span>](https://www.unicode.org/)
-   <span data-ttu-id="1c8c3-427">Desenvolvendo software internacional.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-427">Developing International Software.</span></span> <span data-ttu-id="1c8c3-428">Dr. International.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-428">Dr. International.</span></span> <span data-ttu-id="1c8c3-429">2º Ed.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-429">2nd ed.</span></span> <span data-ttu-id="1c8c3-430">Redmond, WA: Microsoft Press, 2003.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-430">Redmond, WA: Microsoft Press, 2003.</span></span>

## <a name="getreadingstring"></a><span data-ttu-id="1c8c3-431">Getreadingstring</span><span class="sxs-lookup"><span data-stu-id="1c8c3-431">GetReadingString</span></span>

<span data-ttu-id="1c8c3-432">Obtém informações de cadeia de caracteres de leitura.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-432">Gets reading string information.</span></span>

<span data-ttu-id="1c8c3-433">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-433">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="1c8c3-434"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="1c8c3-434"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="1c8c3-435">\[no \] contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-435">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="1c8c3-436"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span><span class="sxs-lookup"><span data-stu-id="1c8c3-436"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span></span>
</dt> <dd>

<span data-ttu-id="1c8c3-437">\[em \] comprimento de lpwReadingBuf, em WCHAR.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-437">\[in\] Length of lpwReadingBuf, in WCHAR.</span></span> <span data-ttu-id="1c8c3-438">Se for zero, significa que o tamanho do buffer de leitura da consulta.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-438">If it is zero, it means query reading buffer length.</span></span>

</dd> <dt>

<span data-ttu-id="1c8c3-439"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span><span class="sxs-lookup"><span data-stu-id="1c8c3-439"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span></span> 
</dt> <dd>

<span data-ttu-id="1c8c3-440">\[\]cadeia de caracteres de leitura de retorno de saída (não final zero).</span><span class="sxs-lookup"><span data-stu-id="1c8c3-440">\[out\] Return reading string (not zero end).</span></span>

</dd> <dt>

<span data-ttu-id="1c8c3-441"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span><span class="sxs-lookup"><span data-stu-id="1c8c3-441"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="1c8c3-442">\[\]índice de retorno de saída de caractere de erro na cadeia de caracteres de leitura, se houver.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-442">\[out\] Return index of error character in the reading string if there is.</span></span>

</dd> <dt>

<span data-ttu-id="1c8c3-443"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span><span class="sxs-lookup"><span data-stu-id="1c8c3-443"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span></span> 
</dt> <dd>

<span data-ttu-id="1c8c3-444">\[\]se for true, a leitura da interface do usuário será vertical.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-444">\[out\] If it is TRUE, reading UI is vertical.</span></span> <span data-ttu-id="1c8c3-445">Caso contrário, horizontal puMaxReadingLen.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-445">Otherwise, horizontal puMaxReadingLen.</span></span>

</dd> <dt>

<span data-ttu-id="1c8c3-446"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span><span class="sxs-lookup"><span data-stu-id="1c8c3-446"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span></span> 
</dt> <dd>

<span data-ttu-id="1c8c3-447">\[out \] do tamanho da interface do usuário de leitura.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-447">\[out\] The reading UI length.</span></span> <span data-ttu-id="1c8c3-448">O comprimento máximo de leitura não é fixo; Ele depende não apenas do layout do teclado, mas também do modo de entrada (por exemplo, código interno, entrada substituta).</span><span class="sxs-lookup"><span data-stu-id="1c8c3-448">The max reading length is not fixed; it depends not only on keyboard layout, but also on input mode (for example, internal code, surrogate input).</span></span>

</dd> </dl>

<span data-ttu-id="1c8c3-449">**Valores de retorno**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-449">**Return Values**</span></span>

<span data-ttu-id="1c8c3-450">O comprimento da cadeia de caracteres de leitura.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-450">The reading string length.</span></span>

<span data-ttu-id="1c8c3-451">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-451">**Remarks**</span></span>

<span data-ttu-id="1c8c3-452">Se o valor de retorno for maior que o valor de uReadingBufLen, todos os parâmetros de saída serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-452">If the return value is greater than the value of uReadingBufLen, then all output parameters are undefined.</span></span>

<span data-ttu-id="1c8c3-453">Essa função é implementada no CHT IME 6,0 ou posterior e pode ser adquirida por GetProcAddress em um identificador de módulo IME; o identificador do módulo IME pode ser adquirido por ImmGetIMEFileName e LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-453">This function is implemented in CHT IME 6.0 or later, and can be acquired by GetProcAddress on an IME module handle; the IME module handle can be acquired by ImmGetIMEFileName and LoadLibrary.</span></span>

<span data-ttu-id="1c8c3-454">**Requirements**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-454">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="1c8c3-455"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Verga**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-455"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="1c8c3-456">Declarado em IMM. h.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-456">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="1c8c3-457"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importação**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-457"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="1c8c3-458">Use o IMM. lib.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-458">Use Imm.lib.</span></span>

</dd> </dl>

## <a name="showreadingwindow"></a><span data-ttu-id="1c8c3-459">ShowReadingWindow</span><span class="sxs-lookup"><span data-stu-id="1c8c3-459">ShowReadingWindow</span></span>

<span data-ttu-id="1c8c3-460">Mostrar (ou ocultar) a janela de leitura.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-460">Show (or hide) the reading window.</span></span>

<span data-ttu-id="1c8c3-461">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-461">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="1c8c3-462"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span><span class="sxs-lookup"><span data-stu-id="1c8c3-462"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="1c8c3-463">\[no \] contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-463">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="1c8c3-464"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span><span class="sxs-lookup"><span data-stu-id="1c8c3-464"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span></span> 
</dt> <dd>

<span data-ttu-id="1c8c3-465">\[em \] definido como true para mostrar a janela de leitura (ou false para ocultá-la).</span><span class="sxs-lookup"><span data-stu-id="1c8c3-465">\[in\] Set to TRUE to show the reading window (or FALSE to hide it).</span></span>

</dd> </dl>

<span data-ttu-id="1c8c3-466">**Valores de retorno**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-466">**Return Values**</span></span>

<span data-ttu-id="1c8c3-467">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-467">**Remarks**</span></span>

<span data-ttu-id="1c8c3-468">Retorna TRUE se for bem-sucedido ou FALSE, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-468">Return TRUE if successful or FALSE if otherwise.</span></span>

<span data-ttu-id="1c8c3-469">**Requirements**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-469">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="1c8c3-470"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Verga**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-470"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="1c8c3-471">Declarado em IMM. h.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-471">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="1c8c3-472"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Biblioteca de importação**</span><span class="sxs-lookup"><span data-stu-id="1c8c3-472"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="1c8c3-473">Use o IMM. lib.</span><span class="sxs-lookup"><span data-stu-id="1c8c3-473">Use Imm.lib.</span></span>

</dd> </dl>