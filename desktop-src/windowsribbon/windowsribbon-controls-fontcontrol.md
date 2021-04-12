---
title: Controle de fonte
description: Para simplificar a integração e a configuração do suporte a fontes em aplicativos que exigem recursos de processamento de palavras e edição de texto, a estrutura da faixa de opções do Windows fornece um controle de fonte especializado que expõe uma ampla gama de propriedades de fonte, como nome do tipo, estilo, tamanho do ponto e efeitos.
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366272"
---
# <a name="font-control"></a><span data-ttu-id="bed17-103">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="bed17-103">Font Control</span></span>

<span data-ttu-id="bed17-104">Para simplificar a integração e a configuração do suporte a fontes em aplicativos que exigem recursos de processamento de palavras e edição de texto, a estrutura da faixa de opções do Windows fornece um controle de fonte especializado que expõe uma ampla gama de propriedades de fonte, como nome do tipo, estilo, tamanho do ponto e efeitos.</span><span class="sxs-lookup"><span data-stu-id="bed17-104">To simplify the integration and configuration of font support in applications that require word processing and text editing capabilities, the Windows Ribbon framework provides a specialized Font Control that exposes a wide range of font properties such as typeface name, style, point size, and effects.</span></span>

-   [<span data-ttu-id="bed17-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="bed17-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="bed17-106">Uma experiência consistente</span><span class="sxs-lookup"><span data-stu-id="bed17-106">A Consistent Experience</span></span>](#a-consistent-experience)
-   [<span data-ttu-id="bed17-107">Integração e configuração fáceis</span><span class="sxs-lookup"><span data-stu-id="bed17-107">Easy Integration and Configuration</span></span>](#easy-integration-and-configuration)
-   [<span data-ttu-id="bed17-108">Alinhamento com estruturas de texto GDI comuns</span><span class="sxs-lookup"><span data-stu-id="bed17-108">Alignment with Common GDI Text Structures</span></span>](#alignment-with-common-gdi-text-structures)
-   [<span data-ttu-id="bed17-109">Adicionar um FontControl</span><span class="sxs-lookup"><span data-stu-id="bed17-109">Add a FontControl</span></span>](#add-a-fontcontrol)
    -   [<span data-ttu-id="bed17-110">Declarando um FontControl na marcação</span><span class="sxs-lookup"><span data-stu-id="bed17-110">Declaring a FontControl in Markup</span></span>](#declaring-a-fontcontrol-in-markup)
    -   [<span data-ttu-id="bed17-111">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="bed17-111">Font Control Properties</span></span>](#font-control-properties)
-   [<span data-ttu-id="bed17-112">Definir um manipulador de comando FontControl</span><span class="sxs-lookup"><span data-stu-id="bed17-112">Define a FontControl Command Handler</span></span>](#define-a-fontcontrol-command-handler)
-   [<span data-ttu-id="bed17-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bed17-113">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="bed17-114">Introdução</span><span class="sxs-lookup"><span data-stu-id="bed17-114">Introduction</span></span>

<span data-ttu-id="bed17-115">O controle de fonte é um controle composto que consiste em botões, botões de alternância, caixas de listagem suspensas e caixas de combinação, todos usados para especificar uma determinada propriedade de fonte ou opção de formatação.</span><span class="sxs-lookup"><span data-stu-id="bed17-115">The Font Control is a composite control that consists of buttons, toggle buttons, drop-down list boxes, and combo boxes, all of which are used to specify a particular font property or formatting option.</span></span>

<span data-ttu-id="bed17-116">A captura de tela a seguir mostra o controle de fonte da faixa de opções no WordPad do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bed17-116">The following screen shot shows the Ribbon Font Control in WordPad for Windows 7.</span></span>

![captura de tela do elemento fontcontrol com o atributo richfont definido como true.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a><span data-ttu-id="bed17-118">Uma experiência consistente</span><span class="sxs-lookup"><span data-stu-id="bed17-118">A Consistent Experience</span></span>

<span data-ttu-id="bed17-119">Como um controle de faixa de opção interno, o controle de fonte melhora a funcionalidade geral de gerenciamento de fontes, seleção e formatação e fornece uma experiência de usuário sofisticada e consistente em todos os aplicativos de faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="bed17-119">As a built-in Ribbon control, the Font Control improves overall font management, selection and formatting functionality, and provides a rich, consistent user experience across all Ribbon applications.</span></span>

<span data-ttu-id="bed17-120">Essa experiência consistente inclui</span><span class="sxs-lookup"><span data-stu-id="bed17-120">This consistent experience includes</span></span>

-   <span data-ttu-id="bed17-121">Formatação padronizada e seleção de fontes em aplicativos de faixa de opção.</span><span class="sxs-lookup"><span data-stu-id="bed17-121">Standardized formatting and selection of fonts across Ribbon applications.</span></span>
-   <span data-ttu-id="bed17-122">Representação de fonte padronizada em aplicativos de faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="bed17-122">Standardized font representation across Ribbon applications.</span></span>
-   <span data-ttu-id="bed17-123">Automático, no Windows 7, ativação de fonte baseada na configuração **Mostrar** ou **ocultar** para cada fonte no painel de controle **fontes** .</span><span class="sxs-lookup"><span data-stu-id="bed17-123">Automatic, in Windows 7, font activation that is based on the **Show** or **Hide** setting for each font in the **Fonts** control panel.</span></span> <span data-ttu-id="bed17-124">O controle de fonte exibe apenas as fontes que estão definidas para **Mostrar**.</span><span class="sxs-lookup"><span data-stu-id="bed17-124">The Font Control only displays those fonts that are set to **Show**.</span></span>
    > [!Note]  
    > <span data-ttu-id="bed17-125">No Windows Vista, o painel de controle de **fontes** não oferece a funcionalidade de **Mostrar** ou **ocultar** , portanto, todas as fontes são ativadas.</span><span class="sxs-lookup"><span data-stu-id="bed17-125">In Windows Vista, the **Fonts** control panel does not offer the **Show** or **Hide** functionality, so all fonts are activated.</span></span>

     

-   <span data-ttu-id="bed17-126">Gerenciamento de fontes que está disponível diretamente do controle.</span><span class="sxs-lookup"><span data-stu-id="bed17-126">Font management that is available directly from the control.</span></span>

    <span data-ttu-id="bed17-127">A captura de tela a seguir mostra que o painel de controle de **fontes** pode ser acessado diretamente do controle de fonte.</span><span class="sxs-lookup"><span data-stu-id="bed17-127">The following screen shot shows that the **Fonts** control panel can be accessed directly from the Font Control.</span></span>

    ![captura de tela da lista família de fontes no WordPad para Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   <span data-ttu-id="bed17-129">Suporte para visualização automática.</span><span class="sxs-lookup"><span data-stu-id="bed17-129">Support for auto-preview.</span></span>
-   <span data-ttu-id="bed17-130">Exposição de fontes que são mais relevantes para um usuário, como</span><span class="sxs-lookup"><span data-stu-id="bed17-130">Exposure of fonts that are most relevant to a user, such as</span></span>
    -   <span data-ttu-id="bed17-131">Listas de fontes localizadas para usuários internacionais.</span><span class="sxs-lookup"><span data-stu-id="bed17-131">Localized font lists for international users.</span></span>
    -   <span data-ttu-id="bed17-132">Listas de fontes com base no dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="bed17-132">Font lists based on input device.</span></span>

    > [!Note]  
    > <span data-ttu-id="bed17-133">O suporte para essa funcionalidade não está disponível em nenhuma plataforma anterior ao Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bed17-133">Support for this functionality is not available on any platform older than Windows 7.</span></span>

     

## <a name="easy-integration-and-configuration"></a><span data-ttu-id="bed17-134">Integração e configuração fáceis</span><span class="sxs-lookup"><span data-stu-id="bed17-134">Easy Integration and Configuration</span></span>

<span data-ttu-id="bed17-135">Ao fornecer uma funcionalidade padrão, reutilizável e facilmente consumida, o controle de fonte da faixa de faixas alivia a carga da integração do suporte a fontes em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bed17-135">By providing standard, reusable, and easily consumed functionality, the Ribbon Font Control eases the burden of integrating font support into an application.</span></span>

<span data-ttu-id="bed17-136">Os detalhes da seleção e da formatação de fontes são encapsulados em um elemento lógico autocontido que</span><span class="sxs-lookup"><span data-stu-id="bed17-136">The details of font selection and formatting are wrapped in one, self-contained logical element that</span></span>

-   <span data-ttu-id="bed17-137">Elimina o gerenciamento complexo de interdependências de controle típicas de implementações de controle de fonte.</span><span class="sxs-lookup"><span data-stu-id="bed17-137">Eliminates the complex management of control interdependencies typical of font control implementations.</span></span>
-   <span data-ttu-id="bed17-138">Requer um único manipulador de comando para todas as funcionalidades expostas pelos subcontroles de controles Font.</span><span class="sxs-lookup"><span data-stu-id="bed17-138">Requires a single Command handler for all functionality exposed by the Font Control sub-controls.</span></span>

<span data-ttu-id="bed17-139">Esse manipulador de comando único permite que o controle de fonte gerencie a funcionalidade de vários subcontroles internamente; um subcontrole nunca interage diretamente com o aplicativo, independentemente de sua função.</span><span class="sxs-lookup"><span data-stu-id="bed17-139">This single Command handler allows the Font Control to manage the functionality of various sub-controls internally; a sub-control never interacts directly with the application, regardless of its function.</span></span>

<span data-ttu-id="bed17-140">Outros recursos do controle de fonte incluem</span><span class="sxs-lookup"><span data-stu-id="bed17-140">Other features of the Font Control include</span></span>

-   <span data-ttu-id="bed17-141">A geração automática de reconhecimento de DPI de um WYSIWYG (o que você vê é o que você obtém) representação de bitmap para cada fonte no menu **da família de fontes** .</span><span class="sxs-lookup"><span data-stu-id="bed17-141">Automatic, DPI-aware generation of a WYSIWYG (what you see is what you get) bitmap representation for each font in the **Font family** menu.</span></span>
-   <span data-ttu-id="bed17-142">Integração [do Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .</span><span class="sxs-lookup"><span data-stu-id="bed17-142">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) integration.</span></span>
-   <span data-ttu-id="bed17-143">Bitmaps e dicas de ferramentas localizadas da família de fontes.</span><span class="sxs-lookup"><span data-stu-id="bed17-143">Localized font family bitmaps and tooltips.</span></span>
-   <span data-ttu-id="bed17-144">Enumeração de fontes, agrupamento e metadados para gerenciar e apresentar fontes.</span><span class="sxs-lookup"><span data-stu-id="bed17-144">Font enumeration, grouping, and metadata for managing and presenting fonts.</span></span>
    > [!Note]  
    > <span data-ttu-id="bed17-145">O suporte para essa funcionalidade não está disponível em nenhuma plataforma anterior ao Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bed17-145">Support for this functionality is not available on any platform older than Windows 7 .</span></span>

     

-   <span data-ttu-id="bed17-146">Os seletores de cor de cor do **texto** e de **realce de texto** que espelham o comportamento do [selecionador de cores suspenso](windowsribbon-controls-dropdowncolorpicker.md) da faixa de bits.</span><span class="sxs-lookup"><span data-stu-id="bed17-146">The **Text color** and **Text highlight color** drop-down color pickers that mirror the Ribbon [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md) behavior.</span></span>
-   <span data-ttu-id="bed17-147">Suporte à visualização automática por todos os subcontroles baseados na Galeria de controles de fontes: **família de fontes**, **tamanho da fonte**, **cor do texto** e **cor de realce do texto**.</span><span class="sxs-lookup"><span data-stu-id="bed17-147">Support of auto-previewing by all Font Control gallery-based sub-controls: **Font family**, **Font size**, **Text color**, and **Text highlight color**.</span></span>

## <a name="alignment-with-common-gdi-text-structures"></a><span data-ttu-id="bed17-148">Alinhamento com estruturas de texto GDI comuns</span><span class="sxs-lookup"><span data-stu-id="bed17-148">Alignment with Common GDI Text Structures</span></span>

<span data-ttu-id="bed17-149">Os componentes de pilha de texto [do Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) são usados para expor a seleção de fontes e a funcionalidade de formatação por meio do controle de fonte da faixa de</span><span class="sxs-lookup"><span data-stu-id="bed17-149">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text stack components are used to expose font selection and formatting functionality through the Ribbon Font Control.</span></span> <span data-ttu-id="bed17-150">Os vários recursos de fonte com suporte da estrutura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), da [estrutura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)e da [estrutura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) são expostos por meio dos subcontroles incluídos no controle de fonte.</span><span class="sxs-lookup"><span data-stu-id="bed17-150">The various font features supported by the [LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a) are exposed through the sub-controls that are included in the Font Control.</span></span>

<span data-ttu-id="bed17-151">Os subcontroles exibidos no controle de fonte dependem do modelo *FontType* declarado na marcação da faixa de lista.</span><span class="sxs-lookup"><span data-stu-id="bed17-151">The sub-controls that are displayed in the Font Control depend on the *FontType* template declared in the Ribbon markup.</span></span> <span data-ttu-id="bed17-152">Os modelos *FontType* (discutidos mais detalhadamente na seção a seguir) são projetados para serem alinhados com as estruturas de texto comuns do [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .</span><span class="sxs-lookup"><span data-stu-id="bed17-152">The *FontType* templates (discussed in further detail in the following section) are designed to align with the common [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text structures.</span></span>

## <a name="add-a-fontcontrol"></a><span data-ttu-id="bed17-153">Adicionar um FontControl</span><span class="sxs-lookup"><span data-stu-id="bed17-153">Add a FontControl</span></span>

<span data-ttu-id="bed17-154">Esta seção descreve as etapas básicas para adicionar um controle de fonte a um aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="bed17-154">This section outlines the basic steps for adding a Font Control to a Ribbon application.</span></span>

### <a name="declaring-a-fontcontrol-in-markup"></a><span data-ttu-id="bed17-155">Declarando um FontControl na marcação</span><span class="sxs-lookup"><span data-stu-id="bed17-155">Declaring a FontControl in Markup</span></span>

<span data-ttu-id="bed17-156">Assim como outros controles de faixa de forma, o controle de fonte é declarado em marcação com um elemento [**FontControl**](windowsribbon-element-fontcontrol.md) e associado a uma declaração de comando por meio de uma ID de comando.</span><span class="sxs-lookup"><span data-stu-id="bed17-156">Like other Ribbon controls, the Font Control is declared in markup with a [**FontControl**](windowsribbon-element-fontcontrol.md) element and associated with a Command declaration through a Command ID.</span></span> <span data-ttu-id="bed17-157">Quando o aplicativo é compilado, a ID de comando é usada para associar o comando a um manipulador de comando no aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="bed17-157">When the application is compiled, the Command ID is used to bind the Command to a Command handler in the host application.</span></span>

> [!Note]  
> <span data-ttu-id="bed17-158">Se nenhuma ID de comando for declarada com [**FontControl**](windowsribbon-element-fontcontrol.md) na marcação, então uma será gerada pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="bed17-158">If no Command ID is declared with the [**FontControl**](windowsribbon-element-fontcontrol.md) in markup, then one is generated by the framework.</span></span>

 

<span data-ttu-id="bed17-159">Como os subcontroles do controle de fonte não são expostos diretamente, a personalização do controle de fonte é limitada a três modelos de layout de *FontType* definidos pelo Framework.</span><span class="sxs-lookup"><span data-stu-id="bed17-159">Because the sub-controls of the Font Control are not exposed directly, customization of the Font Control is limited to three *FontType* layout templates defined by the framework.</span></span>

<span data-ttu-id="bed17-160">A personalização adicional do controle de fonte pode ser realizada pela combinação do modelo de layout com atributos [**FontControl**](windowsribbon-element-fontcontrol.md) , como *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible* e *IsUnderlineButtonVisible*.</span><span class="sxs-lookup"><span data-stu-id="bed17-160">Further customization of the Font Control can be accomplished by combining the layout template with [**FontControl**](windowsribbon-element-fontcontrol.md) attributes such as *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible*, and *IsUnderlineButtonVisible*.</span></span>

> [!Note]  
> <span data-ttu-id="bed17-161">A funcionalidade de fonte além daquela exposta pelos modelos e atributos de controle de fonte padrão requer uma implementação de controle de fonte personalizada que está fora do escopo deste artigo.</span><span class="sxs-lookup"><span data-stu-id="bed17-161">Font functionality beyond that exposed by the standard Font Control templates and attributes requires a custom font control implementation that is outside the scope of this article.</span></span>

 

<span data-ttu-id="bed17-162">A tabela a seguir lista os modelos de controle de fonte e o tipo de controle de edição com os quais cada modelo está alinhado.</span><span class="sxs-lookup"><span data-stu-id="bed17-162">The following table lists the Font Control templates and the edit control type that each template is aligned with.</span></span>



| <span data-ttu-id="bed17-163">Modelo</span><span class="sxs-lookup"><span data-stu-id="bed17-163">Template</span></span>      | <span data-ttu-id="bed17-164">Suporta</span><span class="sxs-lookup"><span data-stu-id="bed17-164">Supports</span></span>                                                                 |
|---------------|--------------------------------------------------------------------------|
| <span data-ttu-id="bed17-165">FontOnly</span><span class="sxs-lookup"><span data-stu-id="bed17-165">FontOnly</span></span>      | [<span data-ttu-id="bed17-166">Estrutura LOGFONT</span><span class="sxs-lookup"><span data-stu-id="bed17-166">LOGFONT Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| <span data-ttu-id="bed17-167">FontWithColor</span><span class="sxs-lookup"><span data-stu-id="bed17-167">FontWithColor</span></span> | [<span data-ttu-id="bed17-168">Estrutura CHOOSEFONT</span><span class="sxs-lookup"><span data-stu-id="bed17-168">CHOOSEFONT Structure</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| <span data-ttu-id="bed17-169">RichFont</span><span class="sxs-lookup"><span data-stu-id="bed17-169">RichFont</span></span>      | [<span data-ttu-id="bed17-170">Estrutura CHARFORMAT2</span><span class="sxs-lookup"><span data-stu-id="bed17-170">CHARFORMAT2 Structure</span></span>](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

<span data-ttu-id="bed17-171">A tabela a seguir lista os controles associados a cada modelo e identifica os controles que são opcionais para um modelo associado.</span><span class="sxs-lookup"><span data-stu-id="bed17-171">The following table lists the controls that are associated with each template and identifies the controls that are optional for an associated template.</span></span>



<span data-ttu-id="bed17-172">Controles</span><span class="sxs-lookup"><span data-stu-id="bed17-172">Controls</span></span>

<span data-ttu-id="bed17-173">Modelos</span><span class="sxs-lookup"><span data-stu-id="bed17-173">Templates</span></span>

<span data-ttu-id="bed17-174">**RichFont**</span><span class="sxs-lookup"><span data-stu-id="bed17-174">**RichFont**</span></span>

<span data-ttu-id="bed17-175">**FontWithColor**</span><span class="sxs-lookup"><span data-stu-id="bed17-175">**FontWithColor**</span></span>

<span data-ttu-id="bed17-176">**FontOnly**</span><span class="sxs-lookup"><span data-stu-id="bed17-176">**FontOnly**</span></span>

<span data-ttu-id="bed17-177">Padrão</span><span class="sxs-lookup"><span data-stu-id="bed17-177">Default</span></span>

<span data-ttu-id="bed17-178">Opcional</span><span class="sxs-lookup"><span data-stu-id="bed17-178">Optional</span></span>

<span data-ttu-id="bed17-179">Padrão</span><span class="sxs-lookup"><span data-stu-id="bed17-179">Default</span></span>

<span data-ttu-id="bed17-180">Opcional</span><span class="sxs-lookup"><span data-stu-id="bed17-180">Optional</span></span>

<span data-ttu-id="bed17-181">Padrão</span><span class="sxs-lookup"><span data-stu-id="bed17-181">Default</span></span>

<span data-ttu-id="bed17-182">Opcional</span><span class="sxs-lookup"><span data-stu-id="bed17-182">Optional</span></span>

<span data-ttu-id="bed17-183">Caixa de combinação de **tamanho da fonte**</span><span class="sxs-lookup"><span data-stu-id="bed17-183">**Font size** combo box</span></span>

<span data-ttu-id="bed17-184">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-184">Yes</span></span>

<span data-ttu-id="bed17-185">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-185">No</span></span>

<span data-ttu-id="bed17-186">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-186">Yes</span></span>

<span data-ttu-id="bed17-187">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-187">No</span></span>

<span data-ttu-id="bed17-188">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-188">Yes</span></span>

<span data-ttu-id="bed17-189">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-189">No</span></span>

<span data-ttu-id="bed17-190">Caixa de combinação **da família de fontes**</span><span class="sxs-lookup"><span data-stu-id="bed17-190">**Font family** combo box</span></span>

<span data-ttu-id="bed17-191">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-191">Yes</span></span>

<span data-ttu-id="bed17-192">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-192">No</span></span>

<span data-ttu-id="bed17-193">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-193">Yes</span></span>

<span data-ttu-id="bed17-194">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-194">No</span></span>

<span data-ttu-id="bed17-195">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-195">Yes</span></span>

<span data-ttu-id="bed17-196">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-196">No</span></span>

<span data-ttu-id="bed17-197">Botão **aumentar fonte**</span><span class="sxs-lookup"><span data-stu-id="bed17-197">**Grow font** button</span></span>

<span data-ttu-id="bed17-198">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-198">Yes</span></span>

<span data-ttu-id="bed17-199">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-199">Yes</span></span>

<span data-ttu-id="bed17-200">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-200">Yes</span></span>

<span data-ttu-id="bed17-201">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-201">Yes</span></span>

\-

\-

<span data-ttu-id="bed17-202">Botão **reduzir fonte**</span><span class="sxs-lookup"><span data-stu-id="bed17-202">**Shrink font** button</span></span>

<span data-ttu-id="bed17-203">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-203">Yes</span></span>

<span data-ttu-id="bed17-204">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-204">Yes</span></span>

<span data-ttu-id="bed17-205">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-205">Yes</span></span>

<span data-ttu-id="bed17-206">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-206">Yes</span></span>

\-

\-

<span data-ttu-id="bed17-207">Botão **negrito**</span><span class="sxs-lookup"><span data-stu-id="bed17-207">**Bold** button</span></span>

<span data-ttu-id="bed17-208">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-208">Yes</span></span>

<span data-ttu-id="bed17-209">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-209">No</span></span>

<span data-ttu-id="bed17-210">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-210">Yes</span></span>

<span data-ttu-id="bed17-211">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-211">No</span></span>

<span data-ttu-id="bed17-212">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-212">Yes</span></span>

<span data-ttu-id="bed17-213">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-213">No</span></span>

<span data-ttu-id="bed17-214">Botão **itálico**</span><span class="sxs-lookup"><span data-stu-id="bed17-214">**Italic** button</span></span>

<span data-ttu-id="bed17-215">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-215">Yes</span></span>

<span data-ttu-id="bed17-216">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-216">No</span></span>

<span data-ttu-id="bed17-217">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-217">Yes</span></span>

<span data-ttu-id="bed17-218">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-218">No</span></span>

<span data-ttu-id="bed17-219">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-219">Yes</span></span>

<span data-ttu-id="bed17-220">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-220">No</span></span>

<span data-ttu-id="bed17-221">Botão **sublinhado**</span><span class="sxs-lookup"><span data-stu-id="bed17-221">**Underline** button</span></span>

<span data-ttu-id="bed17-222">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-222">Yes</span></span>

<span data-ttu-id="bed17-223">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-223">No</span></span>

<span data-ttu-id="bed17-224">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-224">Yes</span></span>

<span data-ttu-id="bed17-225">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-225">Yes</span></span>

<span data-ttu-id="bed17-226">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-226">Yes</span></span>

<span data-ttu-id="bed17-227">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-227">Yes</span></span>

<span data-ttu-id="bed17-228">Botão **tachado**</span><span class="sxs-lookup"><span data-stu-id="bed17-228">**Strikethrough** button</span></span>

<span data-ttu-id="bed17-229">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-229">Yes</span></span>

<span data-ttu-id="bed17-230">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-230">No</span></span>

<span data-ttu-id="bed17-231">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-231">Yes</span></span>

<span data-ttu-id="bed17-232">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-232">Yes</span></span>

<span data-ttu-id="bed17-233">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-233">Yes</span></span>

<span data-ttu-id="bed17-234">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-234">Yes</span></span>

<span data-ttu-id="bed17-235">Botão **subscrito**</span><span class="sxs-lookup"><span data-stu-id="bed17-235">**Subscript** button</span></span>

<span data-ttu-id="bed17-236">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-236">Yes</span></span>

<span data-ttu-id="bed17-237">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-237">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="bed17-238">Botão **sobrescrito**</span><span class="sxs-lookup"><span data-stu-id="bed17-238">**Superscript** button</span></span>

<span data-ttu-id="bed17-239">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-239">Yes</span></span>

<span data-ttu-id="bed17-240">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-240">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="bed17-241">Botão de **cor de realce de texto**</span><span class="sxs-lookup"><span data-stu-id="bed17-241">**Text highlight color** button</span></span>

<span data-ttu-id="bed17-242">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-242">Yes</span></span>

<span data-ttu-id="bed17-243">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-243">No</span></span>

<span data-ttu-id="bed17-244">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-244">Yes</span></span>

<span data-ttu-id="bed17-245">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-245">Yes</span></span>

\-

\-

<span data-ttu-id="bed17-246">Botão de **cor do texto**</span><span class="sxs-lookup"><span data-stu-id="bed17-246">**Text color** button</span></span>

<span data-ttu-id="bed17-247">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-247">Yes</span></span>

<span data-ttu-id="bed17-248">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-248">No</span></span>

<span data-ttu-id="bed17-249">Sim</span><span class="sxs-lookup"><span data-stu-id="bed17-249">Yes</span></span>

<span data-ttu-id="bed17-250">Não</span><span class="sxs-lookup"><span data-stu-id="bed17-250">No</span></span>

\-

\-



 

<span data-ttu-id="bed17-251">Quando o comportamento de layout de um controle de fonte é declarado, a estrutura da faixa de faixas fornece um modelo de layout *SizeDefinition* opcional, `OneFontControl` , que define duas configurações de subcontrole com base no tamanho da faixa de opção e no espaço disponível para o controle de fonte.</span><span class="sxs-lookup"><span data-stu-id="bed17-251">When the layout behavior of a Font Control is declared, the Ribbon framework provides an optional *SizeDefinition* layout template, `OneFontControl`, that defines two sub-control configurations based on the size of the Ribbon and the space available for the Font Control.</span></span> <span data-ttu-id="bed17-252">Para obter mais informações, consulte [Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="bed17-252">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

### <a name="adding-a-fontcontrol-to-a-ribbon"></a><span data-ttu-id="bed17-253">Adicionando um FontControl a uma faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="bed17-253">Adding a FontControl to a Ribbon</span></span>

<span data-ttu-id="bed17-254">Os exemplos de código a seguir demonstram os requisitos básicos de marcação para adicionar um controle de fonte a uma faixa de opções:</span><span class="sxs-lookup"><span data-stu-id="bed17-254">The following code examples demonstrate the basic markup requirements for adding a Font Control to a Ribbon:</span></span>

<span data-ttu-id="bed17-255">Esta seção de código mostra a marcação de declaração de comando [**FontControl**](windowsribbon-element-fontcontrol.md) , incluindo os comandos de [**guia**](windowsribbon-element-tab.md) e de [**grupo**](windowsribbon-element-group.md) que são necessários para exibir um controle na [**faixa de faixas**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="bed17-255">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup, including the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) Commands that are required for displaying a control in the [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="bed17-256">Esta seção de código mostra a marcação necessária para declarar e associar um [**FontControl**](windowsribbon-element-fontcontrol.md) a um [**comando**](windowsribbon-element-command.md) por meio de uma ID de comando.</span><span class="sxs-lookup"><span data-stu-id="bed17-256">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a [**Command**](windowsribbon-element-command.md) through a Command ID.</span></span> <span data-ttu-id="bed17-257">Esse exemplo específico inclui as declarações de [**guia**](windowsribbon-element-tab.md) e de [**grupo**](windowsribbon-element-group.md) , com preferências de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="bed17-257">This particular example includes the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) declarations, with scaling preferences.</span></span>


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a><span data-ttu-id="bed17-258">Adicionando um FontControl a um ContextPopup</span><span class="sxs-lookup"><span data-stu-id="bed17-258">Adding a FontControl to a ContextPopup</span></span>

<span data-ttu-id="bed17-259">A adição de um controle de fonte a um [pop-up de contexto](windowsribbon-controls-contextpopup.md) requer um procedimento semelhante ao da adição de um controle de fonte à faixa de tipos.</span><span class="sxs-lookup"><span data-stu-id="bed17-259">Adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md) requires a procedure similar to that of adding a Font Control to the Ribbon.</span></span> <span data-ttu-id="bed17-260">No entanto, um controle de fonte em um [**Minibarra**](windowsribbon-element-minitoolbar.md) é restrito ao conjunto de subcontroles padrão que são comuns a todos os modelos de controle de fonte: **família de fontes**, **tamanho da fonte**, **negrito** e **itálico**.</span><span class="sxs-lookup"><span data-stu-id="bed17-260">However, a Font Control in a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is restricted to the set of default sub-controls that are common to all Font Control templates: **Font family**, **Font size**, **Bold**, and **Italic**.</span></span>

<span data-ttu-id="bed17-261">Os exemplos de código a seguir demonstram os requisitos básicos de marcação para adicionar um controle de fonte a um [Popup de contexto](windowsribbon-controls-contextpopup.md):</span><span class="sxs-lookup"><span data-stu-id="bed17-261">The following code examples demonstrate the basic markup requirements for adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md):</span></span>

<span data-ttu-id="bed17-262">Esta seção de código mostra a marcação de declaração de comando [**FontControl**](windowsribbon-element-fontcontrol.md) que é necessária para exibir um **FontControl** no [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="bed17-262">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup that is required for displaying a **FontControl** in the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



<span data-ttu-id="bed17-263">Esta seção de código mostra a marcação necessária para declarar e associar um [**FontControl**](windowsribbon-element-fontcontrol.md) a um comando por meio de uma ID de comando.</span><span class="sxs-lookup"><span data-stu-id="bed17-263">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a Command through a Command ID.</span></span>


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a><span data-ttu-id="bed17-264">Dicas de tecla</span><span class="sxs-lookup"><span data-stu-id="bed17-264">Keytips</span></span>

<span data-ttu-id="bed17-265">Cada subcontrole no controle de fonte da faixa de bits pode ser acessado por meio de um atalho de teclado ou KeyTip.</span><span class="sxs-lookup"><span data-stu-id="bed17-265">Each sub-control in the Ribbon Font Control is accessible through a keyboard shortcut, or keytip.</span></span> <span data-ttu-id="bed17-266">Esse KeyTip é predefinido e atribuído a cada subcontrole da estrutura.</span><span class="sxs-lookup"><span data-stu-id="bed17-266">This keytip is predefined and assigned to each sub-control by the framework.</span></span>

<span data-ttu-id="bed17-267">Se um valor de atributo *KeyTip* for atribuído ao elemento [**FontControl**](windowsribbon-element-fontcontrol.md) na marcação, esse valor será adicionado como um prefixo ao KeyTip definido pelo Framework.</span><span class="sxs-lookup"><span data-stu-id="bed17-267">If a *Keytip* attribute value is assigned to the [**FontControl**](windowsribbon-element-fontcontrol.md) element in markup, this value is added as a prefix to the framework-defined keytip.</span></span>

> [!Note]  
> <span data-ttu-id="bed17-268">O aplicativo deve impor uma regra de caractere único para esse prefixo.</span><span class="sxs-lookup"><span data-stu-id="bed17-268">The application should enforce a single-character rule for this prefix.</span></span>

 

<span data-ttu-id="bed17-269">A tabela a seguir lista as keytips definidas pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="bed17-269">The following table lists the keytips defined by the framework.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bed17-270">Subcontrole</span><span class="sxs-lookup"><span data-stu-id="bed17-270">Sub-control</span></span></th>
<th><span data-ttu-id="bed17-271">KeyTip</span><span class="sxs-lookup"><span data-stu-id="bed17-271">Keytip</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bed17-272">Família de fontes</span><span class="sxs-lookup"><span data-stu-id="bed17-272">Font family</span></span></td>
<td><span data-ttu-id="bed17-273">F</span><span class="sxs-lookup"><span data-stu-id="bed17-273">F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed17-274">Estilo da fonte</span><span class="sxs-lookup"><span data-stu-id="bed17-274">Font style</span></span></td>
<td><span data-ttu-id="bed17-275">T</span><span class="sxs-lookup"><span data-stu-id="bed17-275">T</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bed17-276">Tamanho da fonte</span><span class="sxs-lookup"><span data-stu-id="bed17-276">Font size</span></span></td>
<td><span data-ttu-id="bed17-277">S</span><span class="sxs-lookup"><span data-stu-id="bed17-277">S</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed17-278">Aumentar fonte</span><span class="sxs-lookup"><span data-stu-id="bed17-278">Grow font</span></span></td>
<td><span data-ttu-id="bed17-279">G</span><span class="sxs-lookup"><span data-stu-id="bed17-279">G</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bed17-280">Reduzir fonte</span><span class="sxs-lookup"><span data-stu-id="bed17-280">Shrink font</span></span></td>
<td><span data-ttu-id="bed17-281">K</span><span class="sxs-lookup"><span data-stu-id="bed17-281">K</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed17-282">Negrito</span><span class="sxs-lookup"><span data-stu-id="bed17-282">Bold</span></span></td>
<td><span data-ttu-id="bed17-283">B</span><span class="sxs-lookup"><span data-stu-id="bed17-283">B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bed17-284">Itálico</span><span class="sxs-lookup"><span data-stu-id="bed17-284">Italic</span></span></td>
<td><span data-ttu-id="bed17-285">I</span><span class="sxs-lookup"><span data-stu-id="bed17-285">I</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed17-286">Underline</span><span class="sxs-lookup"><span data-stu-id="bed17-286">Underline</span></span></td>
<td><span data-ttu-id="bed17-287">U</span><span class="sxs-lookup"><span data-stu-id="bed17-287">U</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bed17-288">Tachado</span><span class="sxs-lookup"><span data-stu-id="bed17-288">Strikethrough</span></span></td>
<td><span data-ttu-id="bed17-289">X</span><span class="sxs-lookup"><span data-stu-id="bed17-289">X</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed17-290">Sobrescrito</span><span class="sxs-lookup"><span data-stu-id="bed17-290">Superscript</span></span></td>
<td><span data-ttu-id="bed17-291">Y ou Z</span><span class="sxs-lookup"><span data-stu-id="bed17-291">Y or Z</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="bed17-292">Se o atributo <em>KeyTip</em> não for declarado na marcação, o KeyTip padrão será Y; caso contrário, o KeyTip padrão será <em>KeyTip</em> + Z.</span><span class="sxs-lookup"><span data-stu-id="bed17-292">If the <em>Keytip</em> attribute is not declared in markup, the default keytip is Y; otherwise, the default keytip is <em>Keytip</em> + Z.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bed17-293">Subscrito</span><span class="sxs-lookup"><span data-stu-id="bed17-293">Subscript</span></span></td>
<td><span data-ttu-id="bed17-294">Um</span><span class="sxs-lookup"><span data-stu-id="bed17-294">A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed17-295">Cor da fonte</span><span class="sxs-lookup"><span data-stu-id="bed17-295">Font color</span></span></td>
<td><span data-ttu-id="bed17-296">C</span><span class="sxs-lookup"><span data-stu-id="bed17-296">C</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bed17-297">Realce de fonte</span><span class="sxs-lookup"><span data-stu-id="bed17-297">Font highlight</span></span></td>
<td><span data-ttu-id="bed17-298">H</span><span class="sxs-lookup"><span data-stu-id="bed17-298">H</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bed17-299">O prefixo recomendado para uma faixa de opções do MUI (Multilingual User interface) EN-US é ' F ', conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="bed17-299">The recommended prefix for a Multilingual User Interface (MUI) EN-US Ribbon is 'F', as shown in the following example.</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="bed17-300">A captura de tela a seguir ilustra as dicas de teclado do controle de fonte conforme elas são definidas no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="bed17-300">The following screen shot illustrates the Font Control keytips as they are defined in the previous example.</span></span>

![captura de tela do fontcontrol keytips no WordPad para Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a><span data-ttu-id="bed17-302">O arquivo de recurso da faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="bed17-302">The Ribbon Resource File</span></span>

<span data-ttu-id="bed17-303">Quando o arquivo de marcação é compilado, um arquivo de recurso que contém todas as referências de recurso para o aplicativo da faixa de faixas é gerado.</span><span class="sxs-lookup"><span data-stu-id="bed17-303">When the markup file is compiled, a resource file that contains all resource references for the Ribbon application is generated.</span></span>

<span data-ttu-id="bed17-304">Exemplo de um arquivo de recurso simples:</span><span class="sxs-lookup"><span data-stu-id="bed17-304">Example of a simple resource file:</span></span>


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a><span data-ttu-id="bed17-305">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="bed17-305">Font Control Properties</span></span>

<span data-ttu-id="bed17-306">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de fonte e seus subcontroles constituintes.</span><span class="sxs-lookup"><span data-stu-id="bed17-306">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Font Control and its constituent sub-controls.</span></span>

<span data-ttu-id="bed17-307">Normalmente, uma propriedade de controle de fonte é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="bed17-307">Typically, a Font Control property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="bed17-308">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="bed17-308">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="bed17-309">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="bed17-309">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="bed17-310">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="bed17-310">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="bed17-311">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="bed17-311">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="bed17-312">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle de fonte.</span><span class="sxs-lookup"><span data-stu-id="bed17-312">The following table lists the property keys that are associated with the Font Control.</span></span>



| <span data-ttu-id="bed17-313">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="bed17-313">Property Key</span></span>                                                                                                                  | <span data-ttu-id="bed17-314">Observações</span><span class="sxs-lookup"><span data-stu-id="bed17-314">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bed17-315">Interface do usuário \_ PKEY \_ fontproperties</span><span class="sxs-lookup"><span data-stu-id="bed17-315">UI\_PKEY\_FontProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | <span data-ttu-id="bed17-316">Expõe, em Aggregate como um objeto [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) , todas as propriedades de subcontrole de controle Font.</span><span class="sxs-lookup"><span data-stu-id="bed17-316">Exposes, in aggregate as an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) object, all Font Control sub-control properties.</span></span><br/> <span data-ttu-id="bed17-317">A estrutura consulta essa propriedade quando `UI_INVALIDATIONS_VALUE` é passada como o valor dos *sinalizadores* na chamada para [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="bed17-317">The framework queries this property when `UI_INVALIDATIONS_VALUE` is passed as the value of *flags* in the call to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span><br/> |
| [<span data-ttu-id="bed17-318">Interface do usuário \_ PKEY \_ fontproperties \_ alteradoproperties</span><span class="sxs-lookup"><span data-stu-id="bed17-318">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | <span data-ttu-id="bed17-319">Expõe, em agregação como um objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , somente Propriedades de subcontrole de controle de fonte que foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="bed17-319">Exposes, in aggregate as an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object, only Font Control sub-control properties that have changed.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="bed17-320">\_KeyTip PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="bed17-320">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | <span data-ttu-id="bed17-321">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="bed17-321">Can only be updated through invalidation.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="bed17-322">Interface do usuário \_ PKEY \_ habilitada</span><span class="sxs-lookup"><span data-stu-id="bed17-322">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | <span data-ttu-id="bed17-323">Dá suporte a [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="bed17-323">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>                                                                                                                                                                  |



 

<span data-ttu-id="bed17-324">Além das propriedades com suporte pelo controle de fonte em si, a estrutura da faixa de faixas também define uma [chave de propriedade](windowsribbon-reference-properties.md) para cada subcontrole de controle de fonte.</span><span class="sxs-lookup"><span data-stu-id="bed17-324">In addition to the properties supported by the Font Control itself, the Ribbon framework also defines a [property key](windowsribbon-reference-properties.md) for each Font Control sub-control.</span></span> <span data-ttu-id="bed17-325">Essas chaves de propriedade e seus valores são expostos pela estrutura por meio de uma implementação de interface [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) que define os métodos para gerenciar uma coleção, também chamada de recipiente de propriedades, de pares de nome e valor.</span><span class="sxs-lookup"><span data-stu-id="bed17-325">These property keys and their values are exposed by the framework through an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface implementation that defines the methods for managing a collection, also called a property bag, of name and value pairs.</span></span>

<span data-ttu-id="bed17-326">O aplicativo traduz as estruturas de fonte para propriedades que podem ser acessadas por meio dos métodos de interface [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="bed17-326">The application translates the font structures to properties that are accessible through the [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface methods.</span></span> <span data-ttu-id="bed17-327">Esse modelo enfatiza a distinção entre o controle de fonte e os componentes de pilha de texto do Windows Graphics Device Interface (GDI) ([estrutura LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), [estrutura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)e [estrutura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a)) que são suportados pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="bed17-327">This model emphasizes the distinction between the Font Control and the Windows Graphics Device Interface (GDI) text stack components ([LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a)) that are supported by the framework.</span></span>

<span data-ttu-id="bed17-328">A tabela a seguir lista os controles individuais e suas chaves de propriedade associadas.</span><span class="sxs-lookup"><span data-stu-id="bed17-328">The following table lists the individual controls and their associated property keys.</span></span>



| <span data-ttu-id="bed17-329">Controles</span><span class="sxs-lookup"><span data-stu-id="bed17-329">Controls</span></span>                 | <span data-ttu-id="bed17-330">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="bed17-330">Property Key</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="bed17-331">Observações</span><span class="sxs-lookup"><span data-stu-id="bed17-331">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bed17-332">**Tamanho da fonte**</span><span class="sxs-lookup"><span data-stu-id="bed17-332">**Font size**</span></span>            | [<span data-ttu-id="bed17-333">\_Tamanho da \_ fonte de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="bed17-333">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="bed17-334">Quando uma execução de texto de tamanho heterogêneo é realçada, a estrutura da faixa de faixas define o controle de **tamanho da fonte** como em branco e o valor da [interface do usuário \_ PKEY \_ fontproperties \_ tamanho](windowsribbon-reference-properties-uipkey-fontproperties-size.md) como 0.</span><span class="sxs-lookup"><span data-stu-id="bed17-334">When a run of heterogeneously sized text is highlighted, the Ribbon framework sets the **Font size** control to blank and the value of [UI\_PKEY\_FontProperties\_Size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) to 0.</span></span> <span data-ttu-id="bed17-335">Quando o botão **aumentar fonte** ou **reduzir fonte** é clicado, todo o texto realçado é redimensionado, mas a diferença relativa em tamanhos de texto é preservada.</span><span class="sxs-lookup"><span data-stu-id="bed17-335">When the **Grow font** or **Shrink font** button is clicked, all highlighted text is resized but the relative difference in text sizes is preserved.</span></span>                                                                                                                                                    |
| <span data-ttu-id="bed17-336">**Família de fontes**</span><span class="sxs-lookup"><span data-stu-id="bed17-336">**Font family**</span></span>          | [<span data-ttu-id="bed17-337">IU \_ \_ da família PKEY fontproperties \_</span><span class="sxs-lookup"><span data-stu-id="bed17-337">UI\_PKEY\_FontProperties\_Family</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | <span data-ttu-id="bed17-338">Os nomes da família de fontes GDI variam com a localidade do sistema.</span><span class="sxs-lookup"><span data-stu-id="bed17-338">GDI font family names vary with system locale.</span></span> <span data-ttu-id="bed17-339">Assim, se o valor da [interface do usuário \_ PKEY \_ FontProperty \_ ](windowsribbon-reference-properties-uipkey-fontproperties-family.md) for preservado entre as sessões do aplicativo, esse valor deverá ser recuperado em cada nova sessão.</span><span class="sxs-lookup"><span data-stu-id="bed17-339">As such, if the value of [UI\_PKEY\_FontProperties\_Family](windowsribbon-reference-properties-uipkey-fontproperties-family.md) is preserved across application sessions, that value should be retrieved on each new session.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="bed17-340">**Aumentar fonte**</span><span class="sxs-lookup"><span data-stu-id="bed17-340">**Grow font**</span></span>            | [<span data-ttu-id="bed17-341">\_Tamanho da \_ fonte de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="bed17-341">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="bed17-342">Consulte **tamanho da fonte**.</span><span class="sxs-lookup"><span data-stu-id="bed17-342">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="bed17-343">**Reduzir fonte**</span><span class="sxs-lookup"><span data-stu-id="bed17-343">**Shrink font**</span></span>          | [<span data-ttu-id="bed17-344">\_Tamanho da \_ fonte de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="bed17-344">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="bed17-345">Consulte **tamanho da fonte**.</span><span class="sxs-lookup"><span data-stu-id="bed17-345">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="bed17-346">**Negrito**</span><span class="sxs-lookup"><span data-stu-id="bed17-346">**Bold**</span></span>                 | [<span data-ttu-id="bed17-347">Interface do usuário \_ PKEY \_ FontProperty \_ bold</span><span class="sxs-lookup"><span data-stu-id="bed17-347">UI\_PKEY\_FontProperties\_Bold</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="bed17-348">**Itálico**</span><span class="sxs-lookup"><span data-stu-id="bed17-348">**Italic**</span></span>               | [<span data-ttu-id="bed17-349">Interface do usuário \_ PKEY \_ fontproperties \_ itálico</span><span class="sxs-lookup"><span data-stu-id="bed17-349">UI\_PKEY\_FontProperties\_Italic</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="bed17-350">**Aplicar**</span><span class="sxs-lookup"><span data-stu-id="bed17-350">**Underline**</span></span>            | [<span data-ttu-id="bed17-351">Interface do usuário \_ PKEY \_ fontproperties \_ sublinhado</span><span class="sxs-lookup"><span data-stu-id="bed17-351">UI\_PKEY\_FontProperties\_Underline</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="bed17-352">**Tachado**</span><span class="sxs-lookup"><span data-stu-id="bed17-352">**Strikethrough**</span></span>        | [<span data-ttu-id="bed17-353">Interface do usuário \_ PKEY \_ fontproperties \_ tachado</span><span class="sxs-lookup"><span data-stu-id="bed17-353">UI\_PKEY\_FontProperties\_Strikethrough</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="bed17-354">**Subscrito**</span><span class="sxs-lookup"><span data-stu-id="bed17-354">**Subscript**</span></span>            | [<span data-ttu-id="bed17-355">Interface do usuário \_ PKEY \_ fontproperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="bed17-355">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="bed17-356">Se o botão **subscrito** for definido, o **sobrescrito** também não poderá ser definido.</span><span class="sxs-lookup"><span data-stu-id="bed17-356">If the **Subscript** button is set, then the **Superscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="bed17-357">**Sobrescrito**</span><span class="sxs-lookup"><span data-stu-id="bed17-357">**Superscript**</span></span>          | [<span data-ttu-id="bed17-358">Interface do usuário \_ PKEY \_ fontproperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="bed17-358">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="bed17-359">Se o botão **sobrescrito** for definido, o **subscript** também não poderá ser definido.</span><span class="sxs-lookup"><span data-stu-id="bed17-359">If the **Superscript** button is set, then the **Subscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="bed17-360">**Cor de realce de texto**</span><span class="sxs-lookup"><span data-stu-id="bed17-360">**Text highlight color**</span></span> | <span data-ttu-id="bed17-361">[Interface do usuário \_ PKEY \_ fontproperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [IU \_ PKEY \_ FontProperty \_ backgroundcolortype](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="bed17-361">[UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI\_PKEY\_FontProperties\_BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span></span> | <span data-ttu-id="bed17-362">Fornece a mesma funcionalidade que o `HighlightColors` modelo do elemento [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="bed17-362">Provides the same functionality as the `HighlightColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="bed17-363">É altamente recomendável que apenas um valor de **cor de realce de texto** inicial seja definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bed17-363">We highly recommend that only an initial **Text highlight color** value be set by the application.</span></span> <span data-ttu-id="bed17-364">O último valor selecionado deve ser preservado e não definido quando o cursor é reposicionado dentro de um documento.</span><span class="sxs-lookup"><span data-stu-id="bed17-364">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="bed17-365">Isso permite o acesso rápido à última seleção do usuário, e o seletor de cores não precisa ser reaberto.</span><span class="sxs-lookup"><span data-stu-id="bed17-365">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="bed17-366">As amostras de cor não podem ser personalizadas.</span><span class="sxs-lookup"><span data-stu-id="bed17-366">Color swatches cannot be customized.</span></span><br/> |
| <span data-ttu-id="bed17-367">**Cor do texto**</span><span class="sxs-lookup"><span data-stu-id="bed17-367">**Text color**</span></span>           | <span data-ttu-id="bed17-368">[Interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="bed17-368">[UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI\_PKEY\_FontProperties\_ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span></span>           | <span data-ttu-id="bed17-369">Fornece a mesma funcionalidade que o `StandardColors` modelo do elemento [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="bed17-369">Provides the same functionality as the `StandardColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="bed17-370">É altamente recomendável que apenas um valor de **cor de texto** inicial seja definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bed17-370">We highly recommend that only an initial **Text color** value be set by the application.</span></span> <span data-ttu-id="bed17-371">O último valor selecionado deve ser preservado e não definido quando o cursor é reposicionado dentro de um documento.</span><span class="sxs-lookup"><span data-stu-id="bed17-371">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="bed17-372">Isso permite o acesso rápido à última seleção do usuário, e o seletor de cores não precisa ser reaberto.</span><span class="sxs-lookup"><span data-stu-id="bed17-372">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="bed17-373">As amostras de cor não podem ser personalizadas.</span><span class="sxs-lookup"><span data-stu-id="bed17-373">Color swatches cannot be customized.</span></span><br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a><span data-ttu-id="bed17-374">Definir um manipulador de comando FontControl</span><span class="sxs-lookup"><span data-stu-id="bed17-374">Define a FontControl Command Handler</span></span>

<span data-ttu-id="bed17-375">Esta seção descreve as etapas necessárias para associar um controle de fonte a um manipulador de comandos.</span><span class="sxs-lookup"><span data-stu-id="bed17-375">This section describes the steps required to bind a Font Control to a Command handler.</span></span>

> [!WARNING]
> <span data-ttu-id="bed17-376">Qualquer tentativa de selecionar uma amostra de cor do seletor de cores de um controle de fonte pode resultar em uma violação de acesso se nenhum manipulador de comando estiver associado ao controle.</span><span class="sxs-lookup"><span data-stu-id="bed17-376">Any attempt to select a color swatch from the color picker of a Font Control may result in an access violation if no Command handler is associated with the control.</span></span>

 

<span data-ttu-id="bed17-377">O exemplo de código a seguir demonstra como associar comandos que são declarados na marcação a um manipulador de comandos.</span><span class="sxs-lookup"><span data-stu-id="bed17-377">The following code example demonstrates how to bind Commands that are declared in markup to a Command handler.</span></span>


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



<span data-ttu-id="bed17-378">O exemplo de código a seguir ilustra como implementar o método [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para um controle de fonte.</span><span class="sxs-lookup"><span data-stu-id="bed17-378">The following code example illustrates how to implement the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



<span data-ttu-id="bed17-379">O exemplo de código a seguir ilustra como implementar o método [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) para um controle de fonte.</span><span class="sxs-lookup"><span data-stu-id="bed17-379">The following code example illustrates how to implement the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="bed17-380">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bed17-380">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bed17-381">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="bed17-381">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="bed17-382">**Elemento FontControl**</span><span class="sxs-lookup"><span data-stu-id="bed17-382">**FontControl element**</span></span>](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="bed17-383">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="bed17-383">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="bed17-384">Exemplo de FontControl</span><span class="sxs-lookup"><span data-stu-id="bed17-384">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

