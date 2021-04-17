---
description: Este tópico fornece uma visão geral conceitual da tecnologia MUI (Multilingual User interface), o suporte de plataforma que ele fornece para habilitar experiências de usuário multilíngues e os benefícios que ele oferece ao ecossistema do Windows.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Visão geral do MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564145"
---
# <a name="overview-of-mui"></a><span data-ttu-id="8ba9d-103">Visão geral do MUI</span><span class="sxs-lookup"><span data-stu-id="8ba9d-103">Overview of MUI</span></span>

<span data-ttu-id="8ba9d-104">Este tópico fornece uma visão geral conceitual da tecnologia MUI (Multilingual User interface), o suporte de plataforma que ele fornece para habilitar experiências de usuário multilíngues e os benefícios que ele oferece ao ecossistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-104">This topic provides a conceptual overview of the Multilingual User Interface (MUI) technology, the platform support it provides for enabling multilingual user experiences, and the benefits it offers to the Windows ecosystem.</span></span>

<span data-ttu-id="8ba9d-105">Nessa página:</span><span class="sxs-lookup"><span data-stu-id="8ba9d-105">On this page:</span></span>

-   [<span data-ttu-id="8ba9d-106">A necessidade de computação multilíngue</span><span class="sxs-lookup"><span data-stu-id="8ba9d-106">The need for multilingual computing</span></span>](#the-need-for-multilingual-computing)
-   [<span data-ttu-id="8ba9d-107">A função do MUI na habilitação da computação multilíngue</span><span class="sxs-lookup"><span data-stu-id="8ba9d-107">The role of MUI in enabling multilingual computing</span></span>](#the-role-of-mui-in-enabling-multilingual-computing)
-   [<span data-ttu-id="8ba9d-108">Conceitos principais do MUI</span><span class="sxs-lookup"><span data-stu-id="8ba9d-108">Core concepts of MUI</span></span>](#core-concepts-of-mui)
-   [<span data-ttu-id="8ba9d-109">Histórico do MUI no Windows</span><span class="sxs-lookup"><span data-stu-id="8ba9d-109">History of MUI in Windows</span></span>](#history-of-mui-in-windows)
-   [<span data-ttu-id="8ba9d-110">Benefícios da tecnologia MUI</span><span class="sxs-lookup"><span data-stu-id="8ba9d-110">Benefits of MUI technology</span></span>](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a><span data-ttu-id="8ba9d-111">A necessidade de computação multilíngue</span><span class="sxs-lookup"><span data-stu-id="8ba9d-111">The need for multilingual computing</span></span>

<span data-ttu-id="8ba9d-112">Para se beneficiar das oportunidades de crescimento apresentadas por mercados internacionais, as plataformas e os aplicativos da Microsoft dão suporte a mais idiomas, culturas e mercados do que nunca.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-112">To benefit from the growth opportunities presented by international markets, Microsoft's platforms and applications support more languages, cultures and markets than ever before.</span></span>

<span data-ttu-id="8ba9d-113">A linguagem, a cultura e as especificações de mercado ainda são extremamente relevantes para usuários internacionais, apesar de aumentar as tendências de globalização.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-113">Language, culture, and market specifics are still extremely relevant to international users, despite increasing globalization trends.</span></span> <span data-ttu-id="8ba9d-114">O gráfico de pizza a seguir mostra que os palestrantes que não estão em Inglês ainda compõem 91,5% da população do mundo.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-114">The following pie chart shows that non-English speakers still make up 91.5 percent of the world's population.</span></span>

![gráfico de pizza com três segmentos; o rótulo "alto-falantes que não são do Inglês 91,5%" é muito maior do que os outros dois combinados](images/overview-of-mui-fig1.gif)

<span data-ttu-id="8ba9d-116">Em todo o mundo, há 193 países e mais de 6.900 idiomas de vida conhecidos em uso hoje.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-116">Worldwide, there are 193 countries and over 6,900 known living languages in use today.</span></span> <span data-ttu-id="8ba9d-117">O inglês, apesar de sua função como a linguagem de negócios do mundo, é falado apenas em 8,5% da população do mundo como primeira ou segunda linguagem.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-117">English, despite its role as the world's business language, is only spoken by 8.5% of the world's population as a first or second language.</span></span> <span data-ttu-id="8ba9d-118">Para fornecer informações nativas a 94% da população do mundo, essas informações precisariam estar disponíveis no 347 (cerca de 5%) das linguagens do mundo que têm pelo menos um milhão de alto-falantes.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-118">To provide native information to 94% of the world's population, this information would need to be available in the 347 (about 5%) of the world's languages that have at least a million speakers.</span></span> <span data-ttu-id="8ba9d-119">Isso é especialmente verdadeiro, pois as tendências de globalização aumentaram as expectativas desses usuários em relação à tecnologia e à sua disponibilidade em seus mercados.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-119">This is especially true as globalization trends have increased the expectations of these users regarding technology and its availability in their markets.</span></span>

<span data-ttu-id="8ba9d-120">A necessidade de localizar software em mais idiomas aumentou ao longo dos anos e a Microsoft agora está fornecendo o Windows Vista e outros produtos em mais idiomas do que nunca.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-120">The need to localize software in more languages has increased over the years and Microsoft is now providing Windows Vista and other products in more languages than ever.</span></span> <span data-ttu-id="8ba9d-121">Essa evolução é especialmente clara com o Microsoft Windows, já que deixou de dar suporte a 30 idiomas com o Windows 98 a quase 100 com o Windows Vista, conforme ilustrado no gráfico de barras a seguir.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-121">This evolution is especially clear with Microsoft Windows, as it has gone from supporting 30 languages with Windows 98 to almost 100 with Windows Vista, as illustrated in the following bar chart.</span></span>

![gráfico de barras mostrando que o número de idiomas é muito maior no Windows Vista do que no Windows 98 ou no Windows XP](images/overview-of-mui-fig2.gif)

<span data-ttu-id="8ba9d-123">*Figura 2 — número de idiomas com suporte das versões do Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="8ba9d-123">*Figure 2—Number of languages supported by Microsoft Windows releases*</span></span>

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a><span data-ttu-id="8ba9d-124">A função do MUI na habilitação da computação multilíngue</span><span class="sxs-lookup"><span data-stu-id="8ba9d-124">The role of MUI in enabling multilingual computing</span></span>

<span data-ttu-id="8ba9d-125">Conforme discutido na seção anterior, a [globalização](glossary-for-understanding-mui.md) e a [localização](glossary-for-understanding-mui.md) de aplicativos se tornaram uma necessidade em um mundo mais integrado globalmente.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-125">As discussed in the previous section, [globalization](glossary-for-understanding-mui.md) and [localization](glossary-for-understanding-mui.md) of applications have become a necessity in a more globally integrated world.</span></span> <span data-ttu-id="8ba9d-126">Em particular, como cada vez mais empresas estão se tornando globais, seja internamente ou por meio de suas redes comerciais, a necessidade de aplicativos multilíngües é cada vez mais significativa.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-126">In particular, as more and more enterprises are going global, either internally or through their business networks, the need for multi-lingual applications is increasing dramatically.</span></span> <span data-ttu-id="8ba9d-127">Portanto, os obstáculos que essas empresas enfrentam atualmente na implantação desses aplicativos globalmente.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-127">So are the hurdles that these companies currently face in deploying these applications globally.</span></span>

<span data-ttu-id="8ba9d-128">Fornecer suporte para mais idiomas para sistemas operacionais Windows, bem como aplicativos de software criados para a plataforma Windows, requer novas estratégias que permitem que todos os principais cenários sejam implementados com sobrecarga mínima de engenharia.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-128">Providing support for more languages for Windows operating systems, as well as software applications built for the Windows platform, requires new strategies which enable all major scenarios to be implemented with minimal engineering overhead.</span></span>

<span data-ttu-id="8ba9d-129">A tecnologia MUI destina-se a desenvolvedores e ISVs que visam criar e dar suporte a aplicativos multilíngües para a plataforma Windows.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-129">MUI technology is targeted at developers and ISVs aiming to build and support multilingual applications for the Windows platform.</span></span> <span data-ttu-id="8ba9d-130">O MUI também é de importante importância para OEMs e empresas, que pode aproveitá-lo para implantar o sistema operacional Windows e adicionar aplicativos a computadores em diferentes idiomas por meio de implantação de imagem única.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-130">MUI is also of key significance to OEMs and enterprises, who can leverage it to deploy the Windows operating system and add applications to computers across different languages through single image deployment.</span></span>

## <a name="core-concepts-of-mui"></a><span data-ttu-id="8ba9d-131">Conceitos principais do MUI</span><span class="sxs-lookup"><span data-stu-id="8ba9d-131">Core concepts of MUI</span></span>

<span data-ttu-id="8ba9d-132">A ideia fundamental por trás do MUI é [separar o armazenamento de recursos localizáveis do código-fonte do aplicativo](mui-fundamental-concepts-explained.md), para poder arquitetar qualquer aplicativo multilíngue como uma combinação de um binário de núcleo com neutralidade de idioma e um conjunto de arquivos de recursos localizados específicos do idioma.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-132">The fundamental idea behind MUI is to [separate the storage of localizable resources from application source code](mui-fundamental-concepts-explained.md), so as to be able to architect any multilingual application as a combination of a language-neutral core binary and a set of language-specific localized resource files.</span></span>

<span data-ttu-id="8ba9d-133">Depois que o código-fonte do aplicativo é armazenado separadamente dos recursos localizados, fica fácil [carregar dinamicamente os recursos localizados apropriados](mui-fundamental-concepts-explained.md) para um determinado contexto de aplicativo com base em uma lógica que leva em conta as configurações de nível de aplicativo, de usuário e de sistema para o idioma da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-133">Once application source code is stored separately from the localized resources, it becomes easy to [dynamically load the appropriate localized resources](mui-fundamental-concepts-explained.md) for a given application context based on a logic that takes into account system, user and application-level settings for the user interface language.</span></span>

<span data-ttu-id="8ba9d-134">Esses atributos fundamentais do MUI ajudam a facilitar os cenários de negócios, como:</span><span class="sxs-lookup"><span data-stu-id="8ba9d-134">These fundamental attributes of MUI help facilitate business scenarios such as:</span></span>

-   <span data-ttu-id="8ba9d-135">Um modelo de localização aprimorado para o conteúdo da interface do usuário e da ajuda, por meio da separação física do código-fonte do aplicativo e de recursos localizáveis.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-135">An improved localization model for user interface and help content, via the physical separation of application source code and localizable resources.</span></span>
-   <span data-ttu-id="8ba9d-136">Tratar os recursos localizáveis como conteúdo dinâmico e carregá-los de acordo com as configurações de idioma da interface do usuário e as preferências de fallback.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-136">Treating the localizable resources as dynamic content and loading them according to the UI language settings and fallback preferences.</span></span> <span data-ttu-id="8ba9d-137">Isso permite cenários como:</span><span class="sxs-lookup"><span data-stu-id="8ba9d-137">This enables scenarios such as:</span></span>
    -   <span data-ttu-id="8ba9d-138">Alternando de um idioma da interface do usuário para outro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-138">Switching from one UI language to another one at run-time.</span></span>
    -   <span data-ttu-id="8ba9d-139">Criação de imagens de implantação única regionais ou mundiais que abrangem um conjunto de idiomas para OEMs e empresas.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-139">Creating regional or worldwide single deployment images that cover a set of languages for OEMs and enterprises.</span></span>

## <a name="history-of-mui-in-windows"></a><span data-ttu-id="8ba9d-140">Histórico do MUI no Windows</span><span class="sxs-lookup"><span data-stu-id="8ba9d-140">History of MUI in Windows</span></span>

<span data-ttu-id="8ba9d-141">O nível de suporte disponível para uma experiência de usuário multilíngüe no nível do sistema operacional Windows e para o desenvolvimento de aplicativos multilíngues na plataforma Windows evoluiu ao longo do tempo e nas diferentes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-141">The level of support available for a multilingual user experience at the Windows operating system level and for multilingual application development on the Windows platform has evolved over time and across the different versions of Windows.</span></span>

<span data-ttu-id="8ba9d-142">A funcionalidade com suporte [antes do Windows Vista](evolution-of-mui-support-across-windows-versions.md) era bastante básica, com imagens do Windows de idioma único e uma opção para complementar pacotes de interface do usuário multilíngüe em cenários específicos.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-142">The supported functionality [before Windows Vista](evolution-of-mui-support-across-windows-versions.md) was fairly basic, with single-language Windows images and an option to add-on Multilingual User Interface Packs in specific scenarios.</span></span> <span data-ttu-id="8ba9d-143">Nenhum suporte ao desenvolvedor para aplicativos multilíngues estava disponível.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-143">No developer support for multilingual applications was available.</span></span>

<span data-ttu-id="8ba9d-144">[Com o Windows Vista](evolution-of-mui-support-across-windows-versions.md), a Microsoft fez um investimento significativo em MUI, e o Windows Vista foi criado desde o início em uma plataforma mui.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-144">[With Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft made a significant investment in MUI, and Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="8ba9d-145">Embora isso represente um grande avanço na estratégia de localização do Windows, como é um habilitador de chave para a Microsoft fornecer janelas em mais idiomas do que nunca, ela é primeiro e mais importante para usuários, desenvolvedores e clientes do Windows.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-145">While this represents a major advance in Windows localization strategy, as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users, developers, and customers.</span></span> <span data-ttu-id="8ba9d-146">Ele fornece vários benefícios importantes, como:</span><span class="sxs-lookup"><span data-stu-id="8ba9d-146">It provides several major benefits such as:</span></span>

-   <span data-ttu-id="8ba9d-147">Um sistema operacional com neutralidade de idioma com suporte interno para o MUI.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-147">A language-neutral operating system with built-in support for MUI.</span></span>
-   <span data-ttu-id="8ba9d-148">Empacotamento, implantação e instalação configuráveis para dar suporte a cenários multilíngües.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-148">Configurable packaging, deployment, and installation to support multilingual scenarios.</span></span>
-   <span data-ttu-id="8ba9d-149">Implantação de imagem única com vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-149">Single-image deployment with multiple languages.</span></span>
-   <span data-ttu-id="8ba9d-150">Um modelo de manutenção aprimorado em que o código executável pode ser atualizado independentemente dos recursos.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-150">An improved servicing model where the executable code can be updated independently of the resources.</span></span>
-   <span data-ttu-id="8ba9d-151">Suporte ao desenvolvedor para a criação de aplicativos multilíngues.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-151">Developer support for building multilingual applications.</span></span>

<span data-ttu-id="8ba9d-152">A tabela a seguir fornece uma visão geral detalhada do suporte da plataforma Windows para o MUI:</span><span class="sxs-lookup"><span data-stu-id="8ba9d-152">The following table provides a detailed overview of the Windows platform support for MUI:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ba9d-153">Category</span><span class="sxs-lookup"><span data-stu-id="8ba9d-153">Category</span></span></th>
<th><span data-ttu-id="8ba9d-154">Suporte</span><span class="sxs-lookup"><span data-stu-id="8ba9d-154">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ba9d-155">Versões do Windows com suporte (somente suporte para SO)</span><span class="sxs-lookup"><span data-stu-id="8ba9d-155">Supported Windows versions (OS support only)</span></span></td>
<td><ul>
<li><span data-ttu-id="8ba9d-156">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8ba9d-156">Windows 2000 Professional</span></span></li>
<li><span data-ttu-id="8ba9d-157">Família do Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8ba9d-157">Windows 2000 Server family</span></span></li>
<li><span data-ttu-id="8ba9d-158">Windows XP Professional</span><span class="sxs-lookup"><span data-stu-id="8ba9d-158">Windows XP Professional</span></span></li>
<li><span data-ttu-id="8ba9d-159">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="8ba9d-159">Windows XP Tablet PC Edition</span></span></li>
<li><span data-ttu-id="8ba9d-160">Família Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8ba9d-160">Windows Server 2003 family</span></span></li>
<li><span data-ttu-id="8ba9d-161">Windows XP Embedded</span><span class="sxs-lookup"><span data-stu-id="8ba9d-161">Windows XP Embedded</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ba9d-162">Versões do Windows com suporte (so & suporte a aplicativos)</span><span class="sxs-lookup"><span data-stu-id="8ba9d-162">Supported Windows versions (OS & application support)</span></span></td>
<td><ul>
<li><span data-ttu-id="8ba9d-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ba9d-163">Windows Vista</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ba9d-164">Versões do Windows sem suporte</span><span class="sxs-lookup"><span data-stu-id="8ba9d-164">Unsupported Windows versions</span></span></td>
<td><ul>
<li><span data-ttu-id="8ba9d-165">Windows 9x</span><span class="sxs-lookup"><span data-stu-id="8ba9d-165">Windows 9x</span></span></li>
<li><span data-ttu-id="8ba9d-166">Windows me</span><span class="sxs-lookup"><span data-stu-id="8ba9d-166">Windows Me</span></span></li>
<li><span data-ttu-id="8ba9d-167">Windows XP Home Edition</span><span class="sxs-lookup"><span data-stu-id="8ba9d-167">Windows XP Home Edition</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a><span data-ttu-id="8ba9d-168">Benefícios da tecnologia MUI</span><span class="sxs-lookup"><span data-stu-id="8ba9d-168">Benefits of MUI technology</span></span>

<span data-ttu-id="8ba9d-169">O MUI afeta positivamente vários aspectos do ecossistema do Windows:</span><span class="sxs-lookup"><span data-stu-id="8ba9d-169">MUI positively impacts multiple aspects of the Windows ecosystem:</span></span>

-   <span data-ttu-id="8ba9d-170">[Benefícios para os desenvolvedores](benefits-of-mui-explained.md): vários benefícios são oferecidos aos desenvolvedores de aplicativos pela disponibilidade do suporte à API do MUI para criar aplicativos multilíngües modelados nos mesmos princípios que o suporte multilíngue no próprio sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-170">[Benefits for Developers](benefits-of-mui-explained.md): Numerous benefits are offered to application developers by the availability of MUI API support to build multilingual applications modeled on the same principles as the multilingual support in the core Windows operating system itself.</span></span> <span data-ttu-id="8ba9d-171">Esses benefícios incluem:</span><span class="sxs-lookup"><span data-stu-id="8ba9d-171">These benefits include:</span></span>
    -   <span data-ttu-id="8ba9d-172">A capacidade de fornecer uma experiência de linguagem de exibição consistente com o que o próprio sistema operacional oferece.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-172">The ability to provide a display language experience that is consistent with what the operating system itself offers.</span></span>
    -   <span data-ttu-id="8ba9d-173">A capacidade de estender facilmente o suporte a idiomas para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-173">The ability to easily extend the language support for an application.</span></span>
    -   <span data-ttu-id="8ba9d-174">A capacidade de manter e atender facilmente ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-174">The ability to easily maintain and service the application.</span></span>
    -   <span data-ttu-id="8ba9d-175">A capacidade de habilitar a implantação de imagem única de aplicativos por OEMs.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-175">The ability to enable single-image deployment of applications by OEMs.</span></span>
-   <span data-ttu-id="8ba9d-176">[Benefícios para as empresas](benefits-of-mui-explained.md): o principal benefício que o MUI oferece para empresas é a capacidade de distribuir, dar suporte e manter a mesma imagem multilíngue em todo o mundo com uma única instalação.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-176">[Benefits for Enterprises](benefits-of-mui-explained.md): The major benefit that MUI offers for enterprises is the ability to roll out, support, and maintain the same multilingual image worldwide with a single installation.</span></span> <span data-ttu-id="8ba9d-177">Outro ganho significativo é a capacidade de dar suporte a áreas de trabalho multilíngues que oferecem uma interação direta com os usuários com diferentes preferências de idioma.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-177">Another significant win is the ability to support multilingual desktops that offer seamless interaction to users with different language preferences.</span></span>
-   <span data-ttu-id="8ba9d-178">[Benefícios para os OEMs](benefits-of-mui-explained.md): o principal benefício para os OEMs é a instalação de imagem única que o MUI habilita, com suporte para vários idiomas, o que permite um gerenciamento mais eficaz do inventário.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-178">[Benefits for OEMs](benefits-of-mui-explained.md): The major benefit for OEMs is the single image installation that MUI enables, with support for multiple languages, which enables a more effective management of inventory.</span></span> <span data-ttu-id="8ba9d-179">Os OEMs também se beneficiam do suporte do MUI para o desenvolvimento de aplicativos, pois permitem que eles forneçam aplicativos com valor agregado em suas imagens, ao mesmo tempo em que se beneficiam da instalação de uma única imagem, desde que esses aplicativos estejam habilitados para MUI.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-179">OEMs also benefit from the MUI support for application development, as it enables them to provide value-add applications on their images while benefiting from the single image installation, as long as these applications are MUI-enabled.</span></span>

 

 




