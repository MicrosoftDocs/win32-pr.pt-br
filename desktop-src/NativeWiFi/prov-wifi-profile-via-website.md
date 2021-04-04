---
title: Provisionar um perfil de Wi-Fi por meio de um site
description: Permita que os usuários baixem um perfil de um site e provisione-os.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917651"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a><span data-ttu-id="a9362-103">Provisionar um perfil de Wi-Fi por meio de um site</span><span class="sxs-lookup"><span data-stu-id="a9362-103">Provision a Wi-Fi profile via a website</span></span>

<span data-ttu-id="a9362-104">O fluxo de trabalho descrito neste tópico foi introduzido no Windows 10, versão 2004.</span><span class="sxs-lookup"><span data-stu-id="a9362-104">The workflow described in this topic was introduced in Windows 10, version 2004.</span></span> <span data-ttu-id="a9362-105">Este tópico mostra como configurar um site para que um usuário possa provisionar um perfil para uma rede Passpoint (ou para uma rede normal) antes de passar para o intervalo dos pontos de acesso Wi-Fi correspondentes.</span><span class="sxs-lookup"><span data-stu-id="a9362-105">This topic shows how to configure a website so that a user can provision a profile for a Passpoint network (or for a normal network) prior to moving into range of the corresponding Wi-Fi access points.</span></span> <span data-ttu-id="a9362-106">Um cenário de exemplo é que de um usuário que pode estar planejando visitar um aeroporto ou uma conferência pela primeira vez, e quer se preparar antecipadamente baixando e provisionando um perfil em casa.</span><span class="sxs-lookup"><span data-stu-id="a9362-106">An example scenario is that of a user who might be planning to visit an airport or a conference for the first time, and they want to prepare in advance by downloading and provisioning a profile at home.</span></span>

<span data-ttu-id="a9362-107">Como desenvolvedor, você habilita o fluxo de trabalho fornecendo um perfil XML e configurando um site.</span><span class="sxs-lookup"><span data-stu-id="a9362-107">As a developer, you enable the workflow by providing an XML profile, and configuring a website.</span></span> <span data-ttu-id="a9362-108">Os usuários podem, então, provisionar um perfil de Wi-Fi baixando-o de seu site por meio de um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="a9362-108">Your users can then provision a Wi-Fi profile by downloading it from your website via a web browser.</span></span> <span data-ttu-id="a9362-109">No dispositivo do usuário, o perfil de Wi-Fi é provisionado usando a ativação de URI e o aplicativo de **configurações** do Windows.</span><span class="sxs-lookup"><span data-stu-id="a9362-109">On the user's device, the Wi-Fi profile is then provisioned by using URI activation and the Windows **Settings** app.</span></span>

<span data-ttu-id="a9362-110">Este fluxo de trabalho substitui o mecanismo no Internet Explorer para provisionar Wi-Fi perfis, que se baseiam em APIs JavaScript específicas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a9362-110">This workflow supersedes the mechanism in Internet Explorer for provisioning Wi-Fi profiles, which relies on Microsoft-specific JavaScript APIs.</span></span> <span data-ttu-id="a9362-111">Esse novo fluxo de trabalho deve funcionar com todos os principais navegadores.</span><span class="sxs-lookup"><span data-stu-id="a9362-111">This new workflow is expected to work with all major browsers.</span></span>

## <a name="the-workflow-in-more-detail"></a><span data-ttu-id="a9362-112">O fluxo de trabalho em mais detalhes</span><span class="sxs-lookup"><span data-stu-id="a9362-112">The workflow in more detail</span></span>

<span data-ttu-id="a9362-113">Você pode ativar este fluxo de trabalho de um hiperlink que inclui como um argumento o URI de download do documento XML de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="a9362-113">You can activate this workflow from a hyperlink that includes as an argument the download URI of the provisioning XML document.</span></span>

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

<span data-ttu-id="a9362-114">Por exemplo, a marcação HTML a seguir fornece um link para instalar os perfis encontrados em um documento hipotético `http://contoso.com/ProvisioningDoc.xml` .</span><span class="sxs-lookup"><span data-stu-id="a9362-114">For example, the following HTML markup gives a link to install the profile(s) that are found in a hypothetical document `http://contoso.com/ProvisioningDoc.xml`.</span></span>

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

