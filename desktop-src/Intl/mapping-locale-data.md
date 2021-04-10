---
description: O NLS inclui várias funções de API que seus aplicativos podem usar para mapear dados de localidade entre identificadores de localidade e nomes de localidade e listar localidades neutras.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Mapeando dados de localidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164835"
---
# <a name="mapping-locale-data"></a><span data-ttu-id="6f047-103">Mapeando dados de localidade</span><span class="sxs-lookup"><span data-stu-id="6f047-103">Mapping Locale Data</span></span>

<span data-ttu-id="6f047-104">O NLS inclui várias funções de API que seus aplicativos podem usar para mapear dados de localidade entre [identificadores de localidade](locale-identifiers.md) e [nomes de localidade](locale-names.md)e listar localidades neutras.</span><span class="sxs-lookup"><span data-stu-id="6f047-104">NLS includes a number of API functions that your applications can use to map locale data between [locale identifiers](locale-identifiers.md) and [locale names](locale-names.md), and list neutral locales.</span></span> <span data-ttu-id="6f047-105">Este tópico aborda o uso dessas funções no Windows Vista e posterior e em sistemas operacionais anteriores ao Windows Vista (às vezes chamados de "sistemas de nível inferior").</span><span class="sxs-lookup"><span data-stu-id="6f047-105">This topic discusses the use of these functions on Windows Vista and later and on pre-Windows Vista operating systems (sometimes called "downlevel systems").</span></span>

## <a name="map-locale-data-on-windows-vista-and-later"></a><span data-ttu-id="6f047-106">Mapear dados de localidade no Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="6f047-106">Map Locale Data on Windows Vista and Later</span></span>

<span data-ttu-id="6f047-107">O NLS fornece várias funções de mapeamento de localidade para uso por aplicativos que você desenvolve para executar no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="6f047-107">NLS provides several locale mapping functions for use by applications that you develop to run on Windows Vista and later.</span></span> <span data-ttu-id="6f047-108">Ele também inclui funções que seus aplicativos podem usar para enumerar localidades neutras.</span><span class="sxs-lookup"><span data-stu-id="6f047-108">It also includes functions that your applications can use to enumerate neutral locales.</span></span>

<span data-ttu-id="6f047-109">**Usar as funções de conversão padrão para mapeamento de dados**</span><span class="sxs-lookup"><span data-stu-id="6f047-109">**Use the Standard Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="6f047-110">Para mapear entre um nome de localidade e um identificador de localidade, seu aplicativo pode chamar a função [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) .</span><span class="sxs-lookup"><span data-stu-id="6f047-110">To map between a locale name and a locale identifier, your application can call the [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function.</span></span> <span data-ttu-id="6f047-111">O aplicativo usa [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) para mapear entre um identificador de localidade e um nome de localidade.</span><span class="sxs-lookup"><span data-stu-id="6f047-111">The application uses [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to map between a locale identifier and a locale name.</span></span>

<span data-ttu-id="6f047-112">**Listar localidades neutras**</span><span class="sxs-lookup"><span data-stu-id="6f047-112">**List Neutral Locales**</span></span>

<span data-ttu-id="6f047-113">Para enumerar localidades neutras para o Windows 7 e posterior, seu aplicativo pode chamar [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) com *dwFlags* definido como [**locale \_ NEUTRALDATA**](locale-neutraldata.md).</span><span class="sxs-lookup"><span data-stu-id="6f047-113">To enumerate neutral locales for Windows 7 and later, your application can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) with *dwFlags* set to [**LOCALE\_NEUTRALDATA**](locale-neutraldata.md).</span></span> <span data-ttu-id="6f047-114">Ele também pode usar [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) com *LCTYPE* definido como [**localidade \_ INEUTRAL**](locale-ineutral.md).</span><span class="sxs-lookup"><span data-stu-id="6f047-114">It can also use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with *LCType* set to [**LOCALE\_INEUTRAL**](locale-ineutral.md).</span></span>

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="6f047-115">Mapear dados de localidade em sistemas operacionais anteriores ao Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f047-115">Map Locale Data on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="6f047-116">O NLS inclui uma DLL (biblioteca de vínculo direto) a ser usada para aplicativos que você desenvolve para execução em sistemas operacionais anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6f047-116">NLS includes a direct-link library (DLL) to use for applications that you develop to run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="6f047-117">A DLL dá suporte às funções de conversão e listagem para mapeamento de dados.</span><span class="sxs-lookup"><span data-stu-id="6f047-117">The DLL supports both conversion and listing functions for data mapping.</span></span>

> [!Note]  
> <span data-ttu-id="6f047-118">Os aplicativos que só são executados no Windows Vista e posterior não devem usar o mapeamento de nível inferior ou as funções de listagem.</span><span class="sxs-lookup"><span data-stu-id="6f047-118">Applications that only run on Windows Vista and later should not use the downlevel mapping or listing functions.</span></span>

 

<span data-ttu-id="6f047-119">**Usar as funções de conversão de nível inferior para mapeamento de dados**</span><span class="sxs-lookup"><span data-stu-id="6f047-119">**Use the Downlevel Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="6f047-120">Seu aplicativo direcionado a um sistema de nível inferior pode chamar a função [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) para converter um identificador de localidade em um nome de localidade.</span><span class="sxs-lookup"><span data-stu-id="6f047-120">Your application targeted at a downlevel system can call the [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) function to convert a locale identifier to a locale name.</span></span> <span data-ttu-id="6f047-121">Se precisar converter um nome de localidade em um identificador de localidade, ele deverá chamar [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).</span><span class="sxs-lookup"><span data-stu-id="6f047-121">If it needs to convert a locale name to a locale identifier, it should call [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).</span></span>

<span data-ttu-id="6f047-122">**Usar as funções de listagem de nível inferior para enumerar localidades neutras**</span><span class="sxs-lookup"><span data-stu-id="6f047-122">**Use the Downlevel Listing Functions to Enumerate Neutral Locales**</span></span>

<span data-ttu-id="6f047-123">Seu aplicativo deve chamar o [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) para recuperar o identificador de localidade do pai para uma localidade.</span><span class="sxs-lookup"><span data-stu-id="6f047-123">Your application should call the [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) to retrieve the locale identifier of the parent for a locale.</span></span> <span data-ttu-id="6f047-124">Se o aplicativo precisar obter o nome da localidade do pai para a localidade, ele deverá chamar [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).</span><span class="sxs-lookup"><span data-stu-id="6f047-124">If the application needs to get the locale name of the parent for the locale, it should call [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f047-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6f047-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f047-126">Usando o suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="6f047-126">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="6f047-127">Identificadores de localidade</span><span class="sxs-lookup"><span data-stu-id="6f047-127">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="6f047-128">Nomes de localidade</span><span class="sxs-lookup"><span data-stu-id="6f047-128">Locale Names</span></span>](locale-names.md)
</dt> </dl>

 

 



