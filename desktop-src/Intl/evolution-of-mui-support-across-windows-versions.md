---
description: Evolução do suporte do MUI em versões do Windows
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Evolução do suporte do MUI em versões do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810485"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a><span data-ttu-id="d0ae7-103">Evolução do suporte do MUI em versões do Windows</span><span class="sxs-lookup"><span data-stu-id="d0ae7-103">Evolution of MUI Support across Windows Versions</span></span>

-   [<span data-ttu-id="d0ae7-104">Antes do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0ae7-104">Before Windows Vista</span></span>](#before-windows-vista)
-   [<span data-ttu-id="d0ae7-105">Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="d0ae7-105">Windows Vista and Beyond</span></span>](#windows-vista-and-beyond)
    -   [<span data-ttu-id="d0ae7-106">Um sistema operacional de linguagem neutra/MUI</span><span class="sxs-lookup"><span data-stu-id="d0ae7-106">A language neutral/MUI operating system</span></span>](#a-language-neutralmui-operating-system)
    -   [<span data-ttu-id="d0ae7-107">Cenários de implantação são totalmente baseados em MUI</span><span class="sxs-lookup"><span data-stu-id="d0ae7-107">Deployment scenarios are fully MUI-based</span></span>](#deployment-scenarios-are-fully-mui-based)
    -   [<span data-ttu-id="d0ae7-108">Implantação de imagem única</span><span class="sxs-lookup"><span data-stu-id="d0ae7-108">Single image deployment</span></span>](#single-image-deployment)
    -   [<span data-ttu-id="d0ae7-109">Modelo de manutenção aprimorado</span><span class="sxs-lookup"><span data-stu-id="d0ae7-109">Improved servicing model</span></span>](#improved-servicing-model)
    -   [<span data-ttu-id="d0ae7-110">Infraestrutura do MUI</span><span class="sxs-lookup"><span data-stu-id="d0ae7-110">MUI infrastructure</span></span>](#mui-infrastructure)
    -   [<span data-ttu-id="d0ae7-111">Gerenciamento de idioma</span><span class="sxs-lookup"><span data-stu-id="d0ae7-111">Language management</span></span>](#language-management)
    -   [<span data-ttu-id="d0ae7-112">Manipulação de recursos</span><span class="sxs-lookup"><span data-stu-id="d0ae7-112">Resource handling</span></span>](#resource-handling)

## <a name="before-windows-vista"></a><span data-ttu-id="d0ae7-113">Antes do Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0ae7-113">Before Windows Vista</span></span>

<span data-ttu-id="d0ae7-114">Antes da versão Windows Vista, o Windows foi fornecido com imagens de idioma único, o que significava que cada versão localizada do Windows continha uma linguagem única para a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-114">Prior to the Windows Vista release, Windows shipped with single-language images, which meant that each localized version of Windows contained a single language for its user interface.</span></span> <span data-ttu-id="d0ae7-115">O MUI foi um complemento à versão em inglês do sistema operacional, e os pacotes de interface do usuário multilíngüe só podiam ser adicionados a determinadas versões em inglês do Windows.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-115">MUI was an add-on to the English version of the operating system, and the Multilingual User Interface Packs could only be added to certain English versions of Windows.</span></span> <span data-ttu-id="d0ae7-116">Quando instalado na versão em inglês do Windows, o MUI permitia que o idioma da interface do usuário do sistema operacional fosse alterado de acordo com as preferências de usuários individuais para um dos idiomas com suporte.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-116">When installed on the English version of Windows, MUI allowed the user interface language of the operating system to be changed according to the preferences of individual users to one of the supported languages.</span></span>

<span data-ttu-id="d0ae7-117">O modelo de MUI Pack não expôs o suporte a MUI para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-117">The MUI Pack model did not expose MUI support for applications.</span></span> <span data-ttu-id="d0ae7-118">Embora os desenvolvedores pudessem criar aplicativos multilíngües, eles tinham que criar seus próprios mecanismos para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-118">Although developers could create multi-lingual applications, they had to create their own mechanisms to do so.</span></span>

## <a name="windows-vista-and-beyond"></a><span data-ttu-id="d0ae7-119">Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="d0ae7-119">Windows Vista and Beyond</span></span>

<span data-ttu-id="d0ae7-120">Com o Windows Vista, a Microsoft fez um investimento significativo em MUI.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-120">With Windows Vista, Microsoft made a significant investment in MUI.</span></span> <span data-ttu-id="d0ae7-121">O Windows Vista foi criado desde o início em uma plataforma MUI.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-121">Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="d0ae7-122">Embora isso represente um grande avanço na estratégia de localização do Windows, uma vez que é um habilitador principal para a Microsoft fornecer janelas em mais idiomas do que nunca, é primeiro e mais importante para usuários e clientes do Windows.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-122">While this represents a major advance in Windows localization strategy as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users and customers.</span></span>

### <a name="a-language-neutralmui-operating-system"></a><span data-ttu-id="d0ae7-123">Um sistema operacional de linguagem neutra/MUI</span><span class="sxs-lookup"><span data-stu-id="d0ae7-123">A language neutral/MUI operating system</span></span>

<span data-ttu-id="d0ae7-124">A grande maioria dos binários do Windows Vista são compatíveis com o MUI e seus dados localizáveis são armazenados separadamente do código.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-124">The vast majority of Windows Vista binaries are MUI compliant, and their localizable data are stored separately from the code.</span></span> <span data-ttu-id="d0ae7-125">Isso oferece flexibilidade, pois diferentes dados de idioma podem ser adicionados a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-125">This offers flexibility, as different language data can be added at any time.</span></span>

### <a name="deployment-scenarios-are-fully-mui-based"></a><span data-ttu-id="d0ae7-126">Cenários de implantação são totalmente baseados em MUI</span><span class="sxs-lookup"><span data-stu-id="d0ae7-126">Deployment scenarios are fully MUI-based</span></span>

<span data-ttu-id="d0ae7-127">O design de empacotamento e instalação do Windows Vista são baseados em MUI e todos os dados localizáveis são empacotados em pacotes específicos de idioma, e cada pacote de idiomas pode ser implantado em diferentes cenários.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-127">The Windows Vista packaging and installation design are MUI-based and all localizable data are packaged in language-specific packs, and each language pack can be deployed in different scenarios.</span></span> <span data-ttu-id="d0ae7-128">Por exemplo, embora os DVDs de varejo para Windows Vista contenham versões de idioma único, os usuários da edição Ultimate podem baixar pacotes de idiomas adicionais do MUI e podem alternar o idioma da interface do usuário no painel de controle **Opções regionais e de idiomas** .</span><span class="sxs-lookup"><span data-stu-id="d0ae7-128">For example, although the retail DVDs for Windows Vista contain single-language versions, users of the Ultimate edition can download additional MUI language packs and can switch UI language from the **Regional and Language Options** control panel.</span></span> <span data-ttu-id="d0ae7-129">Os licenciados da Enterprise Edition obtêm todos os idiomas e podem implantar qualquer um deles.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-129">Enterprise edition licensees get all languages and can deploy any of them.</span></span>

### <a name="single-image-deployment"></a><span data-ttu-id="d0ae7-130">Implantação de imagem única</span><span class="sxs-lookup"><span data-stu-id="d0ae7-130">Single image deployment</span></span>

<span data-ttu-id="d0ae7-131">Os clientes empresariais e os OEMs agora podem reduzir o número de imagens que precisam manter para implantar o Windows e os aplicativos em computadores em diferentes localidades por meio de implantação de imagem única.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-131">Enterprise customers and OEMs can now reduce the number of images that they need to maintain in order to deploy Windows and applications onto computers across different locales through single image deployment.</span></span>

<span data-ttu-id="d0ae7-132">Com o MUI no Windows Vista, uma imagem que contém vários idiomas pode ser implantada em qualquer usuário de idioma, e os usuários podem determinar suas próprias linguagens preferenciais (na política) durante a instalação ou a "experiência de uso inicial" com o computador.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-132">With MUI on Windows Vista, one image containing multiple languages can be deployed to any language users, and users can determine their own preferred languages (within policy) during setup or initial "out of the box experience" with the computer.</span></span> <span data-ttu-id="d0ae7-133">Em particular, os OEMs podem colocar vários idiomas da interface do usuário em seus novos computadores para permitir que os usuários selecionem um no centro de boas-vindas.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-133">In particular, OEMs can put many UI languages on their new computers to allow users to select one from the Welcome Center.</span></span> <span data-ttu-id="d0ae7-134">Assim, de uma imagem com vários pacotes de idiomas, a instalação exibirá uma lista de idiomas disponíveis e permitirá que os usuários escolham um deles.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-134">Thus, from an image with multiple language packs, Setup will display a list of available languages and enable users to pick one of them.</span></span> <span data-ttu-id="d0ae7-135">Todas as configurações internacionais são então definidas para corresponder ao idioma ou à localidade selecionada.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-135">All international settings are then set to match the selected language or locale.</span></span>

### <a name="improved-servicing-model"></a><span data-ttu-id="d0ae7-136">Modelo de manutenção aprimorado</span><span class="sxs-lookup"><span data-stu-id="d0ae7-136">Improved servicing model</span></span>

<span data-ttu-id="d0ae7-137">O mesmo QFE ou pacote de correção de segurança agora pode ser instalado na parte superior de qualquer sistema de linguagem.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-137">The same QFE or security fix package can now be installed on top of any language systems.</span></span> <span data-ttu-id="d0ae7-138">Isso é essencial, pois permite um retorno mais rápido de correções de segurança em particular e permite que todos os usuários internacionais se beneficiem da disponibilidade de todas as correções de segurança.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-138">This is critical as it enables a faster turnaround of security fixes in particular and enables all international users to benefit from the same time availability of all security fixes.</span></span>

### <a name="mui-infrastructure"></a><span data-ttu-id="d0ae7-139">Infraestrutura do MUI</span><span class="sxs-lookup"><span data-stu-id="d0ae7-139">MUI infrastructure</span></span>

<span data-ttu-id="d0ae7-140">A partir do Windows Vista, as APIs do MUI estão disponíveis para permitir que os desenvolvedores tirem proveito dos mecanismos de MUI para seus próprios aplicativos, sem precisar criar lógica personalizada para manipulação de recursos e gerenciamento de idioma.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-140">Starting with Windows Vista, MUI APIs are available to enable developers to take advantage of the MUI mechanisms for their own applications, without having to create custom logic for resource handling and language management.</span></span>

### <a name="language-management"></a><span data-ttu-id="d0ae7-141">Gerenciamento de idioma</span><span class="sxs-lookup"><span data-stu-id="d0ae7-141">Language management</span></span>

<span data-ttu-id="d0ae7-142">As APIs básicas do MUI que fornecem recursos de gerenciamento de idioma da interface do usuário estão disponíveis como parte da infraestrutura do MUI.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-142">Base MUI APIs that provide UI language management capabilities are available as part of the MUI infrastructure.</span></span> <span data-ttu-id="d0ae7-143">Para ajudar a gerenciar as diferentes configurações de idioma da interface do usuário no nível do sistema, de usuários e de aplicativos, o MUI os combina internamente em uma única lista priorizada.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-143">To help manage the different UI language settings at the system, user, and application level, MUI internally combines them into a single prioritized list.</span></span> <span data-ttu-id="d0ae7-144">Em seguida, o MUI implementa um mecanismo de fallback com base nessa lista priorizada, permitindo soluções de localização parcial, fornecendo aos usuários uma experiência de linguagem de interface do usuário apropriada, se não preferível.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-144">MUI then implements a fallback mechanism based on this prioritized list, allowing for partial localization solutions while providing users with an appropriate—if not preferred—user interface language experience.</span></span>

<span data-ttu-id="d0ae7-145">Por exemplo, um sistema que executa a versão em espanhol do Windows Vista com um LIP (Language Interface Pack) do catalão instalado na parte superior do sistema operacional de base pode dar suporte ao seguinte comportamento: o sistema tentará exibir seus recursos em catalão primeiro e, se esses recursos não estiverem disponíveis no catalão, forneça ao usuário recursos em espanhol.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-145">For example, a system running the Spanish version of Windows Vista with a Catalan language interface pack (LIP) installed on top of the base operating system can support the following behavior: the system will try and display its resources in Catalan first, and if these resources are not available in Catalan, then provide the user with Spanish resources instead.</span></span>

### <a name="resource-handling"></a><span data-ttu-id="d0ae7-146">Manipulação de recursos</span><span class="sxs-lookup"><span data-stu-id="d0ae7-146">Resource handling</span></span>

<span data-ttu-id="d0ae7-147">Com a infraestrutura de MUI aprimorada que está disponível a partir do Windows Vista, as tecnologias de recursos mais comuns são habilitadas para MUI.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-147">With the improved MUI infrastructure that is available starting with Windows Vista, most common resource technologies are MUI-enabled.</span></span> <span data-ttu-id="d0ae7-148">A tabela a seguir fornece detalhes adicionais sobre o suporte à manipulação de recursos disponível no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d0ae7-148">The following table provides additional details on the resource handling support available in Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0ae7-149">Category</span><span class="sxs-lookup"><span data-stu-id="d0ae7-149">Category</span></span></th>
<th><span data-ttu-id="d0ae7-150">Suporte</span><span class="sxs-lookup"><span data-stu-id="d0ae7-150">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d0ae7-151">Tipos de recurso compatíveis</span><span class="sxs-lookup"><span data-stu-id="d0ae7-151">Supported resource types</span></span></td>
<td><ul>
<li><span data-ttu-id="d0ae7-152">Recurso Win32/não gerenciado:. DLL/. EXE/. OCX</span><span class="sxs-lookup"><span data-stu-id="d0ae7-152">Win32/unmanaged resource: .DLL/.EXE/.OCX</span></span></li>
<li><span data-ttu-id="d0ae7-153">Registros relacionados ao shell</span><span class="sxs-lookup"><span data-stu-id="d0ae7-153">Shell-related registrations</span></span></li>
<li><span data-ttu-id="d0ae7-154">Recursos relacionados ao gerenciamento: log de eventos, snap-in/arquivos MSC</span><span class="sxs-lookup"><span data-stu-id="d0ae7-154">Management-related resources: Event log, Snap-in/MSC files</span></span></li>
<li><span data-ttu-id="d0ae7-155">WMI: MOF/MFL</span><span class="sxs-lookup"><span data-stu-id="d0ae7-155">WMI: MOF/MFL</span></span></li>
<li><span data-ttu-id="d0ae7-156">Política de Grupo: ADMX/ADML</span><span class="sxs-lookup"><span data-stu-id="d0ae7-156">Group Policy: ADMX/ADML</span></span></li>
<li><span data-ttu-id="d0ae7-157">Resources.dll gerenciados</span><span class="sxs-lookup"><span data-stu-id="d0ae7-157">Managed Resources.dll</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0ae7-158">Ferramentas de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="d0ae7-158">Development Tools</span></span></td>
<td><ul>
<li><span data-ttu-id="d0ae7-159">Para Win32: RC.exe, MUIRCT.exe e Visual Studio 2005 e posterior</span><span class="sxs-lookup"><span data-stu-id="d0ae7-159">For Win32: RC.exe, MUIRCT.exe and Visual Studio 2005 and later</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0ae7-160">Suporte a tipo de recurso limitado</span><span class="sxs-lookup"><span data-stu-id="d0ae7-160">Limited resource type support</span></span></td>
<td><ul>
<li><span data-ttu-id="d0ae7-161">arquivos de ajuda \*. chm</span><span class="sxs-lookup"><span data-stu-id="d0ae7-161">\*.chm help files</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



