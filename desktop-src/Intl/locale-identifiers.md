---
description: Cada localidade tem um identificador exclusivo, um valor de 32 bits que consiste em um identificador de idioma e um identificador de ordem de classificação.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Identificadores de localidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767631"
---
# <a name="locale-identifiers"></a><span data-ttu-id="c0b0b-103">Identificadores de localidade</span><span class="sxs-lookup"><span data-stu-id="c0b0b-103">Locale Identifiers</span></span>

<span data-ttu-id="c0b0b-104">Cada [localidade](locales-and-languages.md) tem um identificador exclusivo, um valor de 32 bits que consiste em um [identificador de idioma](language-identifiers.md) e um [identificador de ordem de classificação](sort-order-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="c0b0b-104">Each [locale](locales-and-languages.md) has a unique identifier, a 32-bit value that consists of a [language identifier](language-identifiers.md) and a [sort order identifier](sort-order-identifiers.md).</span></span> <span data-ttu-id="c0b0b-105">O identificador de localidade é uma abreviação numérica internacional padrão e tem os componentes necessários para identificar exclusivamente uma das localidades definidas pelo sistema operacional instaladas.</span><span class="sxs-lookup"><span data-stu-id="c0b0b-105">The locale identifier is a standard international numeric abbreviation and has the components necessary to uniquely identify one of the installed operating system-defined locales.</span></span> <span data-ttu-id="c0b0b-106">O NLS dá suporte a identificadores de localidade predefinidos e identificadores personalizados.</span><span class="sxs-lookup"><span data-stu-id="c0b0b-106">NLS supports both predefined locale identifiers and custom identifiers.</span></span>

> [!Note]  
> <span data-ttu-id="c0b0b-107">Os nomes de localidade podem ser usados com funções introduzidas no Windows Vista que usam um [nome de localidade](locale-names.md) como parâmetro, em vez de um identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="c0b0b-107">Locale names can be used with functions introduced in Windows Vista that take a [locale name](locale-names.md) as a parameter, instead of a locale identifier.</span></span> <span data-ttu-id="c0b0b-108">Para obter mais informações, consulte [chamar as funções de "nome de localidade"](calling-the--locale-name--functions.md).</span><span class="sxs-lookup"><span data-stu-id="c0b0b-108">For more information, see [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md).</span></span> <span data-ttu-id="c0b0b-109">O uso de nomes de localidade em vez de identificadores de localidade é sempre preferível.</span><span class="sxs-lookup"><span data-stu-id="c0b0b-109">Use of locale names instead of locale identifiers is always preferable.</span></span>

 

<span data-ttu-id="c0b0b-110">A ilustração a seguir mostra o formato dos bits em um identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="c0b0b-110">The following illustration shows the format of the bits in a locale identifier.</span></span>

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a><span data-ttu-id="c0b0b-111">Identificadores de localidade predefinidos</span><span class="sxs-lookup"><span data-stu-id="c0b0b-111">Predefined Locale Identifiers</span></span>

<span data-ttu-id="c0b0b-112">Os identificadores de localidade predefinidos com suporte pelo NLS são definidos na [referência da API NLS (suporte ao idioma nacional)](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span><span class="sxs-lookup"><span data-stu-id="c0b0b-112">The predefined locale identifiers supported by NLS are defined in the [National Language Support (NLS) API Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span></span>

<span data-ttu-id="c0b0b-113">O NLS usa as seguintes constantes de informações de localidade para representar identificadores de localidade.</span><span class="sxs-lookup"><span data-stu-id="c0b0b-113">NLS uses the following locale information constants to represent locale identifiers.</span></span>

-   <span data-ttu-id="c0b0b-114">[Localidade \_ do SLANGUAGE](locale-slanguage.md) ou [localidade \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span><span class="sxs-lookup"><span data-stu-id="c0b0b-114">[LOCALE\_SLANGUAGE](locale-slanguage.md) or [LOCALE\_SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span></span>
-   [<span data-ttu-id="c0b0b-115">SNAME de localidade \_</span><span class="sxs-lookup"><span data-stu-id="c0b0b-115">LOCALE\_SNAME</span></span>](locale-sname.md)
-   [<span data-ttu-id="c0b0b-116">SSCRIPTS de localidade \_</span><span class="sxs-lookup"><span data-stu-id="c0b0b-116">LOCALE\_SSCRIPTS</span></span>](locale-sscripts.md)
-   [<span data-ttu-id="c0b0b-117">IDEFAULTANSICODEPAGE de localidade \_</span><span class="sxs-lookup"><span data-stu-id="c0b0b-117">LOCALE\_IDEFAULTANSICODEPAGE</span></span>](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a><span data-ttu-id="c0b0b-118">Identificadores de localidade personalizados</span><span class="sxs-lookup"><span data-stu-id="c0b0b-118">Custom Locale Identifiers</span></span>

<span data-ttu-id="c0b0b-119">**Windows Vista:** O NLS dá suporte aos identificadores de localidade personalizados representados pelas seguintes constantes de informações de localidade.</span><span class="sxs-lookup"><span data-stu-id="c0b0b-119">**Windows Vista:** NLS supports the custom locale identifiers represented by the following locale information constants.</span></span>

-   [<span data-ttu-id="c0b0b-120">\_padrão personalizado de localidade \_</span><span class="sxs-lookup"><span data-stu-id="c0b0b-120">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="c0b0b-121">\_ \_ padrão da interface do usuário personalizada de localidade \_</span><span class="sxs-lookup"><span data-stu-id="c0b0b-121">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="c0b0b-122">LOCALIDADE \_ personalizada \_ não especificada</span><span class="sxs-lookup"><span data-stu-id="c0b0b-122">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

## <a name="building-a-locale"></a><span data-ttu-id="c0b0b-123">Criando uma localidade</span><span class="sxs-lookup"><span data-stu-id="c0b0b-123">Building a Locale</span></span>

<span data-ttu-id="c0b0b-124">Você pode usar o utilitário do Locale Builder fornecido pelo NLS para criar localidades.</span><span class="sxs-lookup"><span data-stu-id="c0b0b-124">You can use the Locale Builder utility provided by NLS to build locales.</span></span> <span data-ttu-id="c0b0b-125">Para obter mais informações, consulte [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).</span><span class="sxs-lookup"><span data-stu-id="c0b0b-125">For more information, see [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).</span></span>

<span data-ttu-id="c0b0b-126">Seu aplicativo pode construir um identificador de localidade usando a macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) .</span><span class="sxs-lookup"><span data-stu-id="c0b0b-126">Your application can construct a locale identifier using the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro.</span></span> <span data-ttu-id="c0b0b-127">Como alternativa, ele pode usar um dos identificadores padrão correspondentes às constantes listadas abaixo.</span><span class="sxs-lookup"><span data-stu-id="c0b0b-127">Alternatively it can use one of the default identifiers corresponding to the constants listed below.</span></span>

-   [<span data-ttu-id="c0b0b-128">LOCALIDADE \_ invariável</span><span class="sxs-lookup"><span data-stu-id="c0b0b-128">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="c0b0b-129">\_padrão do sistema de localidade \_</span><span class="sxs-lookup"><span data-stu-id="c0b0b-129">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="c0b0b-130">\_padrão de usuário de localidade \_</span><span class="sxs-lookup"><span data-stu-id="c0b0b-130">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a><span data-ttu-id="c0b0b-131">Recuperação de identificadores de localidade</span><span class="sxs-lookup"><span data-stu-id="c0b0b-131">Retrieval of Locale Identifiers</span></span>

<span data-ttu-id="c0b0b-132">Um aplicativo pode recuperar os identificadores de localidade atuais usando as funções [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) e [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) .</span><span class="sxs-lookup"><span data-stu-id="c0b0b-132">An application can retrieve the current locale identifiers by using the [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) and [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) functions.</span></span> <span data-ttu-id="c0b0b-133">Cada thread pode definir e recuperar sua própria localidade com [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) e [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span><span class="sxs-lookup"><span data-stu-id="c0b0b-133">Each thread can set and retrieve its own locale with [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) and [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0b0b-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0b0b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0b0b-135">Localidades e idiomas</span><span class="sxs-lookup"><span data-stu-id="c0b0b-135">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="c0b0b-136">Identificadores de idioma</span><span class="sxs-lookup"><span data-stu-id="c0b0b-136">Language Identifiers</span></span>](language-identifiers.md)
</dt> <dt>

[<span data-ttu-id="c0b0b-137">Nomes de localidade</span><span class="sxs-lookup"><span data-stu-id="c0b0b-137">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="c0b0b-138">Identificadores de ordem de classificação</span><span class="sxs-lookup"><span data-stu-id="c0b0b-138">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="c0b0b-139">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="c0b0b-139">**MAKELCID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
