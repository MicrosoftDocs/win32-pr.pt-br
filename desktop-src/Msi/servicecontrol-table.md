---
description: A tabela de controle de serviço é usada para controlar os serviços instalados ou desinstalados. Observação os serviços que dependem da presença de um assembly no GAC (cache de assembly global) não podem ser instalados ou iniciados usando as tabelas do serviço de instalação e de controle.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: Tabela de UserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2abd123e937673694dffd53773a16fcbd704c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662530"
---
# <a name="servicecontrol-table"></a><span data-ttu-id="12646-103">Tabela de UserControl</span><span class="sxs-lookup"><span data-stu-id="12646-103">ServiceControl Table</span></span>

<span data-ttu-id="12646-104">A tabela de controle de serviço é usada para controlar os serviços instalados ou desinstalados.</span><span class="sxs-lookup"><span data-stu-id="12646-104">The ServiceControl table is used to control installed or uninstalled services.</span></span>

> [!Note]  
> <span data-ttu-id="12646-105">Os serviços que dependem da presença de um [assembly](assemblies.md) no GAC (cache de assembly global) não podem ser instalados ou iniciados usando as tabelas de serviço e serviço de [instalação](serviceinstall-table.md) .</span><span class="sxs-lookup"><span data-stu-id="12646-105">Services that rely on the presence of an [assembly](assemblies.md) in the Global Assembly Cache (GAC) cannot be installed or started using the [ServiceInstall](serviceinstall-table.md) and ServiceControl tables.</span></span> <span data-ttu-id="12646-106">Se você precisar iniciar um serviço que depende de um assembly no GAC, deverá usar uma ação personalizada sequenciada após a [ação InstallFinalize](installfinalize-action.md) ou uma [ação personalizada Commit](commit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="12646-106">If you need to start a service that depends on an assembly in the GAC, you must use a custom action sequenced after the [InstallFinalize action](installfinalize-action.md) or a [commit custom action](commit-custom-actions.md).</span></span> <span data-ttu-id="12646-107">Para obter informações sobre como instalar assemblies no GAC, consulte [instalação de assemblies no cache de assembly global](installation-of-assemblies-to-the-global-assembly-cache.md).</span><span class="sxs-lookup"><span data-stu-id="12646-107">For information about installing assemblies to the GAC see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md).</span></span>

 

<span data-ttu-id="12646-108">A tabela de controle de origem tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="12646-108">The ServiceControl table has the following columns.</span></span>



