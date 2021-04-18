---
description: 'Windows Vista e posterior: o NLS define várias pseudovariáveis para uso, além das localidades existentes do Windows.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780136"
---
# <a name="pseudo-locales"></a><span data-ttu-id="22c73-103">Pseudo-Locales</span><span class="sxs-lookup"><span data-stu-id="22c73-103">Pseudo-Locales</span></span>

<span data-ttu-id="22c73-104">**Windows Vista e posterior:** O NLS define várias pseudovariáveis para uso, além das localidades existentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="22c73-104">**Windows Vista and later:** NLS defines several pseudo-locales for use in addition to the existing Windows locales.</span></span> <span data-ttu-id="22c73-105">Use essas pseudo-localidades para testar a localização de seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="22c73-105">Use these pseudo-locales for testing the localization of your applications.</span></span> <span data-ttu-id="22c73-106">Para obter detalhes de implementação, consulte [usando Pseudo-Locales para teste de localização](using-pseudo-locales-for-localization-testing.md).</span><span class="sxs-lookup"><span data-stu-id="22c73-106">For implementation details, see [Using Pseudo-Locales for Localization Testing](using-pseudo-locales-for-localization-testing.md).</span></span>

## <a name="supported-pseudo-locales"></a><span data-ttu-id="22c73-107">Pseudo-Locales com suporte</span><span class="sxs-lookup"><span data-stu-id="22c73-107">Supported Pseudo-Locales</span></span>

<span data-ttu-id="22c73-108">As pseudo-localidades com suporte pelo NLS são:</span><span class="sxs-lookup"><span data-stu-id="22c73-108">The pseudo-locales supported by NLS are:</span></span>

-   <span data-ttu-id="22c73-109">Pseudo-localidade base</span><span class="sxs-lookup"><span data-stu-id="22c73-109">Base pseudo-locale</span></span>
-   <span data-ttu-id="22c73-110">Pseudo-localidade espelhada (da direita para a esquerda)</span><span class="sxs-lookup"><span data-stu-id="22c73-110">Mirrored (right-to-left) pseudo-locale</span></span>
-   <span data-ttu-id="22c73-111">Leste Asiático – pseudo-localidade do idioma</span><span class="sxs-lookup"><span data-stu-id="22c73-111">East Asian-language pseudo-locale</span></span>

<span data-ttu-id="22c73-112">Escolha a pseudo-localidade específica a ser usada com base em suas atribuições de página de código e nas cadeias de caracteres para localização, por exemplo, nomes de mês, nomes de dias.</span><span class="sxs-lookup"><span data-stu-id="22c73-112">Choose the particular pseudo-locale to use based on its code page assignments and the strings for localization, for example, month names, day names.</span></span> <span data-ttu-id="22c73-113">Os dados de cada pseudo-localidade incluem não apenas as páginas de código relevantes e as cadeias de caracteres de dia e mês para localização, mas também dados para vários outros casos de teste para NLS.</span><span class="sxs-lookup"><span data-stu-id="22c73-113">Data for each pseudo-locale includes not only relevant code pages and day and month strings for localization, but also data for several other test cases for NLS.</span></span> <span data-ttu-id="22c73-114">Os casos de teste examinam os seguintes tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="22c73-114">The test cases examine the following types of data:</span></span>

-   <span data-ttu-id="22c73-115">[identificadores de localidade](locale-identifiers.md)de 9 bits.</span><span class="sxs-lookup"><span data-stu-id="22c73-115">9-bit [locale identifiers](locale-identifiers.md).</span></span> <span data-ttu-id="22c73-116">As pseudo-locais oferecem uma boa oportunidade para testar a operação de identificadores de localidade de 9 bits.</span><span class="sxs-lookup"><span data-stu-id="22c73-116">Pseudo-locales provide a good opportunity to test the operation of 9-bit locale identifiers.</span></span>
-   <span data-ttu-id="22c73-117">Cadeias de caracteres de idiomas que devem usar fontes pequenas.</span><span class="sxs-lookup"><span data-stu-id="22c73-117">Strings from languages that must use small fonts.</span></span> <span data-ttu-id="22c73-118">Devido a limitações na GDI (Graphics Device Interface), a fonte da interface do usuário para alguns idiomas é menor do que o ideal.</span><span class="sxs-lookup"><span data-stu-id="22c73-118">Because of limitations in the graphics device interface (GDI), the user interface font for some languages is smaller than optimal.</span></span> <span data-ttu-id="22c73-119">As pseudovariáveis incluem várias cadeias de caracteres dessas linguagens, combinadas com cadeias de caracteres de linguagens com mais manipulação de fontes padrão.</span><span class="sxs-lookup"><span data-stu-id="22c73-119">Pseudo-locales include several strings from these languages, combined with strings from languages with more standard font handling.</span></span> <span data-ttu-id="22c73-120">Você pode usar essas cadeias de caracteres no teste para determinar como uma fonte limitada por GDI é renderizada.</span><span class="sxs-lookup"><span data-stu-id="22c73-120">You can use these strings in testing to determine how a GDI-limited font renders.</span></span>
-   <span data-ttu-id="22c73-121">Comprimentos de cadeia de caracteres incomuns.</span><span class="sxs-lookup"><span data-stu-id="22c73-121">Unusual string lengths.</span></span> <span data-ttu-id="22c73-122">Algumas constantes de informações de localidade, por exemplo, a [localidade \_ SLIST](locale-slist.md) e a [localidade \_ ICURRENCY](locale-icurrency.md), têm limites convencionais no tamanho da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="22c73-122">Some locale information constants, for example, [LOCALE\_SLIST](locale-slist.md) and [LOCALE\_ICURRENCY](locale-icurrency.md), have conventional limits on string size.</span></span> <span data-ttu-id="22c73-123">As pseudo-localidades dão suporte ao exame de comprimentos de cadeia de caracteres variados.</span><span class="sxs-lookup"><span data-stu-id="22c73-123">The pseudo-locales support the examination of varied string lengths.</span></span>
-   <span data-ttu-id="22c73-124">Classificações alternativas.</span><span class="sxs-lookup"><span data-stu-id="22c73-124">Alternate sorts.</span></span> <span data-ttu-id="22c73-125">As pseudovariáveis podem ser usadas para testar a funcionalidade de classificação alternativa quando o [identificador da ordem de classificação](sort-order-identifiers.md) alternativa difere do identificador de ordem de classificação base que geralmente está associado à localidade.</span><span class="sxs-lookup"><span data-stu-id="22c73-125">Pseudo-locales can be used to test alternate sort functionality when the alternate [sort order identifier](sort-order-identifiers.md) differs from the base sort order identifier that is usually associated with the locale.</span></span>

