---
description: A lista a seguir lista os eventos com suporte nos logs WMI no Windows Vista e sistemas operacionais posteriores.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: Mensagens de evento WMI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780680"
---
# <a name="wmi-event-messages"></a><span data-ttu-id="64840-103">Mensagens de evento WMI</span><span class="sxs-lookup"><span data-stu-id="64840-103">WMI Event Messages</span></span>

<span data-ttu-id="64840-104">A lista a seguir lista os eventos com suporte nos logs WMI no Windows Vista e sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="64840-104">The following list lists events supported by WMI logs in Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="64840-105">A documentação a seguir foi projetada para desenvolvedores e administradores de ti.</span><span class="sxs-lookup"><span data-stu-id="64840-105">The following documentation is designed for developers and IT administrators.</span></span> <span data-ttu-id="64840-106">Se você estiver tentando resolver uma mensagem de erro WMI em seu sistema doméstico, consulte o site [suporte da Microsoft](https://support.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="64840-106">If you are attempting to resolve a WMI error message on your home system, please refer to the [Microsoft Support](https://support.microsoft.com/) website.</span></span>

 

<dl> <dt>

<span data-ttu-id="64840-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**\_repositório WBEM \_ MC \_ inconsistente**</span><span class="sxs-lookup"><span data-stu-id="64840-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM\_MC\_REPOSITORY\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-108">1073747424 (0x400015E0)</span><span class="sxs-lookup"><span data-stu-id="64840-108">1073747424 (0x400015E0)</span></span>
</dt> <dt>



<span data-ttu-id="64840-109">O serviço de Instrumentação de Gerenciamento do Windows detectou uma inconsistência com o repositório WMI no diretório *% windir% \\ System32 \\ WBEM \\ Repository* e não pôde recuperá-lo.</span><span class="sxs-lookup"><span data-stu-id="64840-109">The Windows Management Instrumentation Service detected an inconsistency with the WMI repository in the directory *%windir%\\system32\\wbem\\repository* and was not able to recover it.</span></span> <span data-ttu-id="64840-110">O repositório WMI será excluído agora, um novo repositório será criado com base no mecanismo de recuperação automática.</span><span class="sxs-lookup"><span data-stu-id="64840-110">The WMI repository will now be deleted, A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**\_carga do \_ \_ provedor do subsistema \_ LOCALSYSTEM do \_ provedor WBEM MC \_**</span><span class="sxs-lookup"><span data-stu-id="64840-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM\_MC\_PROVIDER\_SUBSYSTEM\_LOCALSYSTEM\_PROVIDER\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-112">2147483711 (0x8000003F)</span><span class="sxs-lookup"><span data-stu-id="64840-112">2147483711 (0x8000003F)</span></span>
</dt> <dt>



<span data-ttu-id="64840-113">Um provedor, %1, foi registrado no namespace Instrumentação de Gerenciamento do Windows %2 para usar a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="64840-113">A provider, %1, has been registered in the Windows Management Instrumentation namespace %2 to use the LocalSystem account.</span></span> <span data-ttu-id="64840-114">Essa conta é privilegiada e o provedor pode causar uma violação de segurança se não representar corretamente as solicitações do usuário.</span><span class="sxs-lookup"><span data-stu-id="64840-114">This account is privileged and the provider may cause a security violation if it does not correctly impersonate user requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM \_ MC \_ MOF \_ não \_ carregado \_ na \_ recuperação**</span><span class="sxs-lookup"><span data-stu-id="64840-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM\_MC\_MOF\_NOT\_LOADED\_AT\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-116">3221225476 (0xC0000004)</span><span class="sxs-lookup"><span data-stu-id="64840-116">3221225476 (0xC0000004)</span></span>
</dt> <dt>



<span data-ttu-id="64840-117">Erro %1 encontrado ao tentar carregar o MOF %2 durante a recuperação. Arquivo MOF marcado com AutoRecuperação.</span><span class="sxs-lookup"><span data-stu-id="64840-117">Error %1 encountered when trying to load MOF %2 while recovering .MOF file marked with autorecover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**o WBEM \_ MC \_ não pode \_ ativar o \_ filtro**</span><span class="sxs-lookup"><span data-stu-id="64840-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM\_MC\_CANNOT\_ACTIVATE\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-119">3221225482 (0xC000000A)</span><span class="sxs-lookup"><span data-stu-id="64840-119">3221225482 (0xC000000A)</span></span>
</dt> <dt>



<span data-ttu-id="64840-120">Não foi possível reativar o filtro de eventos com a consulta "%2" no namespace "%1" devido ao erro %3.</span><span class="sxs-lookup"><span data-stu-id="64840-120">Event filter with query "%2" could not be reactivated in namespace "%1" because of error %3.</span></span> <span data-ttu-id="64840-121">Os eventos não podem ser entregues por meio desse filtro até que o problema seja corrigido.</span><span class="sxs-lookup"><span data-stu-id="64840-121">Events cannot be delivered through this filter until the problem is corrected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**\_consulta do \_ \_ provedor de eventos inválido WBEM MC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64840-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-123">3221225493 (0xC0000015)</span><span class="sxs-lookup"><span data-stu-id="64840-123">3221225493 (0xC0000015)</span></span>
</dt> <dt>



<span data-ttu-id="64840-124">O provedor de eventos %1 tentou registrar uma consulta sintaticamente inválida "%2".</span><span class="sxs-lookup"><span data-stu-id="64840-124">Event provider %1 attempted to register a syntactically invalid query "%2".</span></span> <span data-ttu-id="64840-125">A consulta será ignorada.</span><span class="sxs-lookup"><span data-stu-id="64840-125">The query will be ignored.</span></span> <span data-ttu-id="64840-126">A consulta pode ser corrigida examinando o repositório WMI com o CIM Studio e atualizando as assinaturas permanentes para o provedor e a consulta listados.</span><span class="sxs-lookup"><span data-stu-id="64840-126">The query can be corrected by examining the WMI repository with CIM studio and updating the permanent subscriptions for the listed provider and query.</span></span> <span data-ttu-id="64840-127">Se a assinatura permanente for criada com o arquivo MOF que vem com um produto instalado, o fornecedor do aplicativo deverá ser contatado para corrigir o registro com falha.</span><span class="sxs-lookup"><span data-stu-id="64840-127">If the permanent subscription is created with MOF file coming with an installed product, the application vendor must be contacted to correct the faulty registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**\_ \_ \_ \_ consulta intrínseca do provedor de eventos inválido \_ \_ WBEM MC**</span><span class="sxs-lookup"><span data-stu-id="64840-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_INTRINSIC\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-129">3221225494 (0xC0000016)</span><span class="sxs-lookup"><span data-stu-id="64840-129">3221225494 (0xC0000016)</span></span>
</dt> <dt>



<span data-ttu-id="64840-130">O provedor de eventos %1 tentou registrar uma consulta de evento intrínseca "%2" no namespace %3 para o qual o conjunto de classes de objeto de destino não pôde ser determinado.</span><span class="sxs-lookup"><span data-stu-id="64840-130">Event provider %1 attempted to register an intrinsic event query "%2" in %3 namespace for which the set of target object classes could not be determined.</span></span> <span data-ttu-id="64840-131">A consulta será ignorada.</span><span class="sxs-lookup"><span data-stu-id="64840-131">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**\_consulta do provedor de eventos WBEM MC \_ \_ \_ \_ muito \_ ampla**</span><span class="sxs-lookup"><span data-stu-id="64840-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-133">3221225495 (0xC0000017)</span><span class="sxs-lookup"><span data-stu-id="64840-133">3221225495 (0xC0000017)</span></span>
</dt> <dt>



<span data-ttu-id="64840-134">O provedor de eventos %1 tentou registrar a consulta "%2" no namespace %3, o que é muito amplo.</span><span class="sxs-lookup"><span data-stu-id="64840-134">Event provider %1 attempted to register query "%2" in %3 namespace which is too broad.</span></span> <span data-ttu-id="64840-135">Os provedores de eventos não podem fornecer eventos que são fornecidos pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="64840-135">Event providers cannot provide events that are provided by the system.</span></span> <span data-ttu-id="64840-136">A consulta será ignorada.</span><span class="sxs-lookup"><span data-stu-id="64840-136">The query will be ignored.</span></span> <span data-ttu-id="64840-137">Contate o fornecedor do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="64840-137">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_consulta do provedor de eventos WBEM MC \_ \_ \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="64840-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-139">3221225496 (0xC0000018)</span><span class="sxs-lookup"><span data-stu-id="64840-139">3221225496 (0xC0000018)</span></span>
</dt> <dt>



<span data-ttu-id="64840-140">O provedor de eventos %1 tentou registrar a consulta "%2" cuja classe de destino "%3" no namespace %4 não existe.</span><span class="sxs-lookup"><span data-stu-id="64840-140">Event provider %1 attempted to register query "%2" whose target class "%3" in %4 namespace does not exist.</span></span> <span data-ttu-id="64840-141">A consulta será ignorada.</span><span class="sxs-lookup"><span data-stu-id="64840-141">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**\_consulta do provedor de eventos WBEM MC \_ \_ \_ \_ não \_ evento**</span><span class="sxs-lookup"><span data-stu-id="64840-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-143">3221225497 (0xC0000019)</span><span class="sxs-lookup"><span data-stu-id="64840-143">3221225497 (0xC0000019)</span></span>
</dt> <dt>



<span data-ttu-id="64840-144">O provedor de eventos %1 tentou registrar a consulta &quot; %2 &quot; cuja classe de destino &quot; %3 &quot; não é uma classe de evento.</span><span class="sxs-lookup"><span data-stu-id="64840-144">Event provider %1 attempted to register query &quot;%2&quot; whose target class &quot;%3&quot; is not an event class.</span></span> <span data-ttu-id="64840-145">A consulta será ignorada.</span><span class="sxs-lookup"><span data-stu-id="64840-145">The query will be ignored.</span></span> <span data-ttu-id="64840-146">Contate o fornecedor do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="64840-146">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**falha de núcleo do WBEM \_ MC \_ WBEM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="64840-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM\_MC\_WBEM\_CORE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-148">3221225500 (0xC000001C)</span><span class="sxs-lookup"><span data-stu-id="64840-148">3221225500 (0xC000001C)</span></span>
</dt> <dt>



<span data-ttu-id="64840-149">Falha ao inicializar o núcleo do WMI ou o subsistema do provedor ou o subsistema de eventos com o número de erro %1.</span><span class="sxs-lookup"><span data-stu-id="64840-149">Failed to Initialize WMI Core or Provider SubSystem or Event SubSystem with error number %1.</span></span> <span data-ttu-id="64840-150">Isso pode ser devido a uma versão mal instalada do WMI, falha na atualização do repositório WMI, espaço em disco insuficiente ou memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="64840-150">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**\_ \_ \_ falha na conexão do WBEM MC ADAP \_**</span><span class="sxs-lookup"><span data-stu-id="64840-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**WBEM\_MC\_ADAP\_CONNECTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-152">3221225515 (0xC000002B)</span><span class="sxs-lookup"><span data-stu-id="64840-152">3221225515 (0xC000002B)</span></span>
</dt> <dt>



<span data-ttu-id="64840-153">Falha do ADAP Instrumentação de Gerenciamento do Windows ao se conectar ao namespace %1 com o seguinte erro %2.</span><span class="sxs-lookup"><span data-stu-id="64840-153">Windows Management Instrumentation ADAP failed to connect to namespace %1 with the following error %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**falha do WBEM \_ MC \_ ADAP \_ \_ PUTCLASS \_**</span><span class="sxs-lookup"><span data-stu-id="64840-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM\_MC\_ADAP\_PERFLIB\_PUTCLASS\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-155">3221225520 (0xC0000030)</span><span class="sxs-lookup"><span data-stu-id="64840-155">3221225520 (0xC0000030)</span></span>
</dt> <dt>



<span data-ttu-id="64840-156">Instrumentação de Gerenciamento do Windows ADAP não pôde salvar o objeto %1 no namespace %2 devido ao seguinte erro %3.</span><span class="sxs-lookup"><span data-stu-id="64840-156">Windows Management Instrumentation ADAP was unable to save object %1 in namespace %2 because of the following error %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ incapaz \_ de \_ Adicionar \_ WIN32PERF**</span><span class="sxs-lookup"><span data-stu-id="64840-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-158">3221225530 (0xC000003A)</span><span class="sxs-lookup"><span data-stu-id="64840-158">3221225530 (0xC000003A)</span></span>
</dt> <dt>



<span data-ttu-id="64840-159">Instrumentação de Gerenciamento do Windows ADAP não pôde criar a \_ classe base de desempenho Win32 em %1: resultado = %2.</span><span class="sxs-lookup"><span data-stu-id="64840-159">Windows Management Instrumentation ADAP was unable to create the Win32\_Perf base class in %1:Result=%2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ incapaz \_ de \_ Adicionar \_ WIN32PERFRAWDATA**</span><span class="sxs-lookup"><span data-stu-id="64840-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERFRAWDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-161">3221225531 (0xC000003B)</span><span class="sxs-lookup"><span data-stu-id="64840-161">3221225531 (0xC000003B)</span></span>
</dt> <dt>



<span data-ttu-id="64840-162">Instrumentação de Gerenciamento do Windows ADAP não pôde criar a classe de \_ base PerfRawData do Win32% 1.</span><span class="sxs-lookup"><span data-stu-id="64840-162">Windows Management Instrumentation ADAP was unable to create the Win32\_PerfRawData base class %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**\_ \_ \_ falha \_ ao \_ iniciar o repositório do WBEM MC**</span><span class="sxs-lookup"><span data-stu-id="64840-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**WBEM\_MC\_REPOSITORY\_FAILED\_TO\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-164">3221231073 (0xC00015E1)</span><span class="sxs-lookup"><span data-stu-id="64840-164">3221231073 (0xC00015E1)</span></span>
</dt> <dt>



<span data-ttu-id="64840-165">O serviço de Instrumentação de Gerenciamento do Windows falhou ao carregar os arquivos de repositório no diretório *% windir% \\ System32 \\ WBEM \\ Repository*.</span><span class="sxs-lookup"><span data-stu-id="64840-165">The Windows Management Instrumentation Service failed to load the repository files under the directory *%windir%\\system32\\wbem\\repository*.</span></span> <span data-ttu-id="64840-166">Isso pode ser causado por um dano nos arquivos do repositório, configurações de segurança nesse diretório, falta de espaço em disco ou outros problemas de recursos do sistema, como a falta de memória.</span><span class="sxs-lookup"><span data-stu-id="64840-166">This can be caused by a corruption in the repository files, security settings on this directory, lack of disk space, or other system resource issues such as lack of memory.</span></span> <span data-ttu-id="64840-167">Se esse erro ocorrer toda vez que o computador for reiniciado, o administrador neste computador poderá precisar parar o serviço WMI, examinar a configuração de segurança nessa pasta e nos arquivos dessa pasta e executar WMIDiag para validar a integridade do Instrumentação de Gerenciamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="64840-167">If this error occurs each time the computer is restarted then the administrator on this computer may need to stop WMI Service, review the security setting on this folder and files under this folder, and run WMIDiag to validate the health of Windows Management Instrumentation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ requer \_ criptografia \_ negada**</span><span class="sxs-lookup"><span data-stu-id="64840-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-169">3221231077 (0xC00015E5)</span><span class="sxs-lookup"><span data-stu-id="64840-169">3221231077 (0xC00015E5)</span></span>
</dt> <dt>



<span data-ttu-id="64840-170">O acesso ao namespace %1 foi negado porque o namespace está marcado com RequiresEncryption, mas o script ou o aplicativo tentou se conectar a esse namespace com um nível de autenticação abaixo da **\_ privacidade do PKT**.</span><span class="sxs-lookup"><span data-stu-id="64840-170">Access to the %1 namespace was denied because the namespace is marked with RequiresEncryption but the script or application attempted to connect to this namespace with an authentication level below **Pkt\_Privacy**.</span></span> <span data-ttu-id="64840-171">Altere o nível de autenticação **para \_ privacidade de PKT** e execute o script ou o aplicativo novamente.</span><span class="sxs-lookup"><span data-stu-id="64840-171">Change the authentication level to **Pkt\_Privacy** and run the script or application again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ requer \_ criptografia \_ assíncrona \_ negada**</span><span class="sxs-lookup"><span data-stu-id="64840-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_ASYNC\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-173">3221231078 (0xC00015E6)</span><span class="sxs-lookup"><span data-stu-id="64840-173">3221231078 (0xC00015E6)</span></span>
</dt> <dt>



<span data-ttu-id="64840-174">O serviço de Instrumentação de Gerenciamento do Windows não pôde entregar resultados de forma assíncrona para o namespace %1.</span><span class="sxs-lookup"><span data-stu-id="64840-174">Windows Management Instrumentation Service could not deliver results asynchronously for %1 namespace.</span></span> <span data-ttu-id="64840-175">O namespace é marcado com RequiresEncryption, mas WinMgmt não pôde estabelecer uma conexão segura de volta para o computador cliente.</span><span class="sxs-lookup"><span data-stu-id="64840-175">The namespace is marked with RequiresEncryption but WinMgmt could not establish a secure connection back to the client computer.</span></span> <span data-ttu-id="64840-176">Verifique se há uma relação de confiança entre os computadores cliente e servidor para que o cliente reconheça a conta de computador do servidor.</span><span class="sxs-lookup"><span data-stu-id="64840-176">Ensure there is a trust relationship between the client and server computers so that the client recognizes the server computer account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**HOST do WBEM \_ MC \_ WBEM \_ \_ eliminado**</span><span class="sxs-lookup"><span data-stu-id="64840-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**WBEM\_MC\_WBEM\_HOST\_KILLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-178">3221231084 (0xC00015EC)</span><span class="sxs-lookup"><span data-stu-id="64840-178">3221231084 (0xC00015EC)</span></span>
</dt> <dt>



<span data-ttu-id="64840-179">Instrumentação de Gerenciamento do Windows parou WMIPRVSE.EXE porque uma cota atingiu um valor de aviso.</span><span class="sxs-lookup"><span data-stu-id="64840-179">Windows Management Instrumentation has stopped WMIPRVSE.EXE because a quota reached a warning value.</span></span> <span data-ttu-id="64840-180">Cota: %1 valor: %2 valor máximo: %3 PID do WMIPRVSE: %4.</span><span class="sxs-lookup"><span data-stu-id="64840-180">Quota: %1 Value: %2 Maximum value: %3 WMIPRVSE PID: %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ REPFILESNOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="64840-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM\_MC\_WBEM\_REPFILESNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-182">3221231086 (0xC00015EE)</span><span class="sxs-lookup"><span data-stu-id="64840-182">3221231086 (0xC00015EE)</span></span>
</dt> <dt>



<span data-ttu-id="64840-183">Durante a inicialização do serviço, o serviço de Instrumentação de Gerenciamento do Windows não pôde localizar os arquivos do repositório.</span><span class="sxs-lookup"><span data-stu-id="64840-183">During the service startup, the Windows Management Instrumentation service was unable to locate the repository files.</span></span> <span data-ttu-id="64840-184">Um novo repositório será criado com base no mecanismo de recuperação automática.</span><span class="sxs-lookup"><span data-stu-id="64840-184">A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM \_ iniciado com \_ êxito**</span><span class="sxs-lookup"><span data-stu-id="64840-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM\_MC\_WBEM\_STARTED\_SUCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-186">3221231087 (0xC00015EF)</span><span class="sxs-lookup"><span data-stu-id="64840-186">3221231087 (0xC00015EF)</span></span>
</dt> <dt>



<span data-ttu-id="64840-187">Instrumentação de Gerenciamento do Windows serviço foi iniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="64840-187">Windows Management Instrumentation Service started successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM \_ MC \_ WBEM \_ principal \_ PSS \_ ESS \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="64840-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM\_MC\_WBEM\_CORE\_PSS\_ESS\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-189">3221231089 (0xC00015F1)</span><span class="sxs-lookup"><span data-stu-id="64840-189">3221231089 (0xC00015F1)</span></span>
</dt> <dt>



<span data-ttu-id="64840-190">Instrumentação de Gerenciamento do Windows subsistemas de serviço inicializados com êxito.</span><span class="sxs-lookup"><span data-stu-id="64840-190">Windows Management Instrumentation Service subsystems initialized successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**\_ \_ \_ \_ falha na inicialização do serviço WBEM MC WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="64840-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**WBEM\_MC\_WBEM\_SERVICE\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-192">3221225501 (0xC000001D)</span><span class="sxs-lookup"><span data-stu-id="64840-192">3221225501 (0xC000001D)</span></span>
</dt> <dt>



<span data-ttu-id="64840-193">O número de erro %1 foi retornado ao tentar inicializar o serviço de Instrumentação de Gerenciamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="64840-193">Error number %1 was returned in trying to initialize Windows Management Instrumentation Service.</span></span> <span data-ttu-id="64840-194">Isso pode ser devido a uma versão mal instalada do WMI, falha na atualização do repositório WMI, espaço em disco insuficiente ou memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="64840-194">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64840-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**repositório do WBEM \_ MC \_ WBEM \_ \_ recriado**</span><span class="sxs-lookup"><span data-stu-id="64840-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**WBEM\_MC\_WBEM\_REPOSITORY\_RECREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64840-196">3221231088 (0xC00015F0)</span><span class="sxs-lookup"><span data-stu-id="64840-196">3221231088 (0xC00015F0)</span></span>
</dt> <dt>



<span data-ttu-id="64840-197">O repositório de Instrumentação de Gerenciamento do Windows recriou com êxito usando o mecanismo de recuperação automatizada.</span><span class="sxs-lookup"><span data-stu-id="64840-197">Windows Management Instrumentation Repository successfully recreated using Autorecovery mechanism.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64840-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64840-198">Requirements</span></span>



| <span data-ttu-id="64840-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="64840-199">Requirement</span></span> | <span data-ttu-id="64840-200">Valor</span><span class="sxs-lookup"><span data-stu-id="64840-200">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="64840-201">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64840-201">Minimum supported client</span></span><br/> | <span data-ttu-id="64840-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64840-202">Windows Vista</span></span><br/>       |
| <span data-ttu-id="64840-203">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64840-203">Minimum supported server</span></span><br/> | <span data-ttu-id="64840-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64840-204">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64840-205">Confira também</span><span class="sxs-lookup"><span data-stu-id="64840-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64840-206">Eventos WMI</span><span class="sxs-lookup"><span data-stu-id="64840-206">WMI Events</span></span>](wmi-events.md)
</dt> <dt>

[<span data-ttu-id="64840-207">Solução de problemas do WMI</span><span class="sxs-lookup"><span data-stu-id="64840-207">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> </dl>

 

 




