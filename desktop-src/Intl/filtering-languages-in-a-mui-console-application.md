---
description: Um aplicativo de console do MUI pode dar suporte a configurações do sistema ou configurações específicas do aplicativo para seus idiomas de interface do usuário. Este tópico discute a filtragem de idiomas para esse tipo de aplicativo.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtrando linguagens em um aplicativo de console do MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d484835af211f59cc559f8e1cd0dd414af13a8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828581"
---
# <a name="filtering-languages-in-a-mui-console-application"></a><span data-ttu-id="60705-104">Filtrando linguagens em um aplicativo de console do MUI</span><span class="sxs-lookup"><span data-stu-id="60705-104">Filtering Languages in a MUI Console Application</span></span>

<span data-ttu-id="60705-105">Um aplicativo de console do MUI pode dar suporte a configurações do sistema ou configurações específicas do aplicativo para seus idiomas de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="60705-105">A MUI console application can support either system settings or application-specific settings for its user interface languages.</span></span> <span data-ttu-id="60705-106">Este tópico discute a filtragem de idiomas para esse tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60705-106">This topic discusses the filtering of languages for this type of application.</span></span>

## <a name="limit-the-languages-to-display"></a><span data-ttu-id="60705-107">Limitar os idiomas a serem exibidos</span><span class="sxs-lookup"><span data-stu-id="60705-107">Limit the Languages to Display</span></span>

<span data-ttu-id="60705-108">Ao contrário de uma janela gráfica, o console do Windows não pode exibir [scripts complexos](uniscribe-glossary.md), como árabe, Hebraico, persa, híndi, Urdu, tailandês e muitos outros.</span><span class="sxs-lookup"><span data-stu-id="60705-108">Unlike a graphical window, the Windows console cannot display [complex scripts](uniscribe-glossary.md), such as Arabic, Hebrew, Persian, Hindi, Urdu, Thai, and many others.</span></span> <span data-ttu-id="60705-109">Portanto, muitos idiomas de interface do usuário não podem ser exibidos pelo console do em nenhuma circunstância.</span><span class="sxs-lookup"><span data-stu-id="60705-109">Therefore, many user interface languages cannot be displayed by the console under any circumstances.</span></span>

<span data-ttu-id="60705-110">O console do pode exibir somente caracteres da [página de código OEM](code-pages.md) única associada ao idioma atual para aplicativos não Unicode.</span><span class="sxs-lookup"><span data-stu-id="60705-110">The console can display only characters from the single [OEM code page](code-pages.md) associated with the current language for non-Unicode applications.</span></span> <span data-ttu-id="60705-111">Para cada página de código OEM, o console do usa uma fonte específica, e isso pode não fornecer cobertura completa para essa página de código.</span><span class="sxs-lookup"><span data-stu-id="60705-111">For each OEM code page, the console uses a particular font, and this might not provide full coverage for that code page.</span></span>

<span data-ttu-id="60705-112">Essas limitações relacionadas ao console reduzem o número de idiomas de interface do usuário que o console do pode exibir em um determinado computador.</span><span class="sxs-lookup"><span data-stu-id="60705-112">These console-related limitations reduce the number of user interface languages that the console can display on a particular computer.</span></span> <span data-ttu-id="60705-113">Por exemplo, se o idioma atual para aplicativos não-Unicode for japonês e o usuário tentar exibir o texto em alemão no console, os caracteres com trema não serão exibidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="60705-113">For example, if the current language for non-Unicode applications is Japanese and the user tries to display German text in the console, characters with umlauts do not display correctly.</span></span> <span data-ttu-id="60705-114">Se o idioma atual para aplicativos não-Unicode for alemão e o usuário quiser exibir texto em japonês no console, os resultados serão muito piores, renderizando o texto quase incompreensível.</span><span class="sxs-lookup"><span data-stu-id="60705-114">If the current language for non-Unicode applications is German and the user wants to display Japanese text in the console, the results are much worse, rendering the text almost incomprehensible.</span></span>

> [!Note]  
> <span data-ttu-id="60705-115">Ao fornecer suporte ao console para seus aplicativos MUI, lembre-se de que o console do fornece apenas suporte limitado para [editores de método de entrada](input-method-manager.md).</span><span class="sxs-lookup"><span data-stu-id="60705-115">When providing console support for your MUI applications, remember that the console provides only limited support for [input method editors](input-method-manager.md).</span></span>

 

## <a name="set-the-language-for-console-output"></a><span data-ttu-id="60705-116">Definir o idioma da saída do console</span><span class="sxs-lookup"><span data-stu-id="60705-116">Set the Language for Console Output</span></span>

<span data-ttu-id="60705-117">No Windows Vista e posterior, um aplicativo de console define o idioma para dar suporte à exibição do console chamando [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="60705-117">On Windows Vista and later, a console application sets the language to support the console display by calling [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span> <span data-ttu-id="60705-118">Nesta chamada, o aplicativo passa o \_ filtro do console \_ do MUI no parâmetro *dwFlags* e **nulo** para *pwszLanguagesBuffer*.</span><span class="sxs-lookup"><span data-stu-id="60705-118">In this call, the application passes MUI\_CONSOLE\_FILTER in the *dwFlags* parameter and **NULL** for *pwszLanguagesBuffer*.</span></span> <span data-ttu-id="60705-119">Uma alternativa é chamar [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) com um identificador de idioma de 0.</span><span class="sxs-lookup"><span data-stu-id="60705-119">An alternative is to call [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span> <span data-ttu-id="60705-120">Essa configuração faz com que a função selecione o idioma que melhor dá suporte à exibição do console.</span><span class="sxs-lookup"><span data-stu-id="60705-120">This setting causes the function to select the language that best supports the console display.</span></span>

<span data-ttu-id="60705-121">No Windows XP, o aplicativo só pode definir o idioma da saída do console chamando [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) com um identificador de idioma 0.</span><span class="sxs-lookup"><span data-stu-id="60705-121">On Windows XP, the application can only set the language for console output by calling [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60705-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60705-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60705-123">Definindo preferências de idioma do aplicativo</span><span class="sxs-lookup"><span data-stu-id="60705-123">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
</dt> </dl>

 

 