## <a name="pseudo-locale-names-and-identifiers"></a><span data-ttu-id="22c73-126">Nomes e identificadores de pseudo-localidade</span><span class="sxs-lookup"><span data-stu-id="22c73-126">Pseudo-locale Names and Identifiers</span></span>

<span data-ttu-id="22c73-127">As pseudo-localidades têm [nomes de localidade](locale-names.md) que são escolhidos do espaço de uso privado para evitar conflitos com possíveis cadeias de caracteres introduzidas nos padrões organização internacional de normalização (iso) 639 e ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="22c73-127">The pseudo-locales have [locale names](locale-names.md) that are chosen from the private use space to avoid conflict with possible strings introduced into the International Organization for Standardization (ISO) 639 and ISO 3166 standards.</span></span> <span data-ttu-id="22c73-128">Cada pseudo-localidade também tem seu próprio identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="22c73-128">Each pseudo-locale also has its own locale identifier.</span></span> <span data-ttu-id="22c73-129">A tabela a seguir fornece os nomes e identificadores para os pseudo locais definidos.</span><span class="sxs-lookup"><span data-stu-id="22c73-129">The following table provides the names and identifiers for the defined pseudo-locales.</span></span>



| <span data-ttu-id="22c73-130">Pseudo-localidade</span><span class="sxs-lookup"><span data-stu-id="22c73-130">Pseudo-locale</span></span>       | <span data-ttu-id="22c73-131">Nome da localidade</span><span class="sxs-lookup"><span data-stu-id="22c73-131">Locale name</span></span> | <span data-ttu-id="22c73-132">Identificador de localidade</span><span class="sxs-lookup"><span data-stu-id="22c73-132">Locale identifier</span></span> |
|---------------------|-------------|-------------------|
| <span data-ttu-id="22c73-133">Base</span><span class="sxs-lookup"><span data-stu-id="22c73-133">Base</span></span>                | <span data-ttu-id="22c73-134">qps-ploc</span><span class="sxs-lookup"><span data-stu-id="22c73-134">qps-ploc</span></span>    | <span data-ttu-id="22c73-135">0501</span><span class="sxs-lookup"><span data-stu-id="22c73-135">0501</span></span>              |
| <span data-ttu-id="22c73-136">Espelhado</span><span class="sxs-lookup"><span data-stu-id="22c73-136">Mirrored</span></span>            | <span data-ttu-id="22c73-137">qps-plocm</span><span class="sxs-lookup"><span data-stu-id="22c73-137">qps-plocm</span></span>   | <span data-ttu-id="22c73-138">09ff</span><span class="sxs-lookup"><span data-stu-id="22c73-138">09ff</span></span>              |
| <span data-ttu-id="22c73-139">Leste Asiático-idioma</span><span class="sxs-lookup"><span data-stu-id="22c73-139">East Asian-language</span></span> | <span data-ttu-id="22c73-140">qps-ploca</span><span class="sxs-lookup"><span data-stu-id="22c73-140">qps-ploca</span></span>   | <span data-ttu-id="22c73-141">05fe</span><span class="sxs-lookup"><span data-stu-id="22c73-141">05fe</span></span>              |



 

## <a name="example"></a><span data-ttu-id="22c73-142">Exemplo</span><span class="sxs-lookup"><span data-stu-id="22c73-142">Example</span></span>

<span data-ttu-id="22c73-143">O exemplo a seguir mostra o texto exibido para uma pseudo-localidade base:</span><span class="sxs-lookup"><span data-stu-id="22c73-143">The following example shows text displayed for a base pseudo-locale:</span></span>

<span data-ttu-id="22c73-144">\[Шěđлеśđαỳ!!! \] , 8 ōf \[ Μäŕςћ!! \] ōf 2006</span><span class="sxs-lookup"><span data-stu-id="22c73-144">\[Шěđлеśđαỳ !!!\], 8 ōf \[Μäŕςћ !!\] ōf 2006</span></span>

## <a name="related-topics"></a><span data-ttu-id="22c73-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22c73-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c73-146">Localidades e idiomas</span><span class="sxs-lookup"><span data-stu-id="22c73-146">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="22c73-147">Identificadores de localidade</span><span class="sxs-lookup"><span data-stu-id="22c73-147">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="22c73-148">Nomes de localidade</span><span class="sxs-lookup"><span data-stu-id="22c73-148">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="22c73-149">Identificadores de ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="22c73-149">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="22c73-150">Usando Pseudo-Locales para teste de localização</span><span class="sxs-lookup"><span data-stu-id="22c73-150">Using Pseudo-Locales for Localization Testing</span></span>](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



