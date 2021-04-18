---
description: O termo &\# 0034; language&\# 0034; indica uma coleção de propriedades usadas em comunicação falada e escrita.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Localidades e idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767627"
---
# <a name="locales-and-languages"></a><span data-ttu-id="a2115-103">Localidades e idiomas</span><span class="sxs-lookup"><span data-stu-id="a2115-103">Locales and Languages</span></span>

<span data-ttu-id="a2115-104">O termo "Language" indica uma coleção de propriedades usadas em comunicação falada e escrita.</span><span class="sxs-lookup"><span data-stu-id="a2115-104">The term "language" indicates a collection of properties used in spoken and written communication.</span></span> <span data-ttu-id="a2115-105">Cada idioma tem um nome de idioma e um identificador de idioma que indicam a [página de código](code-pages.md) específica (ANSI, dos, Macintosh) usada para representar a [localização geográfica](table-of-geographical-locations.md) do idioma no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a2115-105">Each language has a language name and a language identifier that indicate the particular [code page](code-pages.md) (ANSI, DOS, Macintosh) used to represent the [geographical location](table-of-geographical-locations.md) for the language on the operating system.</span></span> <span data-ttu-id="a2115-106">Uma linguagem neutra é indicada por um nome como "en" para inglês.</span><span class="sxs-lookup"><span data-stu-id="a2115-106">A neutral language is indicated by a name such as "en" for English.</span></span> <span data-ttu-id="a2115-107">Uma linguagem mais específica geograficamente pode ser indicada por um nome que inclui informações de localidade e país/região.</span><span class="sxs-lookup"><span data-stu-id="a2115-107">A more geographically specific language can be indicated by a name that includes both locale and country/region information.</span></span> <span data-ttu-id="a2115-108">Por exemplo, a localidade inglês (Estados Unidos) tem o nome da linguagem "en-US".</span><span class="sxs-lookup"><span data-stu-id="a2115-108">For example, the locale English (United States) has the language name "en-US".</span></span>

<span data-ttu-id="a2115-109">Uma "localidade" é uma coleção de informações de preferência do usuário relacionadas à linguagem representada como uma lista de valores.</span><span class="sxs-lookup"><span data-stu-id="a2115-109">A "locale" is a collection of language-related user preference information represented as a list of values.</span></span> <span data-ttu-id="a2115-110">O Windows XP dá suporte a mais de 150 localidades, e o Windows Vista dá suporte a aproximadamente 200.</span><span class="sxs-lookup"><span data-stu-id="a2115-110">Windows XP supports more than 150 locales, and Windows Vista supports about 200.</span></span> <span data-ttu-id="a2115-111">Cada localidade é definida por um idioma e uma ordem de classificação e tem um nome de localidade e um identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="a2115-111">Each locale is defined by a language and a sort order, and has both a locale name and a locale identifier.</span></span> <span data-ttu-id="a2115-112">Um exemplo de um nome de localidade para alemão (Alemanha) é " \_ descatálogo de lista telefônica".</span><span class="sxs-lookup"><span data-stu-id="a2115-112">An example of a locale name for German (Germany) is "de-DE\_phonebook".</span></span>

