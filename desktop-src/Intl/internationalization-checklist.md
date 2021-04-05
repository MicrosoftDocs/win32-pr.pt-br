---
description: Este tópico fornece ações a serem executadas para criar um código que dê suporte a vários mercados. Considere essas instruções como um guia durante o design do código e as métricas ao avaliar as compilações.
ms.assetid: cf2ac58e-7fc3-4635-8b82-586a0732b2a3
title: Lista de verificação de internacionalização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b18ef8cf88efa8d496d19c0b66208cd44abaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826786"
---
# <a name="internationalization-checklist"></a><span data-ttu-id="c091f-104">Lista de verificação de internacionalização</span><span class="sxs-lookup"><span data-stu-id="c091f-104">Internationalization Checklist</span></span>

<span data-ttu-id="c091f-105">Este tópico fornece ações a serem executadas para criar um código que dê suporte a vários mercados.</span><span class="sxs-lookup"><span data-stu-id="c091f-105">This topic provides actions to take to create code that supports multiple markets.</span></span> <span data-ttu-id="c091f-106">Considere essas instruções como um guia durante o design do código e as métricas ao avaliar as compilações.</span><span class="sxs-lookup"><span data-stu-id="c091f-106">Consider these statements as a guide during code design, and as metrics when you evaluate the builds.</span></span>

-   <span data-ttu-id="c091f-107">Crie especificações de programa que contam para considerações internacionais desde o início.</span><span class="sxs-lookup"><span data-stu-id="c091f-107">Create program specifications that account for international considerations from the outset.</span></span>
    -   <span data-ttu-id="c091f-108">Crie ícones e bitmaps para serem significativos e não ofensivos em seus mercados de destino e não contenham texto.</span><span class="sxs-lookup"><span data-stu-id="c091f-108">Design icons and bitmaps to be meaningful and not offensive in your target markets, and to not contain text.</span></span>
    -   <span data-ttu-id="c091f-109">Menus de design e caixas de diálogo para deixar espaço para a expansão de texto.</span><span class="sxs-lookup"><span data-stu-id="c091f-109">Design menus and dialog boxes to leave room for text expansion.</span></span> <span data-ttu-id="c091f-110">Por exemplo, cadeias de caracteres em inglês geralmente se expandem por 40% quando convertidas em alemão ou holandês.</span><span class="sxs-lookup"><span data-stu-id="c091f-110">For example, English strings often expand by 40% when translated into German or Dutch.</span></span>
    -   <span data-ttu-id="c091f-111">Não use referências gírias ou culturalmente específicas em mensagens ou elementos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c091f-111">Do not use slang or culturally-specific references in UI elements or messages.</span></span>
    -   <span data-ttu-id="c091f-112">Crie combinações de teclas de atalho que são acessíveis em teclados internacionais.</span><span class="sxs-lookup"><span data-stu-id="c091f-112">Create shortcut key combinations that are accessible on international keyboards.</span></span> <span data-ttu-id="c091f-113">Por exemplo, evite usar chaves de caractere de Pontuação como teclas de atalho porque elas nem sempre são encontradas em teclados internacionais ou facilmente produzidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c091f-113">For example, avoid using punctuation character keys as shortcut keys because they are not always found on international keyboards or easily produced by the user.</span></span> <span data-ttu-id="c091f-114">Para obter exemplos de layouts de teclado, consulte [layouts de teclado do Windows](https://msdn.microsoft.com/goglobal/bb964651.aspx).</span><span class="sxs-lookup"><span data-stu-id="c091f-114">For examples of keyboard layouts, see [Windows Keyboard Layouts](https://msdn.microsoft.com/goglobal/bb964651.aspx).</span></span>
    -   <span data-ttu-id="c091f-115">Considere as leis locais que afetam os designs de recursos, como requisitos que as entidades governamentais adquirem software que dá suporte a vários idiomas oficiais.</span><span class="sxs-lookup"><span data-stu-id="c091f-115">Consider local laws affecting feature designs, such as requirements that government entities purchase software that supports multiple official languages.</span></span>
    -   <span data-ttu-id="c091f-116">Desenvolva contratos de terceiros que dão suporte aos padrões da interface do usuário internacional da sua organização e às decisões de design.</span><span class="sxs-lookup"><span data-stu-id="c091f-116">Develop third-party agreements that support your organization's international UI standards and design decisions.</span></span>
    -   <span data-ttu-id="c091f-117">Use uma terminologia consistente nas cadeias de caracteres da interface do usuário que devem ser convertidas.</span><span class="sxs-lookup"><span data-stu-id="c091f-117">Use consistent terminology in user interface strings that must be translated.</span></span>

