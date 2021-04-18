---
description: A tabela MsiServiceConfig configura um serviço que está instalado ou sendo instalado pelo pacote atual.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Tabela MsiServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780509"
---
# <a name="msiserviceconfig-table"></a><span data-ttu-id="3365c-103">Tabela MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="3365c-103">MsiServiceConfig Table</span></span>

<span data-ttu-id="3365c-104">A tabela MsiServiceConfig configura um serviço que está instalado ou sendo instalado pelo pacote atual.</span><span class="sxs-lookup"><span data-stu-id="3365c-104">The MsiServiceConfig table configures a service that is installed or being installed by the current package.</span></span>

<span data-ttu-id="3365c-105">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="3365c-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="3365c-106">Esta tabela está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="3365c-106">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="3365c-107">A tabela MsiServiceConfig tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="3365c-107">The MsiServiceConfig table has the following columns.</span></span>



| <span data-ttu-id="3365c-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="3365c-108">Column</span></span>           | <span data-ttu-id="3365c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3365c-109">Type</span></span>                         | <span data-ttu-id="3365c-110">Chave</span><span class="sxs-lookup"><span data-stu-id="3365c-110">Key</span></span> | <span data-ttu-id="3365c-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="3365c-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="3365c-112">MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="3365c-112">MsiServiceConfig</span></span> | [<span data-ttu-id="3365c-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="3365c-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="3365c-114">S</span><span class="sxs-lookup"><span data-stu-id="3365c-114">Y</span></span>   | <span data-ttu-id="3365c-115">N</span><span class="sxs-lookup"><span data-stu-id="3365c-115">N</span></span>        |
| <span data-ttu-id="3365c-116">Nome</span><span class="sxs-lookup"><span data-stu-id="3365c-116">Name</span></span>             | [<span data-ttu-id="3365c-117">Binário</span><span class="sxs-lookup"><span data-stu-id="3365c-117">Formatted</span></span>](formatted.md)   | <span data-ttu-id="3365c-118">N</span><span class="sxs-lookup"><span data-stu-id="3365c-118">N</span></span>   | <span data-ttu-id="3365c-119">N</span><span class="sxs-lookup"><span data-stu-id="3365c-119">N</span></span>        |
| <span data-ttu-id="3365c-120">Evento</span><span class="sxs-lookup"><span data-stu-id="3365c-120">Event</span></span>            | [<span data-ttu-id="3365c-121">Inteiro</span><span class="sxs-lookup"><span data-stu-id="3365c-121">Integer</span></span>](integer.md)       | <span data-ttu-id="3365c-122">N</span><span class="sxs-lookup"><span data-stu-id="3365c-122">N</span></span>   | <span data-ttu-id="3365c-123">N</span><span class="sxs-lookup"><span data-stu-id="3365c-123">N</span></span>        |
| <span data-ttu-id="3365c-124">ConfigType</span><span class="sxs-lookup"><span data-stu-id="3365c-124">ConfigType</span></span>       | [<span data-ttu-id="3365c-125">Inteiro</span><span class="sxs-lookup"><span data-stu-id="3365c-125">Integer</span></span>](integer.md)       | <span data-ttu-id="3365c-126">N</span><span class="sxs-lookup"><span data-stu-id="3365c-126">N</span></span>   | <span data-ttu-id="3365c-127">N</span><span class="sxs-lookup"><span data-stu-id="3365c-127">N</span></span>        |
| <span data-ttu-id="3365c-128">Argumento</span><span class="sxs-lookup"><span data-stu-id="3365c-128">Argument</span></span>         | [<span data-ttu-id="3365c-129">Binário</span><span class="sxs-lookup"><span data-stu-id="3365c-129">Formatted</span></span>](formatted.md)   | <span data-ttu-id="3365c-130">N</span><span class="sxs-lookup"><span data-stu-id="3365c-130">N</span></span>   | <span data-ttu-id="3365c-131">S</span><span class="sxs-lookup"><span data-stu-id="3365c-131">Y</span></span>        |
| <span data-ttu-id="3365c-132">Componente\_</span><span class="sxs-lookup"><span data-stu-id="3365c-132">Component\_</span></span>      | [<span data-ttu-id="3365c-133">Identificador</span><span class="sxs-lookup"><span data-stu-id="3365c-133">Identifier</span></span>](identifier.md) | <span data-ttu-id="3365c-134">N</span><span class="sxs-lookup"><span data-stu-id="3365c-134">N</span></span>   | <span data-ttu-id="3365c-135">N</span><span class="sxs-lookup"><span data-stu-id="3365c-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3365c-136">Colunas</span><span class="sxs-lookup"><span data-stu-id="3365c-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3365c-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="3365c-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span></span>
</dt> <dd>

