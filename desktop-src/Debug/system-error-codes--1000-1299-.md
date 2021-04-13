---
description: Descreve os códigos de erro 1000-1299 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Códigos de erro do sistema (1000-1299) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 592bd5c6653526d87fed05d6ec76f739355ae359
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500966"
---
# <a name="system-error-codes-1000-1299"></a><span data-ttu-id="aa39e-103">Códigos de erro do sistema (1000-1299)</span><span class="sxs-lookup"><span data-stu-id="aa39e-103">System Error Codes (1000-1299)</span></span>

> [!NOTE]
> <span data-ttu-id="aa39e-104">Essas informações destinam-se a desenvolvedores Depurando erros do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa39e-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="aa39e-105">Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="aa39e-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="aa39e-106">A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) para erros 1000 a 1299.</span><span class="sxs-lookup"><span data-stu-id="aa39e-106">The following list describes [system error codes](system-error-codes.md) for errors 1000 to 1299.</span></span> <span data-ttu-id="aa39e-107">Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham.</span><span class="sxs-lookup"><span data-stu-id="aa39e-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="aa39e-108">Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="aa39e-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="aa39e-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**\_estouro de pilha de erros \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**ERROR\_STACK\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-110">1001 (0x3E9)</span><span class="sxs-lookup"><span data-stu-id="aa39e-110">1001 (0x3E9)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-111">Recursão muito profunda; a pilha estourou.</span><span class="sxs-lookup"><span data-stu-id="aa39e-111">Recursion too deep; the stack overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**mensagem de erro \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**ERROR\_INVALID\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-113">1002 (0x3EA)</span><span class="sxs-lookup"><span data-stu-id="aa39e-113">1002 (0x3EA)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-114">A janela não pode atuar na mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="aa39e-114">The window cannot act on the sent message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**ERRO \_ \_ não pode \_ ser concluído**</span><span class="sxs-lookup"><span data-stu-id="aa39e-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**ERROR\_CAN\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-116">1003 (0x3EB)</span><span class="sxs-lookup"><span data-stu-id="aa39e-116">1003 (0x3EB)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-117">Não é possível concluir esta função.</span><span class="sxs-lookup"><span data-stu-id="aa39e-117">Cannot complete this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**\_Sinalizadores inválidos de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-119">1004 (0x3EC)</span><span class="sxs-lookup"><span data-stu-id="aa39e-119">1004 (0x3EC)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-120">Sinalizadores inválidos.</span><span class="sxs-lookup"><span data-stu-id="aa39e-120">Invalid flags.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERRO de \_ volume não reconhecido \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERROR\_UNRECOGNIZED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-122">1005 (0x3ED)</span><span class="sxs-lookup"><span data-stu-id="aa39e-122">1005 (0x3ED)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-123">O volume não contém um sistema de arquivos reconhecido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-123">The volume does not contain a recognized file system.</span></span> <span data-ttu-id="aa39e-124">Certifique-se de que todos os drivers de sistema de arquivos necessários estejam carregados e que o volume não esteja corrompido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-124">Please make sure that all required file system drivers are loaded and that the volume is not corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**arquivo de erro \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**ERROR\_FILE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-126">1006 (0x3EE)</span><span class="sxs-lookup"><span data-stu-id="aa39e-126">1006 (0x3EE)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-127">O volume de um arquivo foi alterado externamente para que o arquivo aberto não seja mais válido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-127">The volume for a file has been externally altered so that the opened file is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERRO no \_ modo de tela inteira \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERROR\_FULLSCREEN\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-129">1007 (0x3EF)</span><span class="sxs-lookup"><span data-stu-id="aa39e-129">1007 (0x3EF)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-130">A operação solicitada não pode ser executada no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="aa39e-130">The requested operation cannot be performed in full-screen mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERRO \_ sem \_ token**</span><span class="sxs-lookup"><span data-stu-id="aa39e-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERROR\_NO\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-132">1008 (0x3F0)</span><span class="sxs-lookup"><span data-stu-id="aa39e-132">1008 (0x3F0)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-133">Foi feita uma tentativa de fazer referência a um token que não existe.</span><span class="sxs-lookup"><span data-stu-id="aa39e-133">An attempt was made to reference a token that does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERRO \_ BADDB**</span><span class="sxs-lookup"><span data-stu-id="aa39e-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERROR\_BADDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-135">1009 (0x3F1)</span><span class="sxs-lookup"><span data-stu-id="aa39e-135">1009 (0x3F1)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-136">O banco de dados do registro de configuração está corrompido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-136">The configuration registry database is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERRO \_ BADKEY**</span><span class="sxs-lookup"><span data-stu-id="aa39e-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERROR\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-138">1010 (0x3F2)</span><span class="sxs-lookup"><span data-stu-id="aa39e-138">1010 (0x3F2)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-139">A chave do registro de configuração é inválida.</span><span class="sxs-lookup"><span data-stu-id="aa39e-139">The configuration registry key is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERRO \_ CANTOPEN**</span><span class="sxs-lookup"><span data-stu-id="aa39e-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERROR\_CANTOPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-141">1011 (0x3F3)</span><span class="sxs-lookup"><span data-stu-id="aa39e-141">1011 (0x3F3)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-142">Não foi possível abrir a chave do registro de configuração.</span><span class="sxs-lookup"><span data-stu-id="aa39e-142">The configuration registry key could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERRO ao \_ DEStrilha**</span><span class="sxs-lookup"><span data-stu-id="aa39e-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERROR\_CANTREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-144">1012 (0x3F4)</span><span class="sxs-lookup"><span data-stu-id="aa39e-144">1012 (0x3F4)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-145">Não foi possível ler a chave do registro de configuração.</span><span class="sxs-lookup"><span data-stu-id="aa39e-145">The configuration registry key could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERRO \_ CANTWRITE**</span><span class="sxs-lookup"><span data-stu-id="aa39e-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERROR\_CANTWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-147">1013 (0x3F5)</span><span class="sxs-lookup"><span data-stu-id="aa39e-147">1013 (0x3F5)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-148">A chave do registro de configuração não pôde ser gravada.</span><span class="sxs-lookup"><span data-stu-id="aa39e-148">The configuration registry key could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**registro de erro \_ \_ recuperado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**ERROR\_REGISTRY\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-150">1014 (0x3F6)</span><span class="sxs-lookup"><span data-stu-id="aa39e-150">1014 (0x3F6)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-151">Um dos arquivos no banco de dados do registro precisava ser recuperado pelo uso de um log ou cópia alternativa.</span><span class="sxs-lookup"><span data-stu-id="aa39e-151">One of the files in the registry database had to be recovered by use of a log or alternate copy.</span></span> <span data-ttu-id="aa39e-152">A recuperação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="aa39e-152">The recovery was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**registro de erro \_ \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**ERROR\_REGISTRY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-154">1015 (0x3F7)</span><span class="sxs-lookup"><span data-stu-id="aa39e-154">1015 (0x3F7)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-155">O registro está corrompido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-155">The registry is corrupted.</span></span> <span data-ttu-id="aa39e-156">A estrutura de um dos arquivos que contêm dados do registro está corrompida ou a imagem de memória do sistema do arquivo está corrompida ou o arquivo não pôde ser recuperado porque a cópia ou o log alternativo estava ausente ou corrompido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-156">The structure of one of the files containing registry data is corrupted, or the system's memory image of the file is corrupted, or the file could not be recovered because the alternate copy or log was absent or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**\_ \_ falha na e/s do registro de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERROR\_REGISTRY\_IO\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-158">1016 (0x3F8)</span><span class="sxs-lookup"><span data-stu-id="aa39e-158">1016 (0x3F8)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-159">Uma operação de e/s iniciada pelo registro falhou irrecuperável.</span><span class="sxs-lookup"><span data-stu-id="aa39e-159">An I/O operation initiated by the registry failed unrecoverably.</span></span> <span data-ttu-id="aa39e-160">O registro não pôde ler, ou gravar ou liberar, um dos arquivos que contêm a imagem do registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa39e-160">The registry could not read in, or write out, or flush, one of the files that contain the system's image of the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERRO \_ não \_ arquivo de registro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERROR\_NOT\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-162">1017 (0x3F9)</span><span class="sxs-lookup"><span data-stu-id="aa39e-162">1017 (0x3F9)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-163">O sistema tentou carregar ou restaurar um arquivo no registro, mas o arquivo especificado não está em um formato de arquivo de registro.</span><span class="sxs-lookup"><span data-stu-id="aa39e-163">The system has attempted to load or restore a file into the registry, but the specified file is not in a registry file format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**chave de erro \_ \_ excluída**</span><span class="sxs-lookup"><span data-stu-id="aa39e-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**ERROR\_KEY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-165">1018 (0x3FA)</span><span class="sxs-lookup"><span data-stu-id="aa39e-165">1018 (0x3FA)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-166">Tentativa de operação ilegal em uma chave do registro que foi marcada para exclusão.</span><span class="sxs-lookup"><span data-stu-id="aa39e-166">Illegal operation attempted on a registry key that has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERRO \_ nenhum \_ espaço de log \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERROR\_NO\_LOG\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-168">1019 (0x3FB)</span><span class="sxs-lookup"><span data-stu-id="aa39e-168">1019 (0x3FB)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-169">O sistema não pôde alocar o espaço necessário em um log do registro.</span><span class="sxs-lookup"><span data-stu-id="aa39e-169">System could not allocate the required space in a registry log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**a \_ chave de erro \_ tem \_ filhos**</span><span class="sxs-lookup"><span data-stu-id="aa39e-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**ERROR\_KEY\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-171">1020 (0x3FC)</span><span class="sxs-lookup"><span data-stu-id="aa39e-171">1020 (0x3FC)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-172">Não é possível criar um link simbólico em uma chave do registro que já tenha subchaves ou valores.</span><span class="sxs-lookup"><span data-stu-id="aa39e-172">Cannot create a symbolic link in a registry key that already has subkeys or values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**o \_ filho do erro \_ deve \_ ser \_ volátil**</span><span class="sxs-lookup"><span data-stu-id="aa39e-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**ERROR\_CHILD\_MUST\_BE\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-174">1021 (0x3FD)</span><span class="sxs-lookup"><span data-stu-id="aa39e-174">1021 (0x3FD)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-175">Não é possível criar uma subchave estável em uma chave pai volátil.</span><span class="sxs-lookup"><span data-stu-id="aa39e-175">Cannot create a stable subkey under a volatile parent key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERRO ao \_ notificar o \_ diretório de enumeração \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERROR\_NOTIFY\_ENUM\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-177">1022 (0x3FE)</span><span class="sxs-lookup"><span data-stu-id="aa39e-177">1022 (0x3FE)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-178">Uma solicitação de notificação de alteração está sendo concluída e as informações não estão sendo retornadas no buffer do chamador.</span><span class="sxs-lookup"><span data-stu-id="aa39e-178">A notify change request is being completed and the information is not being returned in the caller's buffer.</span></span> <span data-ttu-id="aa39e-179">O chamador agora precisa enumerar os arquivos para localizar as alterações.</span><span class="sxs-lookup"><span data-stu-id="aa39e-179">The caller now needs to enumerate the files to find the changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**\_serviços dependentes de erro \_ \_ em execução**</span><span class="sxs-lookup"><span data-stu-id="aa39e-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**ERROR\_DEPENDENT\_SERVICES\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-181">1051 (0x41B)</span><span class="sxs-lookup"><span data-stu-id="aa39e-181">1051 (0x41B)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-182">Um controle de parada foi enviado a um serviço no qual outros serviços em execução dependem.</span><span class="sxs-lookup"><span data-stu-id="aa39e-182">A stop control has been sent to a service that other running services are dependent on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERRO \_ de \_ controle de serviço inválido \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERROR\_INVALID\_SERVICE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-184">1052 (0x41C)</span><span class="sxs-lookup"><span data-stu-id="aa39e-184">1052 (0x41C)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-185">O controle solicitado não é válido para este serviço.</span><span class="sxs-lookup"><span data-stu-id="aa39e-185">The requested control is not valid for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**\_ \_ tempo limite de solicitação de serviço de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**ERROR\_SERVICE\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-187">1053 (0x41D)</span><span class="sxs-lookup"><span data-stu-id="aa39e-187">1053 (0x41D)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-188">O serviço não respondeu à solicitação de início ou de controle em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="aa39e-188">The service did not respond to the start or control request in a timely fashion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**serviço de erro \_ \_ sem \_ thread**</span><span class="sxs-lookup"><span data-stu-id="aa39e-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**ERROR\_SERVICE\_NO\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-190">1054 (0x41E)</span><span class="sxs-lookup"><span data-stu-id="aa39e-190">1054 (0x41E)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-191">Não foi possível criar um thread para o serviço.</span><span class="sxs-lookup"><span data-stu-id="aa39e-191">A thread could not be created for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**banco de dados do serviço de erro \_ \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**ERROR\_SERVICE\_DATABASE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-193">1055 (0x41F)</span><span class="sxs-lookup"><span data-stu-id="aa39e-193">1055 (0x41F)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-194">O banco de dados de serviço está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-194">The service database is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**serviço de erro \_ \_ já \_ em execução**</span><span class="sxs-lookup"><span data-stu-id="aa39e-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**ERROR\_SERVICE\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-196">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="aa39e-196">1056 (0x420)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-197">Uma instância do serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="aa39e-197">An instance of the service is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERRO \_ de \_ conta de serviço inválida \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERROR\_INVALID\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-199">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="aa39e-199">1057 (0x421)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-200">O nome da conta é inválido ou não existe, ou a senha é inválida para o nome de conta especificado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-200">The account name is invalid or does not exist, or the password is invalid for the account name specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**serviço de erro \_ \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**ERROR\_SERVICE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-202">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="aa39e-202">1058 (0x422)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-203">Não é possível iniciar o serviço porque ele está desabilitado ou porque não há dispositivos habilitados associados a ele.</span><span class="sxs-lookup"><span data-stu-id="aa39e-203">The service cannot be started, either because it is disabled or because it has no enabled devices associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**\_dependência circular de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**ERROR\_CIRCULAR\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-205">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="aa39e-205">1059 (0x423)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-206">A dependência de serviço circular foi especificada.</span><span class="sxs-lookup"><span data-stu-id="aa39e-206">Circular service dependency was specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**o serviço de erro não \_ \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="aa39e-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**ERROR\_SERVICE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-208">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="aa39e-208">1060 (0x424)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-209">O serviço especificado não existe como um serviço instalado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-209">The specified service does not exist as an installed service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**o \_ serviço de erro \_ não pode \_ aceitar \_ Ctrl**</span><span class="sxs-lookup"><span data-stu-id="aa39e-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**ERROR\_SERVICE\_CANNOT\_ACCEPT\_CTRL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-211">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="aa39e-211">1061 (0x425)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-212">O serviço não pode aceitar mensagens de controle no momento.</span><span class="sxs-lookup"><span data-stu-id="aa39e-212">The service cannot accept control messages at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**serviço de erro \_ \_ não \_ ativo**</span><span class="sxs-lookup"><span data-stu-id="aa39e-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**ERROR\_SERVICE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-214">1062 (0x426)</span><span class="sxs-lookup"><span data-stu-id="aa39e-214">1062 (0x426)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-215">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-215">The service has not been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERRO \_ falha \_ ao \_ conectar o controlador de serviço \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-217">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="aa39e-217">1063 (0x427)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-218">O processo de serviço não pôde se conectar ao controlador de serviço.</span><span class="sxs-lookup"><span data-stu-id="aa39e-218">The service process could not connect to the service controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**\_exceção \_ de erro no \_ serviço**</span><span class="sxs-lookup"><span data-stu-id="aa39e-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**ERROR\_EXCEPTION\_IN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-220">1064 (0x428)</span><span class="sxs-lookup"><span data-stu-id="aa39e-220">1064 (0x428)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-221">Ocorreu uma exceção no serviço ao manipular a solicitação de controle.</span><span class="sxs-lookup"><span data-stu-id="aa39e-221">An exception occurred in the service when handling the control request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**\_o banco de dados de erro \_ \_ não \_ existe**</span><span class="sxs-lookup"><span data-stu-id="aa39e-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**ERROR\_DATABASE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-223">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="aa39e-223">1065 (0x429)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-224">O banco de dados especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="aa39e-224">The database specified does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**\_ \_ erro específico do serviço de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**ERROR\_SERVICE\_SPECIFIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-226">1066 (0x42A)</span><span class="sxs-lookup"><span data-stu-id="aa39e-226">1066 (0x42A)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-227">O serviço retornou um código de erro específico do serviço.</span><span class="sxs-lookup"><span data-stu-id="aa39e-227">The service has returned a service-specific error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**processo de erro \_ \_ anulado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**ERROR\_PROCESS\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-229">1067 (0x42B)</span><span class="sxs-lookup"><span data-stu-id="aa39e-229">1067 (0x42B)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-230">O processo foi finalizado inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="aa39e-230">The process terminated unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**\_ \_ falha na dependência do serviço de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**ERROR\_SERVICE\_DEPENDENCY\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-232">1068 (0x42C)</span><span class="sxs-lookup"><span data-stu-id="aa39e-232">1068 (0x42C)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-233">Falha ao iniciar o serviço ou grupo de dependência.</span><span class="sxs-lookup"><span data-stu-id="aa39e-233">The dependency service or group failed to start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**\_ \_ falha no logon do serviço de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**ERROR\_SERVICE\_LOGON\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-235">1069 (0x42D)</span><span class="sxs-lookup"><span data-stu-id="aa39e-235">1069 (0x42D)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-236">O serviço não foi iniciado devido a uma falha de logon.</span><span class="sxs-lookup"><span data-stu-id="aa39e-236">The service did not start due to a logon failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**\_falha ao \_ iniciar o serviço de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERROR\_SERVICE\_START\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-238">1070 (0x42E)</span><span class="sxs-lookup"><span data-stu-id="aa39e-238">1070 (0x42E)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-239">Depois de iniciar, o serviço foi suspenso em um estado de início pendente.</span><span class="sxs-lookup"><span data-stu-id="aa39e-239">After starting, the service hung in a start-pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERRO \_ de \_ bloqueio de serviço inválido \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERROR\_INVALID\_SERVICE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-241">1071 (0x42F)</span><span class="sxs-lookup"><span data-stu-id="aa39e-241">1071 (0x42F)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-242">O bloqueio do banco de dados do serviço especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-242">The specified service database lock is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_serviço \_ de erro marcado \_ para \_ exclusão**</span><span class="sxs-lookup"><span data-stu-id="aa39e-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**ERROR\_SERVICE\_MARKED\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-244">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="aa39e-244">1072 (0x430)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-245">O serviço especificado foi marcado para exclusão.</span><span class="sxs-lookup"><span data-stu-id="aa39e-245">The specified service has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**o \_ serviço de erro \_ existe**</span><span class="sxs-lookup"><span data-stu-id="aa39e-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**ERROR\_SERVICE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-247">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="aa39e-247">1073 (0x431)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-248">O serviço especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="aa39e-248">The specified service already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERRO \_ já \_ em execução \_ LKG**</span><span class="sxs-lookup"><span data-stu-id="aa39e-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERROR\_ALREADY\_RUNNING\_LKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-250">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="aa39e-250">1074 (0x432)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-251">O sistema está em execução no momento com a última configuração válida conhecida.</span><span class="sxs-lookup"><span data-stu-id="aa39e-251">The system is currently running with the last-known-good configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**dependência de serviço de erro \_ \_ \_ excluída**</span><span class="sxs-lookup"><span data-stu-id="aa39e-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**ERROR\_SERVICE\_DEPENDENCY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-253">1075 (0x433)</span><span class="sxs-lookup"><span data-stu-id="aa39e-253">1075 (0x433)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-254">O serviço de dependência não existe ou foi marcado para exclusão.</span><span class="sxs-lookup"><span data-stu-id="aa39e-254">The dependency service does not exist or has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERRO de \_ inicialização \_ já \_ aceita**</span><span class="sxs-lookup"><span data-stu-id="aa39e-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERROR\_BOOT\_ALREADY\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-256">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="aa39e-256">1076 (0x434)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-257">A inicialização atual já foi aceita para uso como o último conjunto de controle mais conhecido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-257">The current boot has already been accepted for use as the last-known-good control set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**serviço de erro \_ \_ nunca \_ iniciado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**ERROR\_SERVICE\_NEVER\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-259">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="aa39e-259">1077 (0x435)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-260">Nenhuma tentativa de iniciar o serviço foi feita desde a última inicialização.</span><span class="sxs-lookup"><span data-stu-id="aa39e-260">No attempts to start the service have been made since the last boot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERRO \_ de \_ nome de serviço duplicado \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERROR\_DUPLICATE\_SERVICE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-262">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="aa39e-262">1078 (0x436)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-263">O nome já está em uso como um nome de serviço ou um nome de exibição de serviço.</span><span class="sxs-lookup"><span data-stu-id="aa39e-263">The name is already in use as either a service name or a service display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERRO \_ de \_ conta de serviço diferente \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERROR\_DIFFERENT\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-265">1079 (0x437)</span><span class="sxs-lookup"><span data-stu-id="aa39e-265">1079 (0x437)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-266">A conta especificada para esse serviço é diferente da conta especificada para outros serviços em execução no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="aa39e-266">The account specified for this service is different from the account specified for other services running in the same process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERRO \_ não é possível \_ detectar \_ falha do driver \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERROR\_CANNOT\_DETECT\_DRIVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-268">1080 (0x438)</span><span class="sxs-lookup"><span data-stu-id="aa39e-268">1080 (0x438)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-269">As ações de falha só podem ser definidas para serviços Win32, não para drivers.</span><span class="sxs-lookup"><span data-stu-id="aa39e-269">Failure actions can only be set for Win32 services, not for drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERRO \_ não é possível \_ detectar a \_ \_ anulação do processo**</span><span class="sxs-lookup"><span data-stu-id="aa39e-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERROR\_CANNOT\_DETECT\_PROCESS\_ABORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-271">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="aa39e-271">1081 (0x439)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-272">Esse serviço é executado no mesmo processo que o Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="aa39e-272">This service runs in the same process as the service control manager.</span></span> <span data-ttu-id="aa39e-273">Portanto, o Gerenciador de controle de serviço não poderá tomar medidas se o processo desse serviço for encerrado inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="aa39e-273">Therefore, the service control manager cannot take action if this service's process terminates unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERRO \_ sem \_ programa de recuperação \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERROR\_NO\_RECOVERY\_PROGRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-275">1082 (0x43A)</span><span class="sxs-lookup"><span data-stu-id="aa39e-275">1082 (0x43A)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-276">Nenhum programa de recuperação foi configurado para este serviço.</span><span class="sxs-lookup"><span data-stu-id="aa39e-276">No recovery program has been configured for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**\_serviço \_ de erro não está \_ no \_ exe**</span><span class="sxs-lookup"><span data-stu-id="aa39e-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**ERROR\_SERVICE\_NOT\_IN\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-278">1083 (0x43B)</span><span class="sxs-lookup"><span data-stu-id="aa39e-278">1083 (0x43B)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-279">O programa executável em que esse serviço está configurado para ser executado não implementa o serviço.</span><span class="sxs-lookup"><span data-stu-id="aa39e-279">The executable program that this service is configured to run in does not implement the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERRO \_ não é um \_ serviço de inicialização segura \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERROR\_NOT\_SAFEBOOT\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-281">1084 (0x43C)</span><span class="sxs-lookup"><span data-stu-id="aa39e-281">1084 (0x43C)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-282">Este serviço não pode ser iniciado no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="aa39e-282">This service cannot be started in Safe Mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**ERRO ao \_ fim \_ da \_ mídia**</span><span class="sxs-lookup"><span data-stu-id="aa39e-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**ERROR\_END\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-284">1100 (0x44C)</span><span class="sxs-lookup"><span data-stu-id="aa39e-284">1100 (0x44C)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-285">A extremidade física da fita foi atingida.</span><span class="sxs-lookup"><span data-stu-id="aa39e-285">The physical end of the tape has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**marca de caixa de erro \_ \_ detectada**</span><span class="sxs-lookup"><span data-stu-id="aa39e-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**ERROR\_FILEMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-287">1101 (0x44D)</span><span class="sxs-lookup"><span data-stu-id="aa39e-287">1101 (0x44D)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-288">Um acesso à fita atingiu uma marca de um.</span><span class="sxs-lookup"><span data-stu-id="aa39e-288">A tape access reached a filemark.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERRO no \_ início \_ da \_ mídia**</span><span class="sxs-lookup"><span data-stu-id="aa39e-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERROR\_BEGINNING\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-290">1102 (0x44E)</span><span class="sxs-lookup"><span data-stu-id="aa39e-290">1102 (0x44E)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-291">O início da fita ou de uma partição foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-291">The beginning of the tape or a partition was encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERRO \_ setmark \_ detectado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERROR\_SETMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-293">1103 (0x44F)</span><span class="sxs-lookup"><span data-stu-id="aa39e-293">1103 (0x44F)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-294">Um acesso à fita atingiu o final de um conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="aa39e-294">A tape access reached the end of a set of files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERRO \_ nenhum \_ dado \_ detectado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERROR\_NO\_DATA\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-296">1104 (0x450)</span><span class="sxs-lookup"><span data-stu-id="aa39e-296">1104 (0x450)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-297">Não há mais dados na fita.</span><span class="sxs-lookup"><span data-stu-id="aa39e-297">No more data is on the tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**\_falha na partição de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**ERROR\_PARTITION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-299">1105 (0x451)</span><span class="sxs-lookup"><span data-stu-id="aa39e-299">1105 (0x451)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-300">Não foi possível particionar a fita.</span><span class="sxs-lookup"><span data-stu-id="aa39e-300">Tape could not be partitioned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERRO \_ de \_ comprimento de bloco inválido \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERROR\_INVALID\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-302">1106 (0x452)</span><span class="sxs-lookup"><span data-stu-id="aa39e-302">1106 (0x452)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-303">Ao acessar uma nova fita de uma partição multivolume, o tamanho atual do bloco está incorreto.</span><span class="sxs-lookup"><span data-stu-id="aa39e-303">When accessing a new tape of a multivolume partition, the current block size is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**dispositivo de erro \_ \_ não \_ particionado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERROR\_DEVICE\_NOT\_PARTITIONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-305">1107 (0x453)</span><span class="sxs-lookup"><span data-stu-id="aa39e-305">1107 (0x453)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-306">Não foi possível encontrar informações de partição de fita ao carregar uma fita.</span><span class="sxs-lookup"><span data-stu-id="aa39e-306">Tape partition information could not be found when loading a tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERRO \_ não é possível \_ \_ Bloquear \_ mídia**</span><span class="sxs-lookup"><span data-stu-id="aa39e-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERROR\_UNABLE\_TO\_LOCK\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-308">1108 (0x454)</span><span class="sxs-lookup"><span data-stu-id="aa39e-308">1108 (0x454)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-309">Não é possível bloquear o mecanismo de ejeção de mídia.</span><span class="sxs-lookup"><span data-stu-id="aa39e-309">Unable to lock the media eject mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERRO \_ não é possível \_ \_ descarregar a \_ mídia**</span><span class="sxs-lookup"><span data-stu-id="aa39e-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERROR\_UNABLE\_TO\_UNLOAD\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-311">1109 (0x455)</span><span class="sxs-lookup"><span data-stu-id="aa39e-311">1109 (0x455)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-312">Não é possível descarregar a mídia.</span><span class="sxs-lookup"><span data-stu-id="aa39e-312">Unable to unload the media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**mídia de erro \_ \_ alterada**</span><span class="sxs-lookup"><span data-stu-id="aa39e-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**ERROR\_MEDIA\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-314">1110 (0x456)</span><span class="sxs-lookup"><span data-stu-id="aa39e-314">1110 (0x456)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-315">A mídia na unidade pode ter sido alterada.</span><span class="sxs-lookup"><span data-stu-id="aa39e-315">The media in the drive may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**redefinição de barramento de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**ERROR\_BUS\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-317">1111 (0x457)</span><span class="sxs-lookup"><span data-stu-id="aa39e-317">1111 (0x457)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-318">O barramento de e/s foi redefinido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-318">The I/O bus was reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERRO \_ sem \_ mídia \_ na \_ unidade**</span><span class="sxs-lookup"><span data-stu-id="aa39e-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERROR\_NO\_MEDIA\_IN\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-320">1112 (0x458)</span><span class="sxs-lookup"><span data-stu-id="aa39e-320">1112 (0x458)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-321">Nenhuma mídia na unidade.</span><span class="sxs-lookup"><span data-stu-id="aa39e-321">No media in drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERRO \_ sem \_ \_ tradução Unicode**</span><span class="sxs-lookup"><span data-stu-id="aa39e-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERROR\_NO\_UNICODE\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-323">1113 (0x459)</span><span class="sxs-lookup"><span data-stu-id="aa39e-323">1113 (0x459)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-324">Não existe mapeamento para o caractere Unicode na página de código de vários bytes de destino.</span><span class="sxs-lookup"><span data-stu-id="aa39e-324">No mapping for the Unicode character exists in the target multi-byte code page.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**\_ \_ falha na inicialização da DLL de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERROR\_DLL\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-326">1114 (0x45A)</span><span class="sxs-lookup"><span data-stu-id="aa39e-326">1114 (0x45A)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-327">Falha em uma rotina de inicialização da biblioteca de vínculo dinâmico (DLL).</span><span class="sxs-lookup"><span data-stu-id="aa39e-327">A dynamic link library (DLL) initialization routine failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERRO \_ de desligamento \_ em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="aa39e-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-329">1115 (0x45B)</span><span class="sxs-lookup"><span data-stu-id="aa39e-329">1115 (0x45B)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-330">Um desligamento do sistema está em andamento.</span><span class="sxs-lookup"><span data-stu-id="aa39e-330">A system shutdown is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERRO \_ nenhum \_ desligamento \_ em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="aa39e-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERROR\_NO\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-332">1116 (0x45C)</span><span class="sxs-lookup"><span data-stu-id="aa39e-332">1116 (0x45C)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-333">Não é possível anular o desligamento do sistema porque nenhum desligamento estava em andamento.</span><span class="sxs-lookup"><span data-stu-id="aa39e-333">Unable to abort the system shutdown because no shutdown was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**\_dispositivo de e/s de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERROR\_IO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-335">1117 (0x45D)</span><span class="sxs-lookup"><span data-stu-id="aa39e-335">1117 (0x45D)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-336">Não foi possível executar a solicitação devido a um erro de dispositivo de E/S.</span><span class="sxs-lookup"><span data-stu-id="aa39e-336">The request could not be performed because of an I/O device error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERRO de \_ serial \_ sem \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="aa39e-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERROR\_SERIAL\_NO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-338">1118 (0x45E)</span><span class="sxs-lookup"><span data-stu-id="aa39e-338">1118 (0x45E)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-339">Nenhum dispositivo serial foi inicializado com êxito.</span><span class="sxs-lookup"><span data-stu-id="aa39e-339">No serial device was successfully initialized.</span></span> <span data-ttu-id="aa39e-340">O driver serial será descarregado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-340">The serial driver will unload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERRO de \_ IRQ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERROR\_IRQ\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-342">1119 (0x45F)</span><span class="sxs-lookup"><span data-stu-id="aa39e-342">1119 (0x45F)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-343">Não é possível abrir um dispositivo que estava compartilhando uma solicitação de interrupção (IRQ) com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aa39e-343">Unable to open a device that was sharing an interrupt request (IRQ) with other devices.</span></span> <span data-ttu-id="aa39e-344">Pelo menos um outro dispositivo que usa esse IRQ já foi aberto.</span><span class="sxs-lookup"><span data-stu-id="aa39e-344">At least one other device that uses that IRQ was already opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERRO \_ mais \_ gravações**</span><span class="sxs-lookup"><span data-stu-id="aa39e-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERROR\_MORE\_WRITES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-346">1120 (0x460)</span><span class="sxs-lookup"><span data-stu-id="aa39e-346">1120 (0x460)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-347">Uma operação de e/s serial foi concluída por outra gravação na porta serial.</span><span class="sxs-lookup"><span data-stu-id="aa39e-347">A serial I/O operation was completed by another write to the serial port.</span></span> <span data-ttu-id="aa39e-348">O \_ contador serial \_ XOFF do IOCTL \_ atingiu zero.)</span><span class="sxs-lookup"><span data-stu-id="aa39e-348">The IOCTL\_SERIAL\_XOFF\_COUNTER reached zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**\_tempo limite do contador de erros \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**ERROR\_COUNTER\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-350">1121 (0x461)</span><span class="sxs-lookup"><span data-stu-id="aa39e-350">1121 (0x461)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-351">Uma operação de e/s serial foi concluída porque o período de tempo limite expirou.</span><span class="sxs-lookup"><span data-stu-id="aa39e-351">A serial I/O operation completed because the timeout period expired.</span></span> <span data-ttu-id="aa39e-352">O contador de IOCTL \_ serial \_ XOFF \_ não alcançou zero.)</span><span class="sxs-lookup"><span data-stu-id="aa39e-352">The IOCTL\_SERIAL\_XOFF\_COUNTER did not reach zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**marca de ID do disquete de erro \_ \_ \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="aa39e-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERROR\_FLOPPY\_ID\_MARK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-354">1122 (0x462)</span><span class="sxs-lookup"><span data-stu-id="aa39e-354">1122 (0x462)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-355">Nenhuma marca de endereço de ID encontrada no disquete.</span><span class="sxs-lookup"><span data-stu-id="aa39e-355">No ID address mark was found on the floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERRO de \_ cilindro de disquete \_ incorreto \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERROR\_FLOPPY\_WRONG\_CYLINDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-357">1123 (0x463)</span><span class="sxs-lookup"><span data-stu-id="aa39e-357">1123 (0x463)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-358">Incompatibilidade entre o campo ID de setor de disquete e o endereço de rastreamento do controlador de disquete.</span><span class="sxs-lookup"><span data-stu-id="aa39e-358">Mismatch between the floppy disk sector ID field and the floppy disk controller track address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**\_ \_ erro desconhecido no disquete de erros \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**ERROR\_FLOPPY\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-360">1124 (0x464)</span><span class="sxs-lookup"><span data-stu-id="aa39e-360">1124 (0x464)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-361">O controlador de disquete relatou um erro que não é reconhecido pelo driver de disquete.</span><span class="sxs-lookup"><span data-stu-id="aa39e-361">The floppy disk controller reported an error that is not recognized by the floppy disk driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**\_ \_ registros inválidos de disquete de erros \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ERROR\_FLOPPY\_BAD\_REGISTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-363">1125 (0x465)</span><span class="sxs-lookup"><span data-stu-id="aa39e-363">1125 (0x465)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-364">O controlador de disquete retornou resultados inconsistentes em seus registros.</span><span class="sxs-lookup"><span data-stu-id="aa39e-364">The floppy disk controller returned inconsistent results in its registers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**\_ \_ falha ao recalibrar disco de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**ERROR\_DISK\_RECALIBRATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-366">1126 (0x466)</span><span class="sxs-lookup"><span data-stu-id="aa39e-366">1126 (0x466)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-367">Ao acessar o disco rígido, uma operação de recalibração falhou, mesmo após novas tentativas.</span><span class="sxs-lookup"><span data-stu-id="aa39e-367">While accessing the hard disk, a recalibrate operation failed, even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**\_ \_ falha na operação de disco de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERROR\_DISK\_OPERATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-369">1127 (0x467)</span><span class="sxs-lookup"><span data-stu-id="aa39e-369">1127 (0x467)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-370">Ao acessar o disco rígido, uma operação de disco falhou mesmo após novas tentativas.</span><span class="sxs-lookup"><span data-stu-id="aa39e-370">While accessing the hard disk, a disk operation failed even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERRO \_ \_ ao redefinir disco \_ com falha**</span><span class="sxs-lookup"><span data-stu-id="aa39e-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERROR\_DISK\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-372">1128 (0x468)</span><span class="sxs-lookup"><span data-stu-id="aa39e-372">1128 (0x468)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-373">Ao acessar o disco rígido, uma redefinição de controlador de disco era necessária, mas mesmo que falhou.</span><span class="sxs-lookup"><span data-stu-id="aa39e-373">While accessing the hard disk, a disk controller reset was needed, but even that failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**\_estouro de eom de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERROR\_EOM\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-375">1129 (0x469)</span><span class="sxs-lookup"><span data-stu-id="aa39e-375">1129 (0x469)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-376">Foi encontrado o final físico da fita.</span><span class="sxs-lookup"><span data-stu-id="aa39e-376">Physical end of tape encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERRO \_ \_ insuficiente \_ na \_ memória do servidor**</span><span class="sxs-lookup"><span data-stu-id="aa39e-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERROR\_NOT\_ENOUGH\_SERVER\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-378">1130 (0x46A)</span><span class="sxs-lookup"><span data-stu-id="aa39e-378">1130 (0x46A)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-379">não há armazenamento suficiente de servidor disponível para processar este comando.</span><span class="sxs-lookup"><span data-stu-id="aa39e-379">Not enough server storage is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERRO \_ possível \_ deadlock**</span><span class="sxs-lookup"><span data-stu-id="aa39e-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERROR\_POSSIBLE\_DEADLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-381">1131 (0x46B)</span><span class="sxs-lookup"><span data-stu-id="aa39e-381">1131 (0x46B)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-382">Foi detectada uma possível condição de deadlock.</span><span class="sxs-lookup"><span data-stu-id="aa39e-382">A potential deadlock condition has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**\_alinhamento mapeado de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**ERROR\_MAPPED\_ALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-384">1132 (0x46C)</span><span class="sxs-lookup"><span data-stu-id="aa39e-384">1132 (0x46C)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-385">O endereço base ou o deslocamento do arquivo especificado não tem o alinhamento adequado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-385">The base address or the file offset specified does not have the proper alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERRO \_ definir o \_ estado de energia \_ \_ vetado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERROR\_SET\_POWER\_STATE\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-387">1140 (0x474)</span><span class="sxs-lookup"><span data-stu-id="aa39e-387">1140 (0x474)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-388">Uma tentativa de alterar o estado de energia do sistema foi vetada por outro aplicativo ou driver.</span><span class="sxs-lookup"><span data-stu-id="aa39e-388">An attempt to change the system power state was vetoed by another application or driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERRO \_ ao definir o \_ estado de energia \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERROR\_SET\_POWER\_STATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-390">1141 (0x475)</span><span class="sxs-lookup"><span data-stu-id="aa39e-390">1141 (0x475)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-391">O BIOS do sistema falhou ao tentar alterar o estado de energia do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa39e-391">The system BIOS failed an attempt to change the system power state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERRO \_ de \_ muitos \_ links**</span><span class="sxs-lookup"><span data-stu-id="aa39e-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERROR\_TOO\_MANY\_LINKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-393">1142 (0x476)</span><span class="sxs-lookup"><span data-stu-id="aa39e-393">1142 (0x476)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-394">Foi feita uma tentativa de criar mais links em um arquivo do que o sistema de arquivos dá suporte.</span><span class="sxs-lookup"><span data-stu-id="aa39e-394">An attempt was made to create more links on a file than the file system supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERRO \_ de \_ versão antiga do Win \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERROR\_OLD\_WIN\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-396">1150 (0x47E)</span><span class="sxs-lookup"><span data-stu-id="aa39e-396">1150 (0x47E)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-397">O programa especificado requer uma versão mais recente do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa39e-397">The specified program requires a newer version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**\_ \_ sistema operacional incorreto do aplicativo de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERROR\_APP\_WRONG\_OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-399">1151 (0x47F)</span><span class="sxs-lookup"><span data-stu-id="aa39e-399">1151 (0x47F)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-400">O programa especificado não é um programa do Windows ou do MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="aa39e-400">The specified program is not a Windows or MS-DOS program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERRO \_ de \_ aplicativo de instância única \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERROR\_SINGLE\_INSTANCE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-402">1152 (0x480)</span><span class="sxs-lookup"><span data-stu-id="aa39e-402">1152 (0x480)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-403">Não é possível iniciar mais de uma instância do programa especificado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-403">Cannot start more than one instance of the specified program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERRO \_ de \_ aplicativo RMODE**</span><span class="sxs-lookup"><span data-stu-id="aa39e-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERROR\_RMODE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-405">1153 (0x481)</span><span class="sxs-lookup"><span data-stu-id="aa39e-405">1153 (0x481)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-406">O programa especificado foi escrito para uma versão anterior do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa39e-406">The specified program was written for an earlier version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**DLL de erro \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERROR\_INVALID\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-408">1154 (0x482)</span><span class="sxs-lookup"><span data-stu-id="aa39e-408">1154 (0x482)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-409">Um dos arquivos de biblioteca necessários para executar este aplicativo está danificado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-409">One of the library files needed to run this application is damaged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERRO \_ sem \_ Associação**</span><span class="sxs-lookup"><span data-stu-id="aa39e-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERROR\_NO\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-411">1155 (0x483)</span><span class="sxs-lookup"><span data-stu-id="aa39e-411">1155 (0x483)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-412">Nenhum aplicativo está associado ao arquivo especificado para esta operação.</span><span class="sxs-lookup"><span data-stu-id="aa39e-412">No application is associated with the specified file for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERRO de \_ DDE \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="aa39e-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERROR\_DDE\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-414">1156 (0x484)</span><span class="sxs-lookup"><span data-stu-id="aa39e-414">1156 (0x484)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-415">Ocorreu um erro ao enviar o comando para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa39e-415">An error occurred in sending the command to the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**DLL de erro \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="aa39e-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**ERROR\_DLL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-417">1157 (0x485)</span><span class="sxs-lookup"><span data-stu-id="aa39e-417">1157 (0x485)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-418">Um dos arquivos de biblioteca necessários para executar este aplicativo não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-418">One of the library files needed to run this application cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERRO \_ não \_ há \_ mais \_ identificadores de usuário**</span><span class="sxs-lookup"><span data-stu-id="aa39e-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERROR\_NO\_MORE\_USER\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-420">1158 (0x486)</span><span class="sxs-lookup"><span data-stu-id="aa39e-420">1158 (0x486)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-421">O processo atual usou toda a sua concessão de sistema de identificadores para objetos do Windows Manager.</span><span class="sxs-lookup"><span data-stu-id="aa39e-421">The current process has used all of its system allowance of handles for Window Manager objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**sincronização de mensagens de erro \_ \_ \_ somente**</span><span class="sxs-lookup"><span data-stu-id="aa39e-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**ERROR\_MESSAGE\_SYNC\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-423">1159 (0x487)</span><span class="sxs-lookup"><span data-stu-id="aa39e-423">1159 (0x487)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-424">A mensagem pode ser usada somente com operações síncronas.</span><span class="sxs-lookup"><span data-stu-id="aa39e-424">The message can be used only with synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**\_elemento fonte de erro \_ \_ vazio**</span><span class="sxs-lookup"><span data-stu-id="aa39e-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**ERROR\_SOURCE\_ELEMENT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-426">1160 (0x488)</span><span class="sxs-lookup"><span data-stu-id="aa39e-426">1160 (0x488)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-427">O elemento de origem indicado não tem mídia.</span><span class="sxs-lookup"><span data-stu-id="aa39e-427">The indicated source element has no media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**elemento de destino do erro \_ \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="aa39e-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERROR\_DESTINATION\_ELEMENT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-429">1161 (0x489)</span><span class="sxs-lookup"><span data-stu-id="aa39e-429">1161 (0x489)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-430">O elemento de destino indicado já contém mídia.</span><span class="sxs-lookup"><span data-stu-id="aa39e-430">The indicated destination element already contains media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERRO \_ de \_ endereço de elemento inválido \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERROR\_ILLEGAL\_ELEMENT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-432">1162 (0x48A)</span><span class="sxs-lookup"><span data-stu-id="aa39e-432">1162 (0x48A)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-433">O elemento indicado não existe.</span><span class="sxs-lookup"><span data-stu-id="aa39e-433">The indicated element does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**a \_ revista de erro \_ não \_ está presente**</span><span class="sxs-lookup"><span data-stu-id="aa39e-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERROR\_MAGAZINE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-435">1163 (0x48B)</span><span class="sxs-lookup"><span data-stu-id="aa39e-435">1163 (0x48B)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-436">O elemento indicado faz parte de uma revista que não está presente.</span><span class="sxs-lookup"><span data-stu-id="aa39e-436">The indicated element is part of a magazine that is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**reinicialização do dispositivo de erro \_ \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="aa39e-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERROR\_DEVICE\_REINITIALIZATION\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-438">1164 (0x48C)</span><span class="sxs-lookup"><span data-stu-id="aa39e-438">1164 (0x48C)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-439">O dispositivo indicado requer reinicialização devido a erros de hardware.</span><span class="sxs-lookup"><span data-stu-id="aa39e-439">The indicated device requires reinitialization due to hardware errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**o \_ dispositivo de erro \_ requer \_ limpeza**</span><span class="sxs-lookup"><span data-stu-id="aa39e-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**ERROR\_DEVICE\_REQUIRES\_CLEANING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-441">1165 (0x48D)</span><span class="sxs-lookup"><span data-stu-id="aa39e-441">1165 (0x48D)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-442">O dispositivo indicou que a limpeza é necessária antes que outras operações sejam tentadas.</span><span class="sxs-lookup"><span data-stu-id="aa39e-442">The device has indicated that cleaning is required before further operations are attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERRO \_ de \_ porta do dispositivo \_ aberta**</span><span class="sxs-lookup"><span data-stu-id="aa39e-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERROR\_DEVICE\_DOOR\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-444">1166 (0x48E)</span><span class="sxs-lookup"><span data-stu-id="aa39e-444">1166 (0x48E)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-445">O dispositivo indicou que sua porta está aberta.</span><span class="sxs-lookup"><span data-stu-id="aa39e-445">The device has indicated that its door is open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**dispositivo de erro \_ \_ não \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERROR\_DEVICE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-447">1167 (0x48F)</span><span class="sxs-lookup"><span data-stu-id="aa39e-447">1167 (0x48F)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-448">O dispositivo não está conectado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-448">The device is not connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERRO \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-450">1168 (0x490)</span><span class="sxs-lookup"><span data-stu-id="aa39e-450">1168 (0x490)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-451">Elemento não encontrado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-451">Element not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERRO \_ sem \_ correspondência**</span><span class="sxs-lookup"><span data-stu-id="aa39e-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERROR\_NO\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-453">1169 (0x491)</span><span class="sxs-lookup"><span data-stu-id="aa39e-453">1169 (0x491)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-454">Não houve correspondência para a chave especificada no índice.</span><span class="sxs-lookup"><span data-stu-id="aa39e-454">There was no match for the specified key in the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**conjunto de erros \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**ERROR\_SET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-456">1170 (0x492)</span><span class="sxs-lookup"><span data-stu-id="aa39e-456">1170 (0x492)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-457">O conjunto de propriedades especificado não existe no objeto.</span><span class="sxs-lookup"><span data-stu-id="aa39e-457">The property set specified does not exist on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**ponto de erro \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**ERROR\_POINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-459">1171 (0x493)</span><span class="sxs-lookup"><span data-stu-id="aa39e-459">1171 (0x493)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-460">O ponto passado para GetMouseMovePoints não está no buffer.</span><span class="sxs-lookup"><span data-stu-id="aa39e-460">The point passed to GetMouseMovePoints is not in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERRO \_ nenhum \_ serviço de rastreamento \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERROR\_NO\_TRACKING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-462">1172 (0x494)</span><span class="sxs-lookup"><span data-stu-id="aa39e-462">1172 (0x494)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-463">O serviço de acompanhamento (estação de trabalho) não está em execução.</span><span class="sxs-lookup"><span data-stu-id="aa39e-463">The tracking (workstation) service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERRO \_ sem \_ ID de volume \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERROR\_NO\_VOLUME\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-465">1173 (0x495)</span><span class="sxs-lookup"><span data-stu-id="aa39e-465">1173 (0x495)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-466">A ID do volume não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="aa39e-466">The Volume ID could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERRO \_ não é possível \_ \_ Remover \_ substituído**</span><span class="sxs-lookup"><span data-stu-id="aa39e-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERROR\_UNABLE\_TO\_REMOVE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-468">1175 (0x497)</span><span class="sxs-lookup"><span data-stu-id="aa39e-468">1175 (0x497)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-469">Não é possível remover o arquivo a ser substituído.</span><span class="sxs-lookup"><span data-stu-id="aa39e-469">Unable to remove the file to be replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERRO \_ não é possível \_ \_ mover a \_ substituição**</span><span class="sxs-lookup"><span data-stu-id="aa39e-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-471">1176 (0x498)</span><span class="sxs-lookup"><span data-stu-id="aa39e-471">1176 (0x498)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-472">Não é possível mover o arquivo de substituição para o arquivo a ser substituído.</span><span class="sxs-lookup"><span data-stu-id="aa39e-472">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="aa39e-473">O arquivo a ser substituído manteve seu nome original.</span><span class="sxs-lookup"><span data-stu-id="aa39e-473">The file to be replaced has retained its original name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERRO \_ não é possível \_ \_ mover a \_ substituição \_ 2**</span><span class="sxs-lookup"><span data-stu-id="aa39e-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-475">1177 (0x499)</span><span class="sxs-lookup"><span data-stu-id="aa39e-475">1177 (0x499)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-476">Não é possível mover o arquivo de substituição para o arquivo a ser substituído.</span><span class="sxs-lookup"><span data-stu-id="aa39e-476">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="aa39e-477">O arquivo a ser substituído foi renomeado usando o nome do backup.</span><span class="sxs-lookup"><span data-stu-id="aa39e-477">The file to be replaced has been renamed using the backup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**\_ \_ exclusão do diário \_ de erros em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="aa39e-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**ERROR\_JOURNAL\_DELETE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-479">1178 (0x49A)</span><span class="sxs-lookup"><span data-stu-id="aa39e-479">1178 (0x49A)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-480">O diário de alterações de volume está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="aa39e-480">The volume change journal is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**o \_ diário de erros \_ não está \_ ativo**</span><span class="sxs-lookup"><span data-stu-id="aa39e-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**ERROR\_JOURNAL\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-482">1179 (0x49B)</span><span class="sxs-lookup"><span data-stu-id="aa39e-482">1179 (0x49B)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-483">O diário de alterações de volume não está ativo.</span><span class="sxs-lookup"><span data-stu-id="aa39e-483">The volume change journal is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**\_arquivo potencial de erro \_ \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**ERROR\_POTENTIAL\_FILE\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-485">1180 (0x49C)</span><span class="sxs-lookup"><span data-stu-id="aa39e-485">1180 (0x49C)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-486">Um arquivo foi encontrado, mas ele pode não ser o arquivo correto.</span><span class="sxs-lookup"><span data-stu-id="aa39e-486">A file was found, but it may not be the correct file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**entrada de diário de erros \_ \_ \_ excluída**</span><span class="sxs-lookup"><span data-stu-id="aa39e-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**ERROR\_JOURNAL\_ENTRY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-488">1181 (0x49D)</span><span class="sxs-lookup"><span data-stu-id="aa39e-488">1181 (0x49D)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-489">A entrada do diário foi excluída do diário.</span><span class="sxs-lookup"><span data-stu-id="aa39e-489">The journal entry has been deleted from the journal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**o \_ desligamento de erro \_ está \_ agendado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**ERROR\_SHUTDOWN\_IS\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-491">1190 (0x4A6)</span><span class="sxs-lookup"><span data-stu-id="aa39e-491">1190 (0x4A6)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-492">Um desligamento do sistema já foi agendado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-492">A system shutdown has already been scheduled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERRO ao \_ desligar \_ os usuários \_ conectados \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERROR\_SHUTDOWN\_USERS\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-494">1191 (0x4A7)</span><span class="sxs-lookup"><span data-stu-id="aa39e-494">1191 (0x4A7)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-495">Não é possível iniciar o desligamento do sistema porque há outros usuários conectados ao computador.</span><span class="sxs-lookup"><span data-stu-id="aa39e-495">The system shutdown cannot be initiated because there are other users logged on to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERRO \_ de \_ dispositivo insatisfatório**</span><span class="sxs-lookup"><span data-stu-id="aa39e-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERROR\_BAD\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-497">1200 (0x4B0)</span><span class="sxs-lookup"><span data-stu-id="aa39e-497">1200 (0x4B0)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-498">O nome do dispositivo especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-498">The specified device name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**conexão de erro não \_ \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="aa39e-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERROR\_CONNECTION\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-500">1201 (0x4B1)</span><span class="sxs-lookup"><span data-stu-id="aa39e-500">1201 (0x4B1)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-501">O dispositivo não está conectado no momento, mas é uma conexão lembrada.</span><span class="sxs-lookup"><span data-stu-id="aa39e-501">The device is not currently connected but it is a remembered connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**dispositivo de erro \_ \_ já \_ lembrado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**ERROR\_DEVICE\_ALREADY\_REMEMBERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-503">1202 (0x4B2)</span><span class="sxs-lookup"><span data-stu-id="aa39e-503">1202 (0x4B2)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-504">O nome do dispositivo local tem uma conexão lembrada com outro recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="aa39e-504">The local device name has a remembered connection to another network resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERRO \_ sem \_ \_ caminho de rede ou \_ inadequado \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERROR\_NO\_NET\_OR\_BAD\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-506">1203 (0x4B3)</span><span class="sxs-lookup"><span data-stu-id="aa39e-506">1203 (0x4B3)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-507">O caminho de rede foi digitado incorretamente, não existe ou o provedor de rede não está disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="aa39e-507">The network path was either typed incorrectly, does not exist, or the network provider is not currently available.</span></span> <span data-ttu-id="aa39e-508">Tente digitar novamente o caminho ou contate o administrador da rede.</span><span class="sxs-lookup"><span data-stu-id="aa39e-508">Please try retyping the path or contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERRO \_ de \_ provedor insatisfatório**</span><span class="sxs-lookup"><span data-stu-id="aa39e-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERROR\_BAD\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-510">1204 (0x4B4)</span><span class="sxs-lookup"><span data-stu-id="aa39e-510">1204 (0x4B4)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-511">O nome do provedor de rede especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-511">The specified network provider name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERRO \_ não é possível \_ abrir o \_ perfil**</span><span class="sxs-lookup"><span data-stu-id="aa39e-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERROR\_CANNOT\_OPEN\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-513">1205 (0x4B5)</span><span class="sxs-lookup"><span data-stu-id="aa39e-513">1205 (0x4B5)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-514">Não é possível abrir o perfil de conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="aa39e-514">Unable to open the network connection profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERRO \_ de \_ perfil insatisfatório**</span><span class="sxs-lookup"><span data-stu-id="aa39e-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERROR\_BAD\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-516">1206 (0x4B6)</span><span class="sxs-lookup"><span data-stu-id="aa39e-516">1206 (0x4B6)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-517">O perfil de conexão de rede está corrompido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-517">The network connection profile is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERRO \_ não \_ contêiner**</span><span class="sxs-lookup"><span data-stu-id="aa39e-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERROR\_NOT\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-519">1207 (0x4B7)</span><span class="sxs-lookup"><span data-stu-id="aa39e-519">1207 (0x4B7)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-520">Não é possível enumerar um não-contêiner.</span><span class="sxs-lookup"><span data-stu-id="aa39e-520">Cannot enumerate a noncontainer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**erro \_ estendido de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**ERROR\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-522">1208 (0x4B8)</span><span class="sxs-lookup"><span data-stu-id="aa39e-522">1208 (0x4B8)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-523">Ocorreu um erro estendido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-523">An extended error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERRO \_ \_ nome_do_grupo inválido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERROR\_INVALID\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-525">1209 (0x4B9)</span><span class="sxs-lookup"><span data-stu-id="aa39e-525">1209 (0x4B9)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-526">O formato do nome do grupo especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-526">The format of the specified group name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERRO \_ de \_ ComputerName inválido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERROR\_INVALID\_COMPUTERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-528">1210 (0x4BA)</span><span class="sxs-lookup"><span data-stu-id="aa39e-528">1210 (0x4BA)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-529">O formato do nome do computador especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-529">The format of the specified computer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERRO \_ de \_ EventName inválido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERROR\_INVALID\_EVENTNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-531">1211 (0x4BB)</span><span class="sxs-lookup"><span data-stu-id="aa39e-531">1211 (0x4BB)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-532">O formato do nome do evento especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-532">The format of the specified event name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERRO \_ de \_ nome_do_domínio inválido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERROR\_INVALID\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-534">1212 (0x4BC)</span><span class="sxs-lookup"><span data-stu-id="aa39e-534">1212 (0x4BC)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-535">O formato do nome de domínio especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-535">The format of the specified domain name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERRO \_ de \_ ServiceName inválido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERROR\_INVALID\_SERVICENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-537">1213 (0x4BD)</span><span class="sxs-lookup"><span data-stu-id="aa39e-537">1213 (0x4BD)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-538">O formato do nome do serviço especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-538">The format of the specified service name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERRO \_ \_ NetName inválido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERROR\_INVALID\_NETNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-540">1214 (0x4BE)</span><span class="sxs-lookup"><span data-stu-id="aa39e-540">1214 (0x4BE)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-541">O formato do nome de rede especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-541">The format of the specified network name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERRO \_ de \_ ShareName inválido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERROR\_INVALID\_SHARENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-543">1215 (0x4BF)</span><span class="sxs-lookup"><span data-stu-id="aa39e-543">1215 (0x4BF)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-544">O formato do nome de compartilhamento especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-544">The format of the specified share name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERRO \_ \_ passwordname inválido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERROR\_INVALID\_PASSWORDNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-546">1216 (0x4C0)</span><span class="sxs-lookup"><span data-stu-id="aa39e-546">1216 (0x4C0)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-547">O formato da senha especificada é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-547">The format of the specified password is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**mensagem de erro \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERROR\_INVALID\_MESSAGENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-549">1217 (0x4C1)</span><span class="sxs-lookup"><span data-stu-id="aa39e-549">1217 (0x4C1)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-550">O formato do nome da mensagem especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-550">The format of the specified message name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERRO \_ \_ MESSAGEDEST inválido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERROR\_INVALID\_MESSAGEDEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-552">1218 (0x4C2)</span><span class="sxs-lookup"><span data-stu-id="aa39e-552">1218 (0x4C2)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-553">O formato do destino da mensagem especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-553">The format of the specified message destination is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**\_conflito de \_ credenciais de sessão de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**ERROR\_SESSION\_CREDENTIAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-555">1219 (0x4C3)</span><span class="sxs-lookup"><span data-stu-id="aa39e-555">1219 (0x4C3)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-556">Não são permitidas várias conexões com um servidor ou recurso compartilhado pelo mesmo usuário, usando mais de um nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="aa39e-556">Multiple connections to a server or shared resource by the same user, using more than one user name, are not allowed.</span></span> <span data-ttu-id="aa39e-557">Desconecte todas as conexões anteriores ao servidor ou recurso compartilhado e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="aa39e-557">Disconnect all previous connections to the server or shared resource and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**\_limite de sessão remota de erro \_ \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERROR\_REMOTE\_SESSION\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-559">1220 (0x4C4)</span><span class="sxs-lookup"><span data-stu-id="aa39e-559">1220 (0x4C4)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-560">Foi feita uma tentativa de estabelecer uma sessão para um servidor de rede, mas já existem muitas sessões estabelecidas com esse servidor.</span><span class="sxs-lookup"><span data-stu-id="aa39e-560">An attempt was made to establish a session to a network server, but there are already too many sessions established to that server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERRO de \_ Dup de \_ domínio**</span><span class="sxs-lookup"><span data-stu-id="aa39e-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERROR\_DUP\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-562">1221 (0x4C5)</span><span class="sxs-lookup"><span data-stu-id="aa39e-562">1221 (0x4C5)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-563">O nome de domínio ou grupo de trabalho já está em uso por outro computador na rede.</span><span class="sxs-lookup"><span data-stu-id="aa39e-563">The workgroup or domain name is already in use by another computer on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERRO \_ sem \_ rede**</span><span class="sxs-lookup"><span data-stu-id="aa39e-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERROR\_NO\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-565">1222 (0x4C6)</span><span class="sxs-lookup"><span data-stu-id="aa39e-565">1222 (0x4C6)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-566">A rede não está presente ou não foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="aa39e-566">The network is not present or not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERRO \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERROR\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-568">1223 (0x4C7)</span><span class="sxs-lookup"><span data-stu-id="aa39e-568">1223 (0x4C7)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-569">A operação foi cancelada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="aa39e-569">The operation was canceled by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERRO \_ de \_ arquivo mapeado pelo usuário \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERROR\_USER\_MAPPED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-571">1224 (0x4C8)</span><span class="sxs-lookup"><span data-stu-id="aa39e-571">1224 (0x4C8)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-572">A operação solicitada não pode ser executada em um arquivo com uma seção mapeada pelo usuário aberta.</span><span class="sxs-lookup"><span data-stu-id="aa39e-572">The requested operation cannot be performed on a file with a user-mapped section open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**conexão de erro \_ \_ recusada**</span><span class="sxs-lookup"><span data-stu-id="aa39e-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERROR\_CONNECTION\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-574">1225 (0x4C9)</span><span class="sxs-lookup"><span data-stu-id="aa39e-574">1225 (0x4C9)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-575">O computador remoto recusou a conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="aa39e-575">The remote computer refused the network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**desconexão normal de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERROR\_GRACEFUL\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-577">1226 (0x4CA)</span><span class="sxs-lookup"><span data-stu-id="aa39e-577">1226 (0x4CA)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-578">A conexão de rede foi fechada normalmente.</span><span class="sxs-lookup"><span data-stu-id="aa39e-578">The network connection was gracefully closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**Endereço de erro \_ \_ já \_ associado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**ERROR\_ADDRESS\_ALREADY\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-580">1227 (0x4CB)</span><span class="sxs-lookup"><span data-stu-id="aa39e-580">1227 (0x4CB)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-581">O ponto de extremidade de transporte de rede já tem um endereço associado a ele.</span><span class="sxs-lookup"><span data-stu-id="aa39e-581">The network transport endpoint already has an address associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**Endereço de erro \_ \_ não \_ associado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**ERROR\_ADDRESS\_NOT\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-583">1228 (0x4CC)</span><span class="sxs-lookup"><span data-stu-id="aa39e-583">1228 (0x4CC)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-584">Um endereço ainda não foi associado ao ponto de extremidade de rede.</span><span class="sxs-lookup"><span data-stu-id="aa39e-584">An address has not yet been associated with the network endpoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**conexão de erro \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="aa39e-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**ERROR\_CONNECTION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-586">1229 (0x4CD)</span><span class="sxs-lookup"><span data-stu-id="aa39e-586">1229 (0x4CD)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-587">Uma operação foi tentada em uma conexão de rede inexistente.</span><span class="sxs-lookup"><span data-stu-id="aa39e-587">An operation was attempted on a nonexistent network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**conexão de erro \_ \_ ativa**</span><span class="sxs-lookup"><span data-stu-id="aa39e-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERROR\_CONNECTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-589">1230 (0x4CE)</span><span class="sxs-lookup"><span data-stu-id="aa39e-589">1230 (0x4CE)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-590">Uma operação inválida foi tentada em uma conexão de rede ativa.</span><span class="sxs-lookup"><span data-stu-id="aa39e-590">An invalid operation was attempted on an active network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERRO de \_ rede \_ inacessível**</span><span class="sxs-lookup"><span data-stu-id="aa39e-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERROR\_NETWORK\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-592">1231 (0x4CF)</span><span class="sxs-lookup"><span data-stu-id="aa39e-592">1231 (0x4CF)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-593">O local de rede não pode ser acessado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-593">The network location cannot be reached.</span></span> <span data-ttu-id="aa39e-594">Para obter informações sobre solução de problemas de rede, consulte a ajuda do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa39e-594">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**HOST de erro \_ \_ inacessível**</span><span class="sxs-lookup"><span data-stu-id="aa39e-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERROR\_HOST\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-596">1232 (0x4D0)</span><span class="sxs-lookup"><span data-stu-id="aa39e-596">1232 (0x4D0)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-597">O local de rede não pode ser acessado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-597">The network location cannot be reached.</span></span> <span data-ttu-id="aa39e-598">Para obter informações sobre solução de problemas de rede, consulte a ajuda do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa39e-598">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**Protocolo de erro \_ \_ inacessível**</span><span class="sxs-lookup"><span data-stu-id="aa39e-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**ERROR\_PROTOCOL\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-600">1233 (0x4D1)</span><span class="sxs-lookup"><span data-stu-id="aa39e-600">1233 (0x4D1)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-601">O local de rede não pode ser acessado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-601">The network location cannot be reached.</span></span> <span data-ttu-id="aa39e-602">Para obter informações sobre solução de problemas de rede, consulte a ajuda do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa39e-602">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**porta de erro \_ \_ inacessível**</span><span class="sxs-lookup"><span data-stu-id="aa39e-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**ERROR\_PORT\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-604">1234 (0x4D2)</span><span class="sxs-lookup"><span data-stu-id="aa39e-604">1234 (0x4D2)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-605">Nenhum serviço está operando no ponto de extremidade de rede de destino no sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="aa39e-605">No service is operating at the destination network endpoint on the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**solicitação de erro \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="aa39e-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**ERROR\_REQUEST\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-607">1235 (0x4D3)</span><span class="sxs-lookup"><span data-stu-id="aa39e-607">1235 (0x4D3)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-608">A solicitação foi anulada.</span><span class="sxs-lookup"><span data-stu-id="aa39e-608">The request was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERRO de \_ conexão \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="aa39e-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERROR\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-610">1236 (0x4D4)</span><span class="sxs-lookup"><span data-stu-id="aa39e-610">1236 (0x4D4)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-611">A conexão de rede foi anulada pelo sistema local.</span><span class="sxs-lookup"><span data-stu-id="aa39e-611">The network connection was aborted by the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**ERRO de \_ repetição**</span><span class="sxs-lookup"><span data-stu-id="aa39e-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**ERROR\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-613">1237 (0x4D5)</span><span class="sxs-lookup"><span data-stu-id="aa39e-613">1237 (0x4D5)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-614">Não foi possível concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="aa39e-614">The operation could not be completed.</span></span> <span data-ttu-id="aa39e-615">Uma nova tentativa deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="aa39e-615">A retry should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_limite de \_ contagem de conexão de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**ERROR\_CONNECTION\_COUNT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-617">1238 (0x4D6)</span><span class="sxs-lookup"><span data-stu-id="aa39e-617">1238 (0x4D6)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-618">Não foi possível estabelecer uma conexão com o servidor porque o limite do número de conexões simultâneas para esta conta foi atingido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-618">A connection to the server could not be made because the limit on the number of concurrent connections for this account has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**ERRO \_ de \_ restrição de tempo de logon \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**ERROR\_LOGIN\_TIME\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-620">1239 (0x4D7)</span><span class="sxs-lookup"><span data-stu-id="aa39e-620">1239 (0x4D7)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-621">Tentando fazer logon durante uma hora não autorizada do dia para esta conta.</span><span class="sxs-lookup"><span data-stu-id="aa39e-621">Attempting to log in during an unauthorized time of day for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERRO \_ de \_ restrição de WKSTA de logon \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERROR\_LOGIN\_WKSTA\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-623">1240 (0x4D8)</span><span class="sxs-lookup"><span data-stu-id="aa39e-623">1240 (0x4D8)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-624">A conta não está autorizada a fazer logon nesta estação.</span><span class="sxs-lookup"><span data-stu-id="aa39e-624">The account is not authorized to log in from this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERRO \_ de \_ endereço incorreto**</span><span class="sxs-lookup"><span data-stu-id="aa39e-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERROR\_INCORRECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-626">1241 (0x4D9)</span><span class="sxs-lookup"><span data-stu-id="aa39e-626">1241 (0x4D9)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-627">O endereço de rede não pôde ser usado para a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="aa39e-627">The network address could not be used for the operation requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERRO \_ já \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERROR\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-629">1242 (0x4DA)</span><span class="sxs-lookup"><span data-stu-id="aa39e-629">1242 (0x4DA)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-630">O serviço já está registrado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-630">The service is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**serviço de erro \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**ERROR\_SERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-632">1243 (0x4DB)</span><span class="sxs-lookup"><span data-stu-id="aa39e-632">1243 (0x4DB)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-633">O serviço especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="aa39e-633">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERRO \_ não \_ autenticado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERROR\_NOT\_AUTHENTICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-635">1244 (0x4DC)</span><span class="sxs-lookup"><span data-stu-id="aa39e-635">1244 (0x4DC)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-636">A operação que está sendo solicitada não foi executada porque o usuário não foi autenticado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-636">The operation being requested was not performed because the user has not been authenticated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERRO \_ não \_ conectado \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERROR\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-638">1245 (0x4DD)</span><span class="sxs-lookup"><span data-stu-id="aa39e-638">1245 (0x4DD)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-639">A operação que está sendo solicitada não foi executada porque o usuário não fez logon na rede.</span><span class="sxs-lookup"><span data-stu-id="aa39e-639">The operation being requested was not performed because the user has not logged on to the network.</span></span> <span data-ttu-id="aa39e-640">O serviço especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="aa39e-640">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERRO de \_ continuação**</span><span class="sxs-lookup"><span data-stu-id="aa39e-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERROR\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-642">1246 (0x4DE)</span><span class="sxs-lookup"><span data-stu-id="aa39e-642">1246 (0x4DE)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-643">Continue com o trabalho em andamento.</span><span class="sxs-lookup"><span data-stu-id="aa39e-643">Continue with work in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERRO \_ já \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-645">1247 (0x4DF)</span><span class="sxs-lookup"><span data-stu-id="aa39e-645">1247 (0x4DF)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-646">Foi feita uma tentativa de executar uma operação de inicialização quando a inicialização já foi concluída.</span><span class="sxs-lookup"><span data-stu-id="aa39e-646">An attempt was made to perform an initialization operation when initialization has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERRO \_ não há \_ mais \_ dispositivos**</span><span class="sxs-lookup"><span data-stu-id="aa39e-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERROR\_NO\_MORE\_DEVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-648">1248 (0x4E0)</span><span class="sxs-lookup"><span data-stu-id="aa39e-648">1248 (0x4E0)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-649">Não há mais dispositivos locais.</span><span class="sxs-lookup"><span data-stu-id="aa39e-649">No more local devices.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERRO \_ sem \_ esse \_ site**</span><span class="sxs-lookup"><span data-stu-id="aa39e-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERROR\_NO\_SUCH\_SITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-651">1249 (0x4E1)</span><span class="sxs-lookup"><span data-stu-id="aa39e-651">1249 (0x4E1)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-652">O site especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="aa39e-652">The specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**ERRO \_ o \_ controlador de domínio \_ existe**</span><span class="sxs-lookup"><span data-stu-id="aa39e-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**ERROR\_DOMAIN\_CONTROLLER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-654">1250 (0x4E2)</span><span class="sxs-lookup"><span data-stu-id="aa39e-654">1250 (0x4E2)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-655">Já existe um controlador de domínio com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-655">A domain controller with the specified name already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERRO \_ somente \_ se \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERROR\_ONLY\_IF\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-657">1251 (0x4E3)</span><span class="sxs-lookup"><span data-stu-id="aa39e-657">1251 (0x4E3)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-658">Esta operação só tem suporte quando você está conectado ao servidor.</span><span class="sxs-lookup"><span data-stu-id="aa39e-658">This operation is supported only when you are connected to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERRO ao \_ substituir \_ noChanges**</span><span class="sxs-lookup"><span data-stu-id="aa39e-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERROR\_OVERRIDE\_NOCHANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-660">1252 (0x4E4)</span><span class="sxs-lookup"><span data-stu-id="aa39e-660">1252 (0x4E4)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-661">A estrutura de diretiva de grupo deve chamar a extensão mesmo se não houver nenhuma alteração.</span><span class="sxs-lookup"><span data-stu-id="aa39e-661">The group policy framework should call the extension even if there are no changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERRO \_ de \_ perfil de usuário insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERROR\_BAD\_USER\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-663">1253 (0x4E5)</span><span class="sxs-lookup"><span data-stu-id="aa39e-663">1253 (0x4E5)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-664">O usuário especificado não tem um perfil válido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-664">The specified user does not have a valid profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERRO \_ sem \_ suporte \_ no \_ SBS**</span><span class="sxs-lookup"><span data-stu-id="aa39e-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERROR\_NOT\_SUPPORTED\_ON\_SBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-666">1254 (0x4E6)</span><span class="sxs-lookup"><span data-stu-id="aa39e-666">1254 (0x4E6)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-667">Não há suporte para esta operação em um computador que esteja executando o Windows Server 2003 para Small Business Server.</span><span class="sxs-lookup"><span data-stu-id="aa39e-667">This operation is not supported on a computer running Windows Server 2003 for Small Business Server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ERRO \_ \_ de desligamento \_ do servidor em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="aa39e-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ERROR\_SERVER\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-669">1255 (0x4E7)</span><span class="sxs-lookup"><span data-stu-id="aa39e-669">1255 (0x4E7)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-670">A máquina do servidor está sendo desligada.</span><span class="sxs-lookup"><span data-stu-id="aa39e-670">The server machine is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERRO ao \_ hospedar \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERROR\_HOST\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-672">1256 (0x4E8)</span><span class="sxs-lookup"><span data-stu-id="aa39e-672">1256 (0x4E8)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-673">O sistema remoto não está disponível.</span><span class="sxs-lookup"><span data-stu-id="aa39e-673">The remote system is not available.</span></span> <span data-ttu-id="aa39e-674">Para obter informações sobre solução de problemas de rede, consulte a ajuda do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa39e-674">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERRO de \_ Sid de não \_ conta \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERROR\_NON\_ACCOUNT\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-676">1257 (0x4E9)</span><span class="sxs-lookup"><span data-stu-id="aa39e-676">1257 (0x4E9)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-677">O identificador de segurança fornecido não é de um domínio de conta.</span><span class="sxs-lookup"><span data-stu-id="aa39e-677">The security identifier provided is not from an account domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERRO \_ não \_ Sid de domínio \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERROR\_NON\_DOMAIN\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-679">1258 (0x4EA)</span><span class="sxs-lookup"><span data-stu-id="aa39e-679">1258 (0x4EA)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-680">O identificador de segurança fornecido não tem um componente de domínio.</span><span class="sxs-lookup"><span data-stu-id="aa39e-680">The security identifier provided does not have a domain component.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**bloco de erro \_ APPHELP \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERROR\_APPHELP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-682">1259 (0x4EB)</span><span class="sxs-lookup"><span data-stu-id="aa39e-682">1259 (0x4EB)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-683">Caixa de diálogo AppHelp cancelada, impedindo o início do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa39e-683">AppHelp dialog canceled thus preventing the application from starting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERRO \_ \_ de acesso desabilitado \_ pela \_ política**</span><span class="sxs-lookup"><span data-stu-id="aa39e-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-685">1260 (0x4EC)</span><span class="sxs-lookup"><span data-stu-id="aa39e-685">1260 (0x4EC)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-686">Este programa está bloqueado pela política de grupo.</span><span class="sxs-lookup"><span data-stu-id="aa39e-686">This program is blocked by group policy.</span></span> <span data-ttu-id="aa39e-687">Para obter mais informações, contate o administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa39e-687">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERRO \_ reg \_ de \_ consumo NAT**</span><span class="sxs-lookup"><span data-stu-id="aa39e-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERROR\_REG\_NAT\_CONSUMPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-689">1261 (0x4ED)</span><span class="sxs-lookup"><span data-stu-id="aa39e-689">1261 (0x4ED)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-690">Um programa tentou usar um valor de registro inválido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-690">A program attempt to use an invalid register value.</span></span> <span data-ttu-id="aa39e-691">Normalmente causado por um registro não inicializado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-691">Normally caused by an uninitialized register.</span></span> <span data-ttu-id="aa39e-692">Esse erro é específico do Itanium.</span><span class="sxs-lookup"><span data-stu-id="aa39e-692">This error is Itanium specific.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERRO \_ CSCSHARE \_ offline**</span><span class="sxs-lookup"><span data-stu-id="aa39e-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERROR\_CSCSHARE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-694">1262 (0x4EE)</span><span class="sxs-lookup"><span data-stu-id="aa39e-694">1262 (0x4EE)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-695">O compartilhamento está offline no momento ou não existe.</span><span class="sxs-lookup"><span data-stu-id="aa39e-695">The share is currently offline or does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**\_falha de PKINIT de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERROR\_PKINIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-697">1263 (0x4EF)</span><span class="sxs-lookup"><span data-stu-id="aa39e-697">1263 (0x4EF)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-698">O protocolo Kerberos encontrou um erro ao validar o certificado KDC durante o logon de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="aa39e-698">The Kerberos protocol encountered an error while validating the KDC certificate during smartcard logon.</span></span> <span data-ttu-id="aa39e-699">Há mais informações no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa39e-699">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERRO \_ \_ falha no subsistema de cartão inteligente \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERROR\_SMARTCARD\_SUBSYSTEM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-701">1264 (0x4F0)</span><span class="sxs-lookup"><span data-stu-id="aa39e-701">1264 (0x4F0)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-702">O protocolo Kerberos encontrou um erro ao tentar utilizar o subsistema de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="aa39e-702">The Kerberos protocol encountered an error while attempting to utilize the smartcard subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**DOWNGRADE de erro \_ \_ detectado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**ERROR\_DOWNGRADE\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-704">1265 (0x4F1)</span><span class="sxs-lookup"><span data-stu-id="aa39e-704">1265 (0x4F1)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-705">O sistema não pode contatar um controlador de domínio para atender à solicitação de autenticação.</span><span class="sxs-lookup"><span data-stu-id="aa39e-705">The system cannot contact a domain controller to service the authentication request.</span></span> <span data-ttu-id="aa39e-706">Tente novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="aa39e-706">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**computador de erro \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**ERROR\_MACHINE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-708">1271 (0x4F7)</span><span class="sxs-lookup"><span data-stu-id="aa39e-708">1271 (0x4F7)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-709">O computador está bloqueado e não pode ser desligado sem a opção Force.</span><span class="sxs-lookup"><span data-stu-id="aa39e-709">The machine is locked and cannot be shut down without the force option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**retorno de chamada de erro de \_ \_ \_ dados inválidos fornecidos \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**ERROR\_CALLBACK\_SUPPLIED\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-711">1273 (0x4F9)</span><span class="sxs-lookup"><span data-stu-id="aa39e-711">1273 (0x4F9)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-712">Um retorno de chamada definido pelo aplicativo fornecia dados inválidos quando chamado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-712">An application-defined callback gave invalid data when called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERRO ao \_ sincronizar a \_ atualização em primeiro plano \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="aa39e-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERROR\_SYNC\_FOREGROUND\_REFRESH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-714">1274 (0x4FA)</span><span class="sxs-lookup"><span data-stu-id="aa39e-714">1274 (0x4FA)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-715">A estrutura de diretiva de grupo deve chamar a extensão na atualização da política de primeiro plano síncrona.</span><span class="sxs-lookup"><span data-stu-id="aa39e-715">The group policy framework should call the extension in the synchronous foreground policy refresh.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**Driver de erro \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**ERROR\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-717">1275 (0x4FB)</span><span class="sxs-lookup"><span data-stu-id="aa39e-717">1275 (0x4FB)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-718">O carregamento deste driver foi bloqueado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-718">This driver has been blocked from loading.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERRO \_ \_ de importação inválida \_ de \_ não \_ dll**</span><span class="sxs-lookup"><span data-stu-id="aa39e-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERROR\_INVALID\_IMPORT\_OF\_NON\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-720">1276 (0x4FC)</span><span class="sxs-lookup"><span data-stu-id="aa39e-720">1276 (0x4FC)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-721">Uma DLL (biblioteca de vínculo dinâmico) referenciou um módulo que não era uma DLL nem a imagem executável do processo.</span><span class="sxs-lookup"><span data-stu-id="aa39e-721">A dynamic link library (DLL) referenced a module that was neither a DLL nor the process's executable image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERRO ao \_ acessar o \_ \_ webblade desabilitado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-723">1277 (0x4FD)</span><span class="sxs-lookup"><span data-stu-id="aa39e-723">1277 (0x4FD)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-724">O Windows não pode abrir este programa porque ele foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-724">Windows cannot open this program since it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERRO ao \_ acessar a \_ \_ adulteração da webblade desabilitada \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE\_TAMPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-726">1278 (0x4FE)</span><span class="sxs-lookup"><span data-stu-id="aa39e-726">1278 (0x4FE)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-727">O Windows não pode abrir este programa porque o sistema de imposição de licença foi violado ou se tornou corrompido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-727">Windows cannot open this program because the license enforcement system has been tampered with or become corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**\_falha na recuperação de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERROR\_RECOVERY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-729">1279 (0x4FF)</span><span class="sxs-lookup"><span data-stu-id="aa39e-729">1279 (0x4FF)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-730">Falha na recuperação de uma transação.</span><span class="sxs-lookup"><span data-stu-id="aa39e-730">A transaction recover failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERRO \_ já \_ Fiber**</span><span class="sxs-lookup"><span data-stu-id="aa39e-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERROR\_ALREADY\_FIBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-732">1280 (0x500)</span><span class="sxs-lookup"><span data-stu-id="aa39e-732">1280 (0x500)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-733">O thread atual já foi convertido em uma fibra.</span><span class="sxs-lookup"><span data-stu-id="aa39e-733">The current thread has already been converted to a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERRO \_ já \_ thread**</span><span class="sxs-lookup"><span data-stu-id="aa39e-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERROR\_ALREADY\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-735">1281 (0x501)</span><span class="sxs-lookup"><span data-stu-id="aa39e-735">1281 (0x501)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-736">O thread atual já foi convertido de uma fibra.</span><span class="sxs-lookup"><span data-stu-id="aa39e-736">The current thread has already been converted from a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**\_estouro de \_ buffer de pilha de erros \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**ERROR\_STACK\_BUFFER\_OVERRUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-738">1282 (0x502)</span><span class="sxs-lookup"><span data-stu-id="aa39e-738">1282 (0x502)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-739">O sistema detectou uma saturação de um buffer baseado em pilha neste aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa39e-739">The system detected an overrun of a stack-based buffer in this application.</span></span> <span data-ttu-id="aa39e-740">Essa saturação pode potencialmente permitir que um usuário mal-intencionado assuma o controle desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa39e-740">This overrun could potentially allow a malicious user to gain control of this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**cota de parâmetro de erro \_ \_ \_ excedida**</span><span class="sxs-lookup"><span data-stu-id="aa39e-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**ERROR\_PARAMETER\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-742">1283 (0x503)</span><span class="sxs-lookup"><span data-stu-id="aa39e-742">1283 (0x503)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-743">Os dados presentes em um dos parâmetros são mais do que a função pode operar.</span><span class="sxs-lookup"><span data-stu-id="aa39e-743">Data present in one of the parameters is more than the function can operate on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**ERRO do \_ depurador \_ inativo**</span><span class="sxs-lookup"><span data-stu-id="aa39e-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**ERROR\_DEBUGGER\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-745">1284 (0x504)</span><span class="sxs-lookup"><span data-stu-id="aa39e-745">1284 (0x504)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-746">Falha ao tentar fazer uma operação em um objeto de depuração porque o objeto está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="aa39e-746">An attempt to do an operation on a debug object failed because the object is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**\_ \_ falha ao carregar o atraso do erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERROR\_DELAY\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-748">1285 (0x505)</span><span class="sxs-lookup"><span data-stu-id="aa39e-748">1285 (0x505)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-749">Falha ao tentar atrasar a carga de um. dll ou obter um endereço de função em um DELAYED. dll.</span><span class="sxs-lookup"><span data-stu-id="aa39e-749">An attempt to delay-load a .dll or get a function address in a delay-loaded .dll failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERRO \_ VDM não \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERROR\_VDM\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-751">1286 (0x506)</span><span class="sxs-lookup"><span data-stu-id="aa39e-751">1286 (0x506)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-752">%1 é um aplicativo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="aa39e-752">%1 is a 16-bit application.</span></span> <span data-ttu-id="aa39e-753">Você não tem permissões para executar aplicativos de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="aa39e-753">You do not have permissions to execute 16-bit applications.</span></span> <span data-ttu-id="aa39e-754">Verifique suas permissões com o administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa39e-754">Check your permissions with your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**erro não \_ identificado \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**ERROR\_UNIDENTIFIED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-756">1287 (0x507)</span><span class="sxs-lookup"><span data-stu-id="aa39e-756">1287 (0x507)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-757">Existem informações insuficientes para identificar a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="aa39e-757">Insufficient information exists to identify the cause of failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERRO \_ \_ parâmetro CRUNTIME \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERROR\_INVALID\_CRUNTIME\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-759">1288 (0x508)</span><span class="sxs-lookup"><span data-stu-id="aa39e-759">1288 (0x508)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-760">O parâmetro passado para uma função de tempo de execução C está incorreto.</span><span class="sxs-lookup"><span data-stu-id="aa39e-760">The parameter passed to a C runtime function is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERRO \_ além de \_ VDL**</span><span class="sxs-lookup"><span data-stu-id="aa39e-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERROR\_BEYOND\_VDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-762">1289 (0x509)</span><span class="sxs-lookup"><span data-stu-id="aa39e-762">1289 (0x509)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-763">A operação ocorreu além do comprimento de dados válido do arquivo.</span><span class="sxs-lookup"><span data-stu-id="aa39e-763">The operation occurred beyond the valid data length of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERRO de \_ tipo de Sid de serviço INcompatível \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_SID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-765">1290 (0x50A)</span><span class="sxs-lookup"><span data-stu-id="aa39e-765">1290 (0x50A)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-766">A inicialização do serviço falhou porque um ou mais serviços no mesmo processo têm uma configuração de tipo de SID de serviço incompatível.</span><span class="sxs-lookup"><span data-stu-id="aa39e-766">The service start failed since one or more services in the same process have an incompatible service SID type setting.</span></span> <span data-ttu-id="aa39e-767">Um serviço com o tipo de SID de serviço restrito só pode coexistir no mesmo processo com outros serviços com um tipo de SID restrito.</span><span class="sxs-lookup"><span data-stu-id="aa39e-767">A service with restricted service SID type can only coexist in the same process with other services with a restricted SID type.</span></span> <span data-ttu-id="aa39e-768">Se o tipo de SID de serviço para esse serviço tiver acabado de ser configurado, o processo de hospedagem deverá ser reiniciado para iniciar esse serviço.</span><span class="sxs-lookup"><span data-stu-id="aa39e-768">If the service SID type for this service was just configured, the hosting process must be restarted in order to start this service.</span></span>

<span data-ttu-id="aa39e-769">No Windows Server 2003 e no Windows XP, um serviço irrestrito não pode coexistir no mesmo processo com outros serviços.</span><span class="sxs-lookup"><span data-stu-id="aa39e-769">On Windows Server 2003 and Windows XP, an unrestricted service cannot coexist in the same process with other services.</span></span> <span data-ttu-id="aa39e-770">O serviço com o tipo de SID de serviço irrestrito deve ser movido para um processo proprietário a fim de iniciar esse serviço.</span><span class="sxs-lookup"><span data-stu-id="aa39e-770">The service with the unrestricted service SID type must be moved to an owned process in order to start this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**processo de driver de erro \_ \_ \_ encerrado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**ERROR\_DRIVER\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-772">1291 (0x50B)</span><span class="sxs-lookup"><span data-stu-id="aa39e-772">1291 (0x50B)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-773">O processo que hospeda o driver para este dispositivo foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="aa39e-773">The process hosting the driver for this device has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**\_limite de implementação de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**ERROR\_IMPLEMENTATION\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-775">1292 (0x50C)</span><span class="sxs-lookup"><span data-stu-id="aa39e-775">1292 (0x50C)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-776">Uma operação tentou exceder um limite definido para implementação.</span><span class="sxs-lookup"><span data-stu-id="aa39e-776">An operation attempted to exceed an implementation-defined limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**o \_ processo de erro \_ está \_ protegido**</span><span class="sxs-lookup"><span data-stu-id="aa39e-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**ERROR\_PROCESS\_IS\_PROTECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-778">1293 (0x50D)</span><span class="sxs-lookup"><span data-stu-id="aa39e-778">1293 (0x50D)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-779">O processo de destino ou o thread de destino que contém o processo é um processo protegido.</span><span class="sxs-lookup"><span data-stu-id="aa39e-779">Either the target process, or the target thread's containing process, is a protected process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**notificação do serviço de erro \_ \_ notificando atraso do \_ cliente \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERROR\_SERVICE\_NOTIFY\_CLIENT\_LAGGING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-781">1294 (0x50E)</span><span class="sxs-lookup"><span data-stu-id="aa39e-781">1294 (0x50E)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-782">O cliente de notificação de serviço está ultrapassando muito atrás do estado atual dos serviços no computador.</span><span class="sxs-lookup"><span data-stu-id="aa39e-782">The service notification client is lagging too far behind the current state of services in the machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**cota de disco de erro \_ \_ \_ excedida**</span><span class="sxs-lookup"><span data-stu-id="aa39e-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**ERROR\_DISK\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-784">1295 (0x50F)</span><span class="sxs-lookup"><span data-stu-id="aa39e-784">1295 (0x50F)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-785">A operação de arquivo solicitada falhou porque a cota de armazenamento foi excedida.</span><span class="sxs-lookup"><span data-stu-id="aa39e-785">The requested file operation failed because the storage quota was exceeded.</span></span> <span data-ttu-id="aa39e-786">Para liberar espaço em disco, mova arquivos para um local diferente ou exclua arquivos desnecessários.</span><span class="sxs-lookup"><span data-stu-id="aa39e-786">To free up disk space, move files to a different location or delete unnecessary files.</span></span> <span data-ttu-id="aa39e-787">Para obter mais informações, contate o administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa39e-787">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**conteúdo de erro \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="aa39e-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**ERROR\_CONTENT\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-789">1296 (0x510)</span><span class="sxs-lookup"><span data-stu-id="aa39e-789">1296 (0x510)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-790">A operação de arquivo solicitada falhou porque a política de armazenamento bloqueia esse tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="aa39e-790">The requested file operation failed because the storage policy blocks that type of file.</span></span> <span data-ttu-id="aa39e-791">Para obter mais informações, contate o administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa39e-791">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERRO de \_ privilégio de serviço INcompatível \_ \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-793">1297 (0x511)</span><span class="sxs-lookup"><span data-stu-id="aa39e-793">1297 (0x511)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-794">Um privilégio que o serviço requer para funcionar corretamente não existe na configuração da conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="aa39e-794">A privilege that the service requires to function properly does not exist in the service account configuration.</span></span> <span data-ttu-id="aa39e-795">Você pode usar o snap-in do MMC (console de gerenciamento Microsoft) de serviços e o snap-in MMC de configurações de segurança local (secpol. msc) para exibir a configuração do serviço e a configuração da conta.</span><span class="sxs-lookup"><span data-stu-id="aa39e-795">You may use the Services Microsoft Management Console (MMC) snap-in (services.msc) and the Local Security Settings MMC snap-in (secpol.msc) to view the service configuration and the account configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**\_falha do aplicativo de erro \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERROR\_APP\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-797">1298 (0x512)</span><span class="sxs-lookup"><span data-stu-id="aa39e-797">1298 (0x512)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-798">Um thread envolvido nesta operação parece não estar respondendo.</span><span class="sxs-lookup"><span data-stu-id="aa39e-798">A thread involved in this operation appears to be unresponsive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="aa39e-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**rótulo de erro \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="aa39e-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**ERROR\_INVALID\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa39e-800">1299 (0x513)</span><span class="sxs-lookup"><span data-stu-id="aa39e-800">1299 (0x513)</span></span>
</dt> <dt>



<span data-ttu-id="aa39e-801">Indica que uma determinada ID de segurança não pode ser atribuída como o rótulo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="aa39e-801">Indicates a particular Security ID may not be assigned as the label of an object.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="aa39e-802">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa39e-802">Requirements</span></span>



| <span data-ttu-id="aa39e-803">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa39e-803">Requirement</span></span> | <span data-ttu-id="aa39e-804">Valor</span><span class="sxs-lookup"><span data-stu-id="aa39e-804">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa39e-805">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa39e-805">Minimum supported client</span></span><br/> | <span data-ttu-id="aa39e-806">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="aa39e-806">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aa39e-807">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa39e-807">Minimum supported server</span></span><br/> | <span data-ttu-id="aa39e-808">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa39e-808">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa39e-809">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa39e-809">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa39e-810"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa39e-810"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa39e-811">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa39e-811">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa39e-812">Códigos de erro do sistema</span><span class="sxs-lookup"><span data-stu-id="aa39e-812">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