<!-- -->

-   <span data-ttu-id="c091f-118">Crie um código que seja independente da localidade.</span><span class="sxs-lookup"><span data-stu-id="c091f-118">Create code that is independent of locale.</span></span>
    -   <span data-ttu-id="c091f-119">Não concatene cadeias de caracteres para formar frases.</span><span class="sxs-lookup"><span data-stu-id="c091f-119">Don't concatenate strings to form sentences.</span></span>
    -   <span data-ttu-id="c091f-120">Não use uma determinada variável de cadeia de caracteres em mais de um contexto, como reutilizar um fragmento de frase em mensagens e prompts diferentes, pois essas cadeias de caracteres podem não ser facilmente traduzidas.</span><span class="sxs-lookup"><span data-stu-id="c091f-120">Don't use a given string variable in more than one context, such as reusing a sentence fragment in different messages and prompts, because such strings may not be easy to translate.</span></span>
    -   <span data-ttu-id="c091f-121">Documente cadeias de caracteres usando comentários para fornecer contexto para tradutores e marque claramente as cadeias de caracteres ou os personagens que não devem ser localizados.</span><span class="sxs-lookup"><span data-stu-id="c091f-121">Document strings using comments to provide context for translators, and clearly mark strings or characters that should not be localized.</span></span>
    -   <span data-ttu-id="c091f-122">Não use constantes de caractere embutido em código, constantes numéricas, posições de tela, nomes de filenames ou demarcadores que presumim um idioma específico.</span><span class="sxs-lookup"><span data-stu-id="c091f-122">Don't use hard-coded character constants, numeric constants, screen positions, filenames, or pathnames that presume a particular language.</span></span>
    -   <span data-ttu-id="c091f-123">Torne os buffers grandes o suficiente para manter as cadeias de caracteres traduzidas.</span><span class="sxs-lookup"><span data-stu-id="c091f-123">Make buffers large enough to hold translated strings.</span></span>
    -   <span data-ttu-id="c091f-124">Permitir a entrada de dados com formatos que variam por localidade, como datas, horas e moedas.</span><span class="sxs-lookup"><span data-stu-id="c091f-124">Allow the input of data with formats that vary by locale, such as dates, times, and currencies.</span></span>
    -   <span data-ttu-id="c091f-125">Use o tamanho do papel, o tamanho do envelope e outros padrões apropriados para uma determinada localidade.</span><span class="sxs-lookup"><span data-stu-id="c091f-125">Use paper size, envelope size, and other defaults that are appropriate to a given locale.</span></span>
    -   <span data-ttu-id="c091f-126">Certifique-se de que cada edição de idioma possa ler documentos criados pelas outras edições.</span><span class="sxs-lookup"><span data-stu-id="c091f-126">Ensure that each language edition can read documents created by the other editions.</span></span>
    -   <span data-ttu-id="c091f-127">Forneça suporte para hardware específico de localidade, se necessário.</span><span class="sxs-lookup"><span data-stu-id="c091f-127">Provide support for locale-specific hardware, if necessary.</span></span>
    -   <span data-ttu-id="c091f-128">Configure recursos que não se aplicam a mercados internacionais como opções de implementação que podem ser desativadas facilmente.</span><span class="sxs-lookup"><span data-stu-id="c091f-128">Configure features that don't apply to international markets as implementation options that can be disabled easily.</span></span>

