---
description: A partir do Windows Vista, os itens do painel de controle incluídos no Windows recebem um nome canônico que pode ser usado em uma chamada à API ou em uma instrução de linha de comando para iniciar esse item programaticamente.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Nomes canônicos de itens do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fc360b0d3db0f85a057977d1898c59d09d5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920754"
---
# <a name="canonical-names-of-control-panel-items"></a><span data-ttu-id="7a489-103">Nomes canônicos de itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7a489-103">Canonical Names of Control Panel Items</span></span>

<span data-ttu-id="7a489-104">A partir do Windows Vista, os itens do painel de controle incluídos no Windows recebem um nome canônico que pode ser usado em uma [chamada à API ou em uma instrução de linha de comando](executing-control-panel-items.md) para iniciar esse item programaticamente.</span><span class="sxs-lookup"><span data-stu-id="7a489-104">As of Windows Vista, Control Panel items included with Windows are given a canonical name that can be used in an [API call or a command-line instruction](executing-control-panel-items.md) to programmatically launch that item.</span></span> <span data-ttu-id="7a489-105">A partir do Windows 7 e do Windows Server 2008 R2, os nomes canônicos podem ser usados em uma política de grupo para ocultar itens específicos do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="7a489-105">As of Windows 7 and Windows Server 2008 R2, canonical names can be used in a group policy to hide specific Control Panel items.</span></span> <span data-ttu-id="7a489-106">Este tópico fornece detalhes para cada item do painel de controle: nome canônico, GUID, nome do módulo e versões do sistema operacional que reconhecem o nome canônico.</span><span class="sxs-lookup"><span data-stu-id="7a489-106">This topic provides details for each Control Panel item: canonical name, GUID, module name, and the operating system versions that recognize the canonical name.</span></span>

> [!Note]  
> <span data-ttu-id="7a489-107">Os nomes canônicos dos itens do painel de controle não têm suporte antes do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7a489-107">Canonical names for Control Panel items are not supported prior to Windows Vista.</span></span>

 

