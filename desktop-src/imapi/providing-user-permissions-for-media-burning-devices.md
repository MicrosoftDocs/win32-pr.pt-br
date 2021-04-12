---
title: Fornecendo permissões de usuário para dispositivos de gravação de mídia
description: Por padrão, o Windows Vista e o Windows Server 2008 concedem acesso de leitura/gravação a administradores e usuários registrados diretamente no computador (usuários intermediários).
ms.assetid: 5bb8c8fc-03b4-45b5-816c-45f6cd580de6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613eb1bba9a18cfb08e1eee3e6b86c34235ab8e9
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104172407"
---
# <a name="providing-user-permissions-for-media-burning-devices"></a><span data-ttu-id="b4107-103">Fornecendo permissões de usuário para dispositivos de gravação de mídia</span><span class="sxs-lookup"><span data-stu-id="b4107-103">Providing User Permissions for Media Burning Devices</span></span>

<span data-ttu-id="b4107-104">Por padrão, o Windows Vista e o Windows Server 2008 concedem acesso de leitura/gravação a administradores e usuários registrados diretamente no computador (usuários intermediários).</span><span class="sxs-lookup"><span data-stu-id="b4107-104">By default, both Windows Vista and Windows Server 2008 grant read/write access to administrators and users logged directly into the machine (intermediate users).</span></span> <span data-ttu-id="b4107-105">No entanto, no Windows XP e no Windows Server 2003, um administrador deve conceder esses privilégios de leitura/gravação de dispositivo a outros grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="b4107-105">However, in Windows XP and Windows Server 2003 an administrator must grant these device read/write privileges to other user groups.</span></span>

<span data-ttu-id="b4107-106">Um administrador pode ajustar permissões específicas relacionadas ao dispositivo para usuários avançados e usuários interativos.</span><span class="sxs-lookup"><span data-stu-id="b4107-106">An administrator may adjust specific device-related permissions for power users and interactive users.</span></span>

<span data-ttu-id="b4107-107">Para acessar o painel de permissões de grupo apropriado no Windows XP, clique em **Iniciar**, **executar**, digite **gpedit. msc** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4107-107">To reach the appropriate group permissions panel in Windows XP, click **Start**, click **Run**, type **gpedit.msc**, and then click **OK**.</span></span> <span data-ttu-id="b4107-108">Na interface Política de Grupo, expanda **configuração do computador**, expanda **configurações do Windows**, expanda **configurações de segurança**, expanda **políticas locais** e clique duas vezes em **Opções de segurança**.</span><span class="sxs-lookup"><span data-stu-id="b4107-108">In the Group Policy interface, expand **Computer Configuration**, expand **Windows Settings**, expand **Security Settings**, expand **Local Policies**, and double-click **Security Options**.</span></span>

![Captura de tela que mostra a janela ' Política de Grupo ' com uma política selecionada no painel ' política '.](images/gpolpanel.jpg)

<span data-ttu-id="b4107-110">Neste painel, um administrador deve especificar as configurações de duas opções de dispositivo para fornecer as permissões de grupo necessárias:</span><span class="sxs-lookup"><span data-stu-id="b4107-110">At this panel, an administrator must specify the settings of two device options to provide the required group permissions:</span></span>

-   <span data-ttu-id="b4107-111">Defina "dispositivos: restringir o acesso ao CD-ROM somente para o usuário conectado localmente" para **habilitado**</span><span class="sxs-lookup"><span data-stu-id="b4107-111">Set "Devices: Restrict CD-ROM access to locally logged-on user only" to **Enabled**</span></span>
-   <span data-ttu-id="b4107-112">Defina "dispositivos: com permissão para formatar e ejetar mídia removível" para **Administradores e usuários avançados**.</span><span class="sxs-lookup"><span data-stu-id="b4107-112">Set "Devices: Allowed to format and eject removable media" to **Administrators and Power Users**.</span></span> <span data-ttu-id="b4107-113">Também é possível emular permissões do Windows Vista definindo essa opção como **Administradores e usuários interativos**.</span><span class="sxs-lookup"><span data-stu-id="b4107-113">It is also possible to emulate Windows Vista permissions by setting this option to **Administrators and Interactive Users**.</span></span>

<span data-ttu-id="b4107-114">Embora uma interface do usuário específica não exista no Windows XP ou no Windows Server 2003 para o uso de [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) ou [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), é possível usar essas APIs para conceder permissões de dispositivo a grupos de usuários personalizados.</span><span class="sxs-lookup"><span data-stu-id="b4107-114">While a specific UI does not exist in Windows XP or Windows Server 2003 for the use of [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) or [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya), it is possible to use these APIs to grant custom user groups device permissions.</span></span> <span data-ttu-id="b4107-115">Por exemplo, uma chamada para **SetSecurityInfo** concederá permissões a grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="b4107-115">For example, a call to **SetSecurityInfo** will grant permissions to user groups.</span></span> <span data-ttu-id="b4107-116">As alterações de permissão com essa API são temporárias e não serão mantidas em uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="b4107-116">Permission changes with this API are temporary and will not persist across a reboot.</span></span> <span data-ttu-id="b4107-117">No entanto, chamar [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) irá implementar as alterações de permissão no registro, que persistirão em uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="b4107-117">However, calling [SetupDiSetDeviceRegistryProperty](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya) will implement the permission changes in the registry, which will persist across a reboot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4107-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4107-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4107-119">Usando o IMAPi</span><span class="sxs-lookup"><span data-stu-id="b4107-119">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="b4107-120">**SetSecurityInfo**</span><span class="sxs-lookup"><span data-stu-id="b4107-120">**SetSecurityInfo**</span></span>](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[<span data-ttu-id="b4107-121">SetupDiSetDeviceRegistryProperty</span><span class="sxs-lookup"><span data-stu-id="b4107-121">SetupDiSetDeviceRegistryProperty</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdisetdeviceregistrypropertya)
</dt> </dl>

 

 