<span data-ttu-id="a2115-113">Cada sistema operacional tem pelo menos uma localidade instalada e, muitas vezes, tem muitas localidades das quais o usuário pode selecionar.</span><span class="sxs-lookup"><span data-stu-id="a2115-113">Each operating system has at least one installed locale and often has many locales from which the user can select.</span></span> <span data-ttu-id="a2115-114">Cada localidade tem uma variedade de informações associadas a ele, além de seu nome e identificador.</span><span class="sxs-lookup"><span data-stu-id="a2115-114">Each locale has a variety of information associated with it, other than its name and identifier.</span></span> <span data-ttu-id="a2115-115">Os tipos de informações de localidade são descritos nas [constantes de informações de localidade](locale-information-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a2115-115">Locale information types are described in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="a2115-116">O sistema operacional atribui uma localidade a cada thread, inicialmente atribuindo a "localidade padrão do sistema", definida pelo [ \_ \_ padrão do sistema de localidade](locale-system-default.md).</span><span class="sxs-lookup"><span data-stu-id="a2115-116">The operating system assigns a locale to each thread, initially assigning the "system default locale," defined by [LOCALE\_SYSTEM\_DEFAULT](locale-system-default.md).</span></span> <span data-ttu-id="a2115-117">Essa localidade é definida quando o sistema operacional é instalado ou quando o usuário a seleciona usando a parte de opções regionais e de idiomas do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="a2115-117">This locale is set when the operating system is installed or when the user selects it using the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="a2115-118">Ao executar um thread em um processo que pertence ao usuário, o sistema operacional atribui a "localidade padrão do usuário" ao thread.</span><span class="sxs-lookup"><span data-stu-id="a2115-118">When running a thread in a process belonging to the user, the operating system assigns the "user default locale" to the thread.</span></span> <span data-ttu-id="a2115-119">Essa localidade é definida por [ \_ \_ padrão de usuário de localidade](locale-user-default.md).</span><span class="sxs-lookup"><span data-stu-id="a2115-119">This locale is defined by [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span> <span data-ttu-id="a2115-120">Um aplicativo pode substituir o padrão usando a função [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) para definir explicitamente a localidade para um thread.</span><span class="sxs-lookup"><span data-stu-id="a2115-120">An application can override either default by using the [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) function to explicitly set the locale for a thread.</span></span>

<span data-ttu-id="a2115-121">A implementação de um idioma requer uma localidade correspondente.</span><span class="sxs-lookup"><span data-stu-id="a2115-121">Implementation of a language requires a corresponding locale.</span></span> <span data-ttu-id="a2115-122">O sistema operacional implementa um idioma neutro, selecionando os dados para a localidade associada a uma versão específica do idioma, geralmente a localidade mais generalizada.</span><span class="sxs-lookup"><span data-stu-id="a2115-122">The operating system implements a neutral language by selecting the data for the locale associated with a specific version of the language, usually the most widespread locale.</span></span>

<span data-ttu-id="a2115-123">A partir do Windows Vista, é possível que uma linguagem específica corresponda a uma localidade suplementar, que é um tipo de localidade personalizada.</span><span class="sxs-lookup"><span data-stu-id="a2115-123">Starting with Windows Vista, it is possible for a particular language to correspond to a supplemental locale, which is a type of custom locale.</span></span> <span data-ttu-id="a2115-124">Como as localidades complementares compartilham um único identificador de localidade, seus aplicativos devem lidar com essas localidades e os idiomas correspondentes por nome, em vez de por identificador.</span><span class="sxs-lookup"><span data-stu-id="a2115-124">Since supplemental locales all share a single locale identifier, your applications should handle these locales and the corresponding languages by name instead of by identifier.</span></span>

<span data-ttu-id="a2115-125">Os conceitos de linguagem estão fortemente relacionados aos conceitos de localidade, mas os dois termos não são intercambiáveis.</span><span class="sxs-lookup"><span data-stu-id="a2115-125">Language concepts are closely related to locale concepts, but the two terms are not interchangeable.</span></span> <span data-ttu-id="a2115-126">Como regra geral, as funções relacionadas à [interface do usuário multilíngue](multilingual-user-interface.md) lidam com linguagens, enquanto as funções NLS agem sobre localidades.</span><span class="sxs-lookup"><span data-stu-id="a2115-126">As a general rule, functions related to the [Multilingual User Interface](multilingual-user-interface.md) deal with languages, while the NLS functions act upon locales.</span></span>

<span data-ttu-id="a2115-127">Os tópicos a seguir são abordados nesta seção:</span><span class="sxs-lookup"><span data-stu-id="a2115-127">The following topics are covered in this section:</span></span>

-   [<span data-ttu-id="a2115-128">Localidades personalizadas</span><span class="sxs-lookup"><span data-stu-id="a2115-128">Custom Locales</span></span>](custom-locales.md)
-   [<span data-ttu-id="a2115-129">Identificadores de idioma</span><span class="sxs-lookup"><span data-stu-id="a2115-129">Language Identifiers</span></span>](language-identifiers.md)
-   [<span data-ttu-id="a2115-130">Nomes de idiomas</span><span class="sxs-lookup"><span data-stu-id="a2115-130">Language Names</span></span>](language-names.md)
-   [<span data-ttu-id="a2115-131">Identificadores de localidade</span><span class="sxs-lookup"><span data-stu-id="a2115-131">Locale Identifiers</span></span>](locale-identifiers.md)
-   [<span data-ttu-id="a2115-132">Nomes de localidade</span><span class="sxs-lookup"><span data-stu-id="a2115-132">Locale Names</span></span>](locale-names.md)
-   [<span data-ttu-id="a2115-133">Pseudo-locais</span><span class="sxs-lookup"><span data-stu-id="a2115-133">Pseudo-Locales</span></span>](pseudo-locales.md)

## <a name="related-topics"></a><span data-ttu-id="a2115-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2115-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2115-135">Sobre o suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="a2115-135">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="a2115-136">Páginas de código</span><span class="sxs-lookup"><span data-stu-id="a2115-136">Code Pages</span></span>](code-pages.md)
</dt> <dt>

[<span data-ttu-id="a2115-137">Constantes de informações de localidade</span><span class="sxs-lookup"><span data-stu-id="a2115-137">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="a2115-138">Interface do Usuário Multilíngue</span><span class="sxs-lookup"><span data-stu-id="a2115-138">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="a2115-139">Tabela de localizações geográficas</span><span class="sxs-lookup"><span data-stu-id="a2115-139">Table of Geographical Locations</span></span>](table-of-geographical-locations.md)
</dt> <dt>

[<span data-ttu-id="a2115-140">Gerenciamento de idioma da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="a2115-140">User Interface Language Management</span></span>](user-interface-language-management.md)
</dt> <dt>

[<span data-ttu-id="a2115-141">**SetThreadLocale**</span><span class="sxs-lookup"><span data-stu-id="a2115-141">**SetThreadLocale**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



