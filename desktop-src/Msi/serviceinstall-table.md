---
description: A tabela de instalação é usada para instalar um serviço e tem as colunas a seguir.
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: Tabela de desinstalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502583802a26c10bfd9572375149720c7c597f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754632"
---
# <a name="serviceinstall-table"></a><span data-ttu-id="43cf1-103">Tabela de desinstalação</span><span class="sxs-lookup"><span data-stu-id="43cf1-103">ServiceInstall Table</span></span>

<span data-ttu-id="43cf1-104">A tabela de instalação é usada para instalar um serviço e tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="43cf1-104">The ServiceInstall table is used to install a service and has the following columns.</span></span>



| <span data-ttu-id="43cf1-105">Coluna</span><span class="sxs-lookup"><span data-stu-id="43cf1-105">Column</span></span>         | <span data-ttu-id="43cf1-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="43cf1-106">Type</span></span>                               | <span data-ttu-id="43cf1-107">Chave</span><span class="sxs-lookup"><span data-stu-id="43cf1-107">Key</span></span> | <span data-ttu-id="43cf1-108">Nullable</span><span class="sxs-lookup"><span data-stu-id="43cf1-108">Nullable</span></span> |
|----------------|------------------------------------|-----|----------|
| <span data-ttu-id="43cf1-109">Instalar o</span><span class="sxs-lookup"><span data-stu-id="43cf1-109">ServiceInstall</span></span> | [<span data-ttu-id="43cf1-110">Identificador</span><span class="sxs-lookup"><span data-stu-id="43cf1-110">Identifier</span></span>](identifier.md)       | <span data-ttu-id="43cf1-111">S</span><span class="sxs-lookup"><span data-stu-id="43cf1-111">Y</span></span>   | <span data-ttu-id="43cf1-112">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-112">N</span></span>        |
| <span data-ttu-id="43cf1-113">Nome</span><span class="sxs-lookup"><span data-stu-id="43cf1-113">Name</span></span>           | [<span data-ttu-id="43cf1-114">Binário</span><span class="sxs-lookup"><span data-stu-id="43cf1-114">Formatted</span></span>](formatted.md)         | <span data-ttu-id="43cf1-115">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-115">N</span></span>   | <span data-ttu-id="43cf1-116">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-116">N</span></span>        |
| <span data-ttu-id="43cf1-117">DisplayName</span><span class="sxs-lookup"><span data-stu-id="43cf1-117">DisplayName</span></span>    | [<span data-ttu-id="43cf1-118">Binário</span><span class="sxs-lookup"><span data-stu-id="43cf1-118">Formatted</span></span>](formatted.md)         | <span data-ttu-id="43cf1-119">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-119">N</span></span>   | <span data-ttu-id="43cf1-120">S</span><span class="sxs-lookup"><span data-stu-id="43cf1-120">Y</span></span>        |
| <span data-ttu-id="43cf1-121">ServiceType</span><span class="sxs-lookup"><span data-stu-id="43cf1-121">ServiceType</span></span>    | [<span data-ttu-id="43cf1-122">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="43cf1-122">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="43cf1-123">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-123">N</span></span>   | <span data-ttu-id="43cf1-124">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-124">N</span></span>        |
| <span data-ttu-id="43cf1-125">StartType</span><span class="sxs-lookup"><span data-stu-id="43cf1-125">StartType</span></span>      | [<span data-ttu-id="43cf1-126">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="43cf1-126">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="43cf1-127">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-127">N</span></span>   | <span data-ttu-id="43cf1-128">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-128">N</span></span>        |
| <span data-ttu-id="43cf1-129">ErrorControl</span><span class="sxs-lookup"><span data-stu-id="43cf1-129">ErrorControl</span></span>   | [<span data-ttu-id="43cf1-130">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="43cf1-130">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="43cf1-131">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-131">N</span></span>   | <span data-ttu-id="43cf1-132">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-132">N</span></span>        |
| <span data-ttu-id="43cf1-133">LoadOrderGroup</span><span class="sxs-lookup"><span data-stu-id="43cf1-133">LoadOrderGroup</span></span> | [<span data-ttu-id="43cf1-134">Binário</span><span class="sxs-lookup"><span data-stu-id="43cf1-134">Formatted</span></span>](formatted.md)         | <span data-ttu-id="43cf1-135">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-135">N</span></span>   | <span data-ttu-id="43cf1-136">S</span><span class="sxs-lookup"><span data-stu-id="43cf1-136">Y</span></span>        |
| <span data-ttu-id="43cf1-137">Dependências</span><span class="sxs-lookup"><span data-stu-id="43cf1-137">Dependencies</span></span>   | [<span data-ttu-id="43cf1-138">Binário</span><span class="sxs-lookup"><span data-stu-id="43cf1-138">Formatted</span></span>](formatted.md)         | <span data-ttu-id="43cf1-139">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-139">N</span></span>   | <span data-ttu-id="43cf1-140">S</span><span class="sxs-lookup"><span data-stu-id="43cf1-140">Y</span></span>        |
| <span data-ttu-id="43cf1-141">StartName</span><span class="sxs-lookup"><span data-stu-id="43cf1-141">StartName</span></span>      | [<span data-ttu-id="43cf1-142">Binário</span><span class="sxs-lookup"><span data-stu-id="43cf1-142">Formatted</span></span>](formatted.md)         | <span data-ttu-id="43cf1-143">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-143">N</span></span>   | <span data-ttu-id="43cf1-144">S</span><span class="sxs-lookup"><span data-stu-id="43cf1-144">Y</span></span>        |
| <span data-ttu-id="43cf1-145">Senha</span><span class="sxs-lookup"><span data-stu-id="43cf1-145">Password</span></span>       | [<span data-ttu-id="43cf1-146">Binário</span><span class="sxs-lookup"><span data-stu-id="43cf1-146">Formatted</span></span>](formatted.md)         | <span data-ttu-id="43cf1-147">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-147">N</span></span>   | <span data-ttu-id="43cf1-148">S</span><span class="sxs-lookup"><span data-stu-id="43cf1-148">Y</span></span>        |
| <span data-ttu-id="43cf1-149">Argumentos</span><span class="sxs-lookup"><span data-stu-id="43cf1-149">Arguments</span></span>      | [<span data-ttu-id="43cf1-150">Binário</span><span class="sxs-lookup"><span data-stu-id="43cf1-150">Formatted</span></span>](formatted.md)         | <span data-ttu-id="43cf1-151">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-151">N</span></span>   | <span data-ttu-id="43cf1-152">S</span><span class="sxs-lookup"><span data-stu-id="43cf1-152">Y</span></span>        |
| <span data-ttu-id="43cf1-153">Componente\_</span><span class="sxs-lookup"><span data-stu-id="43cf1-153">Component\_</span></span>    | [<span data-ttu-id="43cf1-154">Identificador</span><span class="sxs-lookup"><span data-stu-id="43cf1-154">Identifier</span></span>](identifier.md)       | <span data-ttu-id="43cf1-155">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-155">N</span></span>   | <span data-ttu-id="43cf1-156">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-156">N</span></span>        |
| <span data-ttu-id="43cf1-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="43cf1-157">Description</span></span>    | [<span data-ttu-id="43cf1-158">Binário</span><span class="sxs-lookup"><span data-stu-id="43cf1-158">Formatted</span></span>](formatted.md)         | <span data-ttu-id="43cf1-159">N</span><span class="sxs-lookup"><span data-stu-id="43cf1-159">N</span></span>   | <span data-ttu-id="43cf1-160">S</span><span class="sxs-lookup"><span data-stu-id="43cf1-160">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="43cf1-161">Colunas</span><span class="sxs-lookup"><span data-stu-id="43cf1-161">Columns</span></span>

<dl> <dt>

<span data-ttu-id="43cf1-162"><span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>Instalar o</span><span class="sxs-lookup"><span data-stu-id="43cf1-162"><span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>ServiceInstall</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-163">Esta é a chave primária para a tabela.</span><span class="sxs-lookup"><span data-stu-id="43cf1-163">This is the primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="43cf1-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="43cf1-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-165">Essa coluna é a cadeia de caracteres que fornece o nome do serviço a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="43cf1-165">This column is the string that gives the service name to install.</span></span> <span data-ttu-id="43cf1-166">A cadeia de caracteres tem um comprimento máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="43cf1-166">The string has a maximum length of 256 characters.</span></span> <span data-ttu-id="43cf1-167">O banco de dados do Gerenciador de controle de serviço preserva o caso dos caracteres no nome do serviço, mas as comparações de nomes de serviço não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="43cf1-167">The service control manager database preserves the case of the characters in the service name, but comparisons of service names are case insensitive.</span></span> <span data-ttu-id="43cf1-168">Barra (/) e barra invertida ( \\ ) são caracteres de nome de serviço inválidos.</span><span class="sxs-lookup"><span data-stu-id="43cf1-168">Forward-slash (/) and back-slash (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="43cf1-169"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span><span class="sxs-lookup"><span data-stu-id="43cf1-169"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-170">Essa coluna é a cadeia de caracteres localizável que os programas da interface do usuário usam para identificar o serviço.</span><span class="sxs-lookup"><span data-stu-id="43cf1-170">This column is the localizable string that user interface programs use to identify the service.</span></span> <span data-ttu-id="43cf1-171">A cadeia de caracteres tem um comprimento máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="43cf1-171">The string has a maximum length of 256 characters.</span></span> <span data-ttu-id="43cf1-172">O Gerenciador de controle de serviço preserva o caso do nome de exibição, mas as comparações de nome de exibição não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="43cf1-172">The service control manager preserves the case of the display name, but display name comparisons are case insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="43cf1-173"><span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType</span><span class="sxs-lookup"><span data-stu-id="43cf1-173"><span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-174">Esta coluna é um conjunto de sinalizadores de bits que especificam o tipo de serviço.</span><span class="sxs-lookup"><span data-stu-id="43cf1-174">This column is a set of bit flags that specify the type of service.</span></span> <span data-ttu-id="43cf1-175">Um dos seguintes tipos de serviço deve ser especificado nesta coluna.</span><span class="sxs-lookup"><span data-stu-id="43cf1-175">One of the following service types must be specified in this column.</span></span>



| <span data-ttu-id="43cf1-176">Tipo de serviço</span><span class="sxs-lookup"><span data-stu-id="43cf1-176">Type of service</span></span>                | <span data-ttu-id="43cf1-177">Valor</span><span class="sxs-lookup"><span data-stu-id="43cf1-177">Value</span></span>      | <span data-ttu-id="43cf1-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="43cf1-178">Description</span></span>                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43cf1-179">\_ \_ Processo próprio do serviço do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="43cf1-179">SERVICE\_WIN32\_OWN\_PROCESS</span></span>   | <span data-ttu-id="43cf1-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="43cf1-180">0x00000010</span></span> | <span data-ttu-id="43cf1-181">Um serviço Microsoft Win32 que executa seu próprio processo.</span><span class="sxs-lookup"><span data-stu-id="43cf1-181">A Microsoft Win32 service that runs its own process.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="43cf1-182">\_Processo de \_ compartilhamento \_ Win32 do serviço</span><span class="sxs-lookup"><span data-stu-id="43cf1-182">SERVICE\_WIN32\_SHARE\_PROCESS</span></span> | <span data-ttu-id="43cf1-183">0x00000020</span><span class="sxs-lookup"><span data-stu-id="43cf1-183">0x00000020</span></span> | <span data-ttu-id="43cf1-184">Um serviço Win32 que compartilha um processo.</span><span class="sxs-lookup"><span data-stu-id="43cf1-184">A Win32 service that shares a process.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="43cf1-185">\_processo interativo de serviço \_</span><span class="sxs-lookup"><span data-stu-id="43cf1-185">SERVICE\_INTERACTIVE\_PROCESS</span></span>  | <span data-ttu-id="43cf1-186">0x00000100</span><span class="sxs-lookup"><span data-stu-id="43cf1-186">0x00000100</span></span> | <span data-ttu-id="43cf1-187">Um serviço Win32 que interage com a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="43cf1-187">A Win32 service that interacts with the desktop.</span></span> <span data-ttu-id="43cf1-188">Esse valor não pode ser usado sozinha e deve ser adicionado a um dos dois tipos anteriores. A coluna StartName deve ser definida como LocalSystem ou NULL ao usar esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="43cf1-188">This value cannot be used alone and must be added to one of the two previous types.The StartName column must be set to LocalSystem or null when using this flag.</span></span><br/> |



 

<span data-ttu-id="43cf1-189">Não há suporte para os tipos de serviço a seguir.</span><span class="sxs-lookup"><span data-stu-id="43cf1-189">The following types of service are unsupported.</span></span>



| <span data-ttu-id="43cf1-190">Tipo de serviço</span><span class="sxs-lookup"><span data-stu-id="43cf1-190">Type of service</span></span>               | <span data-ttu-id="43cf1-191">Valor</span><span class="sxs-lookup"><span data-stu-id="43cf1-191">Value</span></span>      | <span data-ttu-id="43cf1-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="43cf1-192">Description</span></span>                   |
|-------------------------------|------------|-------------------------------|
| <span data-ttu-id="43cf1-193">\_Driver de kernel de serviço \_</span><span class="sxs-lookup"><span data-stu-id="43cf1-193">SERVICE\_KERNEL\_DRIVER</span></span>       | <span data-ttu-id="43cf1-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="43cf1-194">0x00000001</span></span> | <span data-ttu-id="43cf1-195">Um serviço de driver.</span><span class="sxs-lookup"><span data-stu-id="43cf1-195">A driver service.</span></span>             |
| <span data-ttu-id="43cf1-196">\_Driver do \_ sistema de arquivos de serviço \_</span><span class="sxs-lookup"><span data-stu-id="43cf1-196">SERVICE\_FILE\_SYSTEM\_DRIVER</span></span> | <span data-ttu-id="43cf1-197">0x00000002</span><span class="sxs-lookup"><span data-stu-id="43cf1-197">0x00000002</span></span> | <span data-ttu-id="43cf1-198">Um serviço de driver do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="43cf1-198">A file system driver service.</span></span> |



 

</dd> <dt>

<span data-ttu-id="43cf1-199"><span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType</span><span class="sxs-lookup"><span data-stu-id="43cf1-199"><span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-200">Esta coluna é um conjunto de sinalizadores de bits que especificam quando iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="43cf1-200">This column is a set of bit flags that specify when to start the service.</span></span> <span data-ttu-id="43cf1-201">Um dos seguintes tipos de início de serviço deve ser especificado nesta coluna.</span><span class="sxs-lookup"><span data-stu-id="43cf1-201">One of the following types of service start must be specified in this column.</span></span>



| <span data-ttu-id="43cf1-202">Tipo de início do serviço</span><span class="sxs-lookup"><span data-stu-id="43cf1-202">Type of service start</span></span>  | <span data-ttu-id="43cf1-203">Valor</span><span class="sxs-lookup"><span data-stu-id="43cf1-203">Value</span></span>      | <span data-ttu-id="43cf1-204">Descrição</span><span class="sxs-lookup"><span data-stu-id="43cf1-204">Description</span></span>                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43cf1-205">\_início automático do serviço \_</span><span class="sxs-lookup"><span data-stu-id="43cf1-205">SERVICE\_AUTO\_START</span></span>   | <span data-ttu-id="43cf1-206">0x00000002</span><span class="sxs-lookup"><span data-stu-id="43cf1-206">0x00000002</span></span> | <span data-ttu-id="43cf1-207">Um serviço é iniciado durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="43cf1-207">A service start during startup of the system.</span></span>                                                              |
| <span data-ttu-id="43cf1-208">\_início da demanda de serviço \_</span><span class="sxs-lookup"><span data-stu-id="43cf1-208">SERVICE\_DEMAND\_START</span></span> | <span data-ttu-id="43cf1-209">0x00000003</span><span class="sxs-lookup"><span data-stu-id="43cf1-209">0x00000003</span></span> | <span data-ttu-id="43cf1-210">Um serviço é iniciado quando o Gerenciador de controle de serviço chama a função [**StartService**](/windows/win32/api/winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="43cf1-210">A service start when the service control manager calls the [**StartService**](/windows/win32/api/winsvc/nf-winsvc-startservicea) function.</span></span> |
| <span data-ttu-id="43cf1-211">SERVIÇO \_ desabilitado</span><span class="sxs-lookup"><span data-stu-id="43cf1-211">SERVICE\_DISABLED</span></span>      | <span data-ttu-id="43cf1-212">0x00000004</span><span class="sxs-lookup"><span data-stu-id="43cf1-212">0x00000004</span></span> | <span data-ttu-id="43cf1-213">Especifica um serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="43cf1-213">Specifies a service that can no longer be started.</span></span>                                                         |



 

<span data-ttu-id="43cf1-214">O Windows Installer não pode usar as opções de início de inicialização do serviço e início do \_ \_ sistema de serviço \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="43cf1-214">The Windows Installer cannot use the SERVICE\_BOOT\_START and SERVICE\_SYSTEM\_START options.</span></span>

</dd> <dt>

<span data-ttu-id="43cf1-215"><span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl</span><span class="sxs-lookup"><span data-stu-id="43cf1-215"><span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-216">Essa coluna especifica a ação realizada pelo programa de inicialização se o serviço não for iniciado durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="43cf1-216">This column specifies the action taken by the startup program if the service fails to start during startup.</span></span> <span data-ttu-id="43cf1-217">Esses valores afetam os eventos StartService de controle dos serviços instalados.</span><span class="sxs-lookup"><span data-stu-id="43cf1-217">These values affect the ServiceControl StartService events for installed services.</span></span> <span data-ttu-id="43cf1-218">Um dos seguintes sinalizadores de controle de erro deve ser especificado nesta coluna.</span><span class="sxs-lookup"><span data-stu-id="43cf1-218">One of the following error control flags must be specified in this column.</span></span>

<span data-ttu-id="43cf1-219">Adicionar a constante **msidbServiceInstallErrorControlVital** (Value = 0x08000) aos sinalizadores na tabela a seguir especifica que a instalação geral deverá falhar se o serviço não puder ser instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="43cf1-219">Adding the constant **msidbServiceInstallErrorControlVital** (value = 0x08000) to the flags in the following table specifies that the overall install should fail if the service cannot be installed into the system.</span></span>



| <span data-ttu-id="43cf1-220">Sinalizador de controle de erro</span><span class="sxs-lookup"><span data-stu-id="43cf1-220">Error control flag</span></span>       | <span data-ttu-id="43cf1-221">Valor</span><span class="sxs-lookup"><span data-stu-id="43cf1-221">Value</span></span>      | <span data-ttu-id="43cf1-222">Ação do programa de inicialização</span><span class="sxs-lookup"><span data-stu-id="43cf1-222">Startup program's action</span></span>                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43cf1-223">\_ignorar erro de serviço \_</span><span class="sxs-lookup"><span data-stu-id="43cf1-223">SERVICE\_ERROR\_IGNORE</span></span>   | <span data-ttu-id="43cf1-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="43cf1-224">0x00000000</span></span> | <span data-ttu-id="43cf1-225">Registra o erro e continua com a operação de inicialização.</span><span class="sxs-lookup"><span data-stu-id="43cf1-225">Logs the error and continues with the startup operation.</span></span>                                                                                                                                       |
| <span data-ttu-id="43cf1-226">erro de serviço \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="43cf1-226">SERVICE\_ERROR\_NORMAL</span></span>   | <span data-ttu-id="43cf1-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="43cf1-227">0x00000001</span></span> | <span data-ttu-id="43cf1-228">Registra o erro, exibe uma caixa de mensagem e continua a operação de inicialização.</span><span class="sxs-lookup"><span data-stu-id="43cf1-228">Logs the error, displays a message box and continues the startup operation.</span></span>                                                                                                                    |
| <span data-ttu-id="43cf1-229">\_erro \_ crítico do serviço</span><span class="sxs-lookup"><span data-stu-id="43cf1-229">SERVICE\_ERROR\_CRITICAL</span></span> | <span data-ttu-id="43cf1-230">0x00000003</span><span class="sxs-lookup"><span data-stu-id="43cf1-230">0x00000003</span></span> | <span data-ttu-id="43cf1-231">Registra o erro se for possível e o sistema será reiniciado com a última configuração conhecida como boa.</span><span class="sxs-lookup"><span data-stu-id="43cf1-231">Logs the error if it is possible and the system is restarted with the last configuration known to be good.</span></span> <span data-ttu-id="43cf1-232">Se a última configuração válida estiver sendo iniciada, a operação de inicialização falhará.</span><span class="sxs-lookup"><span data-stu-id="43cf1-232">If the last-known-good configuration is being started, the startup operation fails.</span></span> |



 

</dd> <dt>

<span data-ttu-id="43cf1-233"><span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>OrderGroup</span><span class="sxs-lookup"><span data-stu-id="43cf1-233"><span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-234">Esta coluna contém a cadeia de caracteres que nomeia o grupo de ordenação de carga do qual esse serviço é membro.</span><span class="sxs-lookup"><span data-stu-id="43cf1-234">This column contains the string that names the load ordering group of which this service is a member.</span></span> <span data-ttu-id="43cf1-235">Especifique uma cadeia de caracteres nula ou vazia se o serviço não pertencer a um grupo.</span><span class="sxs-lookup"><span data-stu-id="43cf1-235">Specify null or an empty string if the service does not belong to a group.</span></span>

</dd> <dt>

<span data-ttu-id="43cf1-236"><span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Depend</span><span class="sxs-lookup"><span data-stu-id="43cf1-236"><span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Dependencies</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-237">Esta coluna é uma lista de nomes de serviços ou grupos de ordenação de carga que o sistema deve iniciar antes desse serviço.</span><span class="sxs-lookup"><span data-stu-id="43cf1-237">This column is a list of names of services or load ordering groups that the system must start before this service.</span></span> <span data-ttu-id="43cf1-238">Separe os nomes na lista por nulos.</span><span class="sxs-lookup"><span data-stu-id="43cf1-238">Separate names in the list by Nulls.</span></span> <span data-ttu-id="43cf1-239">Se o serviço não tiver dependências, especifique NULL ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="43cf1-239">If the service has no dependencies, then specify Null or an empty string.</span></span> <span data-ttu-id="43cf1-240">Use a sintaxe \[ ~ \] para inserir um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="43cf1-240">Use the syntax \[~\] to insert a Null.</span></span> <span data-ttu-id="43cf1-241">A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="43cf1-241">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.</span></span>

<span data-ttu-id="43cf1-242">Por exemplo, para exigir que o sistema inicie Service1 e Service2, antes de iniciar o serviço listado na coluna instalar, insira Service1 \[ ~ \] Service2 \[ ~ \] \[ ~ \] na coluna dependências.</span><span class="sxs-lookup"><span data-stu-id="43cf1-242">For example, to require that the system start service1 and service2, before starting the service listed in the ServiceInstall column, enter service1\[~\]service2\[~\]\[~\] into the Dependencies column.</span></span> <span data-ttu-id="43cf1-243">Os identificadores Service1 e Service2 devem ocorrer na chave primária da tabela ou ser o nome do serviço que já está instalado.</span><span class="sxs-lookup"><span data-stu-id="43cf1-243">The identifiers service1 and service2 must either occur in the primary key of the table or be the name of the service that is already installed.</span></span>

<span data-ttu-id="43cf1-244">Você deve prefixar nomes de grupos com + para que eles possam ser diferenciados de um nome de serviço.</span><span class="sxs-lookup"><span data-stu-id="43cf1-244">You must prefix group names with + so that they can be distinguished from a service name.</span></span> <span data-ttu-id="43cf1-245">Para exigir que o sistema inicie o Service1 e pelo menos um membro do grupo de pedidos myGroup antes de iniciar o serviço listado na coluna Service install, insira Service1 \[ ~ \] + myGroup \[ ~ \] \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="43cf1-245">To require that the system start service1 and at least one member of the ordering group MyGroup before starting the service listed in the ServiceInstall column, enter service1\[~\]+MyGroup\[~\]\[~\].</span></span>

</dd> <dt>

<span data-ttu-id="43cf1-246"><span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName</span><span class="sxs-lookup"><span data-stu-id="43cf1-246"><span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-247">O serviço está conectado como o nome fornecido pela cadeia de caracteres nesta coluna.</span><span class="sxs-lookup"><span data-stu-id="43cf1-247">The service is logged on as the name given by the string in this column.</span></span> <span data-ttu-id="43cf1-248">Se o tipo de serviço for serviço de \_ próprio processo do Win32, \_ \_ use um nome de conta no formato: DomainName \\ username.</span><span class="sxs-lookup"><span data-stu-id="43cf1-248">If the service type is SERVICE\_WIN32\_OWN\_PROCESS use an account name in the form: DomainName\\UserName.</span></span> <span data-ttu-id="43cf1-249">Se a conta pertencer ao domínio interno, será permitido especificar. \\ Usu.</span><span class="sxs-lookup"><span data-stu-id="43cf1-249">If the account belongs to the built-in domain it is permitted to specify .\\UserName.</span></span> <span data-ttu-id="43cf1-250">A conta LocalSystem deve ser usada se o tipo de serviço for serviço \_ de \_ compartilhamento do Win32 \_ ou \_ processo interativo do serviço \_ .</span><span class="sxs-lookup"><span data-stu-id="43cf1-250">The LocalSystem account must be used if the type of service is SERVICE\_WIN32\_SHARE\_PROCESS or SERVICE\_INTERACTIVE\_PROCESS.</span></span> <span data-ttu-id="43cf1-251">A função [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) usará a conta LocalSystem se StartName for especificado como NULL e a maioria dos serviços, portanto, deixar essa coluna em branco.</span><span class="sxs-lookup"><span data-stu-id="43cf1-251">The [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) function uses the LocalSystem account if StartName is specified as null and most services therefore leave this column blank.</span></span>

</dd> <dt>

<span data-ttu-id="43cf1-252"><span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>La</span><span class="sxs-lookup"><span data-stu-id="43cf1-252"><span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>Password</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-253">Essa cadeia de caracteres é a senha para o nome da conta especificada na coluna StartName.</span><span class="sxs-lookup"><span data-stu-id="43cf1-253">This string is the password to the account name specified in the StartName column.</span></span> <span data-ttu-id="43cf1-254">Observe que o usuário deve ter permissões para fazer logon como um serviço.</span><span class="sxs-lookup"><span data-stu-id="43cf1-254">Note that the user must have permissions to log on as a service.</span></span> <span data-ttu-id="43cf1-255">O serviço não terá senha se StartName for nulo ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="43cf1-255">The service has no password if StartName is null or an empty string.</span></span> <span data-ttu-id="43cf1-256">O StartName do LocalSystem é nulo e, portanto, a senha dessa instância é nula, portanto, a maioria dos serviços deixa essa coluna em branco.</span><span class="sxs-lookup"><span data-stu-id="43cf1-256">The Startname of LocalSystem is null, and therefore the password in this instance is null, so most services leave this column blank.</span></span>

<span data-ttu-id="43cf1-257">Observe que, depois de excluir um serviço que foi instalado com um nome de usuário e senha, o instalador não pode reverter o serviço sem primeiro usar uma ação personalizada para obter a senha.</span><span class="sxs-lookup"><span data-stu-id="43cf1-257">Note that after deleting a service that was installed with a user name and password, the installer cannot rollback the service without first using a custom action to get the password.</span></span> <span data-ttu-id="43cf1-258">O instalador pode adquirir todas as informações necessárias sobre o serviço, exceto a senha, que é armazenada em uma parte protegida do sistema.</span><span class="sxs-lookup"><span data-stu-id="43cf1-258">The installer can acquire all the necessary information about the service except the password, which is stored in a protected part of the system.</span></span> <span data-ttu-id="43cf1-259">A ação personalizada adquire a senha solicitando o usuário, lendo uma propriedade do banco de dados ou lendo um arquivo.</span><span class="sxs-lookup"><span data-stu-id="43cf1-259">The custom action acquires the password by prompting the user, reading a property from the database, or reading a file.</span></span> <span data-ttu-id="43cf1-260">A ação personalizada deve então chamar [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)para fornecer a senha, antes de reinstalar o serviço.</span><span class="sxs-lookup"><span data-stu-id="43cf1-260">The custom action must then call [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga), to supply the password, before reinstalling the service.</span></span>

<span data-ttu-id="43cf1-261">Windows Installer não grava o valor inserido no campo de senha no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="43cf1-261">Windows Installer does not write the value entered into the Password field into the log file.</span></span>

</dd> <dt>

<span data-ttu-id="43cf1-262"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos</span><span class="sxs-lookup"><span data-stu-id="43cf1-262"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-263">Esta coluna contém quaisquer argumentos de linha de comando ou propriedades necessárias para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="43cf1-263">This column contains any command line arguments or properties required to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="43cf1-264"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="43cf1-264"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-265">Chave externa para a coluna um da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="43cf1-265">External key to column one of the [Component Table](component-table.md).</span></span> <span data-ttu-id="43cf1-266">Observe que para instalar esse serviço usando a tabela InstallService, o caminho Keypara esse componente deve ser o arquivo executável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="43cf1-266">Note that to install this service using the InstallService table, the KeyPath for this component must be the executable file for the service.</span></span>

</dd> <dt>

<span data-ttu-id="43cf1-267"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição</span><span class="sxs-lookup"><span data-stu-id="43cf1-267"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="43cf1-268">Esta coluna contém uma descrição localizável para o serviço que está sendo configurado.</span><span class="sxs-lookup"><span data-stu-id="43cf1-268">This column contains a localizable description for the service being configured.</span></span> <span data-ttu-id="43cf1-269">Se essa coluna for deixada em branco, o instalador usará a descrição existente do serviço, se houver.</span><span class="sxs-lookup"><span data-stu-id="43cf1-269">If this column is left blank the installer uses the existing description of the service if one exists.</span></span> <span data-ttu-id="43cf1-270">Para obter mais informações, consulte \_ a descrição do serviço no kit de desenvolvimento de software (SDK) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="43cf1-270">For more information, see SERVICE\_DESCRIPTION in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="43cf1-271">Para apagar uma descrição existente, insira " \[ ~ \] " nesta coluna.</span><span class="sxs-lookup"><span data-stu-id="43cf1-271">To erase an existing description enter "\[~\]" in this column.</span></span> <span data-ttu-id="43cf1-272">Isso resulta em uma descrição em branco para um serviço novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="43cf1-272">This results in a blank description for either a new or existing service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43cf1-273">Comentários</span><span class="sxs-lookup"><span data-stu-id="43cf1-273">Remarks</span></span>

<span data-ttu-id="43cf1-274">A ação [installservices](installservices-action.md) em [*tabelas de sequência*](s-gly.md) processa as informações nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="43cf1-274">The [InstallServices](installservices-action.md) action in [*sequence tables*](s-gly.md) processes the information in this table.</span></span> <span data-ttu-id="43cf1-275">Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="43cf1-275">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="43cf1-276">Esta tabela tem a maioria dos parâmetros para a função [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) do Win32.</span><span class="sxs-lookup"><span data-stu-id="43cf1-276">This table has most of the parameters to the Win32 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) function.</span></span>

<span data-ttu-id="43cf1-277">Embora seja possível usar a interface do usuário para especificar que um serviço seja instalado como execução da origem, o instalador não dá suporte a esse tipo de instalação.</span><span class="sxs-lookup"><span data-stu-id="43cf1-277">Although it is possible to use the user interface to specify that a service be installed as run-from-source, the installer does not actually support this type of installation.</span></span> <span data-ttu-id="43cf1-278">Os serviços executados com o nível de privilégio do sistema local devem ser instalados para serem executados do disco rígido local.</span><span class="sxs-lookup"><span data-stu-id="43cf1-278">Services that run with the privilege level of the local system must be installed to run from the local hard drive.</span></span> <span data-ttu-id="43cf1-279">Evite instalar serviços que representam os privilégios de um usuário específico, pois isso pode gravar dados de segurança em um log ou no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="43cf1-279">Avoid installing services that impersonate the privileges of a particular user because this may write security data into a log or the system registry.</span></span> <span data-ttu-id="43cf1-280">Isso pode potencialmente criar um problema de segurança, um conflito de senha ou a perda de dados de configuração quando o sistema é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="43cf1-280">This can potentially create a security problem, password conflict, or the loss of configuration data when the system is restarted.</span></span>

<span data-ttu-id="43cf1-281">Para excluir um serviço durante uma desinstalação, deve haver um registro correspondente para o serviço na [tabela de UserControl](servicecontrol-table.md) e o sinalizador **msidbServiceControlEventUninstallDelete** deve aparecer na coluna de evento.</span><span class="sxs-lookup"><span data-stu-id="43cf1-281">To delete a service during an uninstallation, there must be a corresponding record for the service in the [ServiceControl table](servicecontrol-table.md) and the **msidbServiceControlEventUninstallDelete** flag must appear in the Event column.</span></span> <span data-ttu-id="43cf1-282">O instalador não exclui um serviço na tabela de instalação durante a desinstalação sem essa entrada na tabela de UserControl.</span><span class="sxs-lookup"><span data-stu-id="43cf1-282">The installer does not delete a service in the ServiceInstall table during uninstallation without this entry in the ServiceControl table.</span></span>

<span data-ttu-id="43cf1-283">Para obter informações sobre como proteger um serviço, consulte a [tabela MsiLockPermissionsEx](msilockpermissionsex-table.md).</span><span class="sxs-lookup"><span data-stu-id="43cf1-283">For information on how to secure a service see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="43cf1-284">Validação</span><span class="sxs-lookup"><span data-stu-id="43cf1-284">Validation</span></span>

<dl>

[<span data-ttu-id="43cf1-285">ICE03</span><span class="sxs-lookup"><span data-stu-id="43cf1-285">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="43cf1-286">ICE06</span><span class="sxs-lookup"><span data-stu-id="43cf1-286">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="43cf1-287">ICE32</span><span class="sxs-lookup"><span data-stu-id="43cf1-287">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="43cf1-288">ICE45</span><span class="sxs-lookup"><span data-stu-id="43cf1-288">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="43cf1-289">ICE46</span><span class="sxs-lookup"><span data-stu-id="43cf1-289">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="43cf1-290">ICE66</span><span class="sxs-lookup"><span data-stu-id="43cf1-290">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="43cf1-291">ICE69</span><span class="sxs-lookup"><span data-stu-id="43cf1-291">ICE69</span></span>](ice69.md)  
</dl>

 

 
