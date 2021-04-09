---
description: O ICU (componentes internacionais para Unicode) é um conjunto maduro e amplamente utilizado de APIs de globalização de código aberto.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: ICU (Componentes Internacionais para Unicode)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00a72885b37efebf8de0d5eb60a22fe01dfba4f
ms.sourcegitcommit: 176ef0a00690f849282cb48464c97f6526a82113
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/19/2021
ms.locfileid: "103923000"
---
# <a name="international-components-for-unicode-icu"></a><span data-ttu-id="cc4bf-103">ICU (Componentes Internacionais para Unicode)</span><span class="sxs-lookup"><span data-stu-id="cc4bf-103">International Components for Unicode (ICU)</span></span>

<span data-ttu-id="cc4bf-104">O ICU (componentes internacionais para Unicode) é um conjunto maduro e amplamente utilizado de APIs de globalização de código aberto.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-104">International Components for Unicode (ICU) is a mature, widely used set of open-source globalization APIs.</span></span> <span data-ttu-id="cc4bf-105">O ICU utiliza o CLDR (repositório de dados de localidade comum) de Unicode como sua biblioteca de dados, fornecendo suporte à globalização para aplicativos de software.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-105">ICU utilizes Unicode's vast Common Locale Data Repository (CLDR) as its data library, providing globalization support for software applications.</span></span> <span data-ttu-id="cc4bf-106">O ICU é amplamente portátil e dá aos aplicativos os mesmos resultados em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-106">ICU is widely portable and gives applications the same results across on all platforms.</span></span>

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a><span data-ttu-id="cc4bf-107">Destaques dos serviços de API de globalização fornecidos pelo ICU</span><span class="sxs-lookup"><span data-stu-id="cc4bf-107">Highlights of the Globalization API services provided by ICU</span></span>

