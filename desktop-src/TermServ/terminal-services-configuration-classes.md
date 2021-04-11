---
title: Serviços de Área de Trabalho Remota classes de configuração
description: O provedor WMI de configuração de Serviços de Área de Trabalho Remota fornece as seguintes classes. Segue uma ilustração.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc9c58be85b8b4efc35495f35902ab67b35ad153
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366059"
---
# <a name="remote-desktop-services-configuration-classes"></a><span data-ttu-id="a6d70-104">Serviços de Área de Trabalho Remota classes de configuração</span><span class="sxs-lookup"><span data-stu-id="a6d70-104">Remote Desktop Services Configuration classes</span></span>

<span data-ttu-id="a6d70-105">O provedor WMI de configuração de Serviços de Área de Trabalho Remota fornece as seguintes classes.</span><span class="sxs-lookup"><span data-stu-id="a6d70-105">The Remote Desktop Services Configuration WMI provider provides the following classes.</span></span> <span data-ttu-id="a6d70-106">Segue uma ilustração.</span><span class="sxs-lookup"><span data-stu-id="a6d70-106">An illustration follows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a6d70-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a6d70-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a6d70-108">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="a6d70-108">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-109">Representa a associação entre os elementos do sistema gerenciado e a classe de configuração definida para eles.</span><span class="sxs-lookup"><span data-stu-id="a6d70-109">Represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-110">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="a6d70-110">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="a6d70-111">A classe base para todos os componentes do sistema que representam componentes do sistema abstratos, como perfis, processos ou recursos do sistema, na forma de dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="a6d70-111">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-112">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a6d70-112">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="a6d70-113">A classe base para a hierarquia de elementos do sistema.</span><span class="sxs-lookup"><span data-stu-id="a6d70-113">The base class for the system element hierarchy.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-114">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a6d70-114">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="a6d70-115">Representa parâmetros operacionais e relacionados à configuração para um ou mais elementos do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a6d70-115">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-116">**Terminal do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="a6d70-116">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dd>

<span data-ttu-id="a6d70-117">representa um terminal.</span><span class="sxs-lookup"><span data-stu-id="a6d70-117">represents a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-118">**\_TerminalError Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-118">**Win32\_TerminalError**</span></span>](win32-terminalerror.md)
</dt> <dd>

<span data-ttu-id="a6d70-119">Representa um erro de terminal.</span><span class="sxs-lookup"><span data-stu-id="a6d70-119">Represents a terminal error.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-120">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-120">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dd>

<span data-ttu-id="a6d70-121">uma subclasse da classe de [**\_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="a6d70-121">a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="a6d70-122">[**Win32 \_ TerminalService**](win32-terminalservice.md) representa a propriedade **Element** da Associação [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d70-122">[**Win32\_TerminalService**](win32-terminalservice.md) represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-123">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-123">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-124">representa a configuração de um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="a6d70-124">represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-125">**\_TerminalServiceToSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-125">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-126">representa a associação entre uma instância da classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e a configuração de uma determinada propriedade [**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d70-126">represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-127">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-127">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-128">representa as configurações que podem ser aplicadas a um terminal.</span><span class="sxs-lookup"><span data-stu-id="a6d70-128">represents the settings that can be applied to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-129">**\_TerminalTerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-129">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-130">representa a associação entre um terminal e seus parâmetros de configuração.</span><span class="sxs-lookup"><span data-stu-id="a6d70-130">represents the association between a terminal and its configuration settings.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-131">**\_TSAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-131">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> <dd>

<span data-ttu-id="a6d70-132">permite a exclusão de uma conta que existe no [**\_ terminal do Win32**](win32-terminal.md) e a modificação de permissões existentes.</span><span class="sxs-lookup"><span data-stu-id="a6d70-132">allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-133">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-133">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-134">define as definições de configuração para a classe de [**\_ terminal Win32**](win32-terminal.md) relacionada à política de conexão.</span><span class="sxs-lookup"><span data-stu-id="a6d70-134">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-135">**\_TSDiscoveredLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-135">**Win32\_TSDiscoveredLicenseServer**</span></span>](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

<span data-ttu-id="a6d70-136">Fornece detalhes sobre o servidor de licença Área de Trabalho Remota descoberto.</span><span class="sxs-lookup"><span data-stu-id="a6d70-136">Provides details about the discovered Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-137">**\_TSEnvironmentSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-138">define as definições de configuração para a classe de [**\_ terminal do Win32**](win32-terminal.md) , incluindo a diretiva de programa inicial.</span><span class="sxs-lookup"><span data-stu-id="a6d70-138">defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-139">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-139">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-140">representa as configurações gerais do terminal, como o nível de criptografia e o protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="a6d70-140">represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-141">**\_TSLogonSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-142">define as definições de configuração para a classe de [**\_ terminal Win32**](win32-terminal.md) relacionada ao logon do cliente.</span><span class="sxs-lookup"><span data-stu-id="a6d70-142">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-143">**\_TSNetworkAdapterListSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-143">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-144">enumera a lista de adaptadores de rede que podem ser configurados para um [**\_ terminal do Win32**](win32-terminal.md), com base no protocolo de terminal e no método de transporte especificados.</span><span class="sxs-lookup"><span data-stu-id="a6d70-144">enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-145">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-145">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-146">define várias definições de configuração para a classe de [**\_ terminal do Win32**](win32-terminal.md) , incluindo propriedades relacionadas ao adaptador de rede e o número máximo de conexões permitidas.</span><span class="sxs-lookup"><span data-stu-id="a6d70-146">defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-147">**\_TSPermissionsSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-147">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-148">inclui um método para adicionar novas contas ao terminal e um método para restaurar as permissões padrão para um terminal.</span><span class="sxs-lookup"><span data-stu-id="a6d70-148">includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-149">**\_TSRemoteControlSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-150">define as definições de configuração de controle remoto para a classe [**\_ terminal do Win32**](win32-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d70-150">defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-151">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-151">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dd>

<span data-ttu-id="a6d70-152">Define as definições de configuração do agente de Conexão de Área de Trabalho Remota (agente de conexão RD) para a classe [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d70-152">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-153">**\_TSSessionDirectorySetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-153">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-154">Representa a associação entre uma instância da classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e uma instância da classe [**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d70-154">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-155">**\_TSSessionSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-155">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-156">define as definições de configuração para a classe de [**\_ terminal do Win32**](win32-terminal.md) , tais como limites de tempo e ações de desconexão e reconexão.</span><span class="sxs-lookup"><span data-stu-id="a6d70-156">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-157">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-157">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> <dd>

<span data-ttu-id="a6d70-158">Define as configurações de virtualização de protocolo Internet (IP) para um servidor Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="a6d70-158">Defines Internet protocol (IP) virtualization settings for a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="a6d70-159">**\_TSVirtualIPSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a6d70-159">**Win32\_TSVirtualIPSetting**</span></span>](win32-tsvirtualipsetting.md)
</dt> <dd>

<span data-ttu-id="a6d70-160">Representa a associação entre uma classe de elemento [**\_ TerminalService do Win32**](win32-terminalservice.md) e uma classe de configuração [**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md) .</span><span class="sxs-lookup"><span data-stu-id="a6d70-160">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

</dd> </dl>

<span data-ttu-id="a6d70-161">A ilustração a seguir mostra as relações entre essas classes.</span><span class="sxs-lookup"><span data-stu-id="a6d70-161">The following illustration shows the relationships between these classes.</span></span>

![as relações entre as classes com suporte](images/tswmi.png)

 

 