<!-- -->

-   <span data-ttu-id="c091f-129">Crie código que aproveita a funcionalidade internacional oferecida pelo Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c091f-129">Create code that takes advantage of international functionality offered by Microsoft Windows.</span></span>
    -   <span data-ttu-id="c091f-130">Use informações internacionais transportadas pelo sistema (suporte ao idioma nacional).</span><span class="sxs-lookup"><span data-stu-id="c091f-130">Use international information carried by the system (National Language Support).</span></span>
    -   <span data-ttu-id="c091f-131">Use funções do sistema para classificação, conversão de casos e mapeamento de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c091f-131">Use system functions for sorting, case conversion, and string mapping.</span></span>
    -   <span data-ttu-id="c091f-132">Use funções de layout de texto genérico.</span><span class="sxs-lookup"><span data-stu-id="c091f-132">Use generic text layout functions.</span></span>
    -   <span data-ttu-id="c091f-133">Responda a alterações nas configurações internacionais no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="c091f-133">Respond to changes to international settings in Control Panel.</span></span>
    -   <span data-ttu-id="c091f-134">Manipule a mensagem do WM \_ INPUTLANGCHANGEREQUEST.</span><span class="sxs-lookup"><span data-stu-id="c091f-134">Handle the WM\_INPUTLANGCHANGEREQUEST message.</span></span>
    -   <span data-ttu-id="c091f-135">Suporte a editores de método de entrada, texto vertical e regras de quebra de linha nas edições do leste asiático.</span><span class="sxs-lookup"><span data-stu-id="c091f-135">Support input method editors, vertical text, and line-breaking rules in East Asian editions.</span></span>

<!-- -->

-   <span data-ttu-id="c091f-136">Compile todas as edições internacionais do programa de um conjunto de arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="c091f-136">Compile all international editions of the program from one set of source files.</span></span>
    -   <span data-ttu-id="c091f-137">Minimize ou elimine os mecanismos que exigem que o código seja recompilado para diferentes edições de idioma.</span><span class="sxs-lookup"><span data-stu-id="c091f-137">Minimize or eliminate mechanisms that require code to be recompiled for different language editions.</span></span>
    -   <span data-ttu-id="c091f-138">Armazene itens localizáveis, como cadeias de caracteres e ícones, em arquivos de recursos do Windows.</span><span class="sxs-lookup"><span data-stu-id="c091f-138">Store localizable items, such as strings and icons, in Windows resource files.</span></span>
    -   <span data-ttu-id="c091f-139">Armazene documentos em todas as edições de idioma usando o mesmo formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c091f-139">Store documents in all language editions using the same file format.</span></span>

<!-- -->