-   <span data-ttu-id="cc4bf-108">**Conversão de página de código**: converter dados de texto de ou para Unicode e praticamente qualquer outro conjunto de caracteres ou codificação.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-108">**Code Page Conversion**: Convert text data to or from Unicode and nearly any other character set or encoding.</span></span> <span data-ttu-id="cc4bf-109">As tabelas de conversão do ICU são baseadas nos dados de conjunto de caracteres coletados pela IBM ao longo de muitas décadas, e é a mais completa disponível em qualquer lugar.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-109">ICU's conversion tables are based on charset data collected by IBM over the course of many decades, and is the most complete available anywhere.</span></span>
-   <span data-ttu-id="cc4bf-110">**Agrupamento**: comparar cadeias de caracteres de acordo com as convenções e os padrões de um idioma, região ou país específico.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-110">**Collation**: Compare strings according to the conventions and standards of a particular language, region or country.</span></span> <span data-ttu-id="cc4bf-111">O agrupamento do ICU é baseado no algoritmo de agrupamento Unicode mais regras de comparação específicas de localidade do CLDR.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-111">ICU's collation is based on the Unicode Collation Algorithm plus locale-specific comparison rules from CLDR.</span></span>
-   <span data-ttu-id="cc4bf-112">**Formatação**: formatar números, datas, horas e valores de moeda de acordo com as convenções de uma localidade escolhida.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-112">**Formatting**: Format numbers, dates, times and currency amounts according the conventions of a chosen locale.</span></span> <span data-ttu-id="cc4bf-113">Isso inclui a tradução de nomes de mês e dia para o idioma selecionado, a escolha de abreviaturas apropriadas, a ordenação de campos corretamente, etc. Esses dados também vêm do repositório de dados de localidade comum.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-113">This includes translating month and day names into the selected language, choosing appropriate abbreviations, ordering fields correctly, etc. This data also comes from the Common Locale Data Repository.</span></span>
-   <span data-ttu-id="cc4bf-114">**Cálculos de tempo**: vários tipos de calendários são fornecidos além do gregoriano tradicional.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-114">**Time Calculations**: Multiple types of calendars are provided beyond the traditional Gregorian.</span></span> <span data-ttu-id="cc4bf-115">Um conjunto completo de APIs de cálculo de fuso horário é fornecido.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-115">A thorough set of time zone calculation APIs are provided.</span></span>
-   <span data-ttu-id="cc4bf-116">**Suporte a Unicode**: o ICU rastreia com precisão o padrão Unicode, fornecendo acesso fácil a todas as muitas propriedades de caractere Unicode, normalização Unicode, dobramento de caso e outras operações fundamentais, conforme especificado pelo [padrão Unicode](https://www.unicode.org/).</span><span class="sxs-lookup"><span data-stu-id="cc4bf-116">**Unicode Support**: ICU closely tracks the Unicode standard, providing easy access to all of the many Unicode character properties, Unicode Normalization, Case Folding, and other fundamental operations as specified by the [Unicode Standard](https://www.unicode.org/).</span></span>
-   <span data-ttu-id="cc4bf-117">**Expressão regular**: as expressões regulares do ICU oferecem suporte total ao Unicode e, ao mesmo tempo, fornecem um desempenho muito competitivo.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-117">**Regular Expression**: ICU's regular expressions fully support Unicode while providing very competitive performance.</span></span>
-   <span data-ttu-id="cc4bf-118">**Bidi**: suporte para tratamento de texto que contém uma mistura de dados da esquerda para a direita (inglês) e da direita para a esquerda (árabe ou Hebraico).</span><span class="sxs-lookup"><span data-stu-id="cc4bf-118">**Bidi**: Support for handling text containing a mixture of left to right (English) and right to left (Arabic or Hebrew) data.</span></span>

<span data-ttu-id="cc4bf-119">Para obter mais informações, você pode visitar o site do ICU: <http://site.icu-project.org/></span><span class="sxs-lookup"><span data-stu-id="cc4bf-119">For more information, you can visit the ICU website: <http://site.icu-project.org/></span></span>

## <a name="overview"></a><span data-ttu-id="cc4bf-120">Visão geral</span><span class="sxs-lookup"><span data-stu-id="cc4bf-120">Overview</span></span>

<span data-ttu-id="cc4bf-121">Na atualização do Windows 10 para criadores, o ICU foi integrado ao Windows, tornando as APIs C e os dados publicamente acessíveis.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-121">In Windows 10 Creators Update, ICU was integrated into Windows, making the C APIs and data publicly accessible.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc4bf-122">A versão do ICU no Windows expõe apenas as APIs C.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-122">The version of ICU in Windows only exposes the C APIs.</span></span> <span data-ttu-id="cc4bf-123">Ele não expõe nenhuma das APIs do C++.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-123">It does not expose any of the C++ APIs.</span></span> <span data-ttu-id="cc4bf-124">Infelizmente, é impossível expor as APIs do C++ devido à falta de uma ABI estável em C++.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-124">Unfortunately, it is impossible to ever expose the C++ APIs due to the lack of a stable ABI in C++.</span></span>

<span data-ttu-id="cc4bf-125">Para obter a documentação sobre as APIs do ICU C, consulte a página de documentação oficial do ICU aqui: <http://icu-project.org/apiref/icu4c/index.html#Module></span><span class="sxs-lookup"><span data-stu-id="cc4bf-125">For documentation on the ICU C APIs, please refer to the official ICU documentation page here: <http://icu-project.org/apiref/icu4c/index.html#Module></span></span>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a><span data-ttu-id="cc4bf-126">Histórico de alterações na biblioteca do ICU no Windows</span><span class="sxs-lookup"><span data-stu-id="cc4bf-126">History of changes to the ICU library in Windows</span></span>

### <a name="version-1703-creators-update"></a><span data-ttu-id="cc4bf-127">Versão 1703 (atualização para criadores)</span><span class="sxs-lookup"><span data-stu-id="cc4bf-127">Version 1703 (Creators Update)</span></span>
<span data-ttu-id="cc4bf-128">A biblioteca ICU foi adicionada primeiro ao sistema operacional Windows 10 nesta versão.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-128">The ICU library was first added to the Windows 10 OS in this version.</span></span>
<span data-ttu-id="cc4bf-129">Ele foi adicionado como:</span><span class="sxs-lookup"><span data-stu-id="cc4bf-129">It was added as:</span></span>
- <span data-ttu-id="cc4bf-130">Duas DLLs do sistema:</span><span class="sxs-lookup"><span data-stu-id="cc4bf-130">Two system DLLs:</span></span>
    -   <span data-ttu-id="cc4bf-131">**icuuc.dll** (esta é a biblioteca "comum" do ICU)</span><span class="sxs-lookup"><span data-stu-id="cc4bf-131">**icuuc.dll** (this is the ICU "common" library)</span></span>
    -   <span data-ttu-id="cc4bf-132">**icuin.dll** (esta é a biblioteca de "i18n" do ICU)</span><span class="sxs-lookup"><span data-stu-id="cc4bf-132">**icuin.dll** (this is the ICU "i18n" library)</span></span>
- <span data-ttu-id="cc4bf-133">Dois arquivos de cabeçalho no SDK do Windows 10:</span><span class="sxs-lookup"><span data-stu-id="cc4bf-133">Two header files in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="cc4bf-134">**icucommon. h**</span><span class="sxs-lookup"><span data-stu-id="cc4bf-134">**icucommon.h**</span></span>
    -   <span data-ttu-id="cc4bf-135">**icui18n. h**</span><span class="sxs-lookup"><span data-stu-id="cc4bf-135">**icui18n.h**</span></span>
- <span data-ttu-id="cc4bf-136">Dois bibliotecas de importação no SDK do Windows 10:</span><span class="sxs-lookup"><span data-stu-id="cc4bf-136">Two import libs in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="cc4bf-137">**icuuc. lib**</span><span class="sxs-lookup"><span data-stu-id="cc4bf-137">**icuuc.lib**</span></span>
    -   <span data-ttu-id="cc4bf-138">**icuin. lib**</span><span class="sxs-lookup"><span data-stu-id="cc4bf-138">**icuin.lib**</span></span>

### <a name="version-1709-fall-creators-update"></a><span data-ttu-id="cc4bf-139">Versão 1709 (atualização para criadores de outono)</span><span class="sxs-lookup"><span data-stu-id="cc4bf-139">Version 1709 (Fall Creators Update)</span></span>
<span data-ttu-id="cc4bf-140">Um arquivo de cabeçalho combinado, **ICU. h**, foi adicionado, que contém o conteúdo de ambos os arquivos de cabeçalho acima (icucommon. h e icui18n. h) e também altera o tipo de `UCHAR` para `char16_t` .</span><span class="sxs-lookup"><span data-stu-id="cc4bf-140">A combined header file, **icu.h**, was added, which contains the contents of both header files above (icucommon.h and icui18n.h), and also changes the type of `UCHAR` to `char16_t`.</span></span>

### <a name="version-1903-may-2019-update"></a><span data-ttu-id="cc4bf-141">Versão 1903 (atualização de maio de 2019)</span><span class="sxs-lookup"><span data-stu-id="cc4bf-141">Version 1903 (May 2019 Update)</span></span>
<span data-ttu-id="cc4bf-142">Uma nova DLL combinada, **icu.dll**, foi adicionada, que contém as bibliotecas "comum" e "i18n".</span><span class="sxs-lookup"><span data-stu-id="cc4bf-142">A new combined DLL, **icu.dll**, was added, which contains both the "common" and "i18n" libraries.</span></span> <span data-ttu-id="cc4bf-143">Além disso, uma nova biblioteca de importação foi adicionada ao SDK do Windows 10: **ICU. lib**.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-143">Also, a new import library was added to the Windows 10 SDK: **icu.lib**.</span></span>

<span data-ttu-id="cc4bf-144">No futuro, nenhuma nova API será adicionada aos cabeçalhos antigos (icucommon. h e icui18n. h) ou ao bibliotecas de importação antigo (icuuc. lib e icuin. lib).</span><span class="sxs-lookup"><span data-stu-id="cc4bf-144">Going forward, no new APIs will be added to the old headers (icucommon.h and icui18n.h) or to the old import libs (icuuc.lib and icuin.lib).</span></span> <span data-ttu-id="cc4bf-145">Novas APIs serão adicionadas somente ao cabeçalho combinado (ICU. h) e à lib de importação combinada (ICU. lib).</span><span class="sxs-lookup"><span data-stu-id="cc4bf-145">New APIs will only be added to the combined header (icu.h) and the combined import lib (icu.lib).</span></span>

## <a name="getting-started"></a><span data-ttu-id="cc4bf-146">Introdução</span><span class="sxs-lookup"><span data-stu-id="cc4bf-146">Getting Started</span></span>

<span data-ttu-id="cc4bf-147">Há três etapas principais a serem seguidas: (atualização do Windows 10 para criadores ou superior)</span><span class="sxs-lookup"><span data-stu-id="cc4bf-147">There are three main steps to follow: (Windows 10 Creators Update or higher)</span></span>

<dl>

1. <span data-ttu-id="cc4bf-148">Seu aplicativo precisa ter como destino o Windows 10 versão 1703 (Creators Update) ou superior.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-148">Your application needs to target Windows 10 Version 1703 (Creators Update) or higher.</span></span>

2. <span data-ttu-id="cc4bf-149">Adicionar nos cabeçalhos:</span><span class="sxs-lookup"><span data-stu-id="cc4bf-149">Add in the headers:</span></span>

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   <span data-ttu-id="cc4bf-150">No Windows 10 versão 1709 e superior, você deve incluir o cabeçalho combinado em seu lugar:</span><span class="sxs-lookup"><span data-stu-id="cc4bf-150">On Windows 10 Version 1709 and above, you should include the combined header instead:</span></span>

   ``` syntax
   #include <icu.h>
   ```
  
3. <span data-ttu-id="cc4bf-151">Link para as duas bibliotecas:</span><span class="sxs-lookup"><span data-stu-id="cc4bf-151">Link to the two libraries:</span></span>

   -   <span data-ttu-id="cc4bf-152">icuuc. lib</span><span class="sxs-lookup"><span data-stu-id="cc4bf-152">icuuc.lib</span></span>
   -   <span data-ttu-id="cc4bf-153">icuin. lib</span><span class="sxs-lookup"><span data-stu-id="cc4bf-153">icuin.lib</span></span>

   <span data-ttu-id="cc4bf-154">No Windows 10 versão 1903 e superior, você deve usar a biblioteca combinada:</span><span class="sxs-lookup"><span data-stu-id="cc4bf-154">On Windows 10 Version 1903 and above, you should use the combined library instead:</span></span>

   -   <span data-ttu-id="cc4bf-155">ICU. lib</span><span class="sxs-lookup"><span data-stu-id="cc4bf-155">icu.lib</span></span>

</dl>

<span data-ttu-id="cc4bf-156">Em seguida, você pode chamar qualquer API do ICU C dessas bibliotecas que desejar.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-156">Then, you can call whatever ICU C API from these libraries you want.</span></span> <span data-ttu-id="cc4bf-157">(Nenhuma API C++ é exposta.)</span><span class="sxs-lookup"><span data-stu-id="cc4bf-157">(No C++ APIs are exposed.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc4bf-158">Se você estiver usando as bibliotecas de importação herdadas, icuuc. lib e icuin. lib, verifique se elas estão listadas antes das bibliotecas de abrangência, como onecoreuap. lib ou WindowsApp. lib, na configuração do vinculador de dependências adicionais (consulte a imagem abaixo).</span><span class="sxs-lookup"><span data-stu-id="cc4bf-158">If you are using the legacy import libraries, icuuc.lib and icuin.lib, ensure they're listed before the umbrella libraries, like onecoreuap.lib or WindowsApp.lib, in the Additional Dependencies Linker setting (see the image below).</span></span> <span data-ttu-id="cc4bf-159">Caso contrário, o vinculador será vinculado a ICU. lib, o que resultará em uma tentativa de carregar icu.dll durante o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-159">Otherwise, the linker will link to icu.lib, which will result in an attempt to load icu.dll during run time.</span></span> <span data-ttu-id="cc4bf-160">Essa DLL está presente apenas começando com a versão 1903.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-160">That DLL is present only starting with version 1903.</span></span> <span data-ttu-id="cc4bf-161">Portanto, se um usuário atualizar o SDK do Windows 10 em um computador Windows anterior à versão 1903, o aplicativo não será carregado e executado.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-161">So, if a user upgrades the Windows 10 SDK on a pre-version 1903 Windows machine, the app will fail to load and run.</span></span> <span data-ttu-id="cc4bf-162">Para obter um histórico das bibliotecas ICU no Windows, consulte [histórico de alterações na biblioteca do ICU no Windows](#history-of-changes-to-the-icu-library-in-windows).</span><span class="sxs-lookup"><span data-stu-id="cc4bf-162">For a history of the ICU libraries in Windows, see [History of changes to the ICU library in Windows](#history-of-changes-to-the-icu-library-in-windows).</span></span>

![exemplo de ICU](images/icu-example.png)

> [!Note]  
>
> - <span data-ttu-id="cc4bf-164">Esta é a configuração para "todas as plataformas".</span><span class="sxs-lookup"><span data-stu-id="cc4bf-164">This is the configuration for “All Platforms”.</span></span>
> - <span data-ttu-id="cc4bf-165">Para que os aplicativos Win32 usem o ICU, eles precisam chamar [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) primeiro.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-165">For Win32 apps to use ICU, they need to call [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) first.</span></span>
> - <span data-ttu-id="cc4bf-166">Nem todos os dados retornados por APIs do ICU serão alinhados com o sistema operacional Windows, pois esse trabalho de alinhamento ainda está em andamento.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-166">Not all data returned by ICU APIs will align with the Windows OS, as this alignment work is still in progress.</span></span> 

## <a name="icu-example-app"></a><span data-ttu-id="cc4bf-167">Aplicativo de exemplo do ICU</span><span class="sxs-lookup"><span data-stu-id="cc4bf-167">ICU Example App</span></span>

### <a name="example-code-snippet"></a><span data-ttu-id="cc4bf-168">Trecho de código de exemplo</span><span class="sxs-lookup"><span data-stu-id="cc4bf-168">Example code snippet</span></span>

<span data-ttu-id="cc4bf-169">Veja a seguir um exemplo que ilustra o uso de APIs do ICU de dentro de um aplicativo UWP do C++.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-169">The following is an example illustrating the use of ICU APIs from within a C++ UWP application.</span></span> <span data-ttu-id="cc4bf-170">(Não se destina a ser um aplicativo autônomo completo, em vez disso, é apenas um exemplo de chamada de um método ICU.)</span><span class="sxs-lookup"><span data-stu-id="cc4bf-170">(It is not intended to be a full stand-alone application, rather it is just an example of calling an ICU method.)</span></span>

<span data-ttu-id="cc4bf-171">O exemplo pequeno a seguir pressupõe que há métodos **ErrorMessage** e **OutputMessage** que geram as cadeias de caracteres para o usuário de alguma maneira.</span><span class="sxs-lookup"><span data-stu-id="cc4bf-171">The following small example assumes that there are methods **ErrorMessage** and **OutputMessage** that output the strings to the user in some manner.</span></span>

``` syntax
// On Windows 10 Creators Update, include the following two headers. With Windows 10 Fall Creators Update and later, you can just include the single header <icu.h>.
#include <icucommon.h>
#include <icui18n.h>

void FormatDateTimeICU()
{
    UErrorCode status = U_ZERO_ERROR;

    // Create a ICU date formatter, using only the 'short date' style format.
    UDateFormat* dateFormatter = udat_open(UDAT_NONE, UDAT_SHORT, nullptr, nullptr, -1, nullptr, 0, &status);

    if (U_FAILURE(status))
    {
        ErrorMessage(L"Failed to create date formatter.");
        return;
    }

    // Get the current date and time.
    UDate currentDateTime = ucal_getNow();

    int32_t stringSize = 0;
    
    // Determine how large the formatted string from ICU would be.
    stringSize = udat_format(dateFormatter, currentDateTime, nullptr, 0, nullptr, &status);

    if (status == U_BUFFER_OVERFLOW_ERROR)
    {
        status = U_ZERO_ERROR;
        // Allocate space for the formatted string.
        auto dateString = std::make_unique<UChar[]>(stringSize + 1);

        // Format the date time into the string.
        udat_format(dateFormatter, currentDateTime, dateString.get(), stringSize + 1, nullptr, &status);

        if (U_FAILURE(status))
        {
            ErrorMessage(L"Failed to format the date time.");
            return;
        }

        // Output the formatted date time.
        OutputMessage(dateString.get());
    }
    else
    {
        ErrorMessage(L"An error occured while trying to determine the size of the formatted date time.");
        return;
    }

    // We need to close the ICU date formatter.
    udat_close(dateFormatter);
}
```

 

 



