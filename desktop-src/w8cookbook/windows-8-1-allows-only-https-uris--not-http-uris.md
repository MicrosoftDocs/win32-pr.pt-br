---
title: URIs em Windows 8.1
description: Windows 8.1 permite apenas URIs HTTPS, não URIs http
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366554"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a><span data-ttu-id="d6c02-103">Windows 8.1 permite apenas URIs HTTPS, não URIs http</span><span class="sxs-lookup"><span data-stu-id="d6c02-103">Windows 8.1 allows only https URIs, not http URIs</span></span>

## <a name="platforms"></a><span data-ttu-id="d6c02-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="d6c02-104">Platforms</span></span>

<dl> <span data-ttu-id="d6c02-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d6c02-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="d6c02-106">Servidores-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d6c02-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="d6c02-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6c02-107">Description</span></span>

<span data-ttu-id="d6c02-108">Embora os aplicativos criados para o Windows 8 possam incluir URIs http e HTTPS em seus URIs de conteúdo de aplicativo, os aplicativos criados para Windows 8.1 podem incluir somente URIs HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d6c02-108">While apps built for Windows 8 can include http and https URIs in their application content URIs, apps built for Windows 8.1 may include only https URIs.</span></span>

<span data-ttu-id="d6c02-109">A única exceção é para ContentUriRules dinâmicos que são especificados no arquivo de AppxManifest.xml do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6c02-109">The only exception is for dynamic ContentUriRules that are specified in the app’s AppxManifest.xml file.</span></span> <span data-ttu-id="d6c02-110">Com o Dynamic ContentUriRules, os aplicativos podem acessar domínios ou recursos de rede adicionais que são fornecidos pelo administrador, como URIs de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="d6c02-110">With dynamic ContentUriRules, apps can access additional domains or network resources that are provided by the admin, such as Group Policy URIs.</span></span> <span data-ttu-id="d6c02-111">No entanto, os ContentUriRules dinâmicos só estarão disponíveis para aplicativos da Windows Store se atenderem a estas condições:</span><span class="sxs-lookup"><span data-stu-id="d6c02-111">However, dynamic ContentUriRules are only available to Windows Store apps if they meet these conditions:</span></span>

-   <span data-ttu-id="d6c02-112">O Política de Grupo está habilitado</span><span class="sxs-lookup"><span data-stu-id="d6c02-112">The Group Policy is enabled</span></span>
-   <span data-ttu-id="d6c02-113">O pacote especificou o recurso enterpriseAuthentication</span><span class="sxs-lookup"><span data-stu-id="d6c02-113">The package has specified the enterpriseAuthentication capability</span></span>
-   <span data-ttu-id="d6c02-114">O OSMaxVersionTested do pacote é Windows 8.1 ou superior</span><span class="sxs-lookup"><span data-stu-id="d6c02-114">The package’s OSMaxVersionTested is Windows 8.1 or greater</span></span>

<span data-ttu-id="d6c02-115">As novas restrições no Windows 8.1 fazem parte das restrições de segurança aprimoradas para proteger ainda mais a plataforma.</span><span class="sxs-lookup"><span data-stu-id="d6c02-115">The new restrictions in Windows 8.1 are part of enhanced security restrictions to further protect the platform.</span></span>

## <a name="manifestations"></a><span data-ttu-id="d6c02-116">Manifestações</span><span class="sxs-lookup"><span data-stu-id="d6c02-116">Manifestations</span></span>

<span data-ttu-id="d6c02-117">Ao executar um aplicativo criado para o Windows 8 em Windows 8.1, o uso de URIs http no [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) é permitido.</span><span class="sxs-lookup"><span data-stu-id="d6c02-117">When running an app built for Windows 8 on Windows 8.1, the use of http URIs in the [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) is allowed.</span></span>

## <a name="mitigations"></a><span data-ttu-id="d6c02-118">Atenuações</span><span class="sxs-lookup"><span data-stu-id="d6c02-118">Mitigations</span></span>

<span data-ttu-id="d6c02-119">Recomendamos que os desenvolvedores de WWA mudem de [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) para o controle [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-MS-WebView>).</span><span class="sxs-lookup"><span data-stu-id="d6c02-119">We recommend that WWA developers switch from [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) to the [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) control (<x-ms-webview>).</span></span> <span data-ttu-id="d6c02-120">No entanto, se você precisar de suporte para AppCache, IndexedDB, geolocalização ou acesso de área de transferência programático, será necessário continuar usando o</span><span class="sxs-lookup"><span data-stu-id="d6c02-120">However, if you need support for AppCache, IndexedDB, geolocation, or programmatic clipboard access, you will need to continue using</span></span> <iframe> <span data-ttu-id="d6c02-121">para Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="d6c02-121">for Windows 8.1.</span></span>

<span data-ttu-id="d6c02-122">Uso contínuo de</span><span class="sxs-lookup"><span data-stu-id="d6c02-122">Continued usage of</span></span> <iframe> <span data-ttu-id="d6c02-123">para o conteúdo remoto, será necessário uma nova entrada no ApplicationContentUriRules para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6c02-123">for remote content will require a new entry in the ApplicationContentUriRules for the app.</span></span> <span data-ttu-id="d6c02-124">Os aplicativos com WebView exigem novas entradas no ApplicationContentUriRules se o conteúdo da Web precisar invocar Window. external. Notify para gerar um evento [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="d6c02-124">Apps with WebView require new entries in the ApplicationContentUriRules if the web content needs to invoke window.external.notify for generating a [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) event.</span></span> <span data-ttu-id="d6c02-125">Se você não tiver o Visual Studio, poderá atualizar o manifesto do aplicativo adicionando o seguinte XML, incluindo curingas para subdomínios (por exemplo, https:// \* . Microsoft.com):</span><span class="sxs-lookup"><span data-stu-id="d6c02-125">If you do not have Visual Studio, you can update the app manifest by adding the following XML, including wildcards for subdomains (e.g. https://\*.microsoft.com):</span></span>


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a><span data-ttu-id="d6c02-126">Recursos</span><span class="sxs-lookup"><span data-stu-id="d6c02-126">Resources</span></span>

-   [<span data-ttu-id="d6c02-127">ApplicationContentUriRules</span><span class="sxs-lookup"><span data-stu-id="d6c02-127">ApplicationContentUriRules</span></span>](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<span data-ttu-id="d6c02-128"><iframe>objeto de elemento \| <iframe></span><span class="sxs-lookup"><span data-stu-id="d6c02-128"><iframe> element \| <iframe> object</span></span>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [<span data-ttu-id="d6c02-129">Classe WebView</span><span class="sxs-lookup"><span data-stu-id="d6c02-129">Webview class</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [<span data-ttu-id="d6c02-130">Evento WebView. ScriptNotify</span><span class="sxs-lookup"><span data-stu-id="d6c02-130">WebView.ScriptNotify event</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 