<span data-ttu-id="3365c-138">Esta é a chave primária desta tabela.</span><span class="sxs-lookup"><span data-stu-id="3365c-138">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="3365c-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="3365c-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="3365c-140">Esta coluna contém o nome de um serviço que faz parte deste pacote ou que já está instalado.</span><span class="sxs-lookup"><span data-stu-id="3365c-140">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="3365c-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Circunstância</span><span class="sxs-lookup"><span data-stu-id="3365c-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="3365c-142">Esta coluna especifica quando alterar a configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="3365c-142">This column specifies when to change the service configuration.</span></span> <span data-ttu-id="3365c-143">Os valores a seguir podem ser combinados para representar várias operações.</span><span class="sxs-lookup"><span data-stu-id="3365c-143">The following values can be combined to represent multiple operations.</span></span> <span data-ttu-id="3365c-144">Quaisquer valores incluídos a não ser ignorados.</span><span class="sxs-lookup"><span data-stu-id="3365c-144">Any values included other than these are ignored.</span></span>



| <span data-ttu-id="3365c-145">Constante</span><span class="sxs-lookup"><span data-stu-id="3365c-145">Constant</span></span>                                         | <span data-ttu-id="3365c-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="3365c-146">Description</span></span>                                              |
|--------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="3365c-147">**msidbServiceConfigEventInstall** 1</span><span class="sxs-lookup"><span data-stu-id="3365c-147">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="3365c-148">Executa a ação durante a instalação do componente.</span><span class="sxs-lookup"><span data-stu-id="3365c-148">Takes the action during installation of the component.</span></span>   |
| <span data-ttu-id="3365c-149">**msidbServiceConfigEventUninstall** 2</span><span class="sxs-lookup"><span data-stu-id="3365c-149">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="3365c-150">Executa a ação durante a desinstalação do componente.</span><span class="sxs-lookup"><span data-stu-id="3365c-150">Takes the action during uninstallation of the component.</span></span> |
| <span data-ttu-id="3365c-151">**msidbServiceConfigEventReinstall** 4</span><span class="sxs-lookup"><span data-stu-id="3365c-151">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="3365c-152">Executa a ação durante a reinstalação do componente.</span><span class="sxs-lookup"><span data-stu-id="3365c-152">Takes the action during reinstallation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3365c-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span><span class="sxs-lookup"><span data-stu-id="3365c-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span></span>
</dt> <dd>

<span data-ttu-id="3365c-154">O valor nesse campo, combinado com o valor no campo argumentos, especifica a alteração a ser feita na configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="3365c-154">The value in this field, combined with the value in the Arguments field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="3365c-155">A alteração especificada entrará em vigor na próxima vez em que o sistema for iniciado.</span><span class="sxs-lookup"><span data-stu-id="3365c-155">The specified change takes effect the next time the system is started.</span></span>