| <span data-ttu-id="12646-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="12646-109">Column</span></span>         | <span data-ttu-id="12646-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="12646-110">Type</span></span>                         | <span data-ttu-id="12646-111">Chave</span><span class="sxs-lookup"><span data-stu-id="12646-111">Key</span></span> | <span data-ttu-id="12646-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="12646-112">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="12646-113">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="12646-113">ServiceControl</span></span> | [<span data-ttu-id="12646-114">Identificador</span><span class="sxs-lookup"><span data-stu-id="12646-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="12646-115">S</span><span class="sxs-lookup"><span data-stu-id="12646-115">Y</span></span>   | <span data-ttu-id="12646-116">N</span><span class="sxs-lookup"><span data-stu-id="12646-116">N</span></span>        |
| <span data-ttu-id="12646-117">Nome</span><span class="sxs-lookup"><span data-stu-id="12646-117">Name</span></span>           | [<span data-ttu-id="12646-118">Binário</span><span class="sxs-lookup"><span data-stu-id="12646-118">Formatted</span></span>](formatted.md)   | <span data-ttu-id="12646-119">N</span><span class="sxs-lookup"><span data-stu-id="12646-119">N</span></span>   | <span data-ttu-id="12646-120">N</span><span class="sxs-lookup"><span data-stu-id="12646-120">N</span></span>        |
| <span data-ttu-id="12646-121">Evento</span><span class="sxs-lookup"><span data-stu-id="12646-121">Event</span></span>          | [<span data-ttu-id="12646-122">Inteiro</span><span class="sxs-lookup"><span data-stu-id="12646-122">Integer</span></span>](integer.md)       | <span data-ttu-id="12646-123">N</span><span class="sxs-lookup"><span data-stu-id="12646-123">N</span></span>   | <span data-ttu-id="12646-124">N</span><span class="sxs-lookup"><span data-stu-id="12646-124">N</span></span>        |
| <span data-ttu-id="12646-125">Argumentos</span><span class="sxs-lookup"><span data-stu-id="12646-125">Arguments</span></span>      | [<span data-ttu-id="12646-126">Binário</span><span class="sxs-lookup"><span data-stu-id="12646-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="12646-127">N</span><span class="sxs-lookup"><span data-stu-id="12646-127">N</span></span>   | <span data-ttu-id="12646-128">S</span><span class="sxs-lookup"><span data-stu-id="12646-128">Y</span></span>        |
| <span data-ttu-id="12646-129">Aguarde</span><span class="sxs-lookup"><span data-stu-id="12646-129">Wait</span></span>           | [<span data-ttu-id="12646-130">Inteiro</span><span class="sxs-lookup"><span data-stu-id="12646-130">Integer</span></span>](integer.md)       | <span data-ttu-id="12646-131">N</span><span class="sxs-lookup"><span data-stu-id="12646-131">N</span></span>   | <span data-ttu-id="12646-132">S</span><span class="sxs-lookup"><span data-stu-id="12646-132">Y</span></span>        |
| <span data-ttu-id="12646-133">Componente\_</span><span class="sxs-lookup"><span data-stu-id="12646-133">Component\_</span></span>    | [<span data-ttu-id="12646-134">Identificador</span><span class="sxs-lookup"><span data-stu-id="12646-134">Identifier</span></span>](identifier.md) | <span data-ttu-id="12646-135">N</span><span class="sxs-lookup"><span data-stu-id="12646-135">N</span></span>   | <span data-ttu-id="12646-136">N</span><span class="sxs-lookup"><span data-stu-id="12646-136">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="12646-137">Colunas</span><span class="sxs-lookup"><span data-stu-id="12646-137">Columns</span></span>

<dl> <dt>

<span data-ttu-id="12646-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span><span class="sxs-lookup"><span data-stu-id="12646-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span></span>
</dt> <dd>

<span data-ttu-id="12646-139">Esta é a chave primária desta tabela.</span><span class="sxs-lookup"><span data-stu-id="12646-139">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="12646-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="12646-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="12646-141">Esta coluna é a cadeia de caracteres que nomeia o serviço.</span><span class="sxs-lookup"><span data-stu-id="12646-141">This column is the string naming the service.</span></span> <span data-ttu-id="12646-142">Esta coluna pode ser usada para controlar um serviço que não está instalado.</span><span class="sxs-lookup"><span data-stu-id="12646-142">This column can be used to control a service that is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="12646-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Circunstância</span><span class="sxs-lookup"><span data-stu-id="12646-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="12646-144">Esta coluna contém as operações a serem executadas no serviço nomeado.</span><span class="sxs-lookup"><span data-stu-id="12646-144">This column contains the operations to be performed on the named service.</span></span> <span data-ttu-id="12646-145">Observe que, ao parar um serviço, todos os serviços que dependem desse serviço também são interrompidos.</span><span class="sxs-lookup"><span data-stu-id="12646-145">Note that when stopping a service, all services that depend on that service are also stopped.</span></span> <span data-ttu-id="12646-146">Ao excluir um serviço que está em execução, o instalador interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="12646-146">When deleting a service that is running, the installer stops the service.</span></span>

<span data-ttu-id="12646-147">Os valores nesse campo são campos de bits que podem ser combinados em um único valor que representa várias operações.</span><span class="sxs-lookup"><span data-stu-id="12646-147">The values in this field are bit fields that can be combined into a single value that represents several operations.</span></span>

<span data-ttu-id="12646-148">Os valores a seguir são usados apenas durante uma instalação.</span><span class="sxs-lookup"><span data-stu-id="12646-148">The following values are only used during an installation.</span></span>



| <span data-ttu-id="12646-149">Constante</span><span class="sxs-lookup"><span data-stu-id="12646-149">Constant</span></span>                           | <span data-ttu-id="12646-150">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="12646-150">Hexadecimal</span></span> | <span data-ttu-id="12646-151">Decimal</span><span class="sxs-lookup"><span data-stu-id="12646-151">Decimal</span></span> | <span data-ttu-id="12646-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="12646-152">Description</span></span>                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="12646-153">**msidbServiceControlEventStart**</span><span class="sxs-lookup"><span data-stu-id="12646-153">**msidbServiceControlEventStart**</span></span>  | <span data-ttu-id="12646-154">0x001</span><span class="sxs-lookup"><span data-stu-id="12646-154">0x001</span></span>       | <span data-ttu-id="12646-155">1</span><span class="sxs-lookup"><span data-stu-id="12646-155">1</span></span>       | <span data-ttu-id="12646-156">Inicia o serviço durante a [ação iniciarservices](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="12646-156">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="12646-157">**msidbServiceControlEventStop**</span><span class="sxs-lookup"><span data-stu-id="12646-157">**msidbServiceControlEventStop**</span></span>   | <span data-ttu-id="12646-158">0x002</span><span class="sxs-lookup"><span data-stu-id="12646-158">0x002</span></span>       | <span data-ttu-id="12646-159">2</span><span class="sxs-lookup"><span data-stu-id="12646-159">2</span></span>       | <span data-ttu-id="12646-160">Interrompe o serviço durante a [ação StopServices](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="12646-160">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="12646-161">(nenhum)</span><span class="sxs-lookup"><span data-stu-id="12646-161">(none)</span></span>                             | <span data-ttu-id="12646-162">0x004</span><span class="sxs-lookup"><span data-stu-id="12646-162">0x004</span></span>       | <span data-ttu-id="12646-163">4</span><span class="sxs-lookup"><span data-stu-id="12646-163">4</span></span>       | <reserved>                                                                   |
| <span data-ttu-id="12646-164">**msidbServiceControlEventDelete**</span><span class="sxs-lookup"><span data-stu-id="12646-164">**msidbServiceControlEventDelete**</span></span> | <span data-ttu-id="12646-165">0x008</span><span class="sxs-lookup"><span data-stu-id="12646-165">0x008</span></span>       | <span data-ttu-id="12646-166">8</span><span class="sxs-lookup"><span data-stu-id="12646-166">8</span></span>       | <span data-ttu-id="12646-167">Exclui o serviço durante a [ação DeleteServices](deleteservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="12646-167">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

<span data-ttu-id="12646-168">Os valores a seguir são usados apenas durante uma desinstalação.</span><span class="sxs-lookup"><span data-stu-id="12646-168">The following values are only used during an uninstall.</span></span>



| <span data-ttu-id="12646-169">Constante</span><span class="sxs-lookup"><span data-stu-id="12646-169">Constant</span></span>                                    | <span data-ttu-id="12646-170">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="12646-170">Hexadecimal</span></span> | <span data-ttu-id="12646-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="12646-171">Decimal</span></span> | <span data-ttu-id="12646-172">Descrição</span><span class="sxs-lookup"><span data-stu-id="12646-172">Description</span></span>                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="12646-173">**msidbServiceControlEventUninstallStart**</span><span class="sxs-lookup"><span data-stu-id="12646-173">**msidbServiceControlEventUninstallStart**</span></span>  | <span data-ttu-id="12646-174">0x010</span><span class="sxs-lookup"><span data-stu-id="12646-174">0x010</span></span>       | <span data-ttu-id="12646-175">16</span><span class="sxs-lookup"><span data-stu-id="12646-175">16</span></span>      | <span data-ttu-id="12646-176">Inicia o serviço durante a [ação iniciarservices](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="12646-176">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="12646-177">**msidbServiceControlEventUninstallStop**</span><span class="sxs-lookup"><span data-stu-id="12646-177">**msidbServiceControlEventUninstallStop**</span></span>   | <span data-ttu-id="12646-178">0x020</span><span class="sxs-lookup"><span data-stu-id="12646-178">0x020</span></span>       | <span data-ttu-id="12646-179">32</span><span class="sxs-lookup"><span data-stu-id="12646-179">32</span></span>      | <span data-ttu-id="12646-180">Interrompe o serviço durante a [ação StopServices](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="12646-180">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="12646-181">(nenhum)</span><span class="sxs-lookup"><span data-stu-id="12646-181">(none)</span></span>                                      | <span data-ttu-id="12646-182">0x040</span><span class="sxs-lookup"><span data-stu-id="12646-182">0x040</span></span>       | <span data-ttu-id="12646-183">64</span><span class="sxs-lookup"><span data-stu-id="12646-183">64</span></span>      | <reserved>                                                                   |
| <span data-ttu-id="12646-184">**msidbServiceControlEventUninstallDelete**</span><span class="sxs-lookup"><span data-stu-id="12646-184">**msidbServiceControlEventUninstallDelete**</span></span> | <span data-ttu-id="12646-185">0x080</span><span class="sxs-lookup"><span data-stu-id="12646-185">0x080</span></span>       | <span data-ttu-id="12646-186">128</span><span class="sxs-lookup"><span data-stu-id="12646-186">128</span></span>     | <span data-ttu-id="12646-187">Exclui o serviço durante a [ação DeleteServices](deleteservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="12646-187">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="12646-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos</span><span class="sxs-lookup"><span data-stu-id="12646-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="12646-189">Uma lista de argumentos para iniciar serviços.</span><span class="sxs-lookup"><span data-stu-id="12646-189">A list of arguments for starting services.</span></span> <span data-ttu-id="12646-190">Os argumentos são separados por caracteres nulos \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="12646-190">The arguments are separated by null characters \[~\].</span></span> <span data-ttu-id="12646-191">Por exemplo, a lista de argumentos um, dois e três são listados como: um \[ ~ \] dois \[ ~ \] três.</span><span class="sxs-lookup"><span data-stu-id="12646-191">For example, the list of arguments One, Two, and Three are listed as: One\[~\]Two\[~\]Three.</span></span>

</dd> <dt>

<span data-ttu-id="12646-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Esperado</span><span class="sxs-lookup"><span data-stu-id="12646-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Wait</span></span>
</dt> <dd>

<span data-ttu-id="12646-193">Deixar esse campo nulo ou inserir um valor de 1 faz com que o instalador Aguarde um máximo de 30 segundos para que o serviço seja concluído antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="12646-193">Leaving this field null or entering a value of 1 causes the installer to wait a maximum of 30 seconds for the service to complete before proceeding.</span></span> <span data-ttu-id="12646-194">A espera pode ser usada para permitir um tempo adicional para um evento crítico retornar um erro de falha.</span><span class="sxs-lookup"><span data-stu-id="12646-194">The wait can be used to allow additional time for a critical event to return a failure error.</span></span> <span data-ttu-id="12646-195">Um valor de 0 neste campo significa aguardar somente até que o SCM (Gerenciador de controle de serviço) informe que esse serviço está em um estado pendente antes de continuar com a instalação.</span><span class="sxs-lookup"><span data-stu-id="12646-195">A value of 0 in this field means to wait only until the service control manager (SCM) reports that this service is in a pending state before continuing with the installation.</span></span>

</dd> <dt>

<span data-ttu-id="12646-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="12646-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="12646-197">Chave externa para a coluna um da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="12646-197">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12646-198">Comentários</span><span class="sxs-lookup"><span data-stu-id="12646-198">Remarks</span></span>

<span data-ttu-id="12646-199">As ações [startservices](startservices-action.md), [StopServices](stopservices-action.md)e [DeleteServices](deleteservices-action.md) em [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="12646-199">The [StartServices](startservices-action.md), [StopServices](stopservices-action.md), and [DeleteServices](deleteservices-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="12646-200">Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="12646-200">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="12646-201">Use a coluna nome para iniciar, parar ou excluir serviços que estão sendo substituídos pela instalação do ou que dependem de um novo serviço que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="12646-201">Use the Name column to start, stop, or delete services that are being replaced by the installation or that are dependent upon a new service that is being installed.</span></span> <span data-ttu-id="12646-202">Por exemplo, a inserção de MyService na coluna de controle de serviço pode vincular esse serviço a myComponent na \_ coluna Component.</span><span class="sxs-lookup"><span data-stu-id="12646-202">For example, entering MyService into the ServiceControl column can tie this service to MyComponent in the Component\_ column.</span></span> <span data-ttu-id="12646-203">Se o campo de bits na coluna evento for definido como iniciar durante a instalação, o instalador iniciará MyService ao instalar myComponent.</span><span class="sxs-lookup"><span data-stu-id="12646-203">If the bit field in the Event column is set for start while installing, then the installer starts MyService when installing MyComponent.</span></span>

## <a name="validation"></a><span data-ttu-id="12646-204">Validação</span><span class="sxs-lookup"><span data-stu-id="12646-204">Validation</span></span>

<dl>

[<span data-ttu-id="12646-205">ICE03</span><span class="sxs-lookup"><span data-stu-id="12646-205">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="12646-206">ICE06</span><span class="sxs-lookup"><span data-stu-id="12646-206">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="12646-207">ICE32</span><span class="sxs-lookup"><span data-stu-id="12646-207">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="12646-208">ICE45</span><span class="sxs-lookup"><span data-stu-id="12646-208">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="12646-209">ICE46</span><span class="sxs-lookup"><span data-stu-id="12646-209">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="12646-210">ICE69</span><span class="sxs-lookup"><span data-stu-id="12646-210">ICE69</span></span>](ice69.md)  
</dl>

 

 