<span data-ttu-id="a9362-115">O XML deve aderir ao esquema de provisionamento (consulte [provisionamento de conta](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span><span class="sxs-lookup"><span data-stu-id="a9362-115">Your XML must adhere to the provisioning schema (see [Account provisioning](/windows-hardware/drivers/mobilebroadband/account-provisioning)).</span></span> <span data-ttu-id="a9362-116">O XML também deve incluir um ou mais elementos [WLANProfile](./wlan-profileschema-wlanprofile-element.md)   .</span><span class="sxs-lookup"><span data-stu-id="a9362-116">Your XML must also include one or more [WLANProfile](./wlan-profileschema-wlanprofile-element.md) elements.</span></span><span data-ttu-id="a9362-117">Cada perfil será exibido na caixa de diálogo **Adicionar** descrita em Avançar.</span><span class="sxs-lookup"><span data-stu-id="a9362-117"> Each profile will be displayed in the **Add** dialog described next.</span></span>

<span data-ttu-id="a9362-118">Quando o usuário clica no link HTML, o fluxo de trabalho de instalação é invocado no aplicativo **configurações** .</span><span class="sxs-lookup"><span data-stu-id="a9362-118">When the user clicks your HTML link, the installation workflow is invoked in the **Settings** app.</span></span> <span data-ttu-id="a9362-119">O documento XML de provisionamento é baixado pelo aplicativo **configurações** .</span><span class="sxs-lookup"><span data-stu-id="a9362-119">Your provisioning XML document is downloaded by the **Settings** app.</span></span> <span data-ttu-id="a9362-120">Depois de baixado, são exibidas informações sobre os perfis, a assinatura e o assinante (desde que o documento esteja de acordo com o esquema).</span><span class="sxs-lookup"><span data-stu-id="a9362-120">Once it's downloaded, information about the profiles, signature, and signer are displayed (provided that the document adheres to the schema).</span></span>

![O aplicativo configurações](images/install-dialog.png)

<span data-ttu-id="a9362-122">O botão **Adicionar** na caixa de diálogo no aplicativo **configurações** será habilitado somente se o arquivo de provisionamento for assinado e confiável.</span><span class="sxs-lookup"><span data-stu-id="a9362-122">The **Add** button in the dialog in the **Settings** app is enabled only if the provisioning file is signed and trusted.</span></span>

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a><span data-ttu-id="a9362-123">Na página da Web, determine se há suporte para esse fluxo de trabalho</span><span class="sxs-lookup"><span data-stu-id="a9362-123">In your web page, determine whether this workflow is supported</span></span>

<span data-ttu-id="a9362-124">Não há nenhuma maneira em JavaScript determinar a versão de Build exata do Windows.</span><span class="sxs-lookup"><span data-stu-id="a9362-124">There is no way in JavaScript to determine the exact build version of Windows.</span></span> <span data-ttu-id="a9362-125">Mas se o usuário estiver usando o navegador da Web Microsoft Edge, você poderá determinar a versão do Edge inspecionando o valor do `User-agent` cabeçalho http.</span><span class="sxs-lookup"><span data-stu-id="a9362-125">But if your user is using the Microsoft Edge web browser, then you can determine the version of Edge by inspecting the value of the `User-agent` HTTP header.</span></span> <span data-ttu-id="a9362-126">Se a versão for maior ou igual a `18.nnnnn` , o fluxo de trabalho terá suporte.</span><span class="sxs-lookup"><span data-stu-id="a9362-126">If the version is greater than or equal to `18.nnnnn`, then the workflow is supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9362-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a9362-127">Related topics</span></span>

* [<span data-ttu-id="a9362-128">Provisionamento de conta</span><span class="sxs-lookup"><span data-stu-id="a9362-128">Account provisioning</span></span>](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [<span data-ttu-id="a9362-129">Elemento WLANProfile</span><span class="sxs-lookup"><span data-stu-id="a9362-129">WLANProfile element</span></span>](./wlan-profileschema-wlanprofile-element.md)