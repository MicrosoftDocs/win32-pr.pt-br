---
description: No Windows Vista e posterior, você pode usar pseudo-locais para testar a possibilidade de localização de aplicativos. Este tópico inclui procedimentos para usar pseudodispositivos.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Usando pseudo-locais para teste de possibilidade de localização
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: f8c6b435b85a5bef98eff9bf76681096779433e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811025"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a><span data-ttu-id="13872-104">Usando pseudo-locais para teste de possibilidade de localização</span><span class="sxs-lookup"><span data-stu-id="13872-104">Using pseudo-locales for localizability testing</span></span>

<span data-ttu-id="13872-105">As [pseudovariáveis](pseudo-locales.md) são internas do Windows Vista e posteriores, para que você possa acessá-las por meio de APIs NLS (suporte ao idioma nacional).</span><span class="sxs-lookup"><span data-stu-id="13872-105">[Pseudo-locales](pseudo-locales.md) are built in to Windows Vista and later, so that you can access them via National Language Support (NLS) APIs.</span></span> <span data-ttu-id="13872-106">Você pode usar pseudo-locais para testar a [possibilidade de localização](/windows/uwp/design/globalizing/globalizing-portal) de seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="13872-106">You can use pseudo-locales to test the [localizability](/windows/uwp/design/globalizing/globalizing-portal) of your applications.</span></span> <span data-ttu-id="13872-107">Este tópico inclui procedimentos para usar pseudodispositivos.</span><span class="sxs-lookup"><span data-stu-id="13872-107">This topic includes procedures for using pseudo-codes.</span></span>

> [!NOTE]
> <span data-ttu-id="13872-108">Uma tarefa que precisa de consideração especial quando se trata de pseudo-locais é enumerando-as; seja em seu código ou na parte das opções regionais e de idioma do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="13872-108">One task that needs special consideration when it comes to pseudo-locales is enumerating them; whether in your code, or in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="13872-109">Mais informações sobre isso posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="13872-109">More on that later in this topic.</span></span>

<span data-ttu-id="13872-110">Os nomes dos pseudo locais são "qps-ploc", "qps-ploca" e "qps-plocm".</span><span class="sxs-lookup"><span data-stu-id="13872-110">The names of the pseudo-locales are "qps-ploc", "qps-ploca", and "qps-plocm".</span></span> <span data-ttu-id="13872-111">A partir do Windows 10, a pseudo-localidade "qps-Latn-x-sh" também está disponível.</span><span class="sxs-lookup"><span data-stu-id="13872-111">As of Windows 10, the pseudo-locale "qps-Latn-x-sh" is also available.</span></span>

## <a name="retrieve-information-about-pseudo-locales"></a><span data-ttu-id="13872-112">Recuperar informações sobre pseudo-locais</span><span class="sxs-lookup"><span data-stu-id="13872-112">Retrieve information about pseudo-locales</span></span>

<span data-ttu-id="13872-113">Você pode usar [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) para recuperar informações sobre uma pseudo-localidade.</span><span class="sxs-lookup"><span data-stu-id="13872-113">You can use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) to retrieve information about a pseudo-locale.</span></span> <span data-ttu-id="13872-114">Passe para a função o nome da pseudo-localidade específica (consulte a lista de nomes acima).</span><span class="sxs-lookup"><span data-stu-id="13872-114">Pass into the function the name of the particular pseudo-locale (see the list of names above).</span></span> <span data-ttu-id="13872-115">Por exemplo, "qps-plocm" para a pseudo-localidade espelhada.</span><span class="sxs-lookup"><span data-stu-id="13872-115">For example, "qps-plocm" for the mirrored pseudo-locale.</span></span>

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a><span data-ttu-id="13872-116">Usar LocaleNameToLCID com pseudo-localidades</span><span class="sxs-lookup"><span data-stu-id="13872-116">Use LocaleNameToLCID with pseudo-locales</span></span>

<span data-ttu-id="13872-117">Você pode chamar a função de mapeamento NLS [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) com o nome de uma pseudo-localidade.</span><span class="sxs-lookup"><span data-stu-id="13872-117">You can call the NLS mapping function [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) with the name of a pseudo-locale.</span></span>

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a><span data-ttu-id="13872-118">Habilitar pseudo-locais para enumeração</span><span class="sxs-lookup"><span data-stu-id="13872-118">Enable pseudo-locales for enumeration</span></span>

