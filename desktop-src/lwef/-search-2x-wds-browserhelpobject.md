---
title: Chamando o WDS de páginas da Web
description: Você pode chamar o Microsoft Windows Desktop Search (WDS) de qualquer página da Web criada ou mantida usando o BHO (objeto auxiliar do navegador) e o Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "104007220"
---
# <a name="calling-wds-from-web-pages"></a><span data-ttu-id="cdda1-103">Chamando o WDS de páginas da Web</span><span class="sxs-lookup"><span data-stu-id="cdda1-103">Calling WDS from Web Pages</span></span>

> [!NOTE]
> <span data-ttu-id="cdda1-104">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cdda1-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cdda1-105">Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="cdda1-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="cdda1-106">Você pode chamar o Microsoft Windows Desktop Search (WDS) de qualquer página da Web criada ou mantida usando o BHO (objeto auxiliar do navegador) e o Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="cdda1-106">You can call Microsoft Windows Desktop Search (WDS) from any webpage you create or maintain using the Browser Helper Object (BHO) and Windows Internet Explorer.</span></span> <span data-ttu-id="cdda1-107">Você pode ver como isso funciona na página da Web do MSN.</span><span class="sxs-lookup"><span data-stu-id="cdda1-107">You can see how this works on the MSN webpage.</span></span> <span data-ttu-id="cdda1-108">Acima da caixa de pesquisa no https://www.msn.com há vários tipos de pesquisa: Web, notícias, imagens, área de trabalho, Encarta e local.</span><span class="sxs-lookup"><span data-stu-id="cdda1-108">Above the search box on https://www.msn.com are several search types: Web, News, Images, Desktop, Encarta, and Local.</span></span> <span data-ttu-id="cdda1-109">Se você clicar em área de trabalho, os parâmetros de pesquisa serão passados para o Windows Desktop Search, que pesquisará o catálogo e exibirá os resultados na interface do usuário do WDS.</span><span class="sxs-lookup"><span data-stu-id="cdda1-109">If you click Desktop, the search parameters are passed to Windows Desktop Search, which searches the catalog and displays results in the WDS user interface.</span></span> <span data-ttu-id="cdda1-110">Para que os usuários iniciem uma pesquisa de desktop de suas páginas da Web, o WDSBHO deve ser instalado e habilitado em seus sistemas, suas páginas da Web devem ser registradas com o WDS como uma URL permitida e você deve criar um link para passar a consulta User-enetered para o WDS.</span><span class="sxs-lookup"><span data-stu-id="cdda1-110">For users to start a desktop search from your webpage(s), the WDSBHO must be installed and enabled on their systems, your webpage(s) must be registered with WDS as an allowed URL, and you must create a link to pass the user-enetered query to WDS.</span></span>

## <a name="enabling-the-wds-browser-help-object"></a><span data-ttu-id="cdda1-111">Habilitando o objeto de ajuda do navegador WDS</span><span class="sxs-lookup"><span data-stu-id="cdda1-111">Enabling the WDS Browser Help Object</span></span>

<span data-ttu-id="cdda1-112">O BHO é instalado e habilitado no Internet Explorer por padrão quando você instala o WDS, mas você pode verificar facilmente se ele não foi desabilitado ou desinstalado.</span><span class="sxs-lookup"><span data-stu-id="cdda1-112">The BHO is installed and enabled within Internet Explorer by default when you install WDS, but you can easily verify that it hasn't been disabled or uninstalled.</span></span> <span data-ttu-id="cdda1-113">No sistema de um usuário, abra o Internet Explorer, selecione **Opções da Internet** no menu **ferramentas** , clique na guia **programas** e, em seguida, clique em **gerenciar** Complementos.</span><span class="sxs-lookup"><span data-stu-id="cdda1-113">On a user's system, open Internet Explorer , select **Internet Options** from the **Tools** menu, click the **Programs** tab, and then click **Manage Add-Ons**.</span></span> <span data-ttu-id="cdda1-114">Na lista de Complementos, procure a classe dsWebAllowBHO e verifique se ela está habilitada.</span><span class="sxs-lookup"><span data-stu-id="cdda1-114">In your list of add-ons, look for the dsWebAllowBHO Class and make sure it is enabled.</span></span> <span data-ttu-id="cdda1-115">Quando o BHO estiver desabilitado, o WDS continuará a funcionar normalmente; no entanto, você não poderá pesquisar na área de trabalho de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="cdda1-115">When the BHO is disabled, WDS will continue to work normally; however, you will not be able to search the desktop from a webpage.</span></span>

