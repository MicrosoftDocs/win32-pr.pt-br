---
description: Você pode fornecer todas as informações necessárias para configurar adicionar ou remover programas no painel de controle definindo os valores de determinadas propriedades do instalador no pacote de Windows Installer do seu aplicativo.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configurando adicionar/remover programas com Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6850163e18af94aa9cceaf6c4bb2e8059dcf2121
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/30/2021
ms.locfileid: "105994504"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a><span data-ttu-id="b7354-103">Configurando adicionar/remover programas com Windows Installer</span><span class="sxs-lookup"><span data-stu-id="b7354-103">Configuring Add/Remove Programs with Windows Installer</span></span>

<span data-ttu-id="b7354-104">Você pode fornecer todas as informações necessárias para configurar adicionar ou remover programas no painel de controle definindo os valores de determinadas propriedades do instalador no pacote de Windows Installer do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7354-104">You can supply all of the information needed to configure Add/Remove Programs in Control Panel by setting the values of certain installer properties in your application's Windows Installer package.</span></span> <span data-ttu-id="b7354-105">Definir essas propriedades grava automaticamente os valores correspondentes no registro.</span><span class="sxs-lookup"><span data-stu-id="b7354-105">Setting these properties automatically writes the corresponding values into the registry.</span></span> <span data-ttu-id="b7354-106">Se o instalador detectar que o produto está marcado para remoção completa, as operações serão adicionadas automaticamente ao script para remover a pasta adicionar/remover programas nas informações do painel de controle do produto.</span><span class="sxs-lookup"><span data-stu-id="b7354-106">If the installer detects that the product is marked for complete removal, operations are automatically added to the script to remove the Add/Remove Programs folder in Control Panel information for the product.</span></span>