-   [<span data-ttu-id="7a489-108">Nomes canônicos do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7a489-108">Control Panel Canonical Names</span></span>](#control-panel-canonical-names)
-   [<span data-ttu-id="7a489-109">Nomes canônicos do painel de controle preteridos</span><span class="sxs-lookup"><span data-stu-id="7a489-109">Deprecated Control Panel Canonical Names</span></span>](#deprecated-control-panel-canonical-names)
-   [<span data-ttu-id="7a489-110">Usando nomes canônicos no Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="7a489-110">Using Canonical Names in Group Policy</span></span>](#using-canonical-names-in-local-group-policy)
-   [<span data-ttu-id="7a489-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a489-111">Remarks</span></span>](#remarks)

## <a name="control-panel-canonical-names"></a><span data-ttu-id="7a489-112">Nomes canônicos do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7a489-112">Control Panel Canonical Names</span></span>

<span data-ttu-id="7a489-113">Pontos a serem lembrados ao trabalhar com esses valores:</span><span class="sxs-lookup"><span data-stu-id="7a489-113">Points to remember when working with these values:</span></span>

-   <span data-ttu-id="7a489-114">Por definição, os nomes canônicos não são alterados com base no idioma do sistema; Eles estão sempre em inglês, mesmo se o idioma do sistema não for.</span><span class="sxs-lookup"><span data-stu-id="7a489-114">By definition, canonical names do not change based on the system language; they're always in English, even if the system's language is not.</span></span>
-   <span data-ttu-id="7a489-115">Nem todos os itens do painel de controle estão presentes em todas as variedades do Windows.</span><span class="sxs-lookup"><span data-stu-id="7a489-115">Not all Control Panel items are present in all varieties of Windows.</span></span>
-   <span data-ttu-id="7a489-116">Alguns itens do painel de controle só aparecerão se o hardware correto for detectado no sistema.</span><span class="sxs-lookup"><span data-stu-id="7a489-116">Some Control Panel items only appear if the right hardware is detected on the system.</span></span>
-   <span data-ttu-id="7a489-117">Terceiros também podem adicionar itens do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="7a489-117">Third parties can also add Control Panel items.</span></span> <span data-ttu-id="7a489-118">Os nomes canônicos listados aqui são apenas para itens do painel de controle que estão incluídos no Windows.</span><span class="sxs-lookup"><span data-stu-id="7a489-118">The canonical names listed here are only for Control Panel items that are included with Windows.</span></span>

<span data-ttu-id="7a489-119">A seguir estão os itens do painel de controle disponíveis no Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="7a489-119">The following are the Control Panel items available in Windows 8.1:</span></span>

-   [<span data-ttu-id="7a489-120">Central de ações</span><span class="sxs-lookup"><span data-stu-id="7a489-120">Action Center</span></span>](#action-center)
-   [<span data-ttu-id="7a489-121">Ferramentas administrativas</span><span class="sxs-lookup"><span data-stu-id="7a489-121">Administrative Tools</span></span>](#administrative-tools)
-   [<span data-ttu-id="7a489-122">AutoPlay</span><span class="sxs-lookup"><span data-stu-id="7a489-122">AutoPlay</span></span>](#autoplay)
-   [<span data-ttu-id="7a489-123">Dispositivos biométricos</span><span class="sxs-lookup"><span data-stu-id="7a489-123">Biometric Devices</span></span>](#biometric-devices)
-   [<span data-ttu-id="7a489-124">Criptografia de Unidade de Disco BitLocker</span><span class="sxs-lookup"><span data-stu-id="7a489-124">BitLocker Drive Encryption</span></span>](#bitlocker-drive-encryption)
-   [<span data-ttu-id="7a489-125">Gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="7a489-125">Color Management</span></span>](#color-management)
-   [<span data-ttu-id="7a489-126">Gerenciador de Credenciais</span><span class="sxs-lookup"><span data-stu-id="7a489-126">Credential Manager</span></span>](#credential-manager)
-   [<span data-ttu-id="7a489-127">Data e hora</span><span class="sxs-lookup"><span data-stu-id="7a489-127">Date and Time</span></span>](#date-and-time)
-   [<span data-ttu-id="7a489-128">Programas padrão</span><span class="sxs-lookup"><span data-stu-id="7a489-128">Default Programs</span></span>](#default-programs)
-   [<span data-ttu-id="7a489-129">Gerenciador de Dispositivos</span><span class="sxs-lookup"><span data-stu-id="7a489-129">Device Manager</span></span>](#device-manager)
-   [<span data-ttu-id="7a489-130">Dispositivos e impressoras</span><span class="sxs-lookup"><span data-stu-id="7a489-130">Devices and Printers</span></span>](#devices-and-printers)
-   [<span data-ttu-id="7a489-131">Exibição</span><span class="sxs-lookup"><span data-stu-id="7a489-131">Display</span></span>](#display)
-   [<span data-ttu-id="7a489-132">Central de facilidade de acesso</span><span class="sxs-lookup"><span data-stu-id="7a489-132">Ease of Access Center</span></span>](#ease-of-access-center)
-   [<span data-ttu-id="7a489-133">Segurança da família</span><span class="sxs-lookup"><span data-stu-id="7a489-133">Family Safety</span></span>](#family-safety)
-   [<span data-ttu-id="7a489-134">Histórico de arquivos</span><span class="sxs-lookup"><span data-stu-id="7a489-134">File History</span></span>](#file-history)
-   [<span data-ttu-id="7a489-135">Opções de Pasta</span><span class="sxs-lookup"><span data-stu-id="7a489-135">Folder Options</span></span>](#folder-options)
-   [<span data-ttu-id="7a489-136">Fontes</span><span class="sxs-lookup"><span data-stu-id="7a489-136">Fonts</span></span>](#fonts)
-   [<span data-ttu-id="7a489-137">HomeGroup</span><span class="sxs-lookup"><span data-stu-id="7a489-137">HomeGroup</span></span>](#homegroup)
-   [<span data-ttu-id="7a489-138">Opções de indexação</span><span class="sxs-lookup"><span data-stu-id="7a489-138">Indexing Options</span></span>](#indexing-options)
-   [<span data-ttu-id="7a489-139">Infravermelho</span><span class="sxs-lookup"><span data-stu-id="7a489-139">Infrared</span></span>](#infrared)
-   [<span data-ttu-id="7a489-140">Opções da Internet</span><span class="sxs-lookup"><span data-stu-id="7a489-140">Internet Options</span></span>](#internet-options)
-   [<span data-ttu-id="7a489-141">Iniciador iSCSI</span><span class="sxs-lookup"><span data-stu-id="7a489-141">iSCSI Initiator</span></span>](#iscsi-initiator)
-   [<span data-ttu-id="7a489-142">iSNS Server</span><span class="sxs-lookup"><span data-stu-id="7a489-142">iSNS Server</span></span>](#isns-server)
-   [<span data-ttu-id="7a489-143">Teclado</span><span class="sxs-lookup"><span data-stu-id="7a489-143">Keyboard</span></span>](#keyboard)
-   [<span data-ttu-id="7a489-144">Configurações de local</span><span class="sxs-lookup"><span data-stu-id="7a489-144">Location Settings</span></span>](#location-settings)
-   [<span data-ttu-id="7a489-145">Mouse</span><span class="sxs-lookup"><span data-stu-id="7a489-145">Mouse</span></span>](#mouse)
-   [<span data-ttu-id="7a489-146">MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a489-146">MPIOConfiguration</span></span>](#mpioconfiguration)
-   [<span data-ttu-id="7a489-147">Centro de compartilhamento e de rede</span><span class="sxs-lookup"><span data-stu-id="7a489-147">Network and Sharing Center</span></span>](#network-and-sharing-center)
-   [<span data-ttu-id="7a489-148">Ícones da área de notificação</span><span class="sxs-lookup"><span data-stu-id="7a489-148">Notification Area Icons</span></span>](#notification-area-icons)
-   [<span data-ttu-id="7a489-149">Caneta e toque</span><span class="sxs-lookup"><span data-stu-id="7a489-149">Pen and Touch</span></span>](#pen-and-touch)
-   [<span data-ttu-id="7a489-150">Personalização</span><span class="sxs-lookup"><span data-stu-id="7a489-150">Personalization</span></span>](#personalization)
-   [<span data-ttu-id="7a489-151">Telefone e modem</span><span class="sxs-lookup"><span data-stu-id="7a489-151">Phone and Modem</span></span>](#phone-and-modem)
-   [<span data-ttu-id="7a489-152">Opções de Energia</span><span class="sxs-lookup"><span data-stu-id="7a489-152">Power Options</span></span>](#power-options)
-   [<span data-ttu-id="7a489-153">Programas e Recursos</span><span class="sxs-lookup"><span data-stu-id="7a489-153">Programs and Features</span></span>](#programs-and-features)
-   [<span data-ttu-id="7a489-154">Recuperação</span><span class="sxs-lookup"><span data-stu-id="7a489-154">Recovery</span></span>](#recovery)
-   [<span data-ttu-id="7a489-155">Região</span><span class="sxs-lookup"><span data-stu-id="7a489-155">Region</span></span>](#region)
-   [<span data-ttu-id="7a489-156">Conexões de RemoteApp e Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="7a489-156">RemoteApp and Desktop Connections</span></span>](#remoteapp-and-desktop-connections)
-   [<span data-ttu-id="7a489-157">Som</span><span class="sxs-lookup"><span data-stu-id="7a489-157">Sound</span></span>](#sound)
-   [<span data-ttu-id="7a489-158">Reconhecimento de fala</span><span class="sxs-lookup"><span data-stu-id="7a489-158">Speech Recognition</span></span>](#speech-recognition)
-   [<span data-ttu-id="7a489-159">Espaços de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7a489-159">Storage Spaces</span></span>](#storage-spaces)
-   [<span data-ttu-id="7a489-160">Central de Sincronização</span><span class="sxs-lookup"><span data-stu-id="7a489-160">Sync Center</span></span>](#sync-center)
-   [<span data-ttu-id="7a489-161">System</span><span class="sxs-lookup"><span data-stu-id="7a489-161">System</span></span>](#system)
-   [<span data-ttu-id="7a489-162">Configurações do Tablet PC</span><span class="sxs-lookup"><span data-stu-id="7a489-162">Tablet PC Settings</span></span>](#tablet-pc-settings)
-   [<span data-ttu-id="7a489-163">Barra de tarefas e navegação</span><span class="sxs-lookup"><span data-stu-id="7a489-163">Taskbar and Navigation</span></span>](#taskbar-and-navigation)
-   [<span data-ttu-id="7a489-164">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="7a489-164">Troubleshooting</span></span>](#troubleshooting)
-   [<span data-ttu-id="7a489-165">TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="7a489-165">TSAppInstall</span></span>](#tsappinstall)
-   [<span data-ttu-id="7a489-166">Contas de Usuário</span><span class="sxs-lookup"><span data-stu-id="7a489-166">User Accounts</span></span>](#user-accounts)
-   [<span data-ttu-id="7a489-167">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="7a489-167">Windows Anytime Upgrade</span></span>](#windows-anytime-upgrade)
-   [<span data-ttu-id="7a489-168">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="7a489-168">Windows Defender</span></span>](#windows-defender)
-   [<span data-ttu-id="7a489-169">Firewall do Windows</span><span class="sxs-lookup"><span data-stu-id="7a489-169">Windows Firewall</span></span>](#windows-firewall)
-   [<span data-ttu-id="7a489-170">Centro de Mobilidade do Windows</span><span class="sxs-lookup"><span data-stu-id="7a489-170">Windows Mobility Center</span></span>](#windows-mobility-center)
-   [<span data-ttu-id="7a489-171">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="7a489-171">Windows To Go</span></span>](#windows-to-go)
-   [<span data-ttu-id="7a489-172">Windows Update</span><span class="sxs-lookup"><span data-stu-id="7a489-172">Windows Update</span></span>](#windows-update)
-   [<span data-ttu-id="7a489-173">Pastas de trabalho</span><span class="sxs-lookup"><span data-stu-id="7a489-173">Work Folders</span></span>](#work-folders)

### <a name="action-center"></a><span data-ttu-id="7a489-174">Central de Ações</span><span class="sxs-lookup"><span data-stu-id="7a489-174">Action Center</span></span>

-   <span data-ttu-id="7a489-175">**Nome canônico**: Microsoft. ActionCenter</span><span class="sxs-lookup"><span data-stu-id="7a489-175">**Canonical name**: Microsoft.ActionCenter</span></span>
-   <span data-ttu-id="7a489-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span><span class="sxs-lookup"><span data-stu-id="7a489-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span></span>
-   <span data-ttu-id="7a489-177">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-177">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-178">**Nome do módulo**: @% SystemRoot% \\ System32 \\ActionCenterCPL.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-178">**Module name**: @%SystemRoot%\\System32\\ActionCenterCPL.dll,-1</span></span>
-   <span data-ttu-id="7a489-179">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-179">**Pages**</span></span>

    | <span data-ttu-id="7a489-180">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-180">Page Name</span></span>           | <span data-ttu-id="7a489-181">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-181">Opens</span></span>                      |
    |---------------------|----------------------------|
    | <span data-ttu-id="7a489-182">MaintenanceSettings</span><span class="sxs-lookup"><span data-stu-id="7a489-182">MaintenanceSettings</span></span> | <span data-ttu-id="7a489-183">Manutenção automática</span><span class="sxs-lookup"><span data-stu-id="7a489-183">Automatic Maintenance</span></span>      |
    | <span data-ttu-id="7a489-184">pageProblems</span><span class="sxs-lookup"><span data-stu-id="7a489-184">pageProblems</span></span>        | <span data-ttu-id="7a489-185">Relatórios de problemas</span><span class="sxs-lookup"><span data-stu-id="7a489-185">Problem Reports</span></span>            |
    | <span data-ttu-id="7a489-186">pageReliabilityView</span><span class="sxs-lookup"><span data-stu-id="7a489-186">pageReliabilityView</span></span> | <span data-ttu-id="7a489-187">Monitor de confiabilidade</span><span class="sxs-lookup"><span data-stu-id="7a489-187">Reliability Monitor</span></span>        |
    | <span data-ttu-id="7a489-188">pageResponseArchive</span><span class="sxs-lookup"><span data-stu-id="7a489-188">pageResponseArchive</span></span> | <span data-ttu-id="7a489-189">Mensagens arquivadas</span><span class="sxs-lookup"><span data-stu-id="7a489-189">Archived Messages</span></span>          |
    | <span data-ttu-id="7a489-190">pageSettings</span><span class="sxs-lookup"><span data-stu-id="7a489-190">pageSettings</span></span>        | <span data-ttu-id="7a489-191">Configurações de relatório de problemas</span><span class="sxs-lookup"><span data-stu-id="7a489-191">Problem Reporting Settings</span></span> |

    

     

### <a name="administrative-tools"></a><span data-ttu-id="7a489-192">Ferramentas Administrativas</span><span class="sxs-lookup"><span data-stu-id="7a489-192">Administrative Tools</span></span>

-   <span data-ttu-id="7a489-193">**Nome canônico**: Microsoft. AdministrativeTools</span><span class="sxs-lookup"><span data-stu-id="7a489-193">**Canonical name**: Microsoft.AdministrativeTools</span></span>
-   <span data-ttu-id="7a489-194">**GUID**: {D20EA4E1-3957-11D2-A40B-0C5020524153}</span><span class="sxs-lookup"><span data-stu-id="7a489-194">**GUID**: {D20EA4E1-3957-11d2-A40B-0C5020524153}</span></span>
-   <span data-ttu-id="7a489-195">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-195">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-196">**Nome do módulo**: @% SystemRoot% \\ System32 \\shell32.dll,-22982</span><span class="sxs-lookup"><span data-stu-id="7a489-196">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22982</span></span>

### <a name="autoplay"></a><span data-ttu-id="7a489-197">Reprodução Automática</span><span class="sxs-lookup"><span data-stu-id="7a489-197">AutoPlay</span></span>

-   <span data-ttu-id="7a489-198">**Nome canônico**: Microsoft. AutoPlay</span><span class="sxs-lookup"><span data-stu-id="7a489-198">**Canonical name**: Microsoft.AutoPlay</span></span>
-   <span data-ttu-id="7a489-199">**GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}</span><span class="sxs-lookup"><span data-stu-id="7a489-199">**GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}</span></span>
-   <span data-ttu-id="7a489-200">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-200">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-201">**Nome do módulo**: @% SystemRoot% \\ System32 \\autoplay.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-201">**Module name**: @%SystemRoot%\\System32\\autoplay.dll,-1</span></span>

### <a name="biometric-devices"></a><span data-ttu-id="7a489-202">Dispositivos biométricos</span><span class="sxs-lookup"><span data-stu-id="7a489-202">Biometric Devices</span></span>

-   <span data-ttu-id="7a489-203">**Nome canônico**: Microsoft. BiometricDevices</span><span class="sxs-lookup"><span data-stu-id="7a489-203">**Canonical name**: Microsoft.BiometricDevices</span></span>
-   <span data-ttu-id="7a489-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span><span class="sxs-lookup"><span data-stu-id="7a489-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span></span>
-   <span data-ttu-id="7a489-205">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-205">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-206">**Nome do módulo**: @% SystemRoot% \\ System32 \\biocpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-206">**Module name**: @%SystemRoot%\\System32\\biocpl.dll,-1</span></span>

### <a name="bitlocker-drive-encryption"></a><span data-ttu-id="7a489-207">Criptografia de Unidade de Disco BitLocker</span><span class="sxs-lookup"><span data-stu-id="7a489-207">BitLocker Drive Encryption</span></span>

-   <span data-ttu-id="7a489-208">**Nome canônico**: Microsoft. BitLockerDriveEncryption</span><span class="sxs-lookup"><span data-stu-id="7a489-208">**Canonical name**: Microsoft.BitLockerDriveEncryption</span></span>
-   <span data-ttu-id="7a489-209">**GUID**: {D9EF8727-CAC2-4E60-809E-86F80A666C91}</span><span class="sxs-lookup"><span data-stu-id="7a489-209">**GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}</span></span>
-   <span data-ttu-id="7a489-210">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-210">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-211">**Nome do módulo**: @% SystemRoot% \\ System32 \\fvecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-211">**Module name**: @%SystemRoot%\\System32\\fvecpl.dll,-1</span></span>

### <a name="color-management"></a><span data-ttu-id="7a489-212">Gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="7a489-212">Color Management</span></span>

-   <span data-ttu-id="7a489-213">**Nome canônico**: Microsoft. ColorManagement</span><span class="sxs-lookup"><span data-stu-id="7a489-213">**Canonical name**: Microsoft.ColorManagement</span></span>
-   <span data-ttu-id="7a489-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span><span class="sxs-lookup"><span data-stu-id="7a489-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span></span>
-   <span data-ttu-id="7a489-215">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-215">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-216">**Nome do módulo**: @% SystemRoot% \\ System32 \\colorcpl.exe,-6</span><span class="sxs-lookup"><span data-stu-id="7a489-216">**Module name**: @%systemroot%\\system32\\colorcpl.exe,-6</span></span>

### <a name="credential-manager"></a><span data-ttu-id="7a489-217">Gerenciador de Credenciais</span><span class="sxs-lookup"><span data-stu-id="7a489-217">Credential Manager</span></span>

-   <span data-ttu-id="7a489-218">**Nome canônico**: Microsoft. CredentialManager</span><span class="sxs-lookup"><span data-stu-id="7a489-218">**Canonical name**: Microsoft.CredentialManager</span></span>
-   <span data-ttu-id="7a489-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span><span class="sxs-lookup"><span data-stu-id="7a489-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span></span>
-   <span data-ttu-id="7a489-220">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-220">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-221">**Nome do módulo**: @% SystemRoot% \\ System32 \\Vault.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-221">**Module name**: @%SystemRoot%\\system32\\Vault.dll,-1</span></span>
-   <span data-ttu-id="7a489-222">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-222">**Pages**</span></span>

    | <span data-ttu-id="7a489-223">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-223">Page Name</span></span>                   | <span data-ttu-id="7a489-224">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-224">Opens</span></span>               |
    |-----------------------------|---------------------|
    | <span data-ttu-id="7a489-225">? SelectedVault = CredmanVault</span><span class="sxs-lookup"><span data-stu-id="7a489-225">?SelectedVault=CredmanVault</span></span> | <span data-ttu-id="7a489-226">as Credenciais do Windows</span><span class="sxs-lookup"><span data-stu-id="7a489-226">Windows Credentials</span></span> |

    

     

### <a name="date-and-time"></a><span data-ttu-id="7a489-227">Data e hora</span><span class="sxs-lookup"><span data-stu-id="7a489-227">Date and Time</span></span>

-   <span data-ttu-id="7a489-228">**Nome canônico**: Microsoft. DateAndTime</span><span class="sxs-lookup"><span data-stu-id="7a489-228">**Canonical name**: Microsoft.DateAndTime</span></span>
-   <span data-ttu-id="7a489-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span><span class="sxs-lookup"><span data-stu-id="7a489-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span></span>
-   <span data-ttu-id="7a489-230">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-230">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-231">**Nome do módulo**: @% SystemRoot% \\ System32 \\timedate.cpl,-51</span><span class="sxs-lookup"><span data-stu-id="7a489-231">**Module name**: @%SystemRoot%\\System32\\timedate.cpl,-51</span></span>
-   <span data-ttu-id="7a489-232">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-232">**Pages**</span></span>

    | <span data-ttu-id="7a489-233">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-233">Page Name</span></span> | <span data-ttu-id="7a489-234">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-234">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="7a489-235">1</span><span class="sxs-lookup"><span data-stu-id="7a489-235">1</span></span>         | <span data-ttu-id="7a489-236">Relógios adicionais</span><span class="sxs-lookup"><span data-stu-id="7a489-236">Additional Clocks</span></span> |

    

     

### <a name="default-programs"></a><span data-ttu-id="7a489-237">Programas padrão</span><span class="sxs-lookup"><span data-stu-id="7a489-237">Default Programs</span></span>

-   <span data-ttu-id="7a489-238">**Nome canônico**: Microsoft. defaultprograms</span><span class="sxs-lookup"><span data-stu-id="7a489-238">**Canonical name**: Microsoft.DefaultPrograms</span></span>
-   <span data-ttu-id="7a489-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span><span class="sxs-lookup"><span data-stu-id="7a489-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span></span>
-   <span data-ttu-id="7a489-240">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-240">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-241">**Nome do módulo**: @% SystemRoot% \\ System32 \\sud.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-241">**Module name**: @%SystemRoot%\\System32\\sud.dll,-1</span></span>
-   <span data-ttu-id="7a489-242">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-242">**Pages**</span></span>

    | <span data-ttu-id="7a489-243">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-243">Page Name</span></span>          | <span data-ttu-id="7a489-244">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-244">Opens</span></span>                |
    |--------------------|----------------------|
    | <span data-ttu-id="7a489-245">pageDefaultProgram</span><span class="sxs-lookup"><span data-stu-id="7a489-245">pageDefaultProgram</span></span> | <span data-ttu-id="7a489-246">Definir programas padrão</span><span class="sxs-lookup"><span data-stu-id="7a489-246">Set Default Programs</span></span> |
    | <span data-ttu-id="7a489-247">pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="7a489-247">pageFileAssoc</span></span>      | <span data-ttu-id="7a489-248">Definir associações</span><span class="sxs-lookup"><span data-stu-id="7a489-248">Set Associations</span></span>     |

    

     

### <a name="device-manager"></a><span data-ttu-id="7a489-249">Gerenciador de Dispositivos</span><span class="sxs-lookup"><span data-stu-id="7a489-249">Device Manager</span></span>

-   <span data-ttu-id="7a489-250">**Nome canônico**: Microsoft. DeviceManager</span><span class="sxs-lookup"><span data-stu-id="7a489-250">**Canonical name**: Microsoft.DeviceManager</span></span>
-   <span data-ttu-id="7a489-251">**GUID**: {74246bfc-4c96-11D0-ABEF-0020af6b0b7a}</span><span class="sxs-lookup"><span data-stu-id="7a489-251">**GUID**: {74246bfc-4c96-11d0-abef-0020af6b0b7a}</span></span>
-   <span data-ttu-id="7a489-252">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-252">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-253">**Nome do módulo**: @% SystemRoot% \\ System32 \\devmgr.dll,-4</span><span class="sxs-lookup"><span data-stu-id="7a489-253">**Module name**: @%SystemRoot%\\System32\\devmgr.dll,-4</span></span>

### <a name="devices-and-printers"></a><span data-ttu-id="7a489-254">Dispositivos e Impressoras</span><span class="sxs-lookup"><span data-stu-id="7a489-254">Devices and Printers</span></span>

-   <span data-ttu-id="7a489-255">**Nome canônico**: Microsoft. DevicesAndPrinters</span><span class="sxs-lookup"><span data-stu-id="7a489-255">**Canonical name**: Microsoft.DevicesAndPrinters</span></span>
-   <span data-ttu-id="7a489-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span><span class="sxs-lookup"><span data-stu-id="7a489-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span></span>
-   <span data-ttu-id="7a489-257">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-257">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-258">**Nome do módulo**: @% SystemRoot% \\ System32 \\DeviceCenter.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="7a489-258">**Module name**: @%systemroot%\\system32\\DeviceCenter.dll,-1000</span></span>

### <a name="display"></a><span data-ttu-id="7a489-259">Monitor</span><span class="sxs-lookup"><span data-stu-id="7a489-259">Display</span></span>

-   <span data-ttu-id="7a489-260">**Nome canônico**: Microsoft. display</span><span class="sxs-lookup"><span data-stu-id="7a489-260">**Canonical name**: Microsoft.Display</span></span>
-   <span data-ttu-id="7a489-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span><span class="sxs-lookup"><span data-stu-id="7a489-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span></span>
-   <span data-ttu-id="7a489-262">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-262">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-263">**Nome do módulo**: @% SystemRoot% \\ System32 \\Display.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-263">**Module name**: @%SystemRoot%\\System32\\Display.dll,-1</span></span>
-   <span data-ttu-id="7a489-264">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-264">**Pages**</span></span>

    | <span data-ttu-id="7a489-265">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-265">Page Name</span></span> | <span data-ttu-id="7a489-266">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-266">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="7a489-267">Configurações</span><span class="sxs-lookup"><span data-stu-id="7a489-267">Settings</span></span>  | <span data-ttu-id="7a489-268">Resolução de tela</span><span class="sxs-lookup"><span data-stu-id="7a489-268">Screen Resolution</span></span> |

    

     

### <a name="ease-of-access-center"></a><span data-ttu-id="7a489-269">Central de facilidade de acesso</span><span class="sxs-lookup"><span data-stu-id="7a489-269">Ease of Access Center</span></span>

-   <span data-ttu-id="7a489-270">**Nome canônico**: Microsoft. EaseOfAccessCenter</span><span class="sxs-lookup"><span data-stu-id="7a489-270">**Canonical name**: Microsoft.EaseOfAccessCenter</span></span>
-   <span data-ttu-id="7a489-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span><span class="sxs-lookup"><span data-stu-id="7a489-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span></span>
-   <span data-ttu-id="7a489-272">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-272">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-273">**Nome do módulo**: @% SystemRoot% \\ System32 \\accessibilitycpl.dll,-10</span><span class="sxs-lookup"><span data-stu-id="7a489-273">**Module name**: @%SystemRoot%\\System32\\accessibilitycpl.dll,-10</span></span>
-   <span data-ttu-id="7a489-274">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-274">**Pages**</span></span>

    | <span data-ttu-id="7a489-275">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-275">Page Name</span></span>               | <span data-ttu-id="7a489-276">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-276">Opens</span></span>                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | <span data-ttu-id="7a489-277">pageEasierToClick</span><span class="sxs-lookup"><span data-stu-id="7a489-277">pageEasierToClick</span></span>       | <span data-ttu-id="7a489-278">Facilitar o uso do mouse</span><span class="sxs-lookup"><span data-stu-id="7a489-278">Make the mouse easier to use</span></span>                                        |
    | <span data-ttu-id="7a489-279">pageEasierToSee</span><span class="sxs-lookup"><span data-stu-id="7a489-279">pageEasierToSee</span></span>         | <span data-ttu-id="7a489-280">Facilitar a visualização do computador</span><span class="sxs-lookup"><span data-stu-id="7a489-280">Make the computer easier to see</span></span>                                     |
    | <span data-ttu-id="7a489-281">pageEasierWithSounds</span><span class="sxs-lookup"><span data-stu-id="7a489-281">pageEasierWithSounds</span></span>    | <span data-ttu-id="7a489-282">Usar alternativas de texto ou visuais para sons</span><span class="sxs-lookup"><span data-stu-id="7a489-282">Use text or visual alternatives for sounds</span></span>                          |
    | <span data-ttu-id="7a489-283">pageFilterKeysSettings</span><span class="sxs-lookup"><span data-stu-id="7a489-283">pageFilterKeysSettings</span></span>  | <span data-ttu-id="7a489-284">Configurar chaves de filtro</span><span class="sxs-lookup"><span data-stu-id="7a489-284">Set up Filter Keys</span></span>                                                  |
    | <span data-ttu-id="7a489-285">pageKeyboardEasierToUse</span><span class="sxs-lookup"><span data-stu-id="7a489-285">pageKeyboardEasierToUse</span></span> | <span data-ttu-id="7a489-286">Facilitar o uso do teclado</span><span class="sxs-lookup"><span data-stu-id="7a489-286">Make the keyboard easier to use</span></span>                                     |
    | <span data-ttu-id="7a489-287">pageNoMouseOrKeyboard</span><span class="sxs-lookup"><span data-stu-id="7a489-287">pageNoMouseOrKeyboard</span></span>   | <span data-ttu-id="7a489-288">Usar o computador sem mouse ou teclado</span><span class="sxs-lookup"><span data-stu-id="7a489-288">Use the computer without a mouse or keyboard</span></span>                        |
    | <span data-ttu-id="7a489-289">pageNoVisual</span><span class="sxs-lookup"><span data-stu-id="7a489-289">pageNoVisual</span></span>            | <span data-ttu-id="7a489-290">Usar o computador sem uma exibição</span><span class="sxs-lookup"><span data-stu-id="7a489-290">Use the computer without a display</span></span>                                  |
    | <span data-ttu-id="7a489-291">pageQuestionsCognitive</span><span class="sxs-lookup"><span data-stu-id="7a489-291">pageQuestionsCognitive</span></span>  | <span data-ttu-id="7a489-292">Obtenha recomendações para facilitar o uso do seu computador (cognitiva)</span><span class="sxs-lookup"><span data-stu-id="7a489-292">Get recommendations to make your computer easier to use (cognitive)</span></span> |
    | <span data-ttu-id="7a489-293">pageQuestionsEyesight</span><span class="sxs-lookup"><span data-stu-id="7a489-293">pageQuestionsEyesight</span></span>   | <span data-ttu-id="7a489-294">Obtenha recomendações para facilitar o uso do seu computador (eyesight)</span><span class="sxs-lookup"><span data-stu-id="7a489-294">Get recommendations to make your computer easier to use (eyesight)</span></span>  |

    

     

### <a name="family-safety"></a><span data-ttu-id="7a489-295">Segurança da família</span><span class="sxs-lookup"><span data-stu-id="7a489-295">Family Safety</span></span>

-   <span data-ttu-id="7a489-296">**Nome canônico**: Microsoft. ParentalControls</span><span class="sxs-lookup"><span data-stu-id="7a489-296">**Canonical name**: Microsoft.ParentalControls</span></span>
-   <span data-ttu-id="7a489-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span><span class="sxs-lookup"><span data-stu-id="7a489-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span></span>
-   <span data-ttu-id="7a489-298">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-298">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-299">**Nome do módulo**: @% SystemRoot% \\ System32 \\wpccpl.dll,-100</span><span class="sxs-lookup"><span data-stu-id="7a489-299">**Module name**: @%SystemRoot%\\System32\\wpccpl.dll,-100</span></span>
-   <span data-ttu-id="7a489-300">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-300">**Pages**</span></span>

    | <span data-ttu-id="7a489-301">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-301">Page Name</span></span>   | <span data-ttu-id="7a489-302">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-302">Opens</span></span>                                  |
    |-------------|----------------------------------------|
    | <span data-ttu-id="7a489-303">pageUserHub</span><span class="sxs-lookup"><span data-stu-id="7a489-303">pageUserHub</span></span> | <span data-ttu-id="7a489-304">Escolher um usuário e configurar a proteção da família</span><span class="sxs-lookup"><span data-stu-id="7a489-304">Choose a user and set up Family Safety</span></span> |

    

     

### <a name="file-history"></a><span data-ttu-id="7a489-305">Histórico de arquivos</span><span class="sxs-lookup"><span data-stu-id="7a489-305">File History</span></span>

-   <span data-ttu-id="7a489-306">**Nome canônico**: Microsoft. filehistory</span><span class="sxs-lookup"><span data-stu-id="7a489-306">**Canonical name**: Microsoft.FileHistory</span></span>
-   <span data-ttu-id="7a489-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span><span class="sxs-lookup"><span data-stu-id="7a489-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span></span>
-   <span data-ttu-id="7a489-308">**Sistema operacional com suporte**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-308">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-309">**Nome do módulo**: @% SystemRoot% \\ System32 \\fhcpl.dll,-52</span><span class="sxs-lookup"><span data-stu-id="7a489-309">**Module name**: @%SystemRoot%\\System32\\fhcpl.dll,-52</span></span>
-   <span data-ttu-id="7a489-310">O histórico de arquivos inclui uma versão mais recente do item de backup e restauração, mas o nome canônico do item antigo não é remapeado para o histórico de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7a489-310">File History includes a newer version of the Backup and Restore item, but that older item's canonical name does not remap to File History.</span></span>

### <a name="folder-options"></a><span data-ttu-id="7a489-311">Opções de Pasta</span><span class="sxs-lookup"><span data-stu-id="7a489-311">Folder Options</span></span>

-   <span data-ttu-id="7a489-312">**Nome canônico**: Microsoft. FOLDEROPTIONS</span><span class="sxs-lookup"><span data-stu-id="7a489-312">**Canonical name**: Microsoft.FolderOptions</span></span>
-   <span data-ttu-id="7a489-313">**GUID**: {6DFD7C5C-2451-11D3-A299-00C04F8EF6AF}</span><span class="sxs-lookup"><span data-stu-id="7a489-313">**GUID**: {6DFD7C5C-2451-11d3-A299-00C04F8EF6AF}</span></span>
-   <span data-ttu-id="7a489-314">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-314">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-315">**Nome do módulo**: @% SystemRoot% \\ System32 \\shell32.dll,-22985</span><span class="sxs-lookup"><span data-stu-id="7a489-315">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22985</span></span>

### <a name="fonts"></a><span data-ttu-id="7a489-316">Fontes</span><span class="sxs-lookup"><span data-stu-id="7a489-316">Fonts</span></span>

-   <span data-ttu-id="7a489-317">**Nome canônico**: Microsoft. Fonts</span><span class="sxs-lookup"><span data-stu-id="7a489-317">**Canonical name**: Microsoft.Fonts</span></span>
-   <span data-ttu-id="7a489-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span><span class="sxs-lookup"><span data-stu-id="7a489-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span></span>
-   <span data-ttu-id="7a489-319">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-319">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-320">**Nome do módulo**: @% SystemRoot% \\ System32 \\FontExt.dll,-8007</span><span class="sxs-lookup"><span data-stu-id="7a489-320">**Module name**: @%SystemRoot%\\System32\\FontExt.dll,-8007</span></span>

### <a name="homegroup"></a><span data-ttu-id="7a489-321">HomeGroup</span><span class="sxs-lookup"><span data-stu-id="7a489-321">HomeGroup</span></span>

-   <span data-ttu-id="7a489-322">**Nome canônico**: Microsoft. grupo doméstico</span><span class="sxs-lookup"><span data-stu-id="7a489-322">**Canonical name**: Microsoft.HomeGroup</span></span>
-   <span data-ttu-id="7a489-323">**GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span><span class="sxs-lookup"><span data-stu-id="7a489-323">**GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span></span>
-   <span data-ttu-id="7a489-324">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-324">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-325">**Nome do módulo**: @% SystemRoot% \\ System32 \\hgcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-325">**Module name**: @%SystemRoot%\\System32\\hgcpl.dll,-1</span></span>

### <a name="indexing-options"></a><span data-ttu-id="7a489-326">Opções de Indexação</span><span class="sxs-lookup"><span data-stu-id="7a489-326">Indexing Options</span></span>

-   <span data-ttu-id="7a489-327">**Nome canônico**: Microsoft. IndexingOptions</span><span class="sxs-lookup"><span data-stu-id="7a489-327">**Canonical name**: Microsoft.IndexingOptions</span></span>
-   <span data-ttu-id="7a489-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span><span class="sxs-lookup"><span data-stu-id="7a489-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span></span>
-   <span data-ttu-id="7a489-329">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-329">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-330">**Nome do módulo**: @% SystemRoot% \\ System32 \\srchadmin.dll,-601</span><span class="sxs-lookup"><span data-stu-id="7a489-330">**Module name**: @%SystemRoot%\\System32\\srchadmin.dll,-601</span></span>

### <a name="infrared"></a><span data-ttu-id="7a489-331">Infravermelho</span><span class="sxs-lookup"><span data-stu-id="7a489-331">Infrared</span></span>

-   <span data-ttu-id="7a489-332">**Nome canônico**: Microsoft. infravermelho</span><span class="sxs-lookup"><span data-stu-id="7a489-332">**Canonical name**: Microsoft.Infrared</span></span>
-   <span data-ttu-id="7a489-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="7a489-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span>
-   <span data-ttu-id="7a489-334">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-334">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-335">**Nome do módulo**: @% SystemRoot% \\ System32 \\irprops.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-335">**Module name**: @%SystemRoot%\\System32\\irprops.cpl,-1</span></span>

### <a name="internet-options"></a><span data-ttu-id="7a489-336">Opções da Internet</span><span class="sxs-lookup"><span data-stu-id="7a489-336">Internet Options</span></span>

-   <span data-ttu-id="7a489-337">**Nome canônico**: Microsoft. InternetOptions</span><span class="sxs-lookup"><span data-stu-id="7a489-337">**Canonical name**: Microsoft.InternetOptions</span></span>
-   <span data-ttu-id="7a489-338">**GUID**: {A3DD4F92-658A-410f-84FD-6FBBBEF2FFFE}</span><span class="sxs-lookup"><span data-stu-id="7a489-338">**GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}</span></span>
-   <span data-ttu-id="7a489-339">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-339">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-340">**Nome do módulo**: @C: \\ Windows \\ System32 \\inetcpl.cpl,-4312</span><span class="sxs-lookup"><span data-stu-id="7a489-340">**Module name**: @C:\\Windows\\System32\\inetcpl.cpl,-4312</span></span>
-   <span data-ttu-id="7a489-341">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-341">**Pages**</span></span>

    | <span data-ttu-id="7a489-342">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-342">Page Name</span></span> | <span data-ttu-id="7a489-343">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-343">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="7a489-344">1</span><span class="sxs-lookup"><span data-stu-id="7a489-344">1</span></span>         | <span data-ttu-id="7a489-345">Segurança</span><span class="sxs-lookup"><span data-stu-id="7a489-345">Security</span></span>    |
    | <span data-ttu-id="7a489-346">2</span><span class="sxs-lookup"><span data-stu-id="7a489-346">2</span></span>         | <span data-ttu-id="7a489-347">Privacidade</span><span class="sxs-lookup"><span data-stu-id="7a489-347">Privacy</span></span>     |
    | <span data-ttu-id="7a489-348">3</span><span class="sxs-lookup"><span data-stu-id="7a489-348">3</span></span>         | <span data-ttu-id="7a489-349">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="7a489-349">Content</span></span>     |
    | <span data-ttu-id="7a489-350">4</span><span class="sxs-lookup"><span data-stu-id="7a489-350">4</span></span>         | <span data-ttu-id="7a489-351">conexões</span><span class="sxs-lookup"><span data-stu-id="7a489-351">Connections</span></span> |
    | <span data-ttu-id="7a489-352">5</span><span class="sxs-lookup"><span data-stu-id="7a489-352">5</span></span>         | <span data-ttu-id="7a489-353">Programas</span><span class="sxs-lookup"><span data-stu-id="7a489-353">Programs</span></span>    |
    | <span data-ttu-id="7a489-354">6</span><span class="sxs-lookup"><span data-stu-id="7a489-354">6</span></span>         | <span data-ttu-id="7a489-355">Avançado</span><span class="sxs-lookup"><span data-stu-id="7a489-355">Advanced</span></span>    |

    

     

### <a name="iscsi-initiator"></a><span data-ttu-id="7a489-356">Iniciador iSCSI</span><span class="sxs-lookup"><span data-stu-id="7a489-356">iSCSI Initiator</span></span>

-   <span data-ttu-id="7a489-357">**Nome canônico**: Microsoft. iSCSIInitiator</span><span class="sxs-lookup"><span data-stu-id="7a489-357">**Canonical name**: Microsoft.iSCSIInitiator</span></span>
-   <span data-ttu-id="7a489-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span><span class="sxs-lookup"><span data-stu-id="7a489-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span></span>
-   <span data-ttu-id="7a489-359">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-359">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-360">**Nome do módulo**: @% SystemRoot% \\ System32 \\iscsicpl.dll,-5001</span><span class="sxs-lookup"><span data-stu-id="7a489-360">**Module name**: @%SystemRoot%\\System32\\iscsicpl.dll,-5001</span></span>

### <a name="isns-server"></a><span data-ttu-id="7a489-361">iSNS Server</span><span class="sxs-lookup"><span data-stu-id="7a489-361">iSNS Server</span></span>

-   <span data-ttu-id="7a489-362">**Nome canônico**: Microsoft. iSNSServer</span><span class="sxs-lookup"><span data-stu-id="7a489-362">**Canonical name**: Microsoft.iSNSServer</span></span>
-   <span data-ttu-id="7a489-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span><span class="sxs-lookup"><span data-stu-id="7a489-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span></span>
-   <span data-ttu-id="7a489-364">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-364">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-365">**Nome do módulo**: @% SystemRoot% \\ System32 \\isnssrv.dll,-5005</span><span class="sxs-lookup"><span data-stu-id="7a489-365">**Module name**: @%SystemRoot%\\System32\\isnssrv.dll,-5005</span></span>
-   <span data-ttu-id="7a489-366">Este item do painel de controle será visto apenas nas versões de servidor do Windows.</span><span class="sxs-lookup"><span data-stu-id="7a489-366">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="keyboard"></a><span data-ttu-id="7a489-367">Keyboard</span><span class="sxs-lookup"><span data-stu-id="7a489-367">Keyboard</span></span>

-   <span data-ttu-id="7a489-368">**Nome canônico**: Microsoft. Keyboard</span><span class="sxs-lookup"><span data-stu-id="7a489-368">**Canonical name**: Microsoft.Keyboard</span></span>
-   <span data-ttu-id="7a489-369">**GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span><span class="sxs-lookup"><span data-stu-id="7a489-369">**GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span></span>
-   <span data-ttu-id="7a489-370">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-370">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-371">**Nome do módulo**: @% SystemRoot% \\ System32 \\main.cpl,-102</span><span class="sxs-lookup"><span data-stu-id="7a489-371">**Module name**: @%SystemRoot%\\System32\\main.cpl,-102</span></span>

### <a name="location-settings"></a><span data-ttu-id="7a489-372">Configurações de local</span><span class="sxs-lookup"><span data-stu-id="7a489-372">Location Settings</span></span>

-   <span data-ttu-id="7a489-373">**Nome canônico**: Microsoft. LocationSettings</span><span class="sxs-lookup"><span data-stu-id="7a489-373">**Canonical name**: Microsoft.LocationSettings</span></span>
-   <span data-ttu-id="7a489-374">**GUID**: {E9950154-C418-419E-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="7a489-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span></span>
-   <span data-ttu-id="7a489-375">**Sistema operacional com suporte**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-375">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-376">**Nome do módulo**: @% SystemRoot% \\ System32 \\SensorsCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-376">**Module name**: @%SystemRoot%\\System32\\SensorsCpl.dll,-1</span></span>

### <a name="mouse"></a><span data-ttu-id="7a489-377">Mouse</span><span class="sxs-lookup"><span data-stu-id="7a489-377">Mouse</span></span>

-   <span data-ttu-id="7a489-378">**Nome canônico**: Microsoft. mouse</span><span class="sxs-lookup"><span data-stu-id="7a489-378">**Canonical name**: Microsoft.Mouse</span></span>
-   <span data-ttu-id="7a489-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span><span class="sxs-lookup"><span data-stu-id="7a489-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span></span>
-   <span data-ttu-id="7a489-380">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-380">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-381">**Nome do módulo**: @% SystemRoot% \\ System32 \\main.cpl,-100</span><span class="sxs-lookup"><span data-stu-id="7a489-381">**Module name**: @%SystemRoot%\\System32\\main.cpl,-100</span></span>
-   <span data-ttu-id="7a489-382">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-382">**Pages**</span></span>

    | <span data-ttu-id="7a489-383">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-383">Page Name</span></span> | <span data-ttu-id="7a489-384">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-384">Opens</span></span>           |
    |-----------|-----------------|
    | <span data-ttu-id="7a489-385">1</span><span class="sxs-lookup"><span data-stu-id="7a489-385">1</span></span>         | <span data-ttu-id="7a489-386">Ponteiros</span><span class="sxs-lookup"><span data-stu-id="7a489-386">Pointers</span></span>        |
    | <span data-ttu-id="7a489-387">2</span><span class="sxs-lookup"><span data-stu-id="7a489-387">2</span></span>         | <span data-ttu-id="7a489-388">Opções de ponteiro</span><span class="sxs-lookup"><span data-stu-id="7a489-388">Pointer Options</span></span> |
    | <span data-ttu-id="7a489-389">3</span><span class="sxs-lookup"><span data-stu-id="7a489-389">3</span></span>         | <span data-ttu-id="7a489-390">Wheel</span><span class="sxs-lookup"><span data-stu-id="7a489-390">Wheel</span></span>           |
    | <span data-ttu-id="7a489-391">4</span><span class="sxs-lookup"><span data-stu-id="7a489-391">4</span></span>         | <span data-ttu-id="7a489-392">Hardware</span><span class="sxs-lookup"><span data-stu-id="7a489-392">Hardware</span></span>        |

    

     

### <a name="mpioconfiguration"></a><span data-ttu-id="7a489-393">MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a489-393">MPIOConfiguration</span></span>

-   <span data-ttu-id="7a489-394">**Nome canônico**: Microsoft. MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a489-394">**Canonical name**: Microsoft.MPIOConfiguration</span></span>
-   <span data-ttu-id="7a489-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span><span class="sxs-lookup"><span data-stu-id="7a489-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span></span>
-   <span data-ttu-id="7a489-396">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-396">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-397">**Nome do módulo**: @% SystemRoot% \\ System32 \\mpiocpl.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="7a489-397">**Module name**: @%SystemRoot%\\System32\\mpiocpl.dll,-1000</span></span>
-   <span data-ttu-id="7a489-398">Este item do painel de controle será visto apenas nas versões de servidor do Windows.</span><span class="sxs-lookup"><span data-stu-id="7a489-398">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="network-and-sharing-center"></a><span data-ttu-id="7a489-399">Centro de compartilhamento e de rede</span><span class="sxs-lookup"><span data-stu-id="7a489-399">Network and Sharing Center</span></span>

-   <span data-ttu-id="7a489-400">**Nome canônico**: Microsoft. NetworkAndSharingCenter</span><span class="sxs-lookup"><span data-stu-id="7a489-400">**Canonical name**: Microsoft.NetworkAndSharingCenter</span></span>
-   <span data-ttu-id="7a489-401">**GUID**: {8E908FC9-BECC-40F6-915B-F4CA0E70D03D}</span><span class="sxs-lookup"><span data-stu-id="7a489-401">**GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}</span></span>
-   <span data-ttu-id="7a489-402">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-402">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-403">**Nome do módulo**: @% SystemRoot% \\ System32 \\netcenter.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-403">**Module name**: @%SystemRoot%\\System32\\netcenter.dll,-1</span></span>
-   <span data-ttu-id="7a489-404">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-404">**Pages**</span></span>

    | <span data-ttu-id="7a489-405">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-405">Page Name</span></span>  | <span data-ttu-id="7a489-406">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-406">Opens</span></span>                     |
    |------------|---------------------------|
    | <span data-ttu-id="7a489-407">Avançado</span><span class="sxs-lookup"><span data-stu-id="7a489-407">Advanced</span></span>   | <span data-ttu-id="7a489-408">Configurações de compartilhamento avançadas</span><span class="sxs-lookup"><span data-stu-id="7a489-408">Advanced sharing settings</span></span> |
    | <span data-ttu-id="7a489-409">ShareMedia</span><span class="sxs-lookup"><span data-stu-id="7a489-409">ShareMedia</span></span> | <span data-ttu-id="7a489-410">Opções de streaming de mídia</span><span class="sxs-lookup"><span data-stu-id="7a489-410">Media streaming options</span></span>   |

    

     

### <a name="notification-area-icons"></a><span data-ttu-id="7a489-411">Ícones da área de notificação</span><span class="sxs-lookup"><span data-stu-id="7a489-411">Notification Area Icons</span></span>

-   <span data-ttu-id="7a489-412">**Nome canônico**: Microsoft. NotificationAreaIcons</span><span class="sxs-lookup"><span data-stu-id="7a489-412">**Canonical name**: Microsoft.NotificationAreaIcons</span></span>
-   <span data-ttu-id="7a489-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span><span class="sxs-lookup"><span data-stu-id="7a489-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span></span>
-   <span data-ttu-id="7a489-414">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-414">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-415">**Nome do módulo**: @% SystemRoot% \\ System32 \\taskbarcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-415">**Module name**: @%SystemRoot%\\System32\\taskbarcpl.dll,-1</span></span>

### <a name="pen-and-touch"></a><span data-ttu-id="7a489-416">Caneta e toque</span><span class="sxs-lookup"><span data-stu-id="7a489-416">Pen and Touch</span></span>

-   <span data-ttu-id="7a489-417">**Nome canônico**: Microsoft. PenAndTouch</span><span class="sxs-lookup"><span data-stu-id="7a489-417">**Canonical name**: Microsoft.PenAndTouch</span></span>
-   <span data-ttu-id="7a489-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="7a489-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span>
-   <span data-ttu-id="7a489-419">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-419">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-420">**Nome do módulo**: @% SystemRoot% \\ System32 \\tabletpc.cpl,-10103</span><span class="sxs-lookup"><span data-stu-id="7a489-420">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10103</span></span>
-   <span data-ttu-id="7a489-421">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-421">**Pages**</span></span>

    | <span data-ttu-id="7a489-422">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-422">Page Name</span></span> | <span data-ttu-id="7a489-423">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-423">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="7a489-424">1</span><span class="sxs-lookup"><span data-stu-id="7a489-424">1</span></span>         | <span data-ttu-id="7a489-425">Movimentos</span><span class="sxs-lookup"><span data-stu-id="7a489-425">Flicks</span></span>      |
    | <span data-ttu-id="7a489-426">2</span><span class="sxs-lookup"><span data-stu-id="7a489-426">2</span></span>         | <span data-ttu-id="7a489-427">Handwriting</span><span class="sxs-lookup"><span data-stu-id="7a489-427">Handwriting</span></span> |

    

     

### <a name="personalization"></a><span data-ttu-id="7a489-428">Personalização</span><span class="sxs-lookup"><span data-stu-id="7a489-428">Personalization</span></span>

-   <span data-ttu-id="7a489-429">**Nome canônico**: Microsoft. Personalization</span><span class="sxs-lookup"><span data-stu-id="7a489-429">**Canonical name**: Microsoft.Personalization</span></span>
-   <span data-ttu-id="7a489-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span><span class="sxs-lookup"><span data-stu-id="7a489-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span></span>
-   <span data-ttu-id="7a489-431">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-431">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-432">**Nome do módulo**: @% SystemRoot% \\ System32 \\themecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-432">**Module name**: @%SystemRoot%\\System32\\themecpl.dll,-1</span></span>
-   <span data-ttu-id="7a489-433">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-433">**Pages**</span></span>

    | <span data-ttu-id="7a489-434">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-434">Page Name</span></span>        | <span data-ttu-id="7a489-435">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-435">Opens</span></span>                |
    |------------------|----------------------|
    | <span data-ttu-id="7a489-436">pageColorization</span><span class="sxs-lookup"><span data-stu-id="7a489-436">pageColorization</span></span> | <span data-ttu-id="7a489-437">Cor e aparência</span><span class="sxs-lookup"><span data-stu-id="7a489-437">Color and Appearance</span></span> |
    | <span data-ttu-id="7a489-438">pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="7a489-438">pageWallpaper</span></span>    | <span data-ttu-id="7a489-439">Segundo plano da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="7a489-439">Desktop Background</span></span>   |

    

     

### <a name="phone-and-modem"></a><span data-ttu-id="7a489-440">Telefone e modem</span><span class="sxs-lookup"><span data-stu-id="7a489-440">Phone and Modem</span></span>

-   <span data-ttu-id="7a489-441">**Nome canônico**: Microsoft. PhoneAndModem</span><span class="sxs-lookup"><span data-stu-id="7a489-441">**Canonical name**: Microsoft.PhoneAndModem</span></span>
-   <span data-ttu-id="7a489-442">**GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="7a489-442">**GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}</span></span>
-   <span data-ttu-id="7a489-443">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-443">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-444">**Nome do módulo**: @% SystemRoot% \\ System32 \\telephon.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-444">**Module name**: @%SystemRoot%\\System32\\telephon.cpl,-1</span></span>
-   <span data-ttu-id="7a489-445">A janela que esse valor inicia é intitulada "informações de local" em versões do Windows anteriores ao Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a489-445">The window that this value launches is titled "Location Information" in versions of Windows prior to Windows 8.</span></span> <span data-ttu-id="7a489-446">A interface do usuário do item é consideravelmente alterada a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a489-446">The item's UI is considerably changed as of Windows 8.</span></span>

### <a name="power-options"></a><span data-ttu-id="7a489-447">Opções de Energia</span><span class="sxs-lookup"><span data-stu-id="7a489-447">Power Options</span></span>

-   <span data-ttu-id="7a489-448">**Nome canônico**: Microsoft. poweroptions</span><span class="sxs-lookup"><span data-stu-id="7a489-448">**Canonical name**: Microsoft.PowerOptions</span></span>
-   <span data-ttu-id="7a489-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span><span class="sxs-lookup"><span data-stu-id="7a489-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span></span>
-   <span data-ttu-id="7a489-450">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-450">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-451">**Nome do módulo**: @% SystemRoot% \\ System32 \\powercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-451">**Module name**: @%SystemRoot%\\System32\\powercpl.dll,-1</span></span>
-   <span data-ttu-id="7a489-452">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-452">**Pages**</span></span>

    | <span data-ttu-id="7a489-453">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-453">Page Name</span></span>          | <span data-ttu-id="7a489-454">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-454">Opens</span></span>              |
    |--------------------|--------------------|
    | <span data-ttu-id="7a489-455">pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="7a489-455">pageGlobalSettings</span></span> | <span data-ttu-id="7a489-456">Configurações do sistema</span><span class="sxs-lookup"><span data-stu-id="7a489-456">System Settings</span></span>    |
    | <span data-ttu-id="7a489-457">pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="7a489-457">pagePlanSettings</span></span>   | <span data-ttu-id="7a489-458">Editar configurações do plano</span><span class="sxs-lookup"><span data-stu-id="7a489-458">Edit Plan Settings</span></span> |

    

     

### <a name="programs-and-features"></a><span data-ttu-id="7a489-459">Programas e Recursos</span><span class="sxs-lookup"><span data-stu-id="7a489-459">Programs and Features</span></span>

-   <span data-ttu-id="7a489-460">**Nome canônico**: Microsoft. ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="7a489-460">**Canonical name**: Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="7a489-461">**GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span><span class="sxs-lookup"><span data-stu-id="7a489-461">**GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span></span>
-   <span data-ttu-id="7a489-462">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-462">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-463">**Nome do módulo**: @% SystemRoot% \\ System32 \\appwiz.cpl,-159</span><span class="sxs-lookup"><span data-stu-id="7a489-463">**Module name**: @%systemroot%\\system32\\appwiz.cpl,-159</span></span>
-   <span data-ttu-id="7a489-464">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-464">**Pages**</span></span>

    | <span data-ttu-id="7a489-465">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-465">Page Name</span></span>                                | <span data-ttu-id="7a489-466">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-466">Opens</span></span>             |
    |------------------------------------------|-------------------|
    | <span data-ttu-id="7a489-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span><span class="sxs-lookup"><span data-stu-id="7a489-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span></span> | <span data-ttu-id="7a489-468">Atualizações instaladas</span><span class="sxs-lookup"><span data-stu-id="7a489-468">Installed Updates</span></span> |

    

     

### <a name="recovery"></a><span data-ttu-id="7a489-469">Recuperação</span><span class="sxs-lookup"><span data-stu-id="7a489-469">Recovery</span></span>

-   <span data-ttu-id="7a489-470">**Nome canônico**: Microsoft. Recovery</span><span class="sxs-lookup"><span data-stu-id="7a489-470">**Canonical name**: Microsoft.Recovery</span></span>
-   <span data-ttu-id="7a489-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span><span class="sxs-lookup"><span data-stu-id="7a489-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span></span>
-   <span data-ttu-id="7a489-472">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-472">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-473">**Nome do módulo**: @% SystemRoot% \\ System32 \\recovery.dll,-101</span><span class="sxs-lookup"><span data-stu-id="7a489-473">**Module name**: @%SystemRoot%\\System32\\recovery.dll,-101</span></span>

### <a name="region"></a><span data-ttu-id="7a489-474">Região</span><span class="sxs-lookup"><span data-stu-id="7a489-474">Region</span></span>

-   <span data-ttu-id="7a489-475">**Nome canônico**: Microsoft. RegionAndLanguage</span><span class="sxs-lookup"><span data-stu-id="7a489-475">**Canonical name**: Microsoft.RegionAndLanguage</span></span>
-   <span data-ttu-id="7a489-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="7a489-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span>
-   <span data-ttu-id="7a489-477">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-477">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-478">**Nome do módulo**: @% SystemRoot% \\ System32 \\intl.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-478">**Module name**: @%SystemRoot%\\System32\\intl.cpl,-1</span></span>
-   <span data-ttu-id="7a489-479">A região e o item de idioma encontrados no Windows 7 foram divididos a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a489-479">The Region and Language item found in Windows 7 was split as of Windows 8.</span></span> <span data-ttu-id="7a489-480">O Microsoft. RegionAndLanguage agora inicia o item de região.</span><span class="sxs-lookup"><span data-stu-id="7a489-480">Microsoft.RegionAndLanguage now launches the Region item.</span></span> <span data-ttu-id="7a489-481">Para iniciar o item de idioma, use [Microsoft. Language](#location-settings).</span><span class="sxs-lookup"><span data-stu-id="7a489-481">To launch the Language item, use [Microsoft.Language](#location-settings).</span></span>
-   <span data-ttu-id="7a489-482">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-482">**Pages**</span></span>

    | <span data-ttu-id="7a489-483">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-483">Page Name</span></span> | <span data-ttu-id="7a489-484">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-484">Opens</span></span>          |
    |-----------|----------------|
    | <span data-ttu-id="7a489-485">1</span><span class="sxs-lookup"><span data-stu-id="7a489-485">1</span></span>         | <span data-ttu-id="7a489-486">Localização</span><span class="sxs-lookup"><span data-stu-id="7a489-486">Location</span></span>       |
    | <span data-ttu-id="7a489-487">2</span><span class="sxs-lookup"><span data-stu-id="7a489-487">2</span></span>         | <span data-ttu-id="7a489-488">Administrativa</span><span class="sxs-lookup"><span data-stu-id="7a489-488">Administrative</span></span> |

    

     

### <a name="remoteapp-and-desktop-connections"></a><span data-ttu-id="7a489-489">Conexões de RemoteApp e Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="7a489-489">RemoteApp and Desktop Connections</span></span>

-   <span data-ttu-id="7a489-490">**Nome canônico**: Microsoft. RemoteAppAndDesktopConnections</span><span class="sxs-lookup"><span data-stu-id="7a489-490">**Canonical name**: Microsoft.RemoteAppAndDesktopConnections</span></span>
-   <span data-ttu-id="7a489-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span><span class="sxs-lookup"><span data-stu-id="7a489-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span></span>
-   <span data-ttu-id="7a489-492">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-492">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-493">**Nome do módulo**: @% SystemRoot% \\ System32 \\tsworkspace.dll,-15300</span><span class="sxs-lookup"><span data-stu-id="7a489-493">**Module name**: @%SystemRoot%\\System32\\tsworkspace.dll,-15300</span></span>

### <a name="sound"></a><span data-ttu-id="7a489-494">Som</span><span class="sxs-lookup"><span data-stu-id="7a489-494">Sound</span></span>

-   <span data-ttu-id="7a489-495">**Nome canônico**: Microsoft. Sound</span><span class="sxs-lookup"><span data-stu-id="7a489-495">**Canonical name**: Microsoft.Sound</span></span>
-   <span data-ttu-id="7a489-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="7a489-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span>
-   <span data-ttu-id="7a489-497">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-497">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-498">**Nome do módulo**: @% SystemRoot% \\ System32 \\mmsys.cpl,-300</span><span class="sxs-lookup"><span data-stu-id="7a489-498">**Module name**: @%SystemRoot%\\System32\\mmsys.cpl,-300</span></span>

### <a name="speech-recognition"></a><span data-ttu-id="7a489-499">Reconhecimento de fala</span><span class="sxs-lookup"><span data-stu-id="7a489-499">Speech Recognition</span></span>

-   <span data-ttu-id="7a489-500">**Nome canônico**: Microsoft. SpeechRecognition</span><span class="sxs-lookup"><span data-stu-id="7a489-500">**Canonical name**: Microsoft.SpeechRecognition</span></span>
-   <span data-ttu-id="7a489-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="7a489-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span></span>
-   <span data-ttu-id="7a489-502">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-502">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-503">**Nome do módulo**: @% SystemRoot% \\ System32 \\ Speech \\ SpeechUX \\speechuxcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-503">**Module name**: @%SystemRoot%\\System32\\Speech\\SpeechUX\\speechuxcpl.dll,-1</span></span>

### <a name="storage-spaces"></a><span data-ttu-id="7a489-504">Espaços de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="7a489-504">Storage Spaces</span></span>

-   <span data-ttu-id="7a489-505">**Nome canônico**: Microsoft. StorageSpaces</span><span class="sxs-lookup"><span data-stu-id="7a489-505">**Canonical name**: Microsoft.StorageSpaces</span></span>
-   <span data-ttu-id="7a489-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span><span class="sxs-lookup"><span data-stu-id="7a489-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span></span>
-   <span data-ttu-id="7a489-507">**Sistema operacional com suporte**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-507">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-508">**Nome do módulo**: @C: \\ Windows \\ System32 \\SpaceControl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-508">**Module name**: @C:\\Windows\\System32\\SpaceControl.dll,-1</span></span>

### <a name="sync-center"></a><span data-ttu-id="7a489-509">Central de Sincronização</span><span class="sxs-lookup"><span data-stu-id="7a489-509">Sync Center</span></span>

-   <span data-ttu-id="7a489-510">**Nome canônico**: Microsoft. SyncCenter</span><span class="sxs-lookup"><span data-stu-id="7a489-510">**Canonical name**: Microsoft.SyncCenter</span></span>
-   <span data-ttu-id="7a489-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span><span class="sxs-lookup"><span data-stu-id="7a489-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span></span>
-   <span data-ttu-id="7a489-512">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-512">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-513">**Nome do módulo**: @% SystemRoot% \\ System32 \\SyncCenter.dll,-3000</span><span class="sxs-lookup"><span data-stu-id="7a489-513">**Module name**: @%SystemRoot%\\System32\\SyncCenter.dll,-3000</span></span>

### <a name="system"></a><span data-ttu-id="7a489-514">Sistema</span><span class="sxs-lookup"><span data-stu-id="7a489-514">System</span></span>

-   <span data-ttu-id="7a489-515">**Nome canônico**: Microsoft.System</span><span class="sxs-lookup"><span data-stu-id="7a489-515">**Canonical name**: Microsoft.System</span></span>
-   <span data-ttu-id="7a489-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span><span class="sxs-lookup"><span data-stu-id="7a489-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span></span>
-   <span data-ttu-id="7a489-517">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-517">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-518">**Nome do módulo**: @% SystemRoot% \\ System32 \\systemcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-518">**Module name**: @%SystemRoot%\\System32\\systemcpl.dll,-1</span></span>

### <a name="tablet-pc-settings"></a><span data-ttu-id="7a489-519">Configurações do Tablet PC</span><span class="sxs-lookup"><span data-stu-id="7a489-519">Tablet PC Settings</span></span>

-   <span data-ttu-id="7a489-520">**Nome canônico**: Microsoft. TabletPCSettings</span><span class="sxs-lookup"><span data-stu-id="7a489-520">**Canonical name**: Microsoft.TabletPCSettings</span></span>
-   <span data-ttu-id="7a489-521">**GUID**: {80F3F1D5-Feca-45F3-BC32-752C152E456E}</span><span class="sxs-lookup"><span data-stu-id="7a489-521">**GUID**: {80F3F1D5-FECA-45F3-BC32-752C152E456E}</span></span>
-   <span data-ttu-id="7a489-522">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-522">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-523">**Nome do módulo**: @% SystemRoot% \\ System32 \\tabletpc.cpl,-10100</span><span class="sxs-lookup"><span data-stu-id="7a489-523">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10100</span></span>

### <a name="taskbar-and-navigation"></a><span data-ttu-id="7a489-524">Barra de tarefas e navegação</span><span class="sxs-lookup"><span data-stu-id="7a489-524">Taskbar and Navigation</span></span>

-   <span data-ttu-id="7a489-525">**Nome canônico**: Microsoft. Taskbar</span><span class="sxs-lookup"><span data-stu-id="7a489-525">**Canonical name**: Microsoft.Taskbar</span></span>
-   <span data-ttu-id="7a489-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="7a489-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span>
-   <span data-ttu-id="7a489-527">**Sistema operacional com suporte**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-527">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-528">**Nome do módulo**: @% SystemRoot% \\ System32 \\shell32.dll,-32517</span><span class="sxs-lookup"><span data-stu-id="7a489-528">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-32517</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="7a489-529">Solução de problemas</span><span class="sxs-lookup"><span data-stu-id="7a489-529">Troubleshooting</span></span>

-   <span data-ttu-id="7a489-530">**Nome canônico**: Microsoft. Troubleshooting</span><span class="sxs-lookup"><span data-stu-id="7a489-530">**Canonical name**: Microsoft.Troubleshooting</span></span>
-   <span data-ttu-id="7a489-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span><span class="sxs-lookup"><span data-stu-id="7a489-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span></span>
-   <span data-ttu-id="7a489-532">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-532">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-533">**Nome do módulo**: @% SystemRoot% \\ System32 \\DiagCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-533">**Module name**: @%SystemRoot%\\System32\\DiagCpl.dll,-1</span></span>
-   <span data-ttu-id="7a489-534">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-534">**Pages**</span></span>

    | <span data-ttu-id="7a489-535">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-535">Page Name</span></span>   | <span data-ttu-id="7a489-536">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-536">Opens</span></span>   |
    |-------------|---------|
    | <span data-ttu-id="7a489-537">HistoryPage</span><span class="sxs-lookup"><span data-stu-id="7a489-537">HistoryPage</span></span> | <span data-ttu-id="7a489-538">Histórico</span><span class="sxs-lookup"><span data-stu-id="7a489-538">History</span></span> |

    

     

### <a name="tsappinstall"></a><span data-ttu-id="7a489-539">TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="7a489-539">TSAppInstall</span></span>

-   <span data-ttu-id="7a489-540">**Nome canônico**: Microsoft. TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="7a489-540">**Canonical name**: Microsoft.TSAppInstall</span></span>
-   <span data-ttu-id="7a489-541">**GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span><span class="sxs-lookup"><span data-stu-id="7a489-541">**GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span></span>
-   <span data-ttu-id="7a489-542">**Sistema operacional com suporte**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-542">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-543">**Nome do módulo**: @% SystemRoot% \\ System32 \\tsappinstall.exe,-2001</span><span class="sxs-lookup"><span data-stu-id="7a489-543">**Module name**: @%systemroot%\\system32\\tsappinstall.exe,-2001</span></span>

### <a name="user-accounts"></a><span data-ttu-id="7a489-544">Contas de usuário</span><span class="sxs-lookup"><span data-stu-id="7a489-544">User Accounts</span></span>

-   <span data-ttu-id="7a489-545">**Nome canônico**: Microsoft. Accounts</span><span class="sxs-lookup"><span data-stu-id="7a489-545">**Canonical name**: Microsoft.UserAccounts</span></span>
-   <span data-ttu-id="7a489-546">**GUID**: {60632754-C523-4b62-b45c-4172da012619}</span><span class="sxs-lookup"><span data-stu-id="7a489-546">**GUID**: {60632754-c523-4b62-b45c-4172da012619}</span></span>
-   <span data-ttu-id="7a489-547">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-547">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-548">**Nome do módulo**: @% SystemRoot% \\ System32 \\usercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-548">**Module name**: @%SystemRoot%\\System32\\usercpl.dll,-1</span></span>

### <a name="windows-anytime-upgrade"></a><span data-ttu-id="7a489-549">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="7a489-549">Windows Anytime Upgrade</span></span>

-   <span data-ttu-id="7a489-550">**Nome canônico**: Microsoft. WindowsAnytimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="7a489-550">**Canonical name**: Microsoft.WindowsAnytimeUpgrade</span></span>
-   <span data-ttu-id="7a489-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span><span class="sxs-lookup"><span data-stu-id="7a489-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span></span>
-   <span data-ttu-id="7a489-552">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-552">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-553">**Nome do módulo**: @ $ (resourcestring. \_ \_Caminho sys mod \_ ),-1</span><span class="sxs-lookup"><span data-stu-id="7a489-553">**Module name**: @$(resourceString.\_SYS\_MOD\_PATH),-1</span></span>

### <a name="windows-defender"></a><span data-ttu-id="7a489-554">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="7a489-554">Windows Defender</span></span>

-   <span data-ttu-id="7a489-555">**Nome canônico**: Microsoft. WindowsDefender</span><span class="sxs-lookup"><span data-stu-id="7a489-555">**Canonical name**: Microsoft.WindowsDefender</span></span>
-   <span data-ttu-id="7a489-556">**GUID**: {D8559EB9-20C0-410E-Beda-7ED416AECC2A}</span><span class="sxs-lookup"><span data-stu-id="7a489-556">**GUID**: {D8559EB9-20C0-410E-BEDA-7ED416AECC2A}</span></span>
-   <span data-ttu-id="7a489-557">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-557">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-558">**Nome do módulo**: @% ProgramFiles% \\ Windows Defender \\MsMpRes.dll,-104</span><span class="sxs-lookup"><span data-stu-id="7a489-558">**Module name**: @%ProgramFiles%\\Windows Defender\\MsMpRes.dll,-104</span></span>

### <a name="windows-firewall"></a><span data-ttu-id="7a489-559">Firewall do Windows</span><span class="sxs-lookup"><span data-stu-id="7a489-559">Windows Firewall</span></span>

-   <span data-ttu-id="7a489-560">**Nome canônico**: Microsoft. WindowsFirewall</span><span class="sxs-lookup"><span data-stu-id="7a489-560">**Canonical name**: Microsoft.WindowsFirewall</span></span>
-   <span data-ttu-id="7a489-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span><span class="sxs-lookup"><span data-stu-id="7a489-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span></span>
-   <span data-ttu-id="7a489-562">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-562">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-563">**Nome do módulo**: @C: \\ Windows \\ System32 \\FirewallControlPanel.dll,-12122</span><span class="sxs-lookup"><span data-stu-id="7a489-563">**Module name**: @C:\\Windows\\system32\\FirewallControlPanel.dll,-12122</span></span>
-   <span data-ttu-id="7a489-564">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-564">**Pages**</span></span>

    | <span data-ttu-id="7a489-565">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-565">Page Name</span></span>         | <span data-ttu-id="7a489-566">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-566">Opens</span></span>        |
    |-------------------|--------------|
    | <span data-ttu-id="7a489-567">pageConfigureApps</span><span class="sxs-lookup"><span data-stu-id="7a489-567">pageConfigureApps</span></span> | <span data-ttu-id="7a489-568">Aplicativos permitidos</span><span class="sxs-lookup"><span data-stu-id="7a489-568">Allowed apps</span></span> |

    

     

### <a name="windows-mobility-center"></a><span data-ttu-id="7a489-569">Centro de Mobilidade do Windows</span><span class="sxs-lookup"><span data-stu-id="7a489-569">Windows Mobility Center</span></span>

-   <span data-ttu-id="7a489-570">**Nome canônico**: Microsoft. MobilityCenter</span><span class="sxs-lookup"><span data-stu-id="7a489-570">**Canonical name**: Microsoft.MobilityCenter</span></span>
-   <span data-ttu-id="7a489-571">**GUID**: {5ea4f148-308C-46d7-98a9-49041b1dd468}</span><span class="sxs-lookup"><span data-stu-id="7a489-571">**GUID**: {5ea4f148-308c-46d7-98a9-49041b1dd468}</span></span>
-   <span data-ttu-id="7a489-572">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-572">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-573">**Nome do módulo**: @% SystemRoot% \\ System32 \\mblctr.exe,-1002</span><span class="sxs-lookup"><span data-stu-id="7a489-573">**Module name**: @%SystemRoot%\\system32\\mblctr.exe,-1002</span></span>

### <a name="windows-to-go"></a><span data-ttu-id="7a489-574">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="7a489-574">Windows To Go</span></span>

-   <span data-ttu-id="7a489-575">**Nome canônico**: Microsoft. PortableWorkspaceCreator</span><span class="sxs-lookup"><span data-stu-id="7a489-575">**Canonical name**: Microsoft.PortableWorkspaceCreator</span></span>
-   <span data-ttu-id="7a489-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span><span class="sxs-lookup"><span data-stu-id="7a489-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span></span>
-   <span data-ttu-id="7a489-577">**Sistema operacional com suporte**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-577">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-578">**Nome do módulo**: @% SystemRoot% \\ System32 \\pwcreator.exe,-151</span><span class="sxs-lookup"><span data-stu-id="7a489-578">**Module name**: @%SystemRoot%\\System32\\pwcreator.exe,-151</span></span>

### <a name="windows-update"></a><span data-ttu-id="7a489-579">Windows Update</span><span class="sxs-lookup"><span data-stu-id="7a489-579">Windows Update</span></span>

-   <span data-ttu-id="7a489-580">**Nome canônico**: Microsoft. windowsupdate</span><span class="sxs-lookup"><span data-stu-id="7a489-580">**Canonical name**: Microsoft.WindowsUpdate</span></span>
-   <span data-ttu-id="7a489-581">**GUID**: {36eef7db-88ad-4e81-ad49-0e313f0c35f8}</span><span class="sxs-lookup"><span data-stu-id="7a489-581">**GUID**: {36eef7db-88ad-4e81-ad49-0e313f0c35f8}</span></span>
-   <span data-ttu-id="7a489-582">**Sistema operacional com suporte**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-582">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="7a489-583">**Nome do módulo**: @% SystemRoot% \\ System32 \\wucltux.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-583">**Module name**: @%SystemRoot%\\system32\\wucltux.dll,-1</span></span>
-   <span data-ttu-id="7a489-584">**Páginas**</span><span class="sxs-lookup"><span data-stu-id="7a489-584">**Pages**</span></span>

    | <span data-ttu-id="7a489-585">Nome da Página</span><span class="sxs-lookup"><span data-stu-id="7a489-585">Page Name</span></span>         | <span data-ttu-id="7a489-586">Abre</span><span class="sxs-lookup"><span data-stu-id="7a489-586">Opens</span></span>               |
    |-------------------|---------------------|
    | <span data-ttu-id="7a489-587">pageSettings</span><span class="sxs-lookup"><span data-stu-id="7a489-587">pageSettings</span></span>      | <span data-ttu-id="7a489-588">Alterar configurações</span><span class="sxs-lookup"><span data-stu-id="7a489-588">Change settings</span></span>     |
    | <span data-ttu-id="7a489-589">pageUpdateHistory</span><span class="sxs-lookup"><span data-stu-id="7a489-589">pageUpdateHistory</span></span> | <span data-ttu-id="7a489-590">Exibir histórico de atualizações</span><span class="sxs-lookup"><span data-stu-id="7a489-590">View update history</span></span> |

    

     

### <a name="work-folders"></a><span data-ttu-id="7a489-591">Pastas de trabalho</span><span class="sxs-lookup"><span data-stu-id="7a489-591">Work Folders</span></span>

-   <span data-ttu-id="7a489-592">**Nome canônico**: Microsoft. WorkFolders</span><span class="sxs-lookup"><span data-stu-id="7a489-592">**Canonical name**: Microsoft.WorkFolders</span></span>
-   <span data-ttu-id="7a489-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span><span class="sxs-lookup"><span data-stu-id="7a489-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span></span>
-   <span data-ttu-id="7a489-594">**Sistema operacional com suporte**: Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7a489-594">**Supported OS**: Windows 8.1</span></span>
-   <span data-ttu-id="7a489-595">**Nome do módulo**: @C: \\ Windows \\ System32 \\WorkfoldersControl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="7a489-595">**Module name**: @C:\\Windows\\System32\\WorkfoldersControl.dll,-1</span></span>

## <a name="deprecated-control-panel-canonical-names"></a><span data-ttu-id="7a489-596">Nomes canônicos do painel de controle preteridos</span><span class="sxs-lookup"><span data-stu-id="7a489-596">Deprecated Control Panel Canonical Names</span></span>

<span data-ttu-id="7a489-597">Veja a seguir os nomes canônicos que não estão mais em uso a partir de Windows 8.1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7a489-597">The following are canonical names that are no longer in use as of Windows 8.1 or later.</span></span> <span data-ttu-id="7a489-598">Alguns foram completamente removidos.</span><span class="sxs-lookup"><span data-stu-id="7a489-598">Some have been removed altogether.</span></span> <span data-ttu-id="7a489-599">Outros foram remapeados nessas situações:</span><span class="sxs-lookup"><span data-stu-id="7a489-599">Others have been remapped in these situations:</span></span>

-   <span data-ttu-id="7a489-600">Um item do painel de controle é renomeado.</span><span class="sxs-lookup"><span data-stu-id="7a489-600">A Control Panel item is renamed.</span></span> <span data-ttu-id="7a489-601">O item renomeado recebe um novo nome canônico, mas mantém o mesmo GUID.</span><span class="sxs-lookup"><span data-stu-id="7a489-601">The renamed item is given a new canonical name but keeps the same GUID.</span></span> <span data-ttu-id="7a489-602">Nesse caso, o antigo nome canônico inicia o item do painel de controle renomeado.</span><span class="sxs-lookup"><span data-stu-id="7a489-602">In this case, the old canonical name launches the renamed Control Panel item.</span></span> <span data-ttu-id="7a489-603">Lembre-se de que o item que é iniciado pode não usar a mesma interface do usuário que a versão mais antiga do item.</span><span class="sxs-lookup"><span data-stu-id="7a489-603">Be aware that the item that's launched might not use the same UI as that item's older version.</span></span>
-   <span data-ttu-id="7a489-604">A funcionalidade de um ou mais itens do painel de controle é movida ou consolidada em um novo item.</span><span class="sxs-lookup"><span data-stu-id="7a489-604">The functionality of one or more Control Panel items is moved or consolidated into a new item.</span></span> <span data-ttu-id="7a489-605">Nesse caso, o nome canônico antigo é mapeado para o novo item mais apropriado do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="7a489-605">In this case, the old canonical name maps to the most appropriate new Control Panel item.</span></span>

> [!Note]  
> <span data-ttu-id="7a489-606">Existem remapeamentos para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="7a489-606">Remappings exist for backward compatibility.</span></span> <span data-ttu-id="7a489-607">Você não deve usar valores preteridos no novo código.</span><span class="sxs-lookup"><span data-stu-id="7a489-607">You should not use deprecated values in new code.</span></span>

 



| <span data-ttu-id="7a489-608">Nome canônico preterido</span><span class="sxs-lookup"><span data-stu-id="7a489-608">Deprecated canonical name</span></span>                                   | <span data-ttu-id="7a489-609">Item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7a489-609">Control Panel Item</span></span>                | <span data-ttu-id="7a489-610">GUID</span><span class="sxs-lookup"><span data-stu-id="7a489-610">GUID</span></span>                                   | <span data-ttu-id="7a489-611">Observações</span><span class="sxs-lookup"><span data-stu-id="7a489-611">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a489-612">Microsoft. addduro</span><span class="sxs-lookup"><span data-stu-id="7a489-612">Microsoft.AddHardware</span></span>                                       | <span data-ttu-id="7a489-613">Adicionar hardware</span><span class="sxs-lookup"><span data-stu-id="7a489-613">Add Hardware</span></span>                      | <span data-ttu-id="7a489-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span><span class="sxs-lookup"><span data-stu-id="7a489-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span></span> | <span data-ttu-id="7a489-615">Mapeia para [Microsoft. DevicesAndPrinters](#devices-and-printers) a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-615">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7a489-616">Microsoft. AudioDevicesAndSoundThemes</span><span class="sxs-lookup"><span data-stu-id="7a489-616">Microsoft.AudioDevicesAndSoundThemes</span></span>                        | <span data-ttu-id="7a489-617">Som</span><span class="sxs-lookup"><span data-stu-id="7a489-617">Sound</span></span>                             | <span data-ttu-id="7a489-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="7a489-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span> | <span data-ttu-id="7a489-619">Mapeia para [Microsoft. Sound](#sound) a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-619">Maps to [Microsoft.Sound](#sound) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7a489-620">Microsoft. BackupAndRestoreCenter/Microsoft. BackupAndRestore</span><span class="sxs-lookup"><span data-stu-id="7a489-620">Microsoft.BackupAndRestoreCenter/Microsoft.BackupAndRestore</span></span> | <span data-ttu-id="7a489-621">Centro de backup e restauração</span><span class="sxs-lookup"><span data-stu-id="7a489-621">Backup and Restore Center</span></span>         | <span data-ttu-id="7a489-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span><span class="sxs-lookup"><span data-stu-id="7a489-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span></span> | <span data-ttu-id="7a489-623">O Microsoft. BackupAndRestoreCenter é mapeado para Microsoft. BackupAndRestore no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-623">Microsoft.BackupAndRestoreCenter maps to Microsoft.BackupAndRestore in Windows 7.</span></span> <span data-ttu-id="7a489-624">Ambos são removidos a partir do Windows 8; em vez disso, use [o Microsoft. filehistory](#file-history) .</span><span class="sxs-lookup"><span data-stu-id="7a489-624">Both are removed as of Windows 8; use [Microsoft.FileHistory](#file-history) instead.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="7a489-625">Microsoft. CardSpace</span><span class="sxs-lookup"><span data-stu-id="7a489-625">Microsoft.CardSpace</span></span>                                         | <span data-ttu-id="7a489-626">Windows CardSpace</span><span class="sxs-lookup"><span data-stu-id="7a489-626">Windows CardSpace</span></span>                 | <span data-ttu-id="7a489-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span><span class="sxs-lookup"><span data-stu-id="7a489-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span></span> | <span data-ttu-id="7a489-628">Removido do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a489-628">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7a489-629">Microsoft. DesktopGadgets</span><span class="sxs-lookup"><span data-stu-id="7a489-629">Microsoft.DesktopGadgets</span></span>                                    | <span data-ttu-id="7a489-630">Gadgets de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="7a489-630">Desktop Gadgets</span></span>                   | <span data-ttu-id="7a489-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="7a489-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="7a489-632">Removido do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a489-632">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7a489-633">Microsoft. GetProgramsOnline</span><span class="sxs-lookup"><span data-stu-id="7a489-633">Microsoft.GetProgramsOnline</span></span>                                 | <span data-ttu-id="7a489-634">Windows Marketplace</span><span class="sxs-lookup"><span data-stu-id="7a489-634">Windows Marketplace</span></span>               | <span data-ttu-id="7a489-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span><span class="sxs-lookup"><span data-stu-id="7a489-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span></span> | <span data-ttu-id="7a489-636">Removido do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-636">Removed as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7a489-637">Microsoft. Infravermelhooptions</span><span class="sxs-lookup"><span data-stu-id="7a489-637">Microsoft.InfraredOptions</span></span>                                   | <span data-ttu-id="7a489-638">Infravermelho</span><span class="sxs-lookup"><span data-stu-id="7a489-638">Infrared</span></span>                          | <span data-ttu-id="7a489-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="7a489-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span> | <span data-ttu-id="7a489-640">Mapeia para [Microsoft. infravermelho](#infrared) a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-640">Maps to [Microsoft.Infrared](#infrared) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7a489-641">Microsoft. Language</span><span class="sxs-lookup"><span data-stu-id="7a489-641">Microsoft.Language</span></span>                                          | <span data-ttu-id="7a489-642">Idioma</span><span class="sxs-lookup"><span data-stu-id="7a489-642">Language</span></span>                          | <span data-ttu-id="7a489-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span><span class="sxs-lookup"><span data-stu-id="7a489-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span></span> | <span data-ttu-id="7a489-644">Removido a partir do Windows 10, versão 1803</span><span class="sxs-lookup"><span data-stu-id="7a489-644">Removed as of Windows 10, version 1803</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="7a489-645">Microsoft. LocationAndOtherSensors</span><span class="sxs-lookup"><span data-stu-id="7a489-645">Microsoft.LocationAndOtherSensors</span></span>                           | <span data-ttu-id="7a489-646">Local e outros sensores</span><span class="sxs-lookup"><span data-stu-id="7a489-646">Location and Other Sensors</span></span>        | <span data-ttu-id="7a489-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="7a489-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span></span> | <span data-ttu-id="7a489-648">Mapeia para [Microsoft. LocationSettings](#infrared) a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a489-648">Maps to [Microsoft.LocationSettings](#infrared) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="7a489-649">Microsoft. PenAndInputDevices</span><span class="sxs-lookup"><span data-stu-id="7a489-649">Microsoft.PenAndInputDevices</span></span>                                | <span data-ttu-id="7a489-650">Caneta e dispositivos de entrada</span><span class="sxs-lookup"><span data-stu-id="7a489-650">Pen and Input Devices</span></span>             | <span data-ttu-id="7a489-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="7a489-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span> | <span data-ttu-id="7a489-652">Mapeia para [Microsoft. PenAndTouch](#pen-and-touch) a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-652">Maps to [Microsoft.PenAndTouch](#pen-and-touch) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="7a489-653">Microsoft. PeopleNearMe</span><span class="sxs-lookup"><span data-stu-id="7a489-653">Microsoft.PeopleNearMe</span></span>                                      | <span data-ttu-id="7a489-654">Pessoas ao meu redor</span><span class="sxs-lookup"><span data-stu-id="7a489-654">People Near Me</span></span>                    | <span data-ttu-id="7a489-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span><span class="sxs-lookup"><span data-stu-id="7a489-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span></span> | <span data-ttu-id="7a489-656">Removido do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a489-656">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7a489-657">Microsoft. PerformanceInformationAndTools</span><span class="sxs-lookup"><span data-stu-id="7a489-657">Microsoft.PerformanceInformationAndTools</span></span>                    | <span data-ttu-id="7a489-658">Ferramentas e informações de desempenho</span><span class="sxs-lookup"><span data-stu-id="7a489-658">Performance Information and Tools</span></span> | <span data-ttu-id="7a489-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span><span class="sxs-lookup"><span data-stu-id="7a489-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span></span> | <span data-ttu-id="7a489-660">Removido a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="7a489-660">Removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="7a489-661">Microsoft. PhoneAndModemOptions</span><span class="sxs-lookup"><span data-stu-id="7a489-661">Microsoft.PhoneAndModemOptions</span></span>                              | <span data-ttu-id="7a489-662">Telefone e modem</span><span class="sxs-lookup"><span data-stu-id="7a489-662">Phone and Modem</span></span>                   | <span data-ttu-id="7a489-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="7a489-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span></span> | <span data-ttu-id="7a489-664">Mapeia para [Microsoft. PhoneAndModem](#phone-and-modem) a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-664">Maps to [Microsoft.PhoneAndModem](#phone-and-modem) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7a489-665">Microsoft. Printers</span><span class="sxs-lookup"><span data-stu-id="7a489-665">Microsoft.Printers</span></span>                                          | <span data-ttu-id="7a489-666">Impressoras</span><span class="sxs-lookup"><span data-stu-id="7a489-666">Printers</span></span>                          | <span data-ttu-id="7a489-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="7a489-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span></span> | <span data-ttu-id="7a489-668">Mapeia para [Microsoft. DevicesAndPrinters](#devices-and-printers) a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-668">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7a489-669">Microsoft. ProblemReportsAndSolutions</span><span class="sxs-lookup"><span data-stu-id="7a489-669">Microsoft.ProblemReportsAndSolutions</span></span>                        | <span data-ttu-id="7a489-670">Relatórios de problemas e soluções</span><span class="sxs-lookup"><span data-stu-id="7a489-670">Problem Reports and Solutions</span></span>     | <span data-ttu-id="7a489-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span><span class="sxs-lookup"><span data-stu-id="7a489-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span></span> | <span data-ttu-id="7a489-672">Mapeia para [Microsoft. ActionCenter](#action-center) a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-672">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7a489-673">Microsoft. RegionalAndLanguageOptions</span><span class="sxs-lookup"><span data-stu-id="7a489-673">Microsoft.RegionalAndLanguageOptions</span></span>                        | <span data-ttu-id="7a489-674">Opções regionais e de idioma</span><span class="sxs-lookup"><span data-stu-id="7a489-674">Regional and Language Options</span></span>     | <span data-ttu-id="7a489-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="7a489-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span> | <span data-ttu-id="7a489-676">Mapeia para [Microsoft. RegionAndLanguage](#region) a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-676">Maps to [Microsoft.RegionAndLanguage](#region) as of Windows 7.</span></span> <span data-ttu-id="7a489-677">Observe que, a partir do Windows 8, a região e o idioma foram cada um dado ao seu próprio item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="7a489-677">Note that as of Windows 8, Region and Language were each given their own Control Panel item.</span></span> <span data-ttu-id="7a489-678">O Microsoft. RegionalAndLanguageOptions e o Microsoft. RegionAndLanguage atualmente abrem o item de região.</span><span class="sxs-lookup"><span data-stu-id="7a489-678">Both Microsoft.RegionalAndLanguageOptions and Microsoft.RegionAndLanguage currently open the Region item.</span></span> <span data-ttu-id="7a489-679">Você deve usar o [Microsoft. Language](#location-settings) para acessar o item de idioma.</span><span class="sxs-lookup"><span data-stu-id="7a489-679">You must use [Microsoft.Language](#location-settings) to access the Language item.</span></span> |
| <span data-ttu-id="7a489-680">Microsoft. SecurityCenter</span><span class="sxs-lookup"><span data-stu-id="7a489-680">Microsoft.SecurityCenter</span></span>                                    | <span data-ttu-id="7a489-681">Central de Segurança do Windows</span><span class="sxs-lookup"><span data-stu-id="7a489-681">Windows Security Center</span></span>           | <span data-ttu-id="7a489-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span><span class="sxs-lookup"><span data-stu-id="7a489-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span></span> | <span data-ttu-id="7a489-683">Mapeia para [Microsoft. ActionCenter](#action-center) a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-683">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7a489-684">Microsoft. SpeechRecognitionOptions</span><span class="sxs-lookup"><span data-stu-id="7a489-684">Microsoft.SpeechRecognitionOptions</span></span>                          | <span data-ttu-id="7a489-685">Opções de reconhecimento de fala</span><span class="sxs-lookup"><span data-stu-id="7a489-685">Speech Recognition Options</span></span>        | <span data-ttu-id="7a489-686">{58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="7a489-686">{58E3C745-D971-4081-9034-86E34B30836A}</span></span> | <span data-ttu-id="7a489-687">Mapeia para [Microsoft. SpeechRecognition](#speech-recognition) a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-687">Maps to [Microsoft.SpeechRecognition](#speech-recognition) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="7a489-688">Microsoft. TaskbarAndStartMenu</span><span class="sxs-lookup"><span data-stu-id="7a489-688">Microsoft.TaskbarAndStartMenu</span></span>                               | <span data-ttu-id="7a489-689">Barra de tarefas e menu iniciar</span><span class="sxs-lookup"><span data-stu-id="7a489-689">Taskbar and Start Menu</span></span>            | <span data-ttu-id="7a489-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="7a489-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span> | <span data-ttu-id="7a489-691">Mapeia para [Microsoft. Taskbar](#speech-recognition) a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a489-691">Maps to [Microsoft.Taskbar](#speech-recognition) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7a489-692">Microsoft. WelcomeCenter</span><span class="sxs-lookup"><span data-stu-id="7a489-692">Microsoft.WelcomeCenter</span></span>                                     | <span data-ttu-id="7a489-693">Centro de boas-vindas</span><span class="sxs-lookup"><span data-stu-id="7a489-693">Welcome Center</span></span>                    | <span data-ttu-id="7a489-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span><span class="sxs-lookup"><span data-stu-id="7a489-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span></span> | <span data-ttu-id="7a489-695">Mapeia para Microsoft. GettingStarted no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-695">Maps to Microsoft.GettingStarted in Windows 7.</span></span> <span data-ttu-id="7a489-696">Inicia o painel de controle home page a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a489-696">Launches the Control Panel home page as of Windows 8.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7a489-697">Microsoft. WindowsSidebarProperties</span><span class="sxs-lookup"><span data-stu-id="7a489-697">Microsoft.WindowsSidebarProperties</span></span>                          | <span data-ttu-id="7a489-698">Propriedades da barra lateral do Windows</span><span class="sxs-lookup"><span data-stu-id="7a489-698">Windows Sidebar Properties</span></span>        | <span data-ttu-id="7a489-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="7a489-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="7a489-700">Mapeia para Microsoft. DesktopGadgets no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a489-700">Maps to Microsoft.DesktopGadgets in Windows 7.</span></span> <span data-ttu-id="7a489-701">Removido do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a489-701">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="7a489-702">Microsoft. WindowsSideShow</span><span class="sxs-lookup"><span data-stu-id="7a489-702">Microsoft.WindowsSideShow</span></span>                                   | <span data-ttu-id="7a489-703">Windows SideShow</span><span class="sxs-lookup"><span data-stu-id="7a489-703">Windows SideShow</span></span>                  | <span data-ttu-id="7a489-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span><span class="sxs-lookup"><span data-stu-id="7a489-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span></span> | <span data-ttu-id="7a489-705">Recurso preterido no Windows 8, removido a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="7a489-705">Feature deprecated in Windows 8, removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a><span data-ttu-id="7a489-706">Usando nomes canônicos no Política de Grupo local</span><span class="sxs-lookup"><span data-stu-id="7a489-706">Using Canonical Names in Local Group Policy</span></span>

<span data-ttu-id="7a489-707">A partir do Windows 7, você pode usar nomes canônicos para restringir o acesso a itens individuais do painel de controle por meio da diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="7a489-707">As of Windows 7, you can use canonical names to restrict access to individual Control Panel items through group policy.</span></span> <span data-ttu-id="7a489-708">Esse mesmo procedimento pode ser usado no Windows Vista, mas você precisa usar o nome do módulo em vez do nome canônico.</span><span class="sxs-lookup"><span data-stu-id="7a489-708">This same procedure can be used in Windows Vista, but you have to use the module name instead of the canonical name.</span></span>

### <a name="hiding-individual-control-panel-items"></a><span data-ttu-id="7a489-709">Ocultando itens individuais do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7a489-709">Hiding individual Control Panel items</span></span>

<span data-ttu-id="7a489-710">Use esse método se desejar mostrar mais itens do painel de controle do que você deseja ocultar.</span><span class="sxs-lookup"><span data-stu-id="7a489-710">Use this method if you want to show more Control Panel items than you want to hide.</span></span>

1.  <span data-ttu-id="7a489-711">Execute o arquivo gpedit. msc para iniciar o Editor de Política de Grupo Local.</span><span class="sxs-lookup"><span data-stu-id="7a489-711">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="7a489-712">Você também pode digitar "política de grupo" na tela iniciar Windows 8.1 e selecionar **Editar política de grupo** nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7a489-712">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="7a489-713">Selecione **configuração do usuário**  >  **modelos administrativos**  >  **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="7a489-713">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="7a489-714">Selecione **ocultar itens do painel de controle especificados**.</span><span class="sxs-lookup"><span data-stu-id="7a489-714">Select **Hide specified Control Panel items**.</span></span>
4.  <span data-ttu-id="7a489-715">Na janela **ocultar itens do painel de controle especificados** que é aberta, clique em **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="7a489-715">In the **Hide Specified Control Panel Items** window that opens, click **Enabled**.</span></span>
5.  <span data-ttu-id="7a489-716">Clique no botão **Mostrar** no painel de opções para mostrar a lista de itens de painel de controle não permitidos.</span><span class="sxs-lookup"><span data-stu-id="7a489-716">Click the **Show** button in the Options panel to show the list of disallowed Control Panel items.</span></span>
6.  <span data-ttu-id="7a489-717">Na janela **Mostrar conteúdo** que é aberta, digite um nome canônico na coluna **valor** .</span><span class="sxs-lookup"><span data-stu-id="7a489-717">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="7a489-718">Repita conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="7a489-718">Repeat as necessary.</span></span>
7.  <span data-ttu-id="7a489-719">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a489-719">Click **OK**.</span></span>

### <a name="showing-individual-control-panel-items"></a><span data-ttu-id="7a489-720">Mostrando itens individuais do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7a489-720">Showing individual Control Panel items</span></span>

<span data-ttu-id="7a489-721">Use esse método se desejar ocultar mais itens do painel de controle do que você deseja mostrar.</span><span class="sxs-lookup"><span data-stu-id="7a489-721">Use this method if you want to hide more Control Panel items than you want to show.</span></span>

1.  <span data-ttu-id="7a489-722">Execute o arquivo gpedit. msc para iniciar o Editor de Política de Grupo Local.</span><span class="sxs-lookup"><span data-stu-id="7a489-722">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="7a489-723">Você também pode digitar "política de grupo" na tela iniciar Windows 8.1 e selecionar **Editar política de grupo** nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7a489-723">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="7a489-724">Selecione **configuração do usuário**  >  **modelos administrativos**  >  **painel de controle**.</span><span class="sxs-lookup"><span data-stu-id="7a489-724">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="7a489-725">Selecione **Mostrar somente itens do painel de controle especificados**.</span><span class="sxs-lookup"><span data-stu-id="7a489-725">Select **Show only specified Control Panel items**.</span></span>
4.  <span data-ttu-id="7a489-726">Na janela **Mostrar apenas itens do painel de controle especificados** que abre, clique em **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="7a489-726">In the **Show Only Specified Control Panel Items** window that opens, click **Enabled**.</span></span> <span data-ttu-id="7a489-727">Isso oculta tudo no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="7a489-727">This hides everything in the Control Panel.</span></span>
5.  <span data-ttu-id="7a489-728">Clique no botão **Mostrar** no painel de opções para mostrar a lista de itens de painel de controle permitidos.</span><span class="sxs-lookup"><span data-stu-id="7a489-728">Click the **Show** button in the Options panel to show the list of allowed Control Panel items.</span></span>
6.  <span data-ttu-id="7a489-729">Na janela **Mostrar conteúdo** que é aberta, digite um nome canônico na coluna **valor** .</span><span class="sxs-lookup"><span data-stu-id="7a489-729">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="7a489-730">Repita conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="7a489-730">Repeat as necessary.</span></span>
7.  <span data-ttu-id="7a489-731">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a489-731">Click **OK**.</span></span>

<span data-ttu-id="7a489-732">Se você quiser remover todas as entradas que adicionou a uma lista Mostrar ou ocultar itens do painel de controle, retorne à tela na etapa 4 e selecione **não configurado** para limpar a lista.</span><span class="sxs-lookup"><span data-stu-id="7a489-732">If you want to remove all of the entries that you've added to a Show or Hide Control Panel items list, return to the screen in step 4 and select **Not Configured** to clear the list.</span></span> <span data-ttu-id="7a489-733">Se você quiser manter suas entradas, mas suspender as restrições, selecione **desabilitado**.</span><span class="sxs-lookup"><span data-stu-id="7a489-733">If you want to retain your entries but suspend the restrictions, select **Disabled**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a489-734">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a489-734">Remarks</span></span>

<span data-ttu-id="7a489-735">Você pode ver os itens no painel de controle que não estão listados aqui.</span><span class="sxs-lookup"><span data-stu-id="7a489-735">You might see items in your Control Panel that are not listed here.</span></span> <span data-ttu-id="7a489-736">Esses itens não fazem parte do Windows, mas, em vez disso, são adicionados durante a instalação de vários softwares e hardwares, como Microsoft Office ou uma placa de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7a489-736">Those items are not part of Windows, but instead are added during the installation of various software and hardware, such as Microsoft Office or a video card.</span></span> <span data-ttu-id="7a489-737">Os itens do painel de controle que não são do Windows podem ou não ter um nome canônico.</span><span class="sxs-lookup"><span data-stu-id="7a489-737">Non-Windows Control Panel items may or may not have a canonical name.</span></span> <span data-ttu-id="7a489-738">Para localizar o nome canônico de um item do painel de controle não listado aqui, examine o registro nestes caminhos:</span><span class="sxs-lookup"><span data-stu-id="7a489-738">To find the canonical name of a Control Panel item not listed here, look in the registry under these paths:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

<span data-ttu-id="7a489-739">Para obter mais informações que podem ajudá-lo a descobrir os CLSIDs necessários, consulte [como registrar itens do painel de controle do executável](how-to-register-an-executable-control-panel-item-registration-.md) e [como registrar itens do painel de controle da dll](how-to-register-dll-control-panel-item-registration-.md).</span><span class="sxs-lookup"><span data-stu-id="7a489-739">For more information that can help you discover the necessary CLSIDs, see [How to Register Executable Control Panel Items](how-to-register-an-executable-control-panel-item-registration-.md) and [How to Register DLL Control Panel Items](how-to-register-dll-control-panel-item-registration-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a489-740">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a489-740">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a489-741">Executando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="7a489-741">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="7a489-742">**IOpenControlPanel**</span><span class="sxs-lookup"><span data-stu-id="7a489-742">**IOpenControlPanel**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