<span data-ttu-id="cdda1-116">As duas opções a seguir para permitir uma pesquisa na área de trabalho executarão a pesquisa localmente com o aplicativo de pesquisa registrado.</span><span class="sxs-lookup"><span data-stu-id="cdda1-116">Both of the following options for allowing a desktop search will execute the search locally with the registered search application.</span></span>

## <a name="registering-web-page-urls"></a><span data-ttu-id="cdda1-117">Registrando URLs de página da Web</span><span class="sxs-lookup"><span data-stu-id="cdda1-117">Registering Web Page URLs</span></span>

<span data-ttu-id="cdda1-118">O registro inclui uma lista de URLs de domínio "permitidas" das quais o WDS pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="cdda1-118">The Registry includes a list of "allowed" domain URLs from which WDS can be called.</span></span> <span data-ttu-id="cdda1-119">Para incluir suas páginas da Web, você precisa listar suas URLs de domínio como REG \_ sz no registro da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cdda1-119">To include your webpage(s), you need to list your domain URL(s) as REG\_SZ in the Registry as follows:</span></span>

<span data-ttu-id="cdda1-120">**HKEY \_ Software do \_ computador local** \\  \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **permitido**\\*<number>* = <domainURL></span><span class="sxs-lookup"><span data-stu-id="cdda1-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows Desktop Search**\\**DSW**\\**Allowed**\\*<number>* = <domainURL></span></span>

<span data-ttu-id="cdda1-121">Em que **<number>** é numerada sequencialmente e **<domainURL>** é a URL da página da Web que você deseja permitir que o WDS pesquise.</span><span class="sxs-lookup"><span data-stu-id="cdda1-121">Where **<number>** is sequentially numbered, and **<domainURL>** is the URL of the Web Page you want to allow WDS searches from.</span></span> <span data-ttu-id="cdda1-122">Essa cadeia de caracteres de URL pode incluir o asterisco curinga \* no início ou no final da URL.</span><span class="sxs-lookup"><span data-stu-id="cdda1-122">This URL string can include the wildcard asterisk \* at the beginning or end of the URL.</span></span> <span data-ttu-id="cdda1-123">Por exemplo, se a cadeia de caracteres for " \* . mydomain.com", você poderá iniciar uma pesquisa do WDS do https://www.mydomain.com e do https://mydomain.com .</span><span class="sxs-lookup"><span data-stu-id="cdda1-123">For example, if the string is "\*.mydomain.com", then you can start a WDS search from both https://www.mydomain.com and https://mydomain.com.</span></span>

## <a name="enabling-desktop-search-by-url"></a><span data-ttu-id="cdda1-124">Habilitando a pesquisa da área de trabalho por URL</span><span class="sxs-lookup"><span data-stu-id="cdda1-124">Enabling Desktop Search by URL</span></span>

<span data-ttu-id="cdda1-125">Outra opção que não requer acesso ao registro é usar a seguinte URL em suas páginas da Web:</span><span class="sxs-lookup"><span data-stu-id="cdda1-125">Another option that does not require access to the Registry is to use the following URL on your webpage(s):</span></span>

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

<span data-ttu-id="cdda1-126">em que **consulta** é a cadeia de caracteres codificada na URL na qual o usuário está pesquisando, incluindo quaisquer termos de [sintaxe de consulta avançada](-search-2x-wds-aqsreference.md) .</span><span class="sxs-lookup"><span data-stu-id="cdda1-126">where **QUERY** is the URL-encoded string the user is searching on, including any [Advanced Query Syntax](-search-2x-wds-aqsreference.md) terms.</span></span>

 

 