<span data-ttu-id="b7354-107">Se um aplicativo não estiver registrado, ele não estará listado em Adicionar/remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="b7354-107">If an application is not registered, it is not listed in Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="b7354-108">Para obter mais informações, consulte [adicionando e removendo um aplicativo e não deixando nenhum rastreamento no registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="b7354-108">For more information, see [Adding and Removing an Application and Leaving No Trace in the Registry](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span></span>

<span data-ttu-id="b7354-109">Os aplicativos que foram instalados no [contexto de instalação](installation-context.md) por usuário são exibidos em Adicionar/remover programas do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="b7354-109">Applications that have been installed in the per-user [installation context](installation-context.md) are displayed in the Add/Remove Programs of the current user.</span></span> <span data-ttu-id="b7354-110">Os aplicativos que foram instalados no contexto de instalação por máquina são exibidos em Adicionar ou remover programas de todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="b7354-110">Applications that have been installed in the per-machine installation context are displayed in the Add/Remove Programs of all users.</span></span> <span data-ttu-id="b7354-111">Aplicativos que não foram instalados por computador e foram instalados apenas como aplicativos por usuário para usuários que não sejam o usuário atual, não aparecem em Adicionar ou remover programas do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="b7354-111">Applications that have not been installed per-machine, and have only been installed as per-user applications for users other than the current user, do not appear in the Add/Remove Programs of the current user.</span></span>

<span data-ttu-id="b7354-112">Observe que os pacotes de instalação que usam a propriedade [**LIMITUI**](limitui.md) também devem conter o [**ARPNOMODIFY**](arpnomodify.md).</span><span class="sxs-lookup"><span data-stu-id="b7354-112">Note that installation packages that use the [**LIMITUI**](limitui.md) property must also contain the [**ARPNOMODIFY**](arpnomodify.md).</span></span> <span data-ttu-id="b7354-113">Isso é necessário para que um usuário obtenha o comportamento correto em Adicionar ou remover programas no utilitário do painel de controle ao tentar configurar um produto.</span><span class="sxs-lookup"><span data-stu-id="b7354-113">This is required for a user to obtain the correct behavior from Add/Remove Programs in Control Panel utility when attempting to configure a product.</span></span>

<span data-ttu-id="b7354-114">O instalador usa as [Propriedades públicas](public-properties.md) a seguir para gerenciar adicionar/remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="b7354-114">The installer uses the following [public properties](public-properties.md) to manage Add/Remove Programs in Control Panel.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7354-115">Nome da propriedade</span><span class="sxs-lookup"><span data-stu-id="b7354-115">Property name</span></span></th>
<th><span data-ttu-id="b7354-116">Breve descrição da propriedade</span><span class="sxs-lookup"><span data-stu-id="b7354-116">Brief description of property</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7354-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span></span></td>
<td><span data-ttu-id="b7354-118">URL do canal de atualização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7354-118">URL of the update channel for the application.</span></span> <span data-ttu-id="b7354-119">O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</span><span class="sxs-lookup"><span data-stu-id="b7354-119">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7354-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span></span></td>
<td><span data-ttu-id="b7354-121">Fornece comentários para adicionar ou remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="b7354-121">Provides Comments for the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="b7354-122">O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</span><span class="sxs-lookup"><span data-stu-id="b7354-122">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7354-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span></span></td>
<td><span data-ttu-id="b7354-124">Fornece o contato para adicionar ou remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="b7354-124">Provides the Contact for Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="b7354-125">O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</span><span class="sxs-lookup"><span data-stu-id="b7354-125">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7354-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span></span></td>
<td><span data-ttu-id="b7354-127">Caminho totalmente qualificado para a pasta principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7354-127">Fully qualified path to the application's primary folder.</span></span> <span data-ttu-id="b7354-128">O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</span><span class="sxs-lookup"><span data-stu-id="b7354-128">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7354-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span></span></td>
<td><span data-ttu-id="b7354-130">Endereço da Internet, ou URL, para obter suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="b7354-130">Internet address, or URL, for technical support.</span></span> <span data-ttu-id="b7354-131">O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</span><span class="sxs-lookup"><span data-stu-id="b7354-131">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7354-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span></span></td>
<td><span data-ttu-id="b7354-133">Números de telefone de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="b7354-133">Technical support phone numbers.</span></span> <span data-ttu-id="b7354-134">O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</span><span class="sxs-lookup"><span data-stu-id="b7354-134">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7354-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span></span></td>
<td><span data-ttu-id="b7354-136">Impede a exibição de um botão de alteração para o produto em Adicionar ou remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="b7354-136">Prevents display of a Change button for the product in Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="b7354-137">
<b>Observação:</b> Isso afeta apenas a exibição no ARP.</span><span class="sxs-lookup"><span data-stu-id="b7354-137">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="b7354-138">O Windows Installer ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.</span><span class="sxs-lookup"><span data-stu-id="b7354-138">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7354-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span></span></td>
<td><span data-ttu-id="b7354-140">Impede a exibição de um botão remover do produto em Adicionar ou remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="b7354-140">Prevents display of a Remove button for the product in the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="b7354-141">O produto ainda pode ser removido selecionando o botão alterar se o pacote de instalação tiver sido criado com uma interface do usuário que fornece a remoção do produto como uma opção.</span><span class="sxs-lookup"><span data-stu-id="b7354-141">The product can still be removed by selecting the Change button if the installation package has been authored with a user interface that provides product removal as an option.</span></span>
<blockquote><span data-ttu-id="b7354-142">
<b>Observação:</b> Isso afeta apenas a exibição no ARP.</span><span class="sxs-lookup"><span data-stu-id="b7354-142">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="b7354-143">O Windows Installer ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.</span><span class="sxs-lookup"><span data-stu-id="b7354-143">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7354-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span></span></td>
<td><span data-ttu-id="b7354-145">Desabilita o botão reparar em Adicionar ou remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="b7354-145">Disables the Repair button in the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="b7354-146">
<b>Observação:</b> Isso afeta apenas a exibição no ARP.</span><span class="sxs-lookup"><span data-stu-id="b7354-146">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="b7354-147">O Windows Installer ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.</span><span class="sxs-lookup"><span data-stu-id="b7354-147">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7354-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span></span></td>
<td><span data-ttu-id="b7354-149">Identifica o ícone exibido em Adicionar ou remover programas.</span><span class="sxs-lookup"><span data-stu-id="b7354-149">Identifies the icon displayed in Add/Remove Programs.</span></span> <span data-ttu-id="b7354-150">Se essa propriedade não for definida, adicionar/remover programas especificará o ícone de exibição.</span><span class="sxs-lookup"><span data-stu-id="b7354-150">If this property is not defined, Add/Remove Programs specifies the display icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7354-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span></span></td>
<td><span data-ttu-id="b7354-152">Fornece o Leiame para adicionar ou remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="b7354-152">Provides the ReadMe for Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="b7354-153">O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</span><span class="sxs-lookup"><span data-stu-id="b7354-153">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7354-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span></span></td>
<td><span data-ttu-id="b7354-155">Tamanho estimado do aplicativo em KB.</span><span class="sxs-lookup"><span data-stu-id="b7354-155">Estimated size of the application in KB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7354-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="b7354-157">Impede a exibição do aplicativo na lista de programas de adicionar/remover programas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="b7354-157">Prevents display of the application in the Programs List of the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="b7354-158">
<b>Observação:</b> Isso afeta apenas a exibição no ARP.</span><span class="sxs-lookup"><span data-stu-id="b7354-158">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="b7354-159">O Windows Installer ainda é capaz de reparar, instalar sob demanda e desinstalar aplicativos por meio de uma linha de comando ou da interface de programação.</span><span class="sxs-lookup"><span data-stu-id="b7354-159">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7354-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span></span></td>
<td><span data-ttu-id="b7354-161">URL para home page do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7354-161">URL for application's home page.</span></span> <span data-ttu-id="b7354-162">O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</span><span class="sxs-lookup"><span data-stu-id="b7354-162">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7354-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7354-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span></span></td>
<td><span data-ttu-id="b7354-164">URL para informações de atualização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7354-164">URL for application update information.</span></span> <span data-ttu-id="b7354-165">O valor que o instalador grava na <a href="uninstall-registry-key.md">chave de registro de desinstalação</a>.</span><span class="sxs-lookup"><span data-stu-id="b7354-165">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="b7354-166">Para obter informações sobre a ferramenta definir programas e padrões, consulte a seção [trabalhando com definir acesso do programa e padrões do computador](/previous-versions//bb776877(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7354-166">For information regarding the Set Program and Defaults tool, refer to the section [Working with Set Program Access and Computer Defaults](/previous-versions//bb776877(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7354-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7354-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7354-168">Desinstalar chave do registro</span><span class="sxs-lookup"><span data-stu-id="b7354-168">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
</dt> </dl>