-   <span data-ttu-id="c091f-140">Dão suporte a conjuntos de caracteres diferentes, não apenas à página de código latino 1, número 1252.</span><span class="sxs-lookup"><span data-stu-id="c091f-140">Support different character sets, not just the Latin 1 code page, number 1252.</span></span>
    -   <span data-ttu-id="c091f-141">O programa dá suporte a ambientes de rede nos quais os computadores executam sistemas operacionais com páginas de código padrão diferentes.</span><span class="sxs-lookup"><span data-stu-id="c091f-141">Program supports network environments in which computers run operating systems with different default code pages.</span></span>
    -   <span data-ttu-id="c091f-142">Use GetCPInfoEx para recuperar intervalos de bytes potenciais para páginas de código do leste asiático.</span><span class="sxs-lookup"><span data-stu-id="c091f-142">Use GetCPInfoEx to retrieve lead-byte ranges for East Asian code pages.</span></span>
    -   <span data-ttu-id="c091f-143">Analisar caracteres de byte duplo no leste asiático – aplicativos de idioma, a menos que o código seja baseado em Unicode.</span><span class="sxs-lookup"><span data-stu-id="c091f-143">Parse double-byte characters in East Asian–language applications unless the code is based on Unicode.</span></span>
    -   <span data-ttu-id="c091f-144">Suporte a Unicode ou conversão entre Unicode e a página de código local.</span><span class="sxs-lookup"><span data-stu-id="c091f-144">Support Unicode or conversion between Unicode and the local code page.</span></span>
    -   <span data-ttu-id="c091f-145">Não presuma que todos os caracteres sejam de 8 bits ou de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c091f-145">Don't assume that all characters are 8-bit or 16-bit.</span></span>
    -   <span data-ttu-id="c091f-146">Use tipos de dados genéricos e protótipos de função genéricos.</span><span class="sxs-lookup"><span data-stu-id="c091f-146">Use generic data types and generic function prototypes.</span></span>
    -   <span data-ttu-id="c091f-147">Use a propriedade charset de fonte, que chama EnumFontFamiliesEx e a função de caixa de diálogo comum ChooseFont.</span><span class="sxs-lookup"><span data-stu-id="c091f-147">Use the font charset property, which calls EnumFontFamiliesEx and the ChooseFont common dialog function.</span></span>
    -   <span data-ttu-id="c091f-148">Exiba e imprima o texto usando as fontes apropriadas para a localidade.</span><span class="sxs-lookup"><span data-stu-id="c091f-148">Display and print text using the fonts that are appropriate for the locale.</span></span>

<!-- -->

-   <span data-ttu-id="c091f-149">Teste os recursos internacionais do programa.</span><span class="sxs-lookup"><span data-stu-id="c091f-149">Test the international features of the program.</span></span>
    -   <span data-ttu-id="c091f-150">O texto traduzido deve atender aos padrões de oradores nativos.</span><span class="sxs-lookup"><span data-stu-id="c091f-150">Translated text should meet the standards of native speakers.</span></span>
    -   <span data-ttu-id="c091f-151">As caixas de diálogo devem ser redimensionadas corretamente e o texto deve ser hifenizado adequadamente, quando idiomas diferentes são exibidos.</span><span class="sxs-lookup"><span data-stu-id="c091f-151">Dialog boxes should resize properly, and text should be hyphenated appropriately, when different languages are displayed.</span></span>
    -   <span data-ttu-id="c091f-152">Caixas de diálogo, barras de status, barras de ferramentas e menus devem caber na tela e ler legibly quando a exibição é definida em resoluções diferentes, para todos os idiomas traduzidos.</span><span class="sxs-lookup"><span data-stu-id="c091f-152">Dialog boxes, status bars, toolbars, and menus should fit on the screen and read legibly when the display is set at different resolutions, for all translated languages.</span></span>
    -   <span data-ttu-id="c091f-153">Os aceleradores de menu e caixa de diálogo devem ser exclusivos.</span><span class="sxs-lookup"><span data-stu-id="c091f-153">Menu and dialog-box accelerators should be unique.</span></span>
    -   <span data-ttu-id="c091f-154">Os usuários devem ser capazes de digitar caracteres de scripts não europeus em documentos, caixas de diálogo e nomes de texto.</span><span class="sxs-lookup"><span data-stu-id="c091f-154">Users should be able to type characters from non-European scripts into documents, dialog boxes, and filenames.</span></span>
    -   <span data-ttu-id="c091f-155">Os usuários devem ser capazes de recortar, colar, salvar e imprimir caracteres de scripts não europeus com êxito.</span><span class="sxs-lookup"><span data-stu-id="c091f-155">Users should be able to cut, paste, save, and print characters from non-European scripts successfully.</span></span>
    -   <span data-ttu-id="c091f-156">A classificação e a conversão de casos devem ser precisas para localidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="c091f-156">Sorting and case conversion should be accurate for different locales.</span></span>
    -   <span data-ttu-id="c091f-157">O aplicativo deve funcionar corretamente nas edições localizadas do Windows.</span><span class="sxs-lookup"><span data-stu-id="c091f-157">The application should work correctly on localized editions of Windows.</span></span>

 

 



