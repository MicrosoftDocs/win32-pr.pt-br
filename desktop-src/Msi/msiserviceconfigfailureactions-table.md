---
description: A tabela MsiServiceConfigFailureActions lista as operações a serem executadas depois que um serviço falha. As operações especificadas nesta tabela serão executadas na próxima vez em que o sistema for iniciado.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Tabela MsiServiceConfigFailureActions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769313"
---
# <a name="msiserviceconfigfailureactions-table"></a><span data-ttu-id="d6fe0-104">Tabela MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="d6fe0-104">MsiServiceConfigFailureActions Table</span></span>

<span data-ttu-id="d6fe0-105">A tabela MsiServiceConfigFailureActions lista as operações a serem executadas depois que um serviço falha.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-105">The MsiServiceConfigFailureActions table lists operations to be run after a service fails.</span></span> <span data-ttu-id="d6fe0-106">As operações especificadas nesta tabela serão executadas na próxima vez em que o sistema for iniciado.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-106">The operations specified in this table run the next time the system is started.</span></span>

<span data-ttu-id="d6fe0-107">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="d6fe0-108">Esta tabela está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="d6fe0-109">A tabela MsiServiceConfigFailureActions tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-109">The MsiServiceConfigFailureActions table has the following columns.</span></span>



| <span data-ttu-id="d6fe0-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="d6fe0-110">Column</span></span>                         | <span data-ttu-id="d6fe0-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6fe0-111">Type</span></span>                         | <span data-ttu-id="d6fe0-112">Chave</span><span class="sxs-lookup"><span data-stu-id="d6fe0-112">Key</span></span> | <span data-ttu-id="d6fe0-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="d6fe0-113">Nullable</span></span> |
|--------------------------------|------------------------------|-----|----------|
| <span data-ttu-id="d6fe0-114">MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="d6fe0-114">MsiServiceConfigFailureActions</span></span> | [<span data-ttu-id="d6fe0-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="d6fe0-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="d6fe0-116">S</span><span class="sxs-lookup"><span data-stu-id="d6fe0-116">Y</span></span>   | <span data-ttu-id="d6fe0-117">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-117">N</span></span>        |
| <span data-ttu-id="d6fe0-118">Nome</span><span class="sxs-lookup"><span data-stu-id="d6fe0-118">Name</span></span>                           | [<span data-ttu-id="d6fe0-119">Binário</span><span class="sxs-lookup"><span data-stu-id="d6fe0-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d6fe0-120">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-120">N</span></span>   | <span data-ttu-id="d6fe0-121">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-121">N</span></span>        |
| <span data-ttu-id="d6fe0-122">Evento</span><span class="sxs-lookup"><span data-stu-id="d6fe0-122">Event</span></span>                          | [<span data-ttu-id="d6fe0-123">Inteiro</span><span class="sxs-lookup"><span data-stu-id="d6fe0-123">Integer</span></span>](integer.md)       | <span data-ttu-id="d6fe0-124">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-124">N</span></span>   | <span data-ttu-id="d6fe0-125">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-125">N</span></span>        |
| <span data-ttu-id="d6fe0-126">ResetPeriod</span><span class="sxs-lookup"><span data-stu-id="d6fe0-126">ResetPeriod</span></span>                    | [<span data-ttu-id="d6fe0-127">Inteiro</span><span class="sxs-lookup"><span data-stu-id="d6fe0-127">Integer</span></span>](integer.md)       | <span data-ttu-id="d6fe0-128">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-128">N</span></span>   | <span data-ttu-id="d6fe0-129">S</span><span class="sxs-lookup"><span data-stu-id="d6fe0-129">Y</span></span>        |
| <span data-ttu-id="d6fe0-130">RebootMessage</span><span class="sxs-lookup"><span data-stu-id="d6fe0-130">RebootMessage</span></span>                  | [<span data-ttu-id="d6fe0-131">Binário</span><span class="sxs-lookup"><span data-stu-id="d6fe0-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d6fe0-132">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-132">N</span></span>   | <span data-ttu-id="d6fe0-133">Y</span><span class="sxs-lookup"><span data-stu-id="d6fe0-133">Y</span></span>        |
| <span data-ttu-id="d6fe0-134">Comando</span><span class="sxs-lookup"><span data-stu-id="d6fe0-134">Command</span></span>                        | [<span data-ttu-id="d6fe0-135">Binário</span><span class="sxs-lookup"><span data-stu-id="d6fe0-135">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d6fe0-136">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-136">N</span></span>   | <span data-ttu-id="d6fe0-137">S</span><span class="sxs-lookup"><span data-stu-id="d6fe0-137">Y</span></span>        |
| <span data-ttu-id="d6fe0-138">Ações</span><span class="sxs-lookup"><span data-stu-id="d6fe0-138">Actions</span></span>                        | [<span data-ttu-id="d6fe0-139">Text</span><span class="sxs-lookup"><span data-stu-id="d6fe0-139">Text</span></span>](text.md)             | <span data-ttu-id="d6fe0-140">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-140">N</span></span>   | <span data-ttu-id="d6fe0-141">S</span><span class="sxs-lookup"><span data-stu-id="d6fe0-141">Y</span></span>        |
| <span data-ttu-id="d6fe0-142">DelayActions</span><span class="sxs-lookup"><span data-stu-id="d6fe0-142">DelayActions</span></span>                   | [<span data-ttu-id="d6fe0-143">Text</span><span class="sxs-lookup"><span data-stu-id="d6fe0-143">Text</span></span>](text.md)             | <span data-ttu-id="d6fe0-144">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-144">N</span></span>   | <span data-ttu-id="d6fe0-145">S</span><span class="sxs-lookup"><span data-stu-id="d6fe0-145">Y</span></span>        |
| <span data-ttu-id="d6fe0-146">Componente\_</span><span class="sxs-lookup"><span data-stu-id="d6fe0-146">Component\_</span></span>                    | [<span data-ttu-id="d6fe0-147">Identificador</span><span class="sxs-lookup"><span data-stu-id="d6fe0-147">Identifier</span></span>](identifier.md) | <span data-ttu-id="d6fe0-148">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-148">N</span></span>   | <span data-ttu-id="d6fe0-149">N</span><span class="sxs-lookup"><span data-stu-id="d6fe0-149">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d6fe0-150">Colunas</span><span class="sxs-lookup"><span data-stu-id="d6fe0-150">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d6fe0-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="d6fe0-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span></span>
</dt> <dd>

<span data-ttu-id="d6fe0-152">Esta é a chave primária desta tabela que identifica uma ação de falha.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-152">This is the primary key of this table that identifies a failure action.</span></span>

</dd> <dt>

<span data-ttu-id="d6fe0-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="d6fe0-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="d6fe0-154">Esta coluna contém o nome de um serviço que faz parte deste pacote ou que já está instalado.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-154">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="d6fe0-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Circunstância</span><span class="sxs-lookup"><span data-stu-id="d6fe0-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="d6fe0-156">Esta coluna especifica quando alterar a configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-156">This column specifies when to change the service's configuration.</span></span> <span data-ttu-id="d6fe0-157">Os valores a seguir são campos de bits que podem ser combinados para representar várias operações.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-157">The following values are bit fields that can be combined to represent multiple operations.</span></span> <span data-ttu-id="d6fe0-158">Qualquer outro valor de campo de bit é ignorado.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-158">Any other bit field values are ignored.</span></span>



| <span data-ttu-id="d6fe0-159">Constante</span><span class="sxs-lookup"><span data-stu-id="d6fe0-159">Constant</span></span>                                         | <span data-ttu-id="d6fe0-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6fe0-160">Description</span></span>                                     |
|--------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="d6fe0-161">**msidbServiceConfigEventInstall** 1</span><span class="sxs-lookup"><span data-stu-id="d6fe0-161">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="d6fe0-162">Alteração durante a instalação do componente.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-162">Change during installation of the component.</span></span>    |
| <span data-ttu-id="d6fe0-163">**msidbServiceConfigEventUninstall** 2</span><span class="sxs-lookup"><span data-stu-id="d6fe0-163">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="d6fe0-164">Alterar durante a desinstalação do componente.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-164">Change during uninstallation of the component.</span></span>  |
| <span data-ttu-id="d6fe0-165">**msidbServiceConfigEventReinstall** 4</span><span class="sxs-lookup"><span data-stu-id="d6fe0-165">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="d6fe0-166">Alteração durante a reinstalação do componente.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-166">Change during re-installation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d6fe0-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span><span class="sxs-lookup"><span data-stu-id="d6fe0-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span></span>
</dt> <dd>

<span data-ttu-id="d6fe0-168">O período de redefinição em segundos de contagem de falhas do serviço.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-168">The reset period in seconds of service's failure count.</span></span> <span data-ttu-id="d6fe0-169">O SCM ( [Gerenciador de controle de serviço](../services/service-control-manager.md) ) conta o número de vezes que cada serviço falhou desde que o sistema foi reiniciado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-169">The [Service Control Manager](../services/service-control-manager.md) (SCM) counts the number of times each service has failed since the system was last restarted.</span></span> <span data-ttu-id="d6fe0-170">A contagem será redefinida para zero se o serviço não falhar durante o período de redefinição.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-170">The count is reset to zero if the service does not fail for the reset period.</span></span> <span data-ttu-id="d6fe0-171">Quando o serviço falha durante o enésimo horário, o sistema executa a ação especificada no elemento \[ N-1 \] da matriz especificada no campo ações.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-171">When the service fails for the Nth time, the system performs the action specified in the element \[N-1\] of the array specified in the Actions field.</span></span>

<span data-ttu-id="d6fe0-172">Deixe o campo ResetPeriod vazio para indicar que a contagem de falhas nunca deve ser redefinida.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-172">Leave ResetPeriod field empty to indicate that failure count should never be reset.</span></span>

</dd> <dt>

<span data-ttu-id="d6fe0-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span><span class="sxs-lookup"><span data-stu-id="d6fe0-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span></span>
</dt> <dd>

<span data-ttu-id="d6fe0-174">A mensagem enviada aos usuários antes de reiniciar o computador em resposta a uma ação **de \_ \_ reinicialização de ação SC** especificada na coluna ações.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-174">The message sent to users before restarting the computer in response to a **SC\_ACTION\_REBOOT** action specified in the Actions column.</span></span> <span data-ttu-id="d6fe0-175">Você pode usar uma cadeia de caracteres vazia, "", para enviar a mensagem atual inalterada.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-175">You can use an empty string, "", to send the current message unchanged.</span></span> <span data-ttu-id="d6fe0-176">Você pode usar \[ ~ \] a sintaxe do tipo de dados [formatado](formatted.md) para excluir a mensagem atual e não enviar nenhuma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-176">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current message and send no message.</span></span>

</dd> <dt>

<span data-ttu-id="d6fe0-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Linha</span><span class="sxs-lookup"><span data-stu-id="d6fe0-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="d6fe0-178">A linha de comando executada pelo processo criado pela função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) em resposta a uma ação **de \_ \_ \_ comando de execução de ação SC** especificada na coluna ações.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-178">The command line run by the process created by the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function in response to a **SC\_ACTION\_RUN\_COMMAND** action specified in the Actions column.</span></span> <span data-ttu-id="d6fe0-179">O novo processo é executado na mesma conta que o serviço e somente se o campo de ação **é \_ \_ \_ comando de execução de ação SC**.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-179">The new process runs under the same account as the service and only if the Action field is **SC\_ACTION\_RUN\_COMMAND**.</span></span> <span data-ttu-id="d6fe0-180">Você pode usar uma cadeia de caracteres vazia, "", para usar a linha de comando atual inalterada.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-180">You can use an empty string, "", to use the current command line unchanged.</span></span> <span data-ttu-id="d6fe0-181">Você pode usar a \[ ~ \] sintaxe do tipo de dados [formatado](formatted.md) para excluir a linha de comando atual e não executar nenhuma operação quando o serviço falhar.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-181">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current command line and run no operation when the service fails.</span></span>

</dd> <dt>

<span data-ttu-id="d6fe0-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Ações</span><span class="sxs-lookup"><span data-stu-id="d6fe0-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Actions</span></span>
</dt> <dd>

<span data-ttu-id="d6fe0-183">Esse campo contém uma matriz de valores inteiros que especificam as ações executadas pelo SCM se o serviço falhar.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-183">This field contains an array of integer values that specify the actions taken by the SCM if the service fails.</span></span> <span data-ttu-id="d6fe0-184">Separe os valores na matriz por \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="d6fe0-184">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="d6fe0-185">O valor inteiro no elemento enésima da matriz Especifica a ação executada quando o serviço falha durante o enésimo horário.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-185">The integer value in the Nth element of the array specifies the action performed when the service fails for the Nth time.</span></span> <span data-ttu-id="d6fe0-186">Cada membro da matriz é um dos valores inteiros a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-186">Each member of the array is one of following integer values.</span></span>



| <span data-ttu-id="d6fe0-187">Constante</span><span class="sxs-lookup"><span data-stu-id="d6fe0-187">Constant</span></span>                                 | <span data-ttu-id="d6fe0-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6fe0-188">Description</span></span>           |
|------------------------------------------|-----------------------|
| <span data-ttu-id="d6fe0-189">**Sc \_ AÇÃO \_ nenhum** 0</span><span class="sxs-lookup"><span data-stu-id="d6fe0-189">**SC\_ACTION\_NONE** 0</span></span><br/>         | <span data-ttu-id="d6fe0-190">Nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-190">No action.</span></span>            |
| <span data-ttu-id="d6fe0-191">**Sc \_ AÇÃO \_ reinicializar** 2</span><span class="sxs-lookup"><span data-stu-id="d6fe0-191">**SC\_ACTION\_REBOOT** 2</span></span><br/>       | <span data-ttu-id="d6fe0-192">Reinicie o computador.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-192">Restart the computer.</span></span> |
| <span data-ttu-id="d6fe0-193">**Sc \_ AÇÃO \_ reiniciada** 1</span><span class="sxs-lookup"><span data-stu-id="d6fe0-193">**SC\_ACTION\_RESTART** 1</span></span><br/>      | <span data-ttu-id="d6fe0-194">Reinicie o serviço.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-194">Restart the service.</span></span>  |
| <span data-ttu-id="d6fe0-195">**Sc \_ \_ \_ Comando de execução de ação** 3</span><span class="sxs-lookup"><span data-stu-id="d6fe0-195">**SC\_ACTION\_RUN\_COMMAND** 3</span></span><br/> | <span data-ttu-id="d6fe0-196">Execute um comando.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-196">Run a command.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="d6fe0-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span><span class="sxs-lookup"><span data-stu-id="d6fe0-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span></span>
</dt> <dd>

<span data-ttu-id="d6fe0-198">Este campo contém uma matriz de valores inteiros que especificam o tempo em milissegundos a aguardar antes de executar a ação especificada na coluna ação.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-198">This field contains an array of integer values that specify the time in milliseconds to wait before performing the action specified in the Action column.</span></span> <span data-ttu-id="d6fe0-199">Separe os valores na matriz por \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="d6fe0-199">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="d6fe0-200">O número de elementos na matriz DelayActions deve ser igual ao número de elementos na matriz actions.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-200">The number of elements in the DelayActions array must be equal to the number of elements in the Actions array.</span></span> <span data-ttu-id="d6fe0-201">O enésimo elemento da matriz DelayActions especifica o atraso de tempo para o enésimo elemento da matriz actions.</span><span class="sxs-lookup"><span data-stu-id="d6fe0-201">The Nth element of the DelayActions array specifies the time delay for the nth element of the Actions array.</span></span>

</dd> <dt>

<span data-ttu-id="d6fe0-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="d6fe0-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="d6fe0-203">Chave externa para a coluna um da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d6fe0-203">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="d6fe0-204">Validação</span><span class="sxs-lookup"><span data-stu-id="d6fe0-204">Validation</span></span>

<dl>

[<span data-ttu-id="d6fe0-205">ICE102</span><span class="sxs-lookup"><span data-stu-id="d6fe0-205">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="d6fe0-206">ICE03</span><span class="sxs-lookup"><span data-stu-id="d6fe0-206">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d6fe0-207">ICE06</span><span class="sxs-lookup"><span data-stu-id="d6fe0-207">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d6fe0-208">ICE32</span><span class="sxs-lookup"><span data-stu-id="d6fe0-208">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d6fe0-209">ICE45</span><span class="sxs-lookup"><span data-stu-id="d6fe0-209">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="d6fe0-210">ICE46</span><span class="sxs-lookup"><span data-stu-id="d6fe0-210">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="d6fe0-211">ICE69</span><span class="sxs-lookup"><span data-stu-id="d6fe0-211">ICE69</span></span>](ice69.md)  
</dl>

 

 