| <span data-ttu-id="3365c-156">Config</span><span class="sxs-lookup"><span data-stu-id="3365c-156">Config</span></span>                                                      | <span data-ttu-id="3365c-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="3365c-157">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3365c-158">**Serviço \_ do \_ \_ \_ Início automático atrasado de configuração** 3</span><span class="sxs-lookup"><span data-stu-id="3365c-158">**SERVICE\_CONFIG\_DELAYED\_AUTO\_START** 3</span></span><br/>       | <span data-ttu-id="3365c-159">Configure o atraso de tempo de um [serviço de início automático](../services/automatically-starting-services.md).</span><span class="sxs-lookup"><span data-stu-id="3365c-159">Configure the time delay of an [auto-start service](../services/automatically-starting-services.md).</span></span> <br/> <span data-ttu-id="3365c-160">Insira 1 no campo argumento para iniciar o serviço após outros serviços de início automático mais um atraso de tempo.</span><span class="sxs-lookup"><span data-stu-id="3365c-160">Enter 1 in the Argument field to start the service after other auto-start services plus a time delay.</span></span> <br/> <span data-ttu-id="3365c-161">Insira 0 no campo argumento para desativar o atraso do serviço de início automático.</span><span class="sxs-lookup"><span data-stu-id="3365c-161">Enter 0 in the Argument field to turn off the auto-start service delay.</span></span><br/> <span data-ttu-id="3365c-162">Aplica-se somente aos serviços ou serviços de início automático instalados por este pacote com o **\_ \_ início automático do serviço** no campo StartType da tabela do serviço de [instalação](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="3365c-162">Applies only to installed auto-start services or services installed by this package with **SERVICE\_AUTO\_START** in the StartType field of the [ServiceInstall table](serviceinstall-table.md).</span></span><br/>                                                                         |
| <span data-ttu-id="3365c-163">**Serviço \_ do CONFIGURAR \_ \_ \_ informações de privilégios necessários** 6</span><span class="sxs-lookup"><span data-stu-id="3365c-163">**SERVICE\_CONFIG\_REQUIRED\_PRIVILEGES\_INFO** 6</span></span><br/> | <span data-ttu-id="3365c-164">Altere a lista de privilégios exigida pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="3365c-164">Change the list of privileges required by the service.</span></span><br/> <span data-ttu-id="3365c-165">Insira uma lista de privilégios solicitados no campo argumento.</span><span class="sxs-lookup"><span data-stu-id="3365c-165">Enter a list of requested privileges in the Argument field.</span></span> <span data-ttu-id="3365c-166">O valor da cadeia de caracteres [formatada](formatted.md) no campo argumento lista as [**constantes de privilégio**](../secauthz/privilege-constants.md) para os privilégios solicitados.</span><span class="sxs-lookup"><span data-stu-id="3365c-166">The [Formatted](formatted.md) string value in the Argument field lists the [**Privilege Constants**](../secauthz/privilege-constants.md) for the requested privileges.</span></span> <span data-ttu-id="3365c-167">Você pode usar a \[ ~ \] sintaxe da cadeia de caracteres [formatada](formatted.md) para inserir um caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="3365c-167">You can use the \[~\] syntax of the [Formatted](formatted.md) string to insert a null character.</span></span> <span data-ttu-id="3365c-168">Separe as constantes de privilégio na lista por \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="3365c-168">Separate the privilege constants in the list by \[~\].</span></span><br/>                                                                                                                              |
| <span data-ttu-id="3365c-169">**Serviço \_ do \_Informações de \_ SID \_ do serviço de configuração** 5</span><span class="sxs-lookup"><span data-stu-id="3365c-169">**SERVICE\_CONFIG\_SERVICE\_SID\_INFO** 5</span></span><br/>         | <span data-ttu-id="3365c-170">Adicione um tipo de SID de serviço ao token de processo que contém este serviço.</span><span class="sxs-lookup"><span data-stu-id="3365c-170">Add a service SID type to the process token containing this service.</span></span><br/> <span data-ttu-id="3365c-171">Insira no campo de argumento um tipo de SID de serviço válido para a estrutura de [**\_ \_ informações de Sid de serviço**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) : tipo de Sid de serviço **\_ \_ \_ nenhum** (0x00), **tipo de Sid de serviço \_ \_ \_ restrito** (0x03) ou **tipo de Sid de serviço \_ \_ \_ irrestrito** (0x01).</span><span class="sxs-lookup"><span data-stu-id="3365c-171">Enter in the Argument field a valid service SID type for the [**SERVICE\_SID\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) structure: **SERVICE\_SID\_TYPE\_NONE** (0x00), **SERVICE\_SID\_TYPE\_RESTRICTED** (0x03), or **SERVICE\_SID\_TYPE\_UNRESTRICTED** (0x01).</span></span> <br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="3365c-172">**Serviço \_ do CONFIGURAR \_ \_ informações de pré-desligamento** 7</span><span class="sxs-lookup"><span data-stu-id="3365c-172">**SERVICE\_CONFIG\_PRESHUTDOWN\_INFO** 7</span></span><br/>          | <span data-ttu-id="3365c-173">Configure o período de tempo que o SCM ( [Gerenciador de controle de serviço](../services/service-control-manager.md) ) espera antes de prosseguir com outras operações de desligamento.</span><span class="sxs-lookup"><span data-stu-id="3365c-173">Configure the length of the time the [Service Control Manager](../services/service-control-manager.md) (SCM) waits before proceeding with other shutdown operations.</span></span> <span data-ttu-id="3365c-174">O SCM espera por esse período de tempo depois de enviar a notificação de **\_ \_ pré-desligamento de controle de serviço** para o serviço.</span><span class="sxs-lookup"><span data-stu-id="3365c-174">The SCM waits for this period of time after sending the **SERVICE\_CONTROL\_PRESHUTDOWN** notification to the service.</span></span> <br/> <span data-ttu-id="3365c-175">Insira o comprimento do intervalo de tempo, em milissegundos, no campo argumento.</span><span class="sxs-lookup"><span data-stu-id="3365c-175">Enter the time delay length, in milliseconds, in the Argument field.</span></span> <span data-ttu-id="3365c-176">Deixe o campo de argumento vazio para redefinir o tempo de espera para o padrão de 3 minutos.</span><span class="sxs-lookup"><span data-stu-id="3365c-176">Leave the Argument field empty to reset the time delay to the default of 3 minutes.</span></span> <br/>                                                                                                                               |
| <span data-ttu-id="3365c-177">**Serviço \_ do \_Sinalizador de \_ ações \_ de falha de configuração** 4</span><span class="sxs-lookup"><span data-stu-id="3365c-177">**SERVICE\_CONFIG\_FAILURE\_ACTIONS\_FLAG** 4</span></span><br/>     | <span data-ttu-id="3365c-178">Configure quando executar as ações de falha para este serviço.</span><span class="sxs-lookup"><span data-stu-id="3365c-178">Configure when to run the failure actions for this service.</span></span> <span data-ttu-id="3365c-179">Essa configuração será ignorada se o serviço não tiver nenhuma ação de falha configurada.</span><span class="sxs-lookup"><span data-stu-id="3365c-179">This setting is ignored if the service has no configured failure actions.</span></span><br/> <span data-ttu-id="3365c-180">Digite 0 para executar as ações somente se o serviço for encerrado sem que o serviço de relatório seja **\_ interrompido**.</span><span class="sxs-lookup"><span data-stu-id="3365c-180">Enter 0 to run the actions only if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> <span data-ttu-id="3365c-181">Digite 1 para executar as ações se o serviço encerrar o serviço de relatório **\_ interrompido** e o membro **dwWin32ExitCode** da estrutura de [**\_ status do serviço**](/windows/win32/api/winsvc/ns-winsvc-service_status) não for um **\_ êxito de erro**.</span><span class="sxs-lookup"><span data-stu-id="3365c-181">Enter 1 to run the actions if the service terminates reporting **SERVICE\_STOPPED** and the **dwWin32ExitCode** member of [**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) structure is not **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="3365c-182">As ações de falha configuradas também serão executadas se o serviço for encerrado sem que o serviço de relatório seja **\_ interrompido**.</span><span class="sxs-lookup"><span data-stu-id="3365c-182">Configured failure actions are also run if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3365c-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argumento</span><span class="sxs-lookup"><span data-stu-id="3365c-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="3365c-184">O valor nesse campo, combinado com o valor no campo Configtype, especifique a alteração a ser feita na configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="3365c-184">The value in this field, combined with the value in the ConfigType field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="3365c-185">A alteração especificada entrará em vigor na próxima vez em que o sistema for iniciado.</span><span class="sxs-lookup"><span data-stu-id="3365c-185">The specified change takes effect the next time the system is started.</span></span>

</dd> <dt>

<span data-ttu-id="3365c-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="3365c-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="3365c-187">Chave externa para a coluna componente da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="3365c-187">External key to the Component column of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="3365c-188">Validação</span><span class="sxs-lookup"><span data-stu-id="3365c-188">Validation</span></span>

<dl>

[<span data-ttu-id="3365c-189">ICE102</span><span class="sxs-lookup"><span data-stu-id="3365c-189">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="3365c-190">ICE03</span><span class="sxs-lookup"><span data-stu-id="3365c-190">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3365c-191">ICE06</span><span class="sxs-lookup"><span data-stu-id="3365c-191">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3365c-192">ICE32</span><span class="sxs-lookup"><span data-stu-id="3365c-192">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="3365c-193">ICE45</span><span class="sxs-lookup"><span data-stu-id="3365c-193">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="3365c-194">ICE46</span><span class="sxs-lookup"><span data-stu-id="3365c-194">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="3365c-195">ICE69</span><span class="sxs-lookup"><span data-stu-id="3365c-195">ICE69</span></span>](ice69.md)  
</dl>

 

 