<span data-ttu-id="13872-119">Em seu aplicativo, você pode chamar [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) para enumerar as localidades que o sistema reconhece.</span><span class="sxs-lookup"><span data-stu-id="13872-119">In your application, you can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) to enumerate the locales that the system recognizes.</span></span> <span data-ttu-id="13872-120">A parte das opções regionais e de idioma do painel de controle também chama **EnumSystemLocalesEx** para criar a lista de localidades que ele exibe.</span><span class="sxs-lookup"><span data-stu-id="13872-120">The regional and language options portion of the Control Panel also calls **EnumSystemLocalesEx** to build the list of locales that it displays.</span></span> <span data-ttu-id="13872-121">No entanto, por padrão, as quatro pseudo localidades listadas acima não são reconhecidas pelo sistema, portanto, não serão retornadas por **EnumSystemLocalesEx**.</span><span class="sxs-lookup"><span data-stu-id="13872-121">However, by default, the four pseudo-locales listed above are not recognized by the system, so they won't be returned by **EnumSystemLocalesEx**.</span></span> <span data-ttu-id="13872-122">Para sistemas do Windows Vista até e incluindo o Windows 10, versão 1709, a solução é habilitar pseudo localidades adicionando chaves ao registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="13872-122">For systems from Windows Vista up to and including Windows 10, version 1709, the solution is to enable pseudo-locales by adding keys to the Windows Registry.</span></span>

<span data-ttu-id="13872-123">As edições são feitas sob a chave do \_ \_ controle do \\ sistema local \\ CurrentControlSet \\ Control \\ NLS para os idiomas instalados no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="13872-123">The edits are made under the HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Nls key for the languages installed on the operating system.</span></span> <span data-ttu-id="13872-124">Você pode fazer essas configurações para habilitar as pseudo-localidades.</span><span class="sxs-lookup"><span data-stu-id="13872-124">You can make these settings to enable the pseudo-locales.</span></span> <span data-ttu-id="13872-125">Cada chave mostrada abaixo é o LCID hexadecimal correspondente à pseudo-localidade que está sendo habilitada.</span><span class="sxs-lookup"><span data-stu-id="13872-125">Each key shown below is the hexadecimal LCID corresponding to the pseudo-locale being enabled.</span></span> <span data-ttu-id="13872-126">Cada valor é do tipo cadeia de caracteres (REG \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="13872-126">Each value is of type string (REG\_SZ).</span></span>

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

<span data-ttu-id="13872-127">Para o Windows 10, versão 1803, a edição do registro do Windows como esse não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="13872-127">For Windows 10, version 1803, editing the Windows Registry like this has no effect.</span></span> <span data-ttu-id="13872-128">Mas você ainda pode chamar as APIs NLS sem enumeração com os nomes das pseudovariáveis (consulte os exemplos de código acima) para preencher a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="13872-128">But you can still call the non-enumerating NLS APIs with the names of the pseudo-locales (see the code examples above) to populate your user interface (UI).</span></span>

## <a name="related-topics"></a><span data-ttu-id="13872-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13872-129">Related topics</span></span>

* [<span data-ttu-id="13872-130">Usando o suporte ao idioma nacional</span><span class="sxs-lookup"><span data-stu-id="13872-130">Using National Language Support</span></span>](using-national-language-support.md)
* [<span data-ttu-id="13872-131">Pseudo-locais</span><span class="sxs-lookup"><span data-stu-id="13872-131">Pseudo-Locales</span></span>](pseudo-locales.md)
* [<span data-ttu-id="13872-132">EnumSystemLocalesEx</span><span class="sxs-lookup"><span data-stu-id="13872-132">EnumSystemLocalesEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [<span data-ttu-id="13872-133">GetLocaleInfoEx</span><span class="sxs-lookup"><span data-stu-id="13872-133">GetLocaleInfoEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [<span data-ttu-id="13872-134">LocaleNameToLCID</span><span class="sxs-lookup"><span data-stu-id="13872-134">LocaleNameToLCID</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
