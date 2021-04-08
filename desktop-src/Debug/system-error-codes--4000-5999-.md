---
description: Descreve os códigos de erro 4000-5999 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: Códigos de erro do sistema (4000-5999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089242"
---
# <a name="system-error-codes-4000-5999"></a><span data-ttu-id="d746b-103">Códigos de erro do sistema (4000-5999)</span><span class="sxs-lookup"><span data-stu-id="d746b-103">System Error Codes (4000-5999)</span></span>

> [!NOTE]
> <span data-ttu-id="d746b-104">Essas informações destinam-se a desenvolvedores Depurando erros do sistema.</span><span class="sxs-lookup"><span data-stu-id="d746b-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="d746b-105">Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d746b-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="d746b-106">A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) para erros 4000 a 5999.</span><span class="sxs-lookup"><span data-stu-id="d746b-106">The following list describes [system error codes](system-error-codes.md) for errors 4000 to 5999.</span></span> <span data-ttu-id="d746b-107">Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham.</span><span class="sxs-lookup"><span data-stu-id="d746b-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="d746b-108">Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="d746b-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="d746b-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERRO \_ interno do WINS \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERROR\_WINS\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-110">4000 (0xFA0)</span><span class="sxs-lookup"><span data-stu-id="d746b-110">4000 (0xFA0)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-111">O WINS encontrou um erro ao processar o comando.</span><span class="sxs-lookup"><span data-stu-id="d746b-111">WINS encountered an error while processing the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERRO \_ não é possível \_ \_ excluir o \_ \_ WINS local**</span><span class="sxs-lookup"><span data-stu-id="d746b-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERROR\_CAN\_NOT\_DEL\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-113">4001 (0xFA1)</span><span class="sxs-lookup"><span data-stu-id="d746b-113">4001 (0xFA1)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-114">O WINS local não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d746b-114">The local WINS cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERRO \_ de \_ inicialização estática**</span><span class="sxs-lookup"><span data-stu-id="d746b-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERROR\_STATIC\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-116">4002 (0xFA2)</span><span class="sxs-lookup"><span data-stu-id="d746b-116">4002 (0xFA2)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-117">Falha na importação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d746b-117">The importation from the file failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**BACKUP do ERROR \_ Inc \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**ERROR\_INC\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-119">4003 (0xFA3)</span><span class="sxs-lookup"><span data-stu-id="d746b-119">4003 (0xFA3)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-120">Falha no backup.</span><span class="sxs-lookup"><span data-stu-id="d746b-120">The backup failed.</span></span> <span data-ttu-id="d746b-121">Um backup completo foi feito antes?</span><span class="sxs-lookup"><span data-stu-id="d746b-121">Was a full backup done before?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERRO \_ de \_ backup completo**</span><span class="sxs-lookup"><span data-stu-id="d746b-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERROR\_FULL\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-123">4004 (0xFA4)</span><span class="sxs-lookup"><span data-stu-id="d746b-123">4004 (0xFA4)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-124">Falha no backup.</span><span class="sxs-lookup"><span data-stu-id="d746b-124">The backup failed.</span></span> <span data-ttu-id="d746b-125">Verifique o diretório para o qual você está fazendo backup do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d746b-125">Check the directory to which you are backing the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**o erro \_ REC \_ não \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d746b-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**ERROR\_REC\_NON\_EXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-127">4005 (0xFA5)</span><span class="sxs-lookup"><span data-stu-id="d746b-127">4005 (0xFA5)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-128">O nome não existe no banco de dados WINS.</span><span class="sxs-lookup"><span data-stu-id="d746b-128">The name does not exist in the WINS database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERRO \_ RPL \_ não \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="d746b-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERROR\_RPL\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-130">4006 (0xFA6)</span><span class="sxs-lookup"><span data-stu-id="d746b-130">4006 (0xFA6)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-131">A replicação com um parceiro não configurado não é permitida.</span><span class="sxs-lookup"><span data-stu-id="d746b-131">Replication with a nonconfigured partner is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**\_versão do CONTENTINFO de erro PEERDIST \_ \_ \_ sem suporte**</span><span class="sxs-lookup"><span data-stu-id="d746b-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**PEERDIST\_ERROR\_CONTENTINFO\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-133">4050 (0xFD2)</span><span class="sxs-lookup"><span data-stu-id="d746b-133">4050 (0xFD2)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-134">Não há suporte para a versão das informações de conteúdo fornecidas.</span><span class="sxs-lookup"><span data-stu-id="d746b-134">The version of the supplied content information is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**\_erro PEERDIST \_ não pode \_ analisar \_ CONTENTINFO**</span><span class="sxs-lookup"><span data-stu-id="d746b-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**PEERDIST\_ERROR\_CANNOT\_PARSE\_CONTENTINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-136">4051 (0xFD3)</span><span class="sxs-lookup"><span data-stu-id="d746b-136">4051 (0xFD3)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-137">As informações de conteúdo fornecidas estão malformadas.</span><span class="sxs-lookup"><span data-stu-id="d746b-137">The supplied content information is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**\_ \_ dados ausentes no erro PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**PEERDIST\_ERROR\_MISSING\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-139">4052 (0xFD4)</span><span class="sxs-lookup"><span data-stu-id="d746b-139">4052 (0xFD4)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-140">Os dados solicitados não podem ser encontrados em caches locais ou pares.</span><span class="sxs-lookup"><span data-stu-id="d746b-140">The requested data cannot be found in local or peer caches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**\_ \_ não há mais erro no PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**PEERDIST\_ERROR\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-142">4053 (0xFD5)</span><span class="sxs-lookup"><span data-stu-id="d746b-142">4053 (0xFD5)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-143">Não há mais dados disponíveis ou necessários.</span><span class="sxs-lookup"><span data-stu-id="d746b-143">No more data is available or required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**\_erro PEERDIST \_ não \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="d746b-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**PEERDIST\_ERROR\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-145">4054 (0xFD6)</span><span class="sxs-lookup"><span data-stu-id="d746b-145">4054 (0xFD6)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-146">O objeto fornecido não foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="d746b-146">The supplied object has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**\_erro PEERDIST \_ já \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="d746b-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**PEERDIST\_ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-148">4055 (0xFD7)</span><span class="sxs-lookup"><span data-stu-id="d746b-148">4055 (0xFD7)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-149">O objeto fornecido já foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="d746b-149">The supplied object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_ \_ desligamento \_ de erro PEERDIST em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="d746b-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**PEERDIST\_ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-151">4056 (0xFD8)</span><span class="sxs-lookup"><span data-stu-id="d746b-151">4056 (0xFD8)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-152">Uma operação de desligamento já está em andamento.</span><span class="sxs-lookup"><span data-stu-id="d746b-152">A shutdown operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**\_erro PEERDIST \_ invalidado**</span><span class="sxs-lookup"><span data-stu-id="d746b-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**PEERDIST\_ERROR\_INVALIDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-154">4057 (0xFD9)</span><span class="sxs-lookup"><span data-stu-id="d746b-154">4057 (0xFD9)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-155">O objeto fornecido já foi invalidado.</span><span class="sxs-lookup"><span data-stu-id="d746b-155">The supplied object has already been invalidated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**o \_ erro PEERDIST \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d746b-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**PEERDIST\_ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-157">4058 (0xFDA)</span><span class="sxs-lookup"><span data-stu-id="d746b-157">4058 (0xFDA)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-158">Um elemento já existe e não foi substituído.</span><span class="sxs-lookup"><span data-stu-id="d746b-158">An element already exists and was not replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**operação de erro PEERDIST não \_ \_ \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="d746b-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**PEERDIST\_ERROR\_OPERATION\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-160">4059 (0xFDB)</span><span class="sxs-lookup"><span data-stu-id="d746b-160">4059 (0xFDB)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-161">Não é possível cancelar a operação solicitada, pois ela já foi concluída.</span><span class="sxs-lookup"><span data-stu-id="d746b-161">Can not cancel the requested operation as it has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**\_erro PEERDIST \_ já \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="d746b-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**PEERDIST\_ERROR\_ALREADY\_COMPLETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-163">4060 (0xFDC)</span><span class="sxs-lookup"><span data-stu-id="d746b-163">4060 (0xFDC)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-164">Não é possível executar a operação solicitada porque ela já foi executada.</span><span class="sxs-lookup"><span data-stu-id="d746b-164">Can not perform the reqested operation because it has already been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**\_erro PEERDIST \_ fora \_ dos \_ limites**</span><span class="sxs-lookup"><span data-stu-id="d746b-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**PEERDIST\_ERROR\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-166">4061 (0xFDD)</span><span class="sxs-lookup"><span data-stu-id="d746b-166">4061 (0xFDD)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-167">Uma operação acessou dados além dos limites de dados válidos.</span><span class="sxs-lookup"><span data-stu-id="d746b-167">An operation accessed data beyond the bounds of valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**\_versão de erro PEERDIST \_ \_ sem suporte**</span><span class="sxs-lookup"><span data-stu-id="d746b-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**PEERDIST\_ERROR\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-169">4062 (0xFDE)</span><span class="sxs-lookup"><span data-stu-id="d746b-169">4062 (0xFDE)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-170">Não há suporte para a versão solicitada.</span><span class="sxs-lookup"><span data-stu-id="d746b-170">The requested version is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**\_ \_ Configuração inválida de erro PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**PEERDIST\_ERROR\_INVALID\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-172">4063 (0xFDF)</span><span class="sxs-lookup"><span data-stu-id="d746b-172">4063 (0xFDF)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-173">Um valor de configuração é inválido.</span><span class="sxs-lookup"><span data-stu-id="d746b-173">A configuration value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**\_erro PEERDIST \_ não \_ licenciado**</span><span class="sxs-lookup"><span data-stu-id="d746b-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**PEERDIST\_ERROR\_NOT\_LICENSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-175">4064 (0xFE0)</span><span class="sxs-lookup"><span data-stu-id="d746b-175">4064 (0xFE0)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-176">A SKU não está licenciada.</span><span class="sxs-lookup"><span data-stu-id="d746b-176">The SKU is not licensed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**\_serviço de erro PEERDIST \_ \_ indisponível**</span><span class="sxs-lookup"><span data-stu-id="d746b-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**PEERDIST\_ERROR\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-178">4065 (0xFE1)</span><span class="sxs-lookup"><span data-stu-id="d746b-178">4065 (0xFE1)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-179">O serviço PeerDist ainda está sendo inicializado e estará disponível em breve.</span><span class="sxs-lookup"><span data-stu-id="d746b-179">PeerDist Service is still initializing and will be available shortly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**\_falha de \_ confiança de erro PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**PEERDIST\_ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-181">4066 (0xFE2)</span><span class="sxs-lookup"><span data-stu-id="d746b-181">4066 (0xFE2)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-182">A comunicação com um ou mais computadores será temporariamente bloqueada devido a erros recentes.</span><span class="sxs-lookup"><span data-stu-id="d746b-182">Communication with one or more computers will be temporarily blocked due to recent errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERRO \_ de \_ conflito de endereço DHCP \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERROR\_DHCP\_ADDRESS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-184">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="d746b-184">4100 (0x1004)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-185">O cliente DHCP obteve um endereço IP que já está em uso na rede.</span><span class="sxs-lookup"><span data-stu-id="d746b-185">The DHCP client has obtained an IP address that is already in use on the network.</span></span> <span data-ttu-id="d746b-186">A interface local será desabilitada até que o cliente DHCP possa obter um novo endereço.</span><span class="sxs-lookup"><span data-stu-id="d746b-186">The local interface will be disabled until the DHCP client can obtain a new address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERRO \_ \_ GUID WMI \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERROR\_WMI\_GUID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-188">4200 (0x1068)</span><span class="sxs-lookup"><span data-stu-id="d746b-188">4200 (0x1068)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-189">O GUID passado não foi reconhecido como válido por um provedor de dados WMI.</span><span class="sxs-lookup"><span data-stu-id="d746b-189">The GUID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERRO \_ de \_ instância WMI \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="d746b-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERROR\_WMI\_INSTANCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-191">4201 (0x1069)</span><span class="sxs-lookup"><span data-stu-id="d746b-191">4201 (0x1069)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-192">O nome da instância passado não foi reconhecido como válido por um provedor de dados WMI.</span><span class="sxs-lookup"><span data-stu-id="d746b-192">The instance name passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERRO \_ WMI \_ ItemId \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERROR\_WMI\_ITEMID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-194">4202 (0x106A)</span><span class="sxs-lookup"><span data-stu-id="d746b-194">4202 (0x106A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-195">A ID do item de dados passada não foi reconhecida como válida por um provedor de dados WMI.</span><span class="sxs-lookup"><span data-stu-id="d746b-195">The data item ID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERRO de \_ WMI \_ tente \_ novamente**</span><span class="sxs-lookup"><span data-stu-id="d746b-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERROR\_WMI\_TRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-197">4203 (0x106B)</span><span class="sxs-lookup"><span data-stu-id="d746b-197">4203 (0x106B)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-198">A solicitação WMI não pôde ser concluída e deve ser repetida.</span><span class="sxs-lookup"><span data-stu-id="d746b-198">The WMI request could not be completed and should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERRO do \_ WMI \_ DP \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERROR\_WMI\_DP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-200">4204 (0x106C)</span><span class="sxs-lookup"><span data-stu-id="d746b-200">4204 (0x106C)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-201">Não foi possível localizar o provedor de dados WMI.</span><span class="sxs-lookup"><span data-stu-id="d746b-201">The WMI data provider could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERRO \_ \_ referência de instância não resolvida do WMI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERROR\_WMI\_UNRESOLVED\_INSTANCE\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-203">4205 (0x106D)</span><span class="sxs-lookup"><span data-stu-id="d746b-203">4205 (0x106D)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-204">O provedor de dados WMI faz referência a um conjunto de instâncias que não foi registrado.</span><span class="sxs-lookup"><span data-stu-id="d746b-204">The WMI data provider references an instance set that has not been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERRO o \_ WMI \_ já está \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="d746b-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERROR\_WMI\_ALREADY\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-206">4206 (0x106E)</span><span class="sxs-lookup"><span data-stu-id="d746b-206">4206 (0x106E)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-207">A notificação de eventos ou o bloco de dados do WMI já foi habilitado.</span><span class="sxs-lookup"><span data-stu-id="d746b-207">The WMI data block or event notification has already been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERRO \_ \_ GUID WMI \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="d746b-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERROR\_WMI\_GUID\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-209">4207 (0x106F)</span><span class="sxs-lookup"><span data-stu-id="d746b-209">4207 (0x106F)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-210">O bloco de dados WMI não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="d746b-210">The WMI data block is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERRO \_ o \_ servidor WMI \_ não está disponível**</span><span class="sxs-lookup"><span data-stu-id="d746b-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERROR\_WMI\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-212">4208 (0x1070)</span><span class="sxs-lookup"><span data-stu-id="d746b-212">4208 (0x1070)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-213">O serviço de dados WMI não está disponível.</span><span class="sxs-lookup"><span data-stu-id="d746b-213">The WMI data service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERRO \_ \_ \_ falha no WMI DP**</span><span class="sxs-lookup"><span data-stu-id="d746b-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERROR\_WMI\_DP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-215">4209 (0x1071)</span><span class="sxs-lookup"><span data-stu-id="d746b-215">4209 (0x1071)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-216">Falha do provedor de dados WMI ao executar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="d746b-216">The WMI data provider failed to carry out the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERRO \_ \_ MOF inválido do WMI \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERROR\_WMI\_INVALID\_MOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-218">4210 (0x1072)</span><span class="sxs-lookup"><span data-stu-id="d746b-218">4210 (0x1072)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-219">As informações do WMI MOF não são válidas.</span><span class="sxs-lookup"><span data-stu-id="d746b-219">The WMI MOF information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERRO \_ \_ REGINFO inválido do WMI \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERROR\_WMI\_INVALID\_REGINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-221">4211 (0x1073)</span><span class="sxs-lookup"><span data-stu-id="d746b-221">4211 (0x1073)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-222">As informações de registro do WMI não são válidas.</span><span class="sxs-lookup"><span data-stu-id="d746b-222">The WMI registration information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERRO o \_ WMI \_ já está \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="d746b-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERROR\_WMI\_ALREADY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-224">4212 (0x1074)</span><span class="sxs-lookup"><span data-stu-id="d746b-224">4212 (0x1074)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-225">A notificação de eventos ou o bloco de dados do WMI já foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d746b-225">The WMI data block or event notification has already been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERRO \_ \_ somente leitura do WMI \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERROR\_WMI\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-227">4213 (0x1075)</span><span class="sxs-lookup"><span data-stu-id="d746b-227">4213 (0x1075)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-228">O bloco de dados ou o item de dados WMI é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d746b-228">The WMI data item or data block is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERRO \_ ao \_ definir \_ falha do WMI**</span><span class="sxs-lookup"><span data-stu-id="d746b-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERROR\_WMI\_SET\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-230">4214 (0x1076)</span><span class="sxs-lookup"><span data-stu-id="d746b-230">4214 (0x1076)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-231">Não foi possível alterar o bloco de dados ou o item de dados WMI.</span><span class="sxs-lookup"><span data-stu-id="d746b-231">The WMI data item or data block could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERRO \_ não \_ APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="d746b-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERROR\_NOT\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-233">4250 (0x109A)</span><span class="sxs-lookup"><span data-stu-id="d746b-233">4250 (0x109A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-234">Esta operação só é válida no contexto de um contêiner de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d746b-234">This operation is only valid in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERRO de \_ APPCONTAINER \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="d746b-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERROR\_APPCONTAINER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-236">4251 (0x109B)</span><span class="sxs-lookup"><span data-stu-id="d746b-236">4251 (0x109B)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-237">Este aplicativo só pode ser executado no contexto de um contêiner de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d746b-237">This application can only run in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERRO \_ sem \_ suporte \_ no \_ APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="d746b-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERROR\_NOT\_SUPPORTED\_IN\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-239">4252 (0x109C)</span><span class="sxs-lookup"><span data-stu-id="d746b-239">4252 (0x109C)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-240">Não há suporte para essa funcionalidade no contexto de um contêiner de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d746b-240">This functionality is not supported in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERRO \_ de \_ \_ comprimento de Sid de pacote inválido \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERROR\_INVALID\_PACKAGE\_SID\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-242">4253 (0x109D)</span><span class="sxs-lookup"><span data-stu-id="d746b-242">4253 (0x109D)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-243">O comprimento do SID fornecido não é um comprimento válido para SIDs de contêiner de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d746b-243">The length of the SID supplied is not a valid length for app container SIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**\_mídia inválida de erro \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERROR\_INVALID\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-245">4300 (0x10CC)</span><span class="sxs-lookup"><span data-stu-id="d746b-245">4300 (0x10CC)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-246">O identificador de mídia não representa um meio válido.</span><span class="sxs-lookup"><span data-stu-id="d746b-246">The media identifier does not represent a valid medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERRO \_ de \_ biblioteca inválida**</span><span class="sxs-lookup"><span data-stu-id="d746b-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERROR\_INVALID\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-248">4301 (0x10CD)</span><span class="sxs-lookup"><span data-stu-id="d746b-248">4301 (0x10CD)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-249">O identificador de biblioteca não representa uma biblioteca válida.</span><span class="sxs-lookup"><span data-stu-id="d746b-249">The library identifier does not represent a valid library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERRO \_ de \_ pool de mídia inválido \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERROR\_INVALID\_MEDIA\_POOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-251">4302 (0x10CE)</span><span class="sxs-lookup"><span data-stu-id="d746b-251">4302 (0x10CE)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-252">O identificador do pool de mídias não representa um pool de mídia válido.</span><span class="sxs-lookup"><span data-stu-id="d746b-252">The media pool identifier does not represent a valid media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**incompatibilidade de mídia de unidade de erro \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**ERROR\_DRIVE\_MEDIA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-254">4303 (0x10CF)</span><span class="sxs-lookup"><span data-stu-id="d746b-254">4303 (0x10CF)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-255">A unidade e a mídia não são compatíveis ou existem em bibliotecas diferentes.</span><span class="sxs-lookup"><span data-stu-id="d746b-255">The drive and medium are not compatible or exist in different libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**mídia de erro \_ \_ offline**</span><span class="sxs-lookup"><span data-stu-id="d746b-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**ERROR\_MEDIA\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-257">4304 (0x10D0)</span><span class="sxs-lookup"><span data-stu-id="d746b-257">4304 (0x10D0)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-258">A mídia existe atualmente em uma biblioteca offline e deve estar online para executar esta operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-258">The medium currently exists in an offline library and must be online to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**biblioteca de erros \_ \_ offline**</span><span class="sxs-lookup"><span data-stu-id="d746b-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**ERROR\_LIBRARY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-260">4305 (0x10D1)</span><span class="sxs-lookup"><span data-stu-id="d746b-260">4305 (0x10D1)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-261">A operação não pode ser executada em uma biblioteca offline.</span><span class="sxs-lookup"><span data-stu-id="d746b-261">The operation cannot be performed on an offline library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERRO \_ vazio**</span><span class="sxs-lookup"><span data-stu-id="d746b-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERROR\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-263">4306 (0x10D2)</span><span class="sxs-lookup"><span data-stu-id="d746b-263">4306 (0x10D2)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-264">A biblioteca, a unidade ou o pool de mídia está vazio.</span><span class="sxs-lookup"><span data-stu-id="d746b-264">The library, drive, or media pool is empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERRO \_ não \_ vazio**</span><span class="sxs-lookup"><span data-stu-id="d746b-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERROR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-266">4307 (0x10D3)</span><span class="sxs-lookup"><span data-stu-id="d746b-266">4307 (0x10D3)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-267">A biblioteca, a unidade ou o pool de mídias devem estar vazios para executar esta operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-267">The library, drive, or media pool must be empty to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**mídia de erro \_ \_ indisponível**</span><span class="sxs-lookup"><span data-stu-id="d746b-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**ERROR\_MEDIA\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-269">4308 (0x10D4)</span><span class="sxs-lookup"><span data-stu-id="d746b-269">4308 (0x10D4)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-270">Não há mídia disponível no momento neste pool de mídias ou biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d746b-270">No media is currently available in this media pool or library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**recurso de erro \_ \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="d746b-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**ERROR\_RESOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-272">4309 (0x10D5)</span><span class="sxs-lookup"><span data-stu-id="d746b-272">4309 (0x10D5)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-273">Um recurso necessário para esta operação está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d746b-273">A resource required for this operation is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERRO \_ de \_ limpeza inválida**</span><span class="sxs-lookup"><span data-stu-id="d746b-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERROR\_INVALID\_CLEANER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-275">4310 (0x10D6)</span><span class="sxs-lookup"><span data-stu-id="d746b-275">4310 (0x10D6)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-276">O identificador de mídia não representa um limpador válido.</span><span class="sxs-lookup"><span data-stu-id="d746b-276">The media identifier does not represent a valid cleaner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERRO \_ não é possível \_ \_ limpar**</span><span class="sxs-lookup"><span data-stu-id="d746b-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERROR\_UNABLE\_TO\_CLEAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-278">4311 (0x10D7)</span><span class="sxs-lookup"><span data-stu-id="d746b-278">4311 (0x10D7)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-279">A unidade não pode ser limpa ou não dá suporte à limpeza.</span><span class="sxs-lookup"><span data-stu-id="d746b-279">The drive cannot be cleaned or does not support cleaning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**objeto de erro \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**ERROR\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-281">4312 (0x10D8)</span><span class="sxs-lookup"><span data-stu-id="d746b-281">4312 (0x10D8)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-282">O identificador de objeto não representa um objeto válido.</span><span class="sxs-lookup"><span data-stu-id="d746b-282">The object identifier does not represent a valid object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**\_falha no banco de dados de erro \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**ERROR\_DATABASE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-284">4313 (0x10D9)</span><span class="sxs-lookup"><span data-stu-id="d746b-284">4313 (0x10D9)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-285">Não é possível ler ou gravar no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d746b-285">Unable to read from or write to the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**ERRO de \_ banco de dados \_ cheio**</span><span class="sxs-lookup"><span data-stu-id="d746b-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**ERROR\_DATABASE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-287">4314 (0x10DA)</span><span class="sxs-lookup"><span data-stu-id="d746b-287">4314 (0x10DA)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-288">O banco de dados está cheio.</span><span class="sxs-lookup"><span data-stu-id="d746b-288">The database is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**mídia de erro \_ \_ incompatível**</span><span class="sxs-lookup"><span data-stu-id="d746b-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**ERROR\_MEDIA\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-290">4315 (0x10DB)</span><span class="sxs-lookup"><span data-stu-id="d746b-290">4315 (0x10DB)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-291">A mídia não é compatível com o dispositivo ou com o pool de mídias.</span><span class="sxs-lookup"><span data-stu-id="d746b-291">The medium is not compatible with the device or media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**o \_ recurso de erro \_ não \_ está presente**</span><span class="sxs-lookup"><span data-stu-id="d746b-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**ERROR\_RESOURCE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-293">4316 (0x10DC)</span><span class="sxs-lookup"><span data-stu-id="d746b-293">4316 (0x10DC)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-294">O recurso necessário para esta operação não existe.</span><span class="sxs-lookup"><span data-stu-id="d746b-294">The resource required for this operation does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERRO \_ de \_ operação inválida**</span><span class="sxs-lookup"><span data-stu-id="d746b-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERROR\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-296">4317 (0x10DD)</span><span class="sxs-lookup"><span data-stu-id="d746b-296">4317 (0x10DD)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-297">O identificador de operação não é válido.</span><span class="sxs-lookup"><span data-stu-id="d746b-297">The operation identifier is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**mídia de erro \_ \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="d746b-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**ERROR\_MEDIA\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-299">4318 (0x10DE)</span><span class="sxs-lookup"><span data-stu-id="d746b-299">4318 (0x10DE)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-300">A mídia não está montada ou pronta para uso.</span><span class="sxs-lookup"><span data-stu-id="d746b-300">The media is not mounted or ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**dispositivo de erro \_ \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="d746b-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**ERROR\_DEVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-302">4319 (0x10DF)</span><span class="sxs-lookup"><span data-stu-id="d746b-302">4319 (0x10DF)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-303">O dispositivo não está pronto para uso.</span><span class="sxs-lookup"><span data-stu-id="d746b-303">The device is not ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**solicitação de erro \_ \_ recusada**</span><span class="sxs-lookup"><span data-stu-id="d746b-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**ERROR\_REQUEST\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-305">4320 (0x10E0)</span><span class="sxs-lookup"><span data-stu-id="d746b-305">4320 (0x10E0)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-306">O operador ou o administrador recusou a solicitação.</span><span class="sxs-lookup"><span data-stu-id="d746b-306">The operator or administrator has refused the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERRO \_ de \_ objeto de unidade inválido \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERROR\_INVALID\_DRIVE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-308">4321 (0x10E1)</span><span class="sxs-lookup"><span data-stu-id="d746b-308">4321 (0x10E1)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-309">O identificador da unidade não representa uma unidade válida.</span><span class="sxs-lookup"><span data-stu-id="d746b-309">The drive identifier does not represent a valid drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**biblioteca de erros \_ \_ completa**</span><span class="sxs-lookup"><span data-stu-id="d746b-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**ERROR\_LIBRARY\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-311">4322 (0x10E2)</span><span class="sxs-lookup"><span data-stu-id="d746b-311">4322 (0x10E2)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-312">A biblioteca está cheia.</span><span class="sxs-lookup"><span data-stu-id="d746b-312">Library is full.</span></span> <span data-ttu-id="d746b-313">Nenhum slot está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="d746b-313">No slot is available for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**ERRO \_ médio \_ não \_ acessível**</span><span class="sxs-lookup"><span data-stu-id="d746b-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**ERROR\_MEDIUM\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-315">4323 (0x10E3)</span><span class="sxs-lookup"><span data-stu-id="d746b-315">4323 (0x10E3)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-316">O transporte não pode acessar a mídia.</span><span class="sxs-lookup"><span data-stu-id="d746b-316">The transport cannot access the medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERRO \_ não é possível \_ \_ carregar \_ médio**</span><span class="sxs-lookup"><span data-stu-id="d746b-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERROR\_UNABLE\_TO\_LOAD\_MEDIUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-318">4324 (0x10E4)</span><span class="sxs-lookup"><span data-stu-id="d746b-318">4324 (0x10E4)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-319">Não é possível carregar a mídia na unidade.</span><span class="sxs-lookup"><span data-stu-id="d746b-319">Unable to load the medium into the drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERRO \_ não é possível \_ \_ inventariar a \_ unidade**</span><span class="sxs-lookup"><span data-stu-id="d746b-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-321">4325 (0x10E5)</span><span class="sxs-lookup"><span data-stu-id="d746b-321">4325 (0x10E5)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-322">Não é possível recuperar o status da unidade.</span><span class="sxs-lookup"><span data-stu-id="d746b-322">Unable to retrieve the drive status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERRO \_ não é possível \_ \_ inventariar o \_ slot**</span><span class="sxs-lookup"><span data-stu-id="d746b-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_SLOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-324">4326 (0x10E6)</span><span class="sxs-lookup"><span data-stu-id="d746b-324">4326 (0x10E6)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-325">Não é possível recuperar o status do slot.</span><span class="sxs-lookup"><span data-stu-id="d746b-325">Unable to retrieve the slot status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERRO \_ não é possível \_ \_ inventariar o \_ transporte**</span><span class="sxs-lookup"><span data-stu-id="d746b-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_TRANSPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-327">4327 (0x10E7)</span><span class="sxs-lookup"><span data-stu-id="d746b-327">4327 (0x10E7)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-328">Não é possível recuperar o status do transporte.</span><span class="sxs-lookup"><span data-stu-id="d746b-328">Unable to retrieve status about the transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**transporte de erro \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="d746b-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**ERROR\_TRANSPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-330">4328 (0x10E8)</span><span class="sxs-lookup"><span data-stu-id="d746b-330">4328 (0x10E8)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-331">Não é possível usar o transporte porque ele já está em uso.</span><span class="sxs-lookup"><span data-stu-id="d746b-331">Cannot use the transport because it is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERRO ao \_ controlar \_ IEPORT**</span><span class="sxs-lookup"><span data-stu-id="d746b-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERROR\_CONTROLLING\_IEPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-333">4329 (0x10E9)</span><span class="sxs-lookup"><span data-stu-id="d746b-333">4329 (0x10E9)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-334">Não é possível abrir ou fechar a porta de inserção/ejeção.</span><span class="sxs-lookup"><span data-stu-id="d746b-334">Unable to open or close the inject/eject port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERRO \_ não é possível \_ \_ ejetar \_ mídia montada \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERROR\_UNABLE\_TO\_EJECT\_MOUNTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-336">4330 (0x10EA)</span><span class="sxs-lookup"><span data-stu-id="d746b-336">4330 (0x10EA)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-337">Não é possível ejetar a mídia porque ela está em uma unidade.</span><span class="sxs-lookup"><span data-stu-id="d746b-337">Unable to eject the medium because it is in a drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**\_conjunto de slots do limpador de erros \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**ERROR\_CLEANER\_SLOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-339">4331 (0x10EB)</span><span class="sxs-lookup"><span data-stu-id="d746b-339">4331 (0x10EB)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-340">Um slot de limpeza já está reservado.</span><span class="sxs-lookup"><span data-stu-id="d746b-340">A cleaner slot is already reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**ERRO \_ de \_ slot de limpeza \_ não \_ definido**</span><span class="sxs-lookup"><span data-stu-id="d746b-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**ERROR\_CLEANER\_SLOT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-342">4332 (0x10EC)</span><span class="sxs-lookup"><span data-stu-id="d746b-342">4332 (0x10EC)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-343">Um slot de limpeza não está reservado.</span><span class="sxs-lookup"><span data-stu-id="d746b-343">A cleaner slot is not reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**cartucho de limpeza de erro \_ \_ \_ gasto**</span><span class="sxs-lookup"><span data-stu-id="d746b-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**ERROR\_CLEANER\_CARTRIDGE\_SPENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-345">4333 (0x10ED)</span><span class="sxs-lookup"><span data-stu-id="d746b-345">4333 (0x10ED)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-346">O cartucho de limpeza realizou o número máximo de limpezas de unidade.</span><span class="sxs-lookup"><span data-stu-id="d746b-346">The cleaner cartridge has performed the maximum number of drive cleanings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERRO \_ inesperado \_ Omid**</span><span class="sxs-lookup"><span data-stu-id="d746b-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERROR\_UNEXPECTED\_OMID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-348">4334 (0x10EE)</span><span class="sxs-lookup"><span data-stu-id="d746b-348">4334 (0x10EE)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-349">Identificador em-média inesperado.</span><span class="sxs-lookup"><span data-stu-id="d746b-349">Unexpected on-medium identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERRO não é possível \_ \_ excluir o \_ último \_ Item**</span><span class="sxs-lookup"><span data-stu-id="d746b-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERROR\_CANT\_DELETE\_LAST\_ITEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-351">4335 (0x10EF)</span><span class="sxs-lookup"><span data-stu-id="d746b-351">4335 (0x10EF)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-352">O último item restante neste grupo ou recurso não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d746b-352">The last remaining item in this group or resource cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**a \_ mensagem de erro \_ excede o \_ \_ tamanho máximo**</span><span class="sxs-lookup"><span data-stu-id="d746b-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**ERROR\_MESSAGE\_EXCEEDS\_MAX\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-354">4336 (0x10F0)</span><span class="sxs-lookup"><span data-stu-id="d746b-354">4336 (0x10F0)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-355">A mensagem fornecida excede o tamanho máximo permitido para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d746b-355">The message provided exceeds the maximum size allowed for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**o \_ volume de erros \_ contém \_ \_ arquivos sys**</span><span class="sxs-lookup"><span data-stu-id="d746b-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**ERROR\_VOLUME\_CONTAINS\_SYS\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-357">4337 (0x10F1)</span><span class="sxs-lookup"><span data-stu-id="d746b-357">4337 (0x10F1)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-358">O volume contém arquivos de sistema ou de paginação.</span><span class="sxs-lookup"><span data-stu-id="d746b-358">The volume contains system or paging files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**\_tipo de nativos de erro \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**ERROR\_INDIGENOUS\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-360">4338 (0x10F2)</span><span class="sxs-lookup"><span data-stu-id="d746b-360">4338 (0x10F2)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-361">O tipo de mídia não pode ser removido desta biblioteca, pois pelo menos uma unidade na biblioteca relata que pode dar suporte a esse tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d746b-361">The media type cannot be removed from this library since at least one drive in the library reports it can support this media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERRO \_ sem \_ unidades de suporte \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERROR\_NO\_SUPPORTING\_DRIVES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-363">4339 (0x10F3)</span><span class="sxs-lookup"><span data-stu-id="d746b-363">4339 (0x10F3)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-364">Esta mídia offline não pode ser montada neste sistema porque não há unidades habilitadas presentes que possam ser usadas.</span><span class="sxs-lookup"><span data-stu-id="d746b-364">This offline media cannot be mounted on this system since no enabled drives are present which can be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**cartucho de limpeza de erro \_ \_ \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="d746b-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**ERROR\_CLEANER\_CARTRIDGE\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-366">4340 (0x10F4)</span><span class="sxs-lookup"><span data-stu-id="d746b-366">4340 (0x10F4)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-367">Um cartucho de limpeza está presente na biblioteca de fitas.</span><span class="sxs-lookup"><span data-stu-id="d746b-367">A cleaner cartridge is present in the tape library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERRO \_ IEPORT \_ completo**</span><span class="sxs-lookup"><span data-stu-id="d746b-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERROR\_IEPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-369">4341 (0x10F5)</span><span class="sxs-lookup"><span data-stu-id="d746b-369">4341 (0x10F5)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-370">Não é possível usar a porta de inserção/ejeção porque ela não está vazia.</span><span class="sxs-lookup"><span data-stu-id="d746b-370">Cannot use the inject/eject port because it is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**arquivo de erro \_ \_ offline**</span><span class="sxs-lookup"><span data-stu-id="d746b-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**ERROR\_FILE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-372">4350 (0x10FE)</span><span class="sxs-lookup"><span data-stu-id="d746b-372">4350 (0x10FE)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-373">Este arquivo não está disponível no momento para uso neste computador.</span><span class="sxs-lookup"><span data-stu-id="d746b-373">This file is currently not available for use on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERRO \_ o \_ Armazenamento remoto \_ não está \_ ativo**</span><span class="sxs-lookup"><span data-stu-id="d746b-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERROR\_REMOTE\_STORAGE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-375">4351 (0x10FF)</span><span class="sxs-lookup"><span data-stu-id="d746b-375">4351 (0x10FF)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-376">O serviço de armazenamento remoto não está operacional no momento.</span><span class="sxs-lookup"><span data-stu-id="d746b-376">The remote storage service is not operational at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**ERRO \_ de \_ mídia de armazenamento remoto \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**ERROR\_REMOTE\_STORAGE\_MEDIA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-378">4352 (0x1100)</span><span class="sxs-lookup"><span data-stu-id="d746b-378">4352 (0x1100)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-379">O serviço de armazenamento remoto encontrou um erro de mídia.</span><span class="sxs-lookup"><span data-stu-id="d746b-379">The remote storage service encountered a media error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERRO \_ não é \_ um ponto de \_ nova análise \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERROR\_NOT\_A\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-381">4390 (0x1126)</span><span class="sxs-lookup"><span data-stu-id="d746b-381">4390 (0x1126)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-382">O arquivo ou diretório não é um ponto de nova análise.</span><span class="sxs-lookup"><span data-stu-id="d746b-382">The file or directory is not a reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERRO ao \_ analisar \_ conflito de atributo \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-384">4391 (0x1127)</span><span class="sxs-lookup"><span data-stu-id="d746b-384">4391 (0x1127)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-385">O atributo de ponto de nova análise não pode ser definido porque está em conflito com um atributo existente.</span><span class="sxs-lookup"><span data-stu-id="d746b-385">The reparse point attribute cannot be set because it conflicts with an existing attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERRO \_ de \_ dados de nova análise inválidos \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERROR\_INVALID\_REPARSE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-387">4392 (0x1128)</span><span class="sxs-lookup"><span data-stu-id="d746b-387">4392 (0x1128)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-388">Os dados presentes no buffer de ponto de nova análise são inválidos.</span><span class="sxs-lookup"><span data-stu-id="d746b-388">The data present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERRO na \_ marca de nova análise \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="d746b-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERROR\_REPARSE\_TAG\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-390">4393 (0x1129)</span><span class="sxs-lookup"><span data-stu-id="d746b-390">4393 (0x1129)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-391">A marca presente no buffer do ponto de nova análise é inválida.</span><span class="sxs-lookup"><span data-stu-id="d746b-391">The tag present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERRO de \_ \_ incompatibilidade de marca de nova análise \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERROR\_REPARSE\_TAG\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-393">4394 (0x112A)</span><span class="sxs-lookup"><span data-stu-id="d746b-393">4394 (0x112A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-394">Há uma incompatibilidade entre a marca especificada na solicitação e a marca presentes no ponto de nova análise.</span><span class="sxs-lookup"><span data-stu-id="d746b-394">There is a mismatch between the tag specified in the request and the tag present in the reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**dados do aplicativo de erro \_ \_ \_ não \_ encontrados**</span><span class="sxs-lookup"><span data-stu-id="d746b-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**ERROR\_APP\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-396">4400 (0x1130)</span><span class="sxs-lookup"><span data-stu-id="d746b-396">4400 (0x1130)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-397">Dados de cache rápidos não encontrados.</span><span class="sxs-lookup"><span data-stu-id="d746b-397">Fast Cache data not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERRO \_ dados do aplicativo \_ \_ expirados**</span><span class="sxs-lookup"><span data-stu-id="d746b-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERROR\_APP\_DATA\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-399">4401 (0x1131)</span><span class="sxs-lookup"><span data-stu-id="d746b-399">4401 (0x1131)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-400">Dados de cache rápido expirados.</span><span class="sxs-lookup"><span data-stu-id="d746b-400">Fast Cache data expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**dados do aplicativo de erro \_ \_ \_ corrompidos**</span><span class="sxs-lookup"><span data-stu-id="d746b-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ERROR\_APP\_DATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-402">4402 (0x1132)</span><span class="sxs-lookup"><span data-stu-id="d746b-402">4402 (0x1132)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-403">Dados de cache rápidos corrompidos.</span><span class="sxs-lookup"><span data-stu-id="d746b-403">Fast Cache data corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**limite de dados de aplicativo de erro \_ \_ \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="d746b-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**ERROR\_APP\_DATA\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-405">4403 (0x1133)</span><span class="sxs-lookup"><span data-stu-id="d746b-405">4403 (0x1133)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-406">Os dados de cache rápido excederam seu tamanho máximo e não podem ser atualizados.</span><span class="sxs-lookup"><span data-stu-id="d746b-406">Fast Cache data has exceeded its max size and cannot be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERRO \_ ao \_ \_ reinicializar dados do aplicativo \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="d746b-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERROR\_APP\_DATA\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-408">4404 (0x1134)</span><span class="sxs-lookup"><span data-stu-id="d746b-408">4404 (0x1134)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-409">O cache rápido foi rearmado e requer uma reinicialização até que possa ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="d746b-409">Fast Cache has been ReArmed and requires a reboot until it can be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**reversão de SECUREBOOT de erro \_ \_ \_ detectada**</span><span class="sxs-lookup"><span data-stu-id="d746b-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERROR\_SECUREBOOT\_ROLLBACK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-411">4420 (0x1144)</span><span class="sxs-lookup"><span data-stu-id="d746b-411">4420 (0x1144)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-412">A inicialização segura detectou que a reversão de dados protegidos foi tentada.</span><span class="sxs-lookup"><span data-stu-id="d746b-412">Secure Boot detected that rollback of protected data has been attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERRO \_ de \_ violação de política de SECUREBOOT \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERROR\_SECUREBOOT\_POLICY\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-414">4421 (0x1145)</span><span class="sxs-lookup"><span data-stu-id="d746b-414">4421 (0x1145)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-415">O valor é protegido pela política de inicialização segura e não pode ser modificado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="d746b-415">The value is protected by Secure Boot policy and cannot be modified or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERRO ao \_ SECUREBOOT da \_ política inválida \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERROR\_SECUREBOOT\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-417">4422 (0x1146)</span><span class="sxs-lookup"><span data-stu-id="d746b-417">4422 (0x1146)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-418">A política de inicialização segura é inválida.</span><span class="sxs-lookup"><span data-stu-id="d746b-418">The Secure Boot policy is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**Editor de política de SECUREBOOT de erro \_ \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERROR\_SECUREBOOT\_POLICY\_PUBLISHER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-420">4423 (0x1147)</span><span class="sxs-lookup"><span data-stu-id="d746b-420">4423 (0x1147)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-421">Uma nova política de inicialização segura não continha o Publicador atual em sua lista de atualizações.</span><span class="sxs-lookup"><span data-stu-id="d746b-421">A new Secure Boot policy did not contain the current publisher on its update list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**política de SECUREBOOT de erro \_ \_ \_ não \_ assinada**</span><span class="sxs-lookup"><span data-stu-id="d746b-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERROR\_SECUREBOOT\_POLICY\_NOT\_SIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-423">4424 (0x1148)</span><span class="sxs-lookup"><span data-stu-id="d746b-423">4424 (0x1148)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-424">A política de inicialização segura não está assinada ou assinada por um assinante não confiável.</span><span class="sxs-lookup"><span data-stu-id="d746b-424">The Secure Boot policy is either not signed or is signed by a non-trusted signer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERRO \_ SECUREBOOT \_ não \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="d746b-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERROR\_SECUREBOOT\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-426">4425 (0x1149)</span><span class="sxs-lookup"><span data-stu-id="d746b-426">4425 (0x1149)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-427">A inicialização segura não está habilitada neste computador.</span><span class="sxs-lookup"><span data-stu-id="d746b-427">Secure Boot is not enabled on this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERRO \_ do \_ arquivo SECUREBOOT \_ substituído**</span><span class="sxs-lookup"><span data-stu-id="d746b-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERROR\_SECUREBOOT\_FILE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-429">4426 (0x114A)</span><span class="sxs-lookup"><span data-stu-id="d746b-429">4426 (0x114A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-430">A inicialização segura exige que determinados arquivos e drivers não sejam substituídos por outros arquivos ou drivers.</span><span class="sxs-lookup"><span data-stu-id="d746b-430">Secure Boot requires that certain files and drivers are not replaced by other files or drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**descarregamento de erro de \_ \_ leitura \_ FLT \_ não \_ suportado**</span><span class="sxs-lookup"><span data-stu-id="d746b-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-432">4440 (0x1158)</span><span class="sxs-lookup"><span data-stu-id="d746b-432">4440 (0x1158)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-433">A operação de leitura de descarregamento de cópia não é suportada por um filtro.</span><span class="sxs-lookup"><span data-stu-id="d746b-433">The copy offload read operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**descarregamento de erro de \_ \_ gravação \_ FLT \_ não \_ suportado**</span><span class="sxs-lookup"><span data-stu-id="d746b-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-435">4441 (0x1159)</span><span class="sxs-lookup"><span data-stu-id="d746b-435">4441 (0x1159)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-436">A operação de gravação de descarregamento de cópia não é suportada por um filtro.</span><span class="sxs-lookup"><span data-stu-id="d746b-436">The copy offload write operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERRO de \_ descarregamento de \_ \_ arquivo lido \_ não \_ suportado**</span><span class="sxs-lookup"><span data-stu-id="d746b-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-438">4442 (0x115A)</span><span class="sxs-lookup"><span data-stu-id="d746b-438">4442 (0x115A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-439">A operação de leitura de descarregamento de cópia não tem suporte para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d746b-439">The copy offload read operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**\_arquivo de gravação de descarregamento de erro \_ \_ \_ não \_ suportado**</span><span class="sxs-lookup"><span data-stu-id="d746b-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-441">4443 (0x115B)</span><span class="sxs-lookup"><span data-stu-id="d746b-441">4443 (0x115B)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-442">A operação de gravação de descarregamento de cópia não tem suporte para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d746b-442">The copy offload write operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**VOLUME de erro \_ \_ não \_ habilitado para SIS \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**ERROR\_VOLUME\_NOT\_SIS\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-444">4500 (0x1194)</span><span class="sxs-lookup"><span data-stu-id="d746b-444">4500 (0x1194)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-445">O armazenamento de instância única não está disponível neste volume.</span><span class="sxs-lookup"><span data-stu-id="d746b-445">Single Instance Storage is not available on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**\_existe um \_ recurso \_ dependente de erro**</span><span class="sxs-lookup"><span data-stu-id="d746b-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**ERROR\_DEPENDENT\_RESOURCE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-447">5001 (0x1389)</span><span class="sxs-lookup"><span data-stu-id="d746b-447">5001 (0x1389)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-448">A operação não pode ser concluída porque outros recursos dependem desse recurso.</span><span class="sxs-lookup"><span data-stu-id="d746b-448">The operation cannot be completed because other resources are dependent on this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**dependência de erro \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="d746b-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**ERROR\_DEPENDENCY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-450">5002 (0x138A)</span><span class="sxs-lookup"><span data-stu-id="d746b-450">5002 (0x138A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-451">Não é possível encontrar a dependência de recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-451">The cluster resource dependency cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**a \_ dependência de erro \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d746b-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**ERROR\_DEPENDENCY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-453">5003 (0x138B)</span><span class="sxs-lookup"><span data-stu-id="d746b-453">5003 (0x138B)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-454">Não é possível tornar o recurso de cluster dependente do recurso especificado porque ele já é dependente.</span><span class="sxs-lookup"><span data-stu-id="d746b-454">The cluster resource cannot be made dependent on the specified resource because it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**recurso de erro \_ \_ não \_ online**</span><span class="sxs-lookup"><span data-stu-id="d746b-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**ERROR\_RESOURCE\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-456">5004 (0x138C)</span><span class="sxs-lookup"><span data-stu-id="d746b-456">5004 (0x138C)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-457">O recurso de cluster não está online.</span><span class="sxs-lookup"><span data-stu-id="d746b-457">The cluster resource is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**nó de host de erro \_ \_ \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="d746b-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**ERROR\_HOST\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-459">5005 (0x138D)</span><span class="sxs-lookup"><span data-stu-id="d746b-459">5005 (0x138D)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-460">Um nó de cluster não está disponível para esta operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-460">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**recurso de erro \_ \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="d746b-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**ERROR\_RESOURCE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-462">5006 (0x138E)</span><span class="sxs-lookup"><span data-stu-id="d746b-462">5006 (0x138E)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-463">O recurso de cluster não está disponível.</span><span class="sxs-lookup"><span data-stu-id="d746b-463">The cluster resource is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**recurso de erro \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**ERROR\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-465">5007 (0x138F)</span><span class="sxs-lookup"><span data-stu-id="d746b-465">5007 (0x138F)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-466">Não foi possível encontrar o recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-466">The cluster resource could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERRO ao \_ desligar o \_ cluster**</span><span class="sxs-lookup"><span data-stu-id="d746b-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERROR\_SHUTDOWN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-468">5008 (0x1390)</span><span class="sxs-lookup"><span data-stu-id="d746b-468">5008 (0x1390)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-469">O cluster está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="d746b-469">The cluster is being shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERRO não é possível \_ \_ remover o \_ \_ nó ativo**</span><span class="sxs-lookup"><span data-stu-id="d746b-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERROR\_CANT\_EVICT\_ACTIVE\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-471">5009 (0x1391)</span><span class="sxs-lookup"><span data-stu-id="d746b-471">5009 (0x1391)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-472">Um nó de cluster não pode ser removido do cluster, a menos que o nó esteja inoperante ou seja o último nó.</span><span class="sxs-lookup"><span data-stu-id="d746b-472">A cluster node cannot be evicted from the cluster unless the node is down or it is the last node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**o \_ objeto de erro \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d746b-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**ERROR\_OBJECT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-474">5010 (0x1392)</span><span class="sxs-lookup"><span data-stu-id="d746b-474">5010 (0x1392)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-475">O objeto já existe.</span><span class="sxs-lookup"><span data-stu-id="d746b-475">The object already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**\_objeto \_ de erro na \_ lista**</span><span class="sxs-lookup"><span data-stu-id="d746b-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**ERROR\_OBJECT\_IN\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-477">5011 (0x1393)</span><span class="sxs-lookup"><span data-stu-id="d746b-477">5011 (0x1393)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-478">O objeto já está na lista.</span><span class="sxs-lookup"><span data-stu-id="d746b-478">The object is already in the list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**grupo de erros \_ \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="d746b-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**ERROR\_GROUP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-480">5012 (0x1394)</span><span class="sxs-lookup"><span data-stu-id="d746b-480">5012 (0x1394)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-481">O grupo de clusters não está disponível para novas solicitações.</span><span class="sxs-lookup"><span data-stu-id="d746b-481">The cluster group is not available for any new requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**grupo de erros \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**ERROR\_GROUP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-483">5013 (0x1395)</span><span class="sxs-lookup"><span data-stu-id="d746b-483">5013 (0x1395)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-484">O grupo de clusters não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="d746b-484">The cluster group could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**grupo de erros \_ \_ não \_ online**</span><span class="sxs-lookup"><span data-stu-id="d746b-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**ERROR\_GROUP\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-486">5014 (0x1396)</span><span class="sxs-lookup"><span data-stu-id="d746b-486">5014 (0x1396)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-487">A operação não pôde ser concluída porque o grupo de clusters não está online.</span><span class="sxs-lookup"><span data-stu-id="d746b-487">The operation could not be completed because the cluster group is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERRO \_ nó de host \_ \_ não \_ proprietário do recurso \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERROR\_HOST\_NODE\_NOT\_RESOURCE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-489">5015 (0x1397)</span><span class="sxs-lookup"><span data-stu-id="d746b-489">5015 (0x1397)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-490">A operação falhou porque o nó de cluster especificado não é o proprietário do recurso ou o nó não é um possível proprietário do recurso.</span><span class="sxs-lookup"><span data-stu-id="d746b-490">The operation failed because either the specified cluster node is not the owner of the resource, or the node is not a possible owner of the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERRO \_ de \_ nó de host \_ não \_ proprietário do grupo \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERROR\_HOST\_NODE\_NOT\_GROUP\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-492">5016 (0x1398)</span><span class="sxs-lookup"><span data-stu-id="d746b-492">5016 (0x1398)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-493">A operação falhou porque o nó do cluster especificado não é o proprietário do grupo ou o nó não é um possível proprietário do grupo.</span><span class="sxs-lookup"><span data-stu-id="d746b-493">The operation failed because either the specified cluster node is not the owner of the group, or the node is not a possible owner of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERRO \_ \_ ao criar \_ resmon**</span><span class="sxs-lookup"><span data-stu-id="d746b-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERROR\_RESMON\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-495">5017 (0x1399)</span><span class="sxs-lookup"><span data-stu-id="d746b-495">5017 (0x1399)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-496">Não foi possível criar o recurso de cluster no monitor de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="d746b-496">The cluster resource could not be created in the specified resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERRO \_ resmon \_ online \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="d746b-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERROR\_RESMON\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-498">5018 (0x139A)</span><span class="sxs-lookup"><span data-stu-id="d746b-498">5018 (0x139A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-499">O recurso de cluster não pôde ser colocado online pelo monitor de recursos.</span><span class="sxs-lookup"><span data-stu-id="d746b-499">The cluster resource could not be brought online by the resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**recurso de erro \_ \_ online**</span><span class="sxs-lookup"><span data-stu-id="d746b-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**ERROR\_RESOURCE\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-501">5019 (0x139B)</span><span class="sxs-lookup"><span data-stu-id="d746b-501">5019 (0x139B)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-502">A operação não pôde ser concluída porque o recurso de cluster está online.</span><span class="sxs-lookup"><span data-stu-id="d746b-502">The operation could not be completed because the cluster resource is online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**\_recurso de quorum de erro \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**ERROR\_QUORUM\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-504">5020 (0x139C)</span><span class="sxs-lookup"><span data-stu-id="d746b-504">5020 (0x139C)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-505">O recurso de cluster não pôde ser excluído ou colocado offline porque é o recurso de quorum.</span><span class="sxs-lookup"><span data-stu-id="d746b-505">The cluster resource could not be deleted or brought offline because it is the quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERRO \_ não \_ \_ compatível com quorum**</span><span class="sxs-lookup"><span data-stu-id="d746b-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERROR\_NOT\_QUORUM\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-507">5021 (0x139D)</span><span class="sxs-lookup"><span data-stu-id="d746b-507">5021 (0x139D)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-508">O cluster não pôde tornar o recurso especificado um recurso de quorum porque ele não é capaz de ser um recurso de quorum.</span><span class="sxs-lookup"><span data-stu-id="d746b-508">The cluster could not make the specified resource a quorum resource because it is not capable of being a quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERRO \_ ao \_ desligar o cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERROR\_CLUSTER\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-510">5022 (0x139E)</span><span class="sxs-lookup"><span data-stu-id="d746b-510">5022 (0x139E)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-511">O software do cluster está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="d746b-511">The cluster software is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**\_estado inválido do erro \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**ERROR\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-513">5023 (0x139F)</span><span class="sxs-lookup"><span data-stu-id="d746b-513">5023 (0x139F)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-514">O grupo ou recurso não está no estado correto para executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="d746b-514">The group or resource is not in the correct state to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**Propriedades do recurso de erro \_ \_ \_ armazenadas**</span><span class="sxs-lookup"><span data-stu-id="d746b-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**ERROR\_RESOURCE\_PROPERTIES\_STORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-516">5024 (0x13A0)</span><span class="sxs-lookup"><span data-stu-id="d746b-516">5024 (0x13A0)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-517">As propriedades foram armazenadas, mas nem todas as alterações entrarão em vigor até a próxima vez que o recurso for colocado online.</span><span class="sxs-lookup"><span data-stu-id="d746b-517">The properties were stored but not all changes will take effect until the next time the resource is brought online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERRO \_ não \_ classe de quorum \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERROR\_NOT\_QUORUM\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-519">5025 (0x13A1)</span><span class="sxs-lookup"><span data-stu-id="d746b-519">5025 (0x13A1)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-520">O cluster não pôde tornar o recurso especificado um recurso de quorum porque ele não pertence a uma classe de armazenamento compartilhada.</span><span class="sxs-lookup"><span data-stu-id="d746b-520">The cluster could not make the specified resource a quorum resource because it does not belong to a shared storage class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**\_recurso de núcleo de erro \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**ERROR\_CORE\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-522">5026 (0x13A2)</span><span class="sxs-lookup"><span data-stu-id="d746b-522">5026 (0x13A2)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-523">Não foi possível excluir o recurso de cluster porque ele é um recurso principal.</span><span class="sxs-lookup"><span data-stu-id="d746b-523">The cluster resource could not be deleted since it is a core resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERRO \_ \_ falha no recurso de quorum \_ online \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERROR\_QUORUM\_RESOURCE\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-525">5027 (0x13A3)</span><span class="sxs-lookup"><span data-stu-id="d746b-525">5027 (0x13A3)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-526">O recurso de quorum não pôde ser colocado online.</span><span class="sxs-lookup"><span data-stu-id="d746b-526">The quorum resource failed to come online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERRO \_ QUORUMLOG \_ \_ falha ao abrir**</span><span class="sxs-lookup"><span data-stu-id="d746b-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERROR\_QUORUMLOG\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-528">5028 (0x13A4)</span><span class="sxs-lookup"><span data-stu-id="d746b-528">5028 (0x13A4)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-529">Não foi possível criar ou montar o log de quorum com êxito.</span><span class="sxs-lookup"><span data-stu-id="d746b-529">The quorum log could not be created or mounted successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERRO \_ CLUSTERLOG \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="d746b-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERROR\_CLUSTERLOG\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-531">5029 (0x13A5)</span><span class="sxs-lookup"><span data-stu-id="d746b-531">5029 (0x13A5)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-532">O log do cluster está corrompido.</span><span class="sxs-lookup"><span data-stu-id="d746b-532">The cluster log is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**o \_ registro CLUSTERLOG de erro \_ \_ excede \_ MaxSize**</span><span class="sxs-lookup"><span data-stu-id="d746b-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_RECORD\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-534">5030 (0x13A6)</span><span class="sxs-lookup"><span data-stu-id="d746b-534">5030 (0x13A6)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-535">Não foi possível gravar o registro no log do cluster, pois ele excede o tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="d746b-535">The record could not be written to the cluster log since it exceeds the maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**o erro \_ CLUSTERLOG \_ excede \_ MaxSize**</span><span class="sxs-lookup"><span data-stu-id="d746b-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-537">5031 (0x13A7)</span><span class="sxs-lookup"><span data-stu-id="d746b-537">5031 (0x13A7)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-538">O log do cluster excede seu tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="d746b-538">The cluster log exceeds its maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERRO \_ CLUSTERLOG \_ CHKPOINT \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERROR\_CLUSTERLOG\_CHKPOINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-540">5032 (0x13A8)</span><span class="sxs-lookup"><span data-stu-id="d746b-540">5032 (0x13A8)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-541">Nenhum registro de ponto de verificação foi encontrado no log do cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-541">No checkpoint record was found in the cluster log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERRO \_ CLUSTERLOG \_ não \_ há \_ espaço suficiente**</span><span class="sxs-lookup"><span data-stu-id="d746b-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERROR\_CLUSTERLOG\_NOT\_ENOUGH\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-543">5033 (0x13A9)</span><span class="sxs-lookup"><span data-stu-id="d746b-543">5033 (0x13A9)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-544">O espaço em disco mínimo necessário para o registro em log não está disponível.</span><span class="sxs-lookup"><span data-stu-id="d746b-544">The minimum required disk space needed for logging is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERRO \_ de \_ proprietário do quorum \_ ativo**</span><span class="sxs-lookup"><span data-stu-id="d746b-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERROR\_QUORUM\_OWNER\_ALIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-546">5034 (0x13AA)</span><span class="sxs-lookup"><span data-stu-id="d746b-546">5034 (0x13AA)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-547">O nó de cluster falhou ao assumir o controle do recurso de quorum porque o recurso pertence a outro nó ativo.</span><span class="sxs-lookup"><span data-stu-id="d746b-547">The cluster node failed to take control of the quorum resource because the resource is owned by another active node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERRO de \_ rede \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="d746b-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERROR\_NETWORK\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-549">5035 (0x13AB)</span><span class="sxs-lookup"><span data-stu-id="d746b-549">5035 (0x13AB)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-550">Uma rede de cluster não está disponível para esta operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-550">A cluster network is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**nó de erro \_ \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="d746b-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**ERROR\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-552">5036 (0x13AC)</span><span class="sxs-lookup"><span data-stu-id="d746b-552">5036 (0x13AC)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-553">Um nó de cluster não está disponível para esta operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-553">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERRO \_ todos os \_ nós \_ não \_ estão disponíveis**</span><span class="sxs-lookup"><span data-stu-id="d746b-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERROR\_ALL\_NODES\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-555">5037 (0x13AD)</span><span class="sxs-lookup"><span data-stu-id="d746b-555">5037 (0x13AD)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-556">Todos os nós de cluster devem estar em execução para executar esta operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-556">All cluster nodes must be running to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**\_falha no recurso de erro \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**ERROR\_RESOURCE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-558">5038 (0x13AE)</span><span class="sxs-lookup"><span data-stu-id="d746b-558">5038 (0x13AE)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-559">Um recurso de cluster falhou.</span><span class="sxs-lookup"><span data-stu-id="d746b-559">A cluster resource failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**ERRO \_ de \_ nó inválido do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**ERROR\_CLUSTER\_INVALID\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-561">5039 (0x13AF)</span><span class="sxs-lookup"><span data-stu-id="d746b-561">5039 (0x13AF)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-562">O nó do cluster não é válido.</span><span class="sxs-lookup"><span data-stu-id="d746b-562">The cluster node is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**o \_ nó de cluster de erros \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d746b-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**ERROR\_CLUSTER\_NODE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-564">5040 (0x13B0)</span><span class="sxs-lookup"><span data-stu-id="d746b-564">5040 (0x13B0)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-565">O nó de cluster já existe.</span><span class="sxs-lookup"><span data-stu-id="d746b-565">The cluster node already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERRO \_ \_ de ingresso \_ no cluster em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="d746b-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-567">5041 (0x13B1)</span><span class="sxs-lookup"><span data-stu-id="d746b-567">5041 (0x13B1)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-568">Um nó está no processo de ingressar no cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-568">A node is in the process of joining the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**nó de cluster de erros \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**ERROR\_CLUSTER\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-570">5042 (0x13B2)</span><span class="sxs-lookup"><span data-stu-id="d746b-570">5042 (0x13B2)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-571">O nó do cluster não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="d746b-571">The cluster node was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**\_nó local do cluster de erros \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**ERROR\_CLUSTER\_LOCAL\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-573">5043 (0x13B3)</span><span class="sxs-lookup"><span data-stu-id="d746b-573">5043 (0x13B3)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-574">As informações do nó local do cluster não foram encontradas.</span><span class="sxs-lookup"><span data-stu-id="d746b-574">The cluster local node information was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERRO a \_ rede de clusters \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d746b-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERROR\_CLUSTER\_NETWORK\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-576">5044 (0x13B4)</span><span class="sxs-lookup"><span data-stu-id="d746b-576">5044 (0x13B4)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-577">A rede de cluster já existe.</span><span class="sxs-lookup"><span data-stu-id="d746b-577">The cluster network already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERRO \_ de \_ rede de cluster \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="d746b-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-579">5045 (0x13B5)</span><span class="sxs-lookup"><span data-stu-id="d746b-579">5045 (0x13B5)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-580">A rede de cluster não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="d746b-580">The cluster network was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERRO o \_ cluster \_ netinterface \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d746b-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERROR\_CLUSTER\_NETINTERFACE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-582">5046 (0x13B6)</span><span class="sxs-lookup"><span data-stu-id="d746b-582">5046 (0x13B6)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-583">A interface de rede do cluster já existe.</span><span class="sxs-lookup"><span data-stu-id="d746b-583">The cluster network interface already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERRO de \_ cluster de \_ netinterface \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERROR\_CLUSTER\_NETINTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-585">5047 (0x13B7)</span><span class="sxs-lookup"><span data-stu-id="d746b-585">5047 (0x13B7)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-586">A interface de rede do cluster não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="d746b-586">The cluster network interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**ERRO de \_ solicitação de cluster \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**ERROR\_CLUSTER\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-588">5048 (0x13B8)</span><span class="sxs-lookup"><span data-stu-id="d746b-588">5048 (0x13B8)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-589">A solicitação de cluster não é válida para este objeto.</span><span class="sxs-lookup"><span data-stu-id="d746b-589">The cluster request is not valid for this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERRO \_ do \_ \_ provedor de rede inválido do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-591">5049 (0x13B9)</span><span class="sxs-lookup"><span data-stu-id="d746b-591">5049 (0x13B9)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-592">O provedor de rede de cluster não é válido.</span><span class="sxs-lookup"><span data-stu-id="d746b-592">The cluster network provider is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**ERRO \_ no \_ nó do cluster \_ inoperante**</span><span class="sxs-lookup"><span data-stu-id="d746b-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**ERROR\_CLUSTER\_NODE\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-594">5050 (0x13BA)</span><span class="sxs-lookup"><span data-stu-id="d746b-594">5050 (0x13BA)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-595">O nó do cluster está inoperante.</span><span class="sxs-lookup"><span data-stu-id="d746b-595">The cluster node is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**nó de cluster de erros \_ \_ \_ inacessível**</span><span class="sxs-lookup"><span data-stu-id="d746b-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERROR\_CLUSTER\_NODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-597">5051 (0x13BB)</span><span class="sxs-lookup"><span data-stu-id="d746b-597">5051 (0x13BB)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-598">O nó do cluster não está acessível.</span><span class="sxs-lookup"><span data-stu-id="d746b-598">The cluster node is not reachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**ERRO \_ nó de cluster \_ \_ não \_ membro**</span><span class="sxs-lookup"><span data-stu-id="d746b-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**ERROR\_CLUSTER\_NODE\_NOT\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-600">5052 (0x13BC)</span><span class="sxs-lookup"><span data-stu-id="d746b-600">5052 (0x13BC)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-601">O nó do cluster não é um membro do cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-601">The cluster node is not a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**ERRO \_ ao \_ ingressar \_ no cluster não está \_ em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="d746b-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-603">5053 (0x13BD)</span><span class="sxs-lookup"><span data-stu-id="d746b-603">5053 (0x13BD)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-604">Uma operação de ingresso no cluster não está em andamento.</span><span class="sxs-lookup"><span data-stu-id="d746b-604">A cluster join operation is not in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERRO \_ de \_ rede inválida do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-606">5054 (0x13BE)</span><span class="sxs-lookup"><span data-stu-id="d746b-606">5054 (0x13BE)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-607">A rede do cluster não é válida.</span><span class="sxs-lookup"><span data-stu-id="d746b-607">The cluster network is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**ERRO \_ no \_ nó do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**ERROR\_CLUSTER\_NODE\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-609">5056 (0x13C0)</span><span class="sxs-lookup"><span data-stu-id="d746b-609">5056 (0x13C0)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-610">O nó do cluster está ativo.</span><span class="sxs-lookup"><span data-stu-id="d746b-610">The cluster node is up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERRO \_ \_ de IPAddr \_ de cluster em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="d746b-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERROR\_CLUSTER\_IPADDR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-612">5057 (0x13C1)</span><span class="sxs-lookup"><span data-stu-id="d746b-612">5057 (0x13C1)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-613">O endereço IP do cluster já está em uso.</span><span class="sxs-lookup"><span data-stu-id="d746b-613">The cluster IP address is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**o \_ nó de cluster de erros não está em \_ \_ \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="d746b-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**ERROR\_CLUSTER\_NODE\_NOT\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-615">5058 (0x13C2)</span><span class="sxs-lookup"><span data-stu-id="d746b-615">5058 (0x13C2)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-616">O nó do cluster não está em pausa.</span><span class="sxs-lookup"><span data-stu-id="d746b-616">The cluster node is not paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**ERRO \_ de \_ cluster \_ sem \_ contexto de segurança**</span><span class="sxs-lookup"><span data-stu-id="d746b-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**ERROR\_CLUSTER\_NO\_SECURITY\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-618">5059 (0x13C3)</span><span class="sxs-lookup"><span data-stu-id="d746b-618">5059 (0x13C3)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-619">Nenhum contexto de segurança do cluster está disponível.</span><span class="sxs-lookup"><span data-stu-id="d746b-619">No cluster security context is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERRO \_ de \_ rede de cluster \_ não \_ interna**</span><span class="sxs-lookup"><span data-stu-id="d746b-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-621">5060 (0x13C4)</span><span class="sxs-lookup"><span data-stu-id="d746b-621">5060 (0x13C4)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-622">A rede de cluster não está configurada para comunicação de cluster interno.</span><span class="sxs-lookup"><span data-stu-id="d746b-622">The cluster network is not configured for internal cluster communication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**o \_ \_ nó \_ de cluster de erros já está \_ ativo**</span><span class="sxs-lookup"><span data-stu-id="d746b-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-624">5061 (0x13C5)</span><span class="sxs-lookup"><span data-stu-id="d746b-624">5061 (0x13C5)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-625">O nó do cluster já está ativo.</span><span class="sxs-lookup"><span data-stu-id="d746b-625">The cluster node is already up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**o \_ nó de cluster de erros \_ \_ já está \_ inoperante**</span><span class="sxs-lookup"><span data-stu-id="d746b-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-627">5062 (0x13C6)</span><span class="sxs-lookup"><span data-stu-id="d746b-627">5062 (0x13C6)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-628">O nó de cluster já está inoperante.</span><span class="sxs-lookup"><span data-stu-id="d746b-628">The cluster node is already down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**a \_ rede de cluster de erros \_ \_ já está \_ online**</span><span class="sxs-lookup"><span data-stu-id="d746b-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-630">5063 (0x13C7)</span><span class="sxs-lookup"><span data-stu-id="d746b-630">5063 (0x13C7)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-631">A rede de cluster já está online.</span><span class="sxs-lookup"><span data-stu-id="d746b-631">The cluster network is already online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**a \_ rede de cluster de erros \_ \_ já está \_ offline**</span><span class="sxs-lookup"><span data-stu-id="d746b-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-633">5064 (0x13C8)</span><span class="sxs-lookup"><span data-stu-id="d746b-633">5064 (0x13C8)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-634">A rede de cluster já está offline.</span><span class="sxs-lookup"><span data-stu-id="d746b-634">The cluster network is already offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**ERRO \_ nó de cluster \_ \_ já \_ membro**</span><span class="sxs-lookup"><span data-stu-id="d746b-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-636">5065 (0x13C9)</span><span class="sxs-lookup"><span data-stu-id="d746b-636">5065 (0x13C9)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-637">O nó de cluster já é um membro do cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-637">The cluster node is already a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**ERRO \_ na \_ última \_ rede interna do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**ERROR\_CLUSTER\_LAST\_INTERNAL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-639">5066 (0x13CA)</span><span class="sxs-lookup"><span data-stu-id="d746b-639">5066 (0x13CA)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-640">A rede de cluster é a única configurada para comunicação de cluster interno entre dois ou mais nós de cluster ativos.</span><span class="sxs-lookup"><span data-stu-id="d746b-640">The cluster network is the only one configured for internal cluster communication between two or more active cluster nodes.</span></span> <span data-ttu-id="d746b-641">A funcionalidade de comunicação interna não pode ser removida da rede.</span><span class="sxs-lookup"><span data-stu-id="d746b-641">The internal communication capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERRO \_ rede de cluster \_ \_ \_ depende de**</span><span class="sxs-lookup"><span data-stu-id="d746b-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERROR\_CLUSTER\_NETWORK\_HAS\_DEPENDENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-643">5067 (0x13CB)</span><span class="sxs-lookup"><span data-stu-id="d746b-643">5067 (0x13CB)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-644">Um ou mais recursos de cluster dependem da rede para fornecer serviço aos clientes.</span><span class="sxs-lookup"><span data-stu-id="d746b-644">One or more cluster resources depend on the network to provide service to clients.</span></span> <span data-ttu-id="d746b-645">A funcionalidade de acesso para cliente não pode ser removida da rede.</span><span class="sxs-lookup"><span data-stu-id="d746b-645">The client access capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERRO \_ \_ de operação inválida \_ no \_ Quorum**</span><span class="sxs-lookup"><span data-stu-id="d746b-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERROR\_INVALID\_OPERATION\_ON\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-647">5068 (0x13CC)</span><span class="sxs-lookup"><span data-stu-id="d746b-647">5068 (0x13CC)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-648">Esta operação não pode ser executada no recurso de cluster como ele é o recurso de quorum.</span><span class="sxs-lookup"><span data-stu-id="d746b-648">This operation cannot be performed on the cluster resource as it the quorum resource.</span></span> <span data-ttu-id="d746b-649">Você não pode colocar o recurso de quorum offline ou modificar sua lista de possíveis proprietários.</span><span class="sxs-lookup"><span data-stu-id="d746b-649">You may not bring the quorum resource offline or modify its possible owners list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**dependência de erro \_ \_ não \_ permitida**</span><span class="sxs-lookup"><span data-stu-id="d746b-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**ERROR\_DEPENDENCY\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-651">5069 (0x13CD)</span><span class="sxs-lookup"><span data-stu-id="d746b-651">5069 (0x13CD)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-652">O recurso de quorum do cluster não tem permissão para ter nenhuma dependência.</span><span class="sxs-lookup"><span data-stu-id="d746b-652">The cluster quorum resource is not allowed to have any dependencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**ERRO no \_ nó de cluster em \_ \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="d746b-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**ERROR\_CLUSTER\_NODE\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-654">5070 (0x13CE)</span><span class="sxs-lookup"><span data-stu-id="d746b-654">5070 (0x13CE)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-655">O nó do cluster está em pausa.</span><span class="sxs-lookup"><span data-stu-id="d746b-655">The cluster node is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**o nó de erro não \_ \_ consegue \_ hospedar \_ recurso**</span><span class="sxs-lookup"><span data-stu-id="d746b-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**ERROR\_NODE\_CANT\_HOST\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-657">5071 (0x13CF)</span><span class="sxs-lookup"><span data-stu-id="d746b-657">5071 (0x13CF)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-658">O recurso de cluster não pode ser colocado online.</span><span class="sxs-lookup"><span data-stu-id="d746b-658">The cluster resource cannot be brought online.</span></span> <span data-ttu-id="d746b-659">O nó proprietário não pode executar este recurso.</span><span class="sxs-lookup"><span data-stu-id="d746b-659">The owner node cannot run this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**o \_ nó de cluster de erros \_ \_ não \_ está pronto**</span><span class="sxs-lookup"><span data-stu-id="d746b-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**ERROR\_CLUSTER\_NODE\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-661">5072 (0x13D0)</span><span class="sxs-lookup"><span data-stu-id="d746b-661">5072 (0x13D0)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-662">O nó do cluster não está pronto para executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="d746b-662">The cluster node is not ready to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERRO \_ ao \_ desligar o nó do cluster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERROR\_CLUSTER\_NODE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-664">5073 (0x13D1)</span><span class="sxs-lookup"><span data-stu-id="d746b-664">5073 (0x13D1)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-665">O nó do cluster está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="d746b-665">The cluster node is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERRO \_ de \_ ingresso no cluster \_ anulado**</span><span class="sxs-lookup"><span data-stu-id="d746b-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERROR\_CLUSTER\_JOIN\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-667">5074 (0x13D2)</span><span class="sxs-lookup"><span data-stu-id="d746b-667">5074 (0x13D2)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-668">A operação de ingresso no cluster foi anulada.</span><span class="sxs-lookup"><span data-stu-id="d746b-668">The cluster join operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**ERRO \_ de \_ versões incompatíveis do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**ERROR\_CLUSTER\_INCOMPATIBLE\_VERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-670">5075 (0x13D3)</span><span class="sxs-lookup"><span data-stu-id="d746b-670">5075 (0x13D3)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-671">A operação de ingresso no cluster falhou devido a versões de software incompatíveis entre o nó de junção e seu patrocinador.</span><span class="sxs-lookup"><span data-stu-id="d746b-671">The cluster join operation failed due to incompatible software versions between the joining node and its sponsor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**ERRO \_ \_ de MAXNUM \_ do cluster de \_ recursos \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="d746b-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**ERROR\_CLUSTER\_MAXNUM\_OF\_RESOURCES\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-673">5076 (0x13D4)</span><span class="sxs-lookup"><span data-stu-id="d746b-673">5076 (0x13D4)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-674">Este recurso não pode ser criado porque o cluster atingiu o limite do número de recursos que ele pode monitorar.</span><span class="sxs-lookup"><span data-stu-id="d746b-674">This resource cannot be created because the cluster has reached the limit on the number of resources it can monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERRO \_ de \_ configuração do sistema de cluster \_ \_ alterado**</span><span class="sxs-lookup"><span data-stu-id="d746b-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERROR\_CLUSTER\_SYSTEM\_CONFIG\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-676">5077 (0x13D5)</span><span class="sxs-lookup"><span data-stu-id="d746b-676">5077 (0x13D5)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-677">A configuração do sistema foi alterada durante a operação de ingresso ou formulário do cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-677">The system configuration changed during the cluster join or form operation.</span></span> <span data-ttu-id="d746b-678">A operação de ingresso ou formulário foi anulada.</span><span class="sxs-lookup"><span data-stu-id="d746b-678">The join or form operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**ERRO de \_ tipo de recurso de cluster \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-680">5078 (0x13D6)</span><span class="sxs-lookup"><span data-stu-id="d746b-680">5078 (0x13D6)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-681">O tipo de recurso especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="d746b-681">The specified resource type was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**ERRO \_ RESTYPE de cluster \_ \_ não \_ suportado**</span><span class="sxs-lookup"><span data-stu-id="d746b-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**ERROR\_CLUSTER\_RESTYPE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-683">5079 (0x13D7)</span><span class="sxs-lookup"><span data-stu-id="d746b-683">5079 (0x13D7)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-684">O nó especificado não oferece suporte a um recurso desse tipo.</span><span class="sxs-lookup"><span data-stu-id="d746b-684">The specified node does not support a resource of this type.</span></span> <span data-ttu-id="d746b-685">Isso pode ser devido a inconsistências de versão ou devido à ausência da DLL de recurso neste nó.</span><span class="sxs-lookup"><span data-stu-id="d746b-685">This may be due to version inconsistencies or due to the absence of the resource DLL on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERRO \_ RESNAME do cluster \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERROR\_CLUSTER\_RESNAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-687">5080 (0x13D8)</span><span class="sxs-lookup"><span data-stu-id="d746b-687">5080 (0x13D8)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-688">Não há suporte para o nome de recurso especificado nesta DLL de recurso.</span><span class="sxs-lookup"><span data-stu-id="d746b-688">The specified resource name is not supported by this resource DLL.</span></span> <span data-ttu-id="d746b-689">Isso pode ser devido a um nome (ou alterado) inadequado fornecido à DLL de recurso.</span><span class="sxs-lookup"><span data-stu-id="d746b-689">This may be due to a bad (or changed) name supplied to the resource DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**ERRO \_ de \_ cluster \_ sem \_ pacotes RPC \_ registrados**</span><span class="sxs-lookup"><span data-stu-id="d746b-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**ERROR\_CLUSTER\_NO\_RPC\_PACKAGES\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-691">5081 (0x13D9)</span><span class="sxs-lookup"><span data-stu-id="d746b-691">5081 (0x13D9)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-692">Nenhum pacote de autenticação pôde ser registrado com o servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="d746b-692">No authentication package could be registered with the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERRO \_ o \_ proprietário \_ do cluster não está \_ em \_ preflist**</span><span class="sxs-lookup"><span data-stu-id="d746b-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERROR\_CLUSTER\_OWNER\_NOT\_IN\_PREFLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-694">5082 (0x13DA)</span><span class="sxs-lookup"><span data-stu-id="d746b-694">5082 (0x13DA)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-695">Não é possível colocar o grupo online porque o proprietário do grupo não está na lista de preferenciais do grupo.</span><span class="sxs-lookup"><span data-stu-id="d746b-695">You cannot bring the group online because the owner of the group is not in the preferred list for the group.</span></span> <span data-ttu-id="d746b-696">Para alterar o nó proprietário do grupo, mova o grupo.</span><span class="sxs-lookup"><span data-stu-id="d746b-696">To change the owner node for the group, move the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERRO \_ de \_ banco de dados de cluster \_ SEQMISMATCH**</span><span class="sxs-lookup"><span data-stu-id="d746b-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERROR\_CLUSTER\_DATABASE\_SEQMISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-698">5083 (0x13DB)</span><span class="sxs-lookup"><span data-stu-id="d746b-698">5083 (0x13DB)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-699">A operação de junção falhou porque o número de sequência do banco de dados do cluster foi alterado ou é incompatível com o nó do armário.</span><span class="sxs-lookup"><span data-stu-id="d746b-699">The join operation failed because the cluster database sequence number has changed or is incompatible with the locker node.</span></span> <span data-ttu-id="d746b-700">Isso pode ocorrer durante uma operação de junção se o banco de dados do cluster fosse alterado durante a junção.</span><span class="sxs-lookup"><span data-stu-id="d746b-700">This may happen during a join operation if the cluster database was changing during the join.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERRO \_ resmon \_ \_ estado inválido**</span><span class="sxs-lookup"><span data-stu-id="d746b-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERROR\_RESMON\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-702">5084 (0x13DC)</span><span class="sxs-lookup"><span data-stu-id="d746b-702">5084 (0x13DC)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-703">O monitor de recursos não permitirá que a operação de falha seja executada enquanto o recurso estiver em seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="d746b-703">The resource monitor will not allow the fail operation to be performed while the resource is in its current state.</span></span> <span data-ttu-id="d746b-704">Isso pode acontecer se o recurso estiver em um estado pendente.</span><span class="sxs-lookup"><span data-stu-id="d746b-704">This may happen if the resource is in a pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERRO de \_ cluster \_ triz \_ não \_ bloqueador**</span><span class="sxs-lookup"><span data-stu-id="d746b-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERROR\_CLUSTER\_GUM\_NOT\_LOCKER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-706">5085 (0x13DD)</span><span class="sxs-lookup"><span data-stu-id="d746b-706">5085 (0x13DD)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-707">Um código não bloqueador recebeu uma solicitação para reservar o bloqueio para fazer atualizações globais.</span><span class="sxs-lookup"><span data-stu-id="d746b-707">A non locker code got a request to reserve the lock for making global updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**ERRO \_ de \_ disco de quorum \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**ERROR\_QUORUM\_DISK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-709">5086 (0x13DE)</span><span class="sxs-lookup"><span data-stu-id="d746b-709">5086 (0x13DE)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-710">O disco de quorum não pôde ser localizado pelo serviço de cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-710">The quorum disk could not be located by the cluster service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERRO de \_ backup do banco de dados \_ \_ corrompido**</span><span class="sxs-lookup"><span data-stu-id="d746b-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERROR\_DATABASE\_BACKUP\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-712">5087 (0x13DF)</span><span class="sxs-lookup"><span data-stu-id="d746b-712">5087 (0x13DF)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-713">O banco de dados de cluster de backup é possivelmente corrompido.</span><span class="sxs-lookup"><span data-stu-id="d746b-713">The backed up cluster database is possibly corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**o \_ nó de cluster de erros \_ \_ já \_ tem a \_ \_ raiz DFS**</span><span class="sxs-lookup"><span data-stu-id="d746b-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_HAS\_DFS\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-715">5088 (0x13E0)</span><span class="sxs-lookup"><span data-stu-id="d746b-715">5088 (0x13E0)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-716">Já existe uma raiz DFS neste nó de cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-716">A DFS root already exists in this cluster node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**Propriedade de recurso de erro \_ \_ \_ inalterável**</span><span class="sxs-lookup"><span data-stu-id="d746b-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**ERROR\_RESOURCE\_PROPERTY\_UNCHANGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-718">5089 (0x13E1)</span><span class="sxs-lookup"><span data-stu-id="d746b-718">5089 (0x13E1)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-719">Falha ao tentar modificar uma propriedade de recurso porque ela está em conflito com outra propriedade existente.</span><span class="sxs-lookup"><span data-stu-id="d746b-719">An attempt to modify a resource property failed because it conflicts with another existing property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ERRO \_ \_ estado inválido de associação de cluster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-721">5890 (0x1702)</span><span class="sxs-lookup"><span data-stu-id="d746b-721">5890 (0x1702)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-722">Foi tentada uma operação que é incompatível com o estado de associação atual do nó.</span><span class="sxs-lookup"><span data-stu-id="d746b-722">An operation was attempted that is incompatible with the current membership state of the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERRO \_ QUORUMLOG do cluster \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d746b-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERROR\_CLUSTER\_QUORUMLOG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-724">5891 (0x1703)</span><span class="sxs-lookup"><span data-stu-id="d746b-724">5891 (0x1703)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-725">O recurso de quorum não contém o log de quorum.</span><span class="sxs-lookup"><span data-stu-id="d746b-725">The quorum resource does not contain the quorum log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERRO \_ ao \_ interromper a associação do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_HALT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-727">5892 (0x1704)</span><span class="sxs-lookup"><span data-stu-id="d746b-727">5892 (0x1704)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-728">O mecanismo de associação solicitou o desligamento do serviço de cluster neste nó.</span><span class="sxs-lookup"><span data-stu-id="d746b-728">The membership engine requested shutdown of the cluster service on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de ID de instância de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERROR\_CLUSTER\_INSTANCE\_ID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-730">5893 (0x1705)</span><span class="sxs-lookup"><span data-stu-id="d746b-730">5893 (0x1705)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-731">Falha na operação de junção porque a ID de instância de cluster do nó de junção não corresponde à ID de instância de cluster do nó patrocinador.</span><span class="sxs-lookup"><span data-stu-id="d746b-731">The join operation failed because the cluster instance ID of the joining node does not match the cluster instance ID of the sponsor node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**ERRO \_ \_ de rede \_ de cluster não \_ encontrada \_ para \_ IP**</span><span class="sxs-lookup"><span data-stu-id="d746b-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND\_FOR\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-733">5894 (0x1706)</span><span class="sxs-lookup"><span data-stu-id="d746b-733">5894 (0x1706)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-734">Não foi possível encontrar uma rede de cluster correspondente para o endereço IP especificado.</span><span class="sxs-lookup"><span data-stu-id="d746b-734">A matching cluster network for the specified IP address could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERRO de \_ tipo de dados de Propriedade do cluster \_ \_ \_ \_ incompatível**</span><span class="sxs-lookup"><span data-stu-id="d746b-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERROR\_CLUSTER\_PROPERTY\_DATA\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-736">5895 (0x1707)</span><span class="sxs-lookup"><span data-stu-id="d746b-736">5895 (0x1707)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-737">O tipo de dados real da propriedade não correspondeu ao tipo de dados esperado da propriedade.</span><span class="sxs-lookup"><span data-stu-id="d746b-737">The actual data type of the property did not match the expected data type of the property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**remoção de cluster de erros \_ \_ \_ sem \_ limpeza**</span><span class="sxs-lookup"><span data-stu-id="d746b-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERROR\_CLUSTER\_EVICT\_WITHOUT\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-739">5896 (0x1708)</span><span class="sxs-lookup"><span data-stu-id="d746b-739">5896 (0x1708)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-740">O nó de cluster foi removido do cluster com êxito, mas o nó não foi limpo.</span><span class="sxs-lookup"><span data-stu-id="d746b-740">The cluster node was evicted from the cluster successfully, but the node was not cleaned up.</span></span> <span data-ttu-id="d746b-741">Para determinar quais etapas de limpeza falharam e como recuperar, consulte o log de eventos do aplicativo clustering de failover usando Visualizador de Eventos.</span><span class="sxs-lookup"><span data-stu-id="d746b-741">To determine what cleanup steps failed and how to recover, see the Failover Clustering application event log using Event Viewer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERRO \_ de \_ incompatibilidade de parâmetro de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERROR\_CLUSTER\_PARAMETER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-743">5897 (0x1709)</span><span class="sxs-lookup"><span data-stu-id="d746b-743">5897 (0x1709)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-744">Dois ou mais valores de parâmetro especificados para as propriedades de um recurso estão em conflito.</span><span class="sxs-lookup"><span data-stu-id="d746b-744">Two or more parameter values specified for a resource's properties are in conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**o \_ nó de erro \_ não pode \_ ser \_ clusterizado**</span><span class="sxs-lookup"><span data-stu-id="d746b-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**ERROR\_NODE\_CANNOT\_BE\_CLUSTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-746">5898 (0x170A)</span><span class="sxs-lookup"><span data-stu-id="d746b-746">5898 (0x170A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-747">Este computador não pode se tornar membro de um cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-747">This computer cannot be made a member of a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERRO \_ na \_ \_ versão do so incorreta do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERROR\_CLUSTER\_WRONG\_OS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-749">5899 (0x170B)</span><span class="sxs-lookup"><span data-stu-id="d746b-749">5899 (0x170B)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-750">Este computador não pode se tornar membro de um cluster porque ele não tem a versão correta do Windows instalada.</span><span class="sxs-lookup"><span data-stu-id="d746b-750">This computer cannot be made a member of a cluster because it does not have the correct version of Windows installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERRO o \_ cluster não \_ consegue criar o nome do \_ \_ \_ cluster dup \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERROR\_CLUSTER\_CANT\_CREATE\_DUP\_CLUSTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-752">5900 (0x170C)</span><span class="sxs-lookup"><span data-stu-id="d746b-752">5900 (0x170C)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-753">Um cluster não pode ser criado com o nome de cluster especificado porque o nome do cluster já está em uso.</span><span class="sxs-lookup"><span data-stu-id="d746b-753">A cluster cannot be created with the specified cluster name because that cluster name is already in use.</span></span> <span data-ttu-id="d746b-754">Especifique um nome diferente para o cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-754">Specify a different name for the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERRO \_ CLUSCFG \_ já \_ confirmado**</span><span class="sxs-lookup"><span data-stu-id="d746b-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERROR\_CLUSCFG\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-756">5901 (0x170D)</span><span class="sxs-lookup"><span data-stu-id="d746b-756">5901 (0x170D)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-757">A ação de configuração de cluster já foi confirmada.</span><span class="sxs-lookup"><span data-stu-id="d746b-757">The cluster configuration action has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERRO \_ CLUSCFG \_ \_ falha na reversão**</span><span class="sxs-lookup"><span data-stu-id="d746b-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERROR\_CLUSCFG\_ROLLBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-759">5902 (0x170E)</span><span class="sxs-lookup"><span data-stu-id="d746b-759">5902 (0x170E)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-760">Não foi possível reverter a ação de configuração do cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-760">The cluster configuration action could not be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERRO \_ CLUSCFG \_ \_ conflito de \_ letra da unidade de disco do \_ sistema \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERROR\_CLUSCFG\_SYSTEM\_DISK\_DRIVE\_LETTER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-762">5903 (0x170F)</span><span class="sxs-lookup"><span data-stu-id="d746b-762">5903 (0x170F)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-763">A letra da unidade atribuída a um disco do sistema em um nó está em conflito com a letra da unidade atribuída a um disco em outro nó.</span><span class="sxs-lookup"><span data-stu-id="d746b-763">The drive letter assigned to a system disk on one node conflicted with the drive letter assigned to a disk on another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**ERRO \_ de \_ versão antiga do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**ERROR\_CLUSTER\_OLD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-765">5904 (0x1710)</span><span class="sxs-lookup"><span data-stu-id="d746b-765">5904 (0x1710)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-766">Um ou mais nós no cluster estão executando uma versão do Windows que não oferece suporte a essa operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-766">One or more nodes in the cluster are running a version of Windows that does not support this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERRO \_ de \_ nome de conta do computador incompatível do cluster \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERROR\_CLUSTER\_MISMATCHED\_COMPUTER\_ACCT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-768">5905 (0x1711)</span><span class="sxs-lookup"><span data-stu-id="d746b-768">5905 (0x1711)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-769">O nome da conta de computador correspondente não corresponde ao nome de rede deste recurso.</span><span class="sxs-lookup"><span data-stu-id="d746b-769">The name of the corresponding computer account doesn't match the Network Name for this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**CLUSTER de erros \_ \_ sem \_ \_ adaptadores de rede**</span><span class="sxs-lookup"><span data-stu-id="d746b-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERROR\_CLUSTER\_NO\_NET\_ADAPTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-771">5906 (0x1712)</span><span class="sxs-lookup"><span data-stu-id="d746b-771">5906 (0x1712)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-772">Não há adaptadores de rede disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d746b-772">No network adapters are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**ERRO de \_ cluster \_ inviabilizada**</span><span class="sxs-lookup"><span data-stu-id="d746b-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**ERROR\_CLUSTER\_POISONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-774">5907 (0x1713)</span><span class="sxs-lookup"><span data-stu-id="d746b-774">5907 (0x1713)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-775">O nó do cluster foi inviabilizada.</span><span class="sxs-lookup"><span data-stu-id="d746b-775">The cluster node has been poisoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERRO \_ ao \_ mover grupo de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERROR\_CLUSTER\_GROUP\_MOVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-777">5908 (0x1714)</span><span class="sxs-lookup"><span data-stu-id="d746b-777">5908 (0x1714)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-778">O grupo não pode aceitar a solicitação porque está se movendo para outro nó.</span><span class="sxs-lookup"><span data-stu-id="d746b-778">The group is unable to accept the request since it is moving to another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**ERRO \_ tipo de recurso de cluster \_ \_ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="d746b-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-780">5909 (0x1715)</span><span class="sxs-lookup"><span data-stu-id="d746b-780">5909 (0x1715)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-781">O tipo de recurso não pode aceitar a solicitação, pois está muito ocupado executando outra operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-781">The resource type cannot accept the request since is too busy performing another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**a \_ chamada de recurso de erro \_ atingiu o \_ tempo \_ limite**</span><span class="sxs-lookup"><span data-stu-id="d746b-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**ERROR\_RESOURCE\_CALL\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-783">5910 (0x1716)</span><span class="sxs-lookup"><span data-stu-id="d746b-783">5910 (0x1716)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-784">A chamada para a DLL de recurso de cluster atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="d746b-784">The call to the cluster resource DLL timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERRO \_ \_ endereço IPv6 do cluster inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERROR\_INVALID\_CLUSTER\_IPV6\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-786">5911 (0x1717)</span><span class="sxs-lookup"><span data-stu-id="d746b-786">5911 (0x1717)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-787">O endereço não é válido para um recurso de endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="d746b-787">The address is not valid for an IPv6 Address resource.</span></span> <span data-ttu-id="d746b-788">Um endereço IPv6 global é necessário e deve corresponder a uma rede de cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-788">A global IPv6 address is required, and it must match a cluster network.</span></span> <span data-ttu-id="d746b-789">Os endereços de compatibilidade não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="d746b-789">Compatibility addresses are not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**ERRO \_ de \_ \_ função interna inválida do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**ERROR\_CLUSTER\_INTERNAL\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-791">5912 (0x1718)</span><span class="sxs-lookup"><span data-stu-id="d746b-791">5912 (0x1718)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-792">Ocorreu um erro de cluster interno.</span><span class="sxs-lookup"><span data-stu-id="d746b-792">An internal cluster error occurred.</span></span> <span data-ttu-id="d746b-793">Uma chamada para uma função inválida foi tentada.</span><span class="sxs-lookup"><span data-stu-id="d746b-793">A call to an invalid function was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**ERRO \_ \_ de parâmetro \_ de cluster fora \_ dos \_ limites**</span><span class="sxs-lookup"><span data-stu-id="d746b-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**ERROR\_CLUSTER\_PARAMETER\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-795">5913 (0x1719)</span><span class="sxs-lookup"><span data-stu-id="d746b-795">5913 (0x1719)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-796">Um valor de parâmetro está fora do intervalo aceitável.</span><span class="sxs-lookup"><span data-stu-id="d746b-796">A parameter value is out of acceptable range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERRO \_ de \_ envio parcial do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERROR\_CLUSTER\_PARTIAL\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-798">5914 (0x171A)</span><span class="sxs-lookup"><span data-stu-id="d746b-798">5914 (0x171A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-799">Ocorreu um erro de rede ao enviar dados para outro nó no cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-799">A network error occurred while sending data to another node in the cluster.</span></span> <span data-ttu-id="d746b-800">O número de bytes transmitidos era menor que o necessário.</span><span class="sxs-lookup"><span data-stu-id="d746b-800">The number of bytes transmitted was less than required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERRO \_ de \_ \_ função inválida no registro de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERROR\_CLUSTER\_REGISTRY\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-802">5915 (0x171B)</span><span class="sxs-lookup"><span data-stu-id="d746b-802">5915 (0x171B)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-803">Tentativa de operação de registro de cluster inválida.</span><span class="sxs-lookup"><span data-stu-id="d746b-803">An invalid cluster registry operation was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**ERRO \_ de \_ encerramento de cadeia de caracteres inválido do cluster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_TERMINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-805">5916 (0x171C)</span><span class="sxs-lookup"><span data-stu-id="d746b-805">5916 (0x171C)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-806">Uma cadeia de caracteres de entrada não é encerrada corretamente.</span><span class="sxs-lookup"><span data-stu-id="d746b-806">An input string of characters is not properly terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERRO \_ de \_ formato de cadeia de caracteres inválido do cluster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-808">5917 (0x171D)</span><span class="sxs-lookup"><span data-stu-id="d746b-808">5917 (0x171D)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-809">Uma cadeia de caracteres de entrada não está em um formato válido para os dados que ele representa.</span><span class="sxs-lookup"><span data-stu-id="d746b-809">An input string of characters is not in a valid format for the data it represents.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERRO \_ \_ \_ \_ na transação de banco de dados de cluster em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="d746b-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-811">5918 (0x171E)</span><span class="sxs-lookup"><span data-stu-id="d746b-811">5918 (0x171E)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-812">Ocorreu um erro de cluster interno.</span><span class="sxs-lookup"><span data-stu-id="d746b-812">An internal cluster error occurred.</span></span> <span data-ttu-id="d746b-813">Uma transação de banco de dados de cluster foi tentada enquanto uma transação já estava em andamento.</span><span class="sxs-lookup"><span data-stu-id="d746b-813">A cluster database transaction was attempted while a transaction was already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERRO \_ \_ \_ \_ de transação de banco de dados de cluster não está \_ em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="d746b-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-815">5919 (0x171F)</span><span class="sxs-lookup"><span data-stu-id="d746b-815">5919 (0x171F)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-816">Ocorreu um erro de cluster interno.</span><span class="sxs-lookup"><span data-stu-id="d746b-816">An internal cluster error occurred.</span></span> <span data-ttu-id="d746b-817">Houve uma tentativa de confirmar uma transação de banco de dados de cluster enquanto nenhuma transação estava em andamento.</span><span class="sxs-lookup"><span data-stu-id="d746b-817">There was an attempt to commit a cluster database transaction while no transaction was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERRO \_ de \_ dados nulos do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERROR\_CLUSTER\_NULL\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-819">5920 (0x1720)</span><span class="sxs-lookup"><span data-stu-id="d746b-819">5920 (0x1720)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-820">Ocorreu um erro de cluster interno.</span><span class="sxs-lookup"><span data-stu-id="d746b-820">An internal cluster error occurred.</span></span> <span data-ttu-id="d746b-821">Os dados não foram inicializados corretamente.</span><span class="sxs-lookup"><span data-stu-id="d746b-821">Data was not properly initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERRO \_ de \_ leitura parcial do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERROR\_CLUSTER\_PARTIAL\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-823">5921 (0x1721)</span><span class="sxs-lookup"><span data-stu-id="d746b-823">5921 (0x1721)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-824">Ocorreu um erro ao ler de um fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="d746b-824">An error occurred while reading from a stream of data.</span></span> <span data-ttu-id="d746b-825">Um número inesperado de bytes foi retornado.</span><span class="sxs-lookup"><span data-stu-id="d746b-825">An unexpected number of bytes was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERRO \_ de \_ gravação parcial do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERROR\_CLUSTER\_PARTIAL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-827">5922 (0x1722)</span><span class="sxs-lookup"><span data-stu-id="d746b-827">5922 (0x1722)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-828">Ocorreu um erro ao gravar em um fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="d746b-828">An error occurred while writing to a stream of data.</span></span> <span data-ttu-id="d746b-829">O número necessário de bytes não pôde ser gravado.</span><span class="sxs-lookup"><span data-stu-id="d746b-829">The required number of bytes could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERRO o \_ cluster não \_ consegue \_ desserializar \_ dados**</span><span class="sxs-lookup"><span data-stu-id="d746b-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERROR\_CLUSTER\_CANT\_DESERIALIZE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-831">5923 (0x1723)</span><span class="sxs-lookup"><span data-stu-id="d746b-831">5923 (0x1723)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-832">Ocorreu um erro ao desserializar um fluxo de dados do cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-832">An error occurred while deserializing a stream of cluster data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**\_conflito de \_ Propriedades de recursos dependentes de \_ erro \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**ERROR\_DEPENDENT\_RESOURCE\_PROPERTY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-834">5924 (0x1724)</span><span class="sxs-lookup"><span data-stu-id="d746b-834">5924 (0x1724)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-835">Um ou mais valores de propriedade para esse recurso estão em conflito com um ou mais valores de propriedade associados a seus recursos dependentes.</span><span class="sxs-lookup"><span data-stu-id="d746b-835">One or more property values for this resource are in conflict with one or more property values associated with its dependent resource(s).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERRO de \_ cluster \_ sem \_ Quorum**</span><span class="sxs-lookup"><span data-stu-id="d746b-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERROR\_CLUSTER\_NO\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-837">5925 (0x1725)</span><span class="sxs-lookup"><span data-stu-id="d746b-837">5925 (0x1725)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-838">Um quorum de nós de cluster não estava presente para formar um cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-838">A quorum of cluster nodes was not present to form a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERRO \_ de \_ \_ rede IPv6 inválida do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-840">5926 (0x1726)</span><span class="sxs-lookup"><span data-stu-id="d746b-840">5926 (0x1726)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-841">A rede de cluster não é válida para um recurso de endereço IPv6 ou não corresponde ao endereço configurado.</span><span class="sxs-lookup"><span data-stu-id="d746b-841">The cluster network is not valid for an IPv6 Address resource, or it does not match the configured address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERRO \_ de \_ \_ rede de \_ túnel \_ IPv6 inválida do cluster**</span><span class="sxs-lookup"><span data-stu-id="d746b-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_TUNNEL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-843">5927 (0x1727)</span><span class="sxs-lookup"><span data-stu-id="d746b-843">5927 (0x1727)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-844">A rede de cluster não é válida para um recurso de túnel IPv6.</span><span class="sxs-lookup"><span data-stu-id="d746b-844">The cluster network is not valid for an IPv6 Tunnel resource.</span></span> <span data-ttu-id="d746b-845">Verifique a configuração do recurso de endereço IP do qual o recurso de túnel IPv6 depende.</span><span class="sxs-lookup"><span data-stu-id="d746b-845">Check the configuration of the IP Address resource on which the IPv6 Tunnel resource depends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_o quorum \_ de erro não é \_ permitido \_ neste \_ \_ grupo**</span><span class="sxs-lookup"><span data-stu-id="d746b-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**ERROR\_QUORUM\_NOT\_ALLOWED\_IN\_THIS\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-847">5928 (0x1728)</span><span class="sxs-lookup"><span data-stu-id="d746b-847">5928 (0x1728)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-848">O recurso de quorum não pode residir no grupo de armazenamento disponível.</span><span class="sxs-lookup"><span data-stu-id="d746b-848">Quorum resource cannot reside in the Available Storage group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**árvore de dependência de erro \_ \_ \_ muito \_ complexa**</span><span class="sxs-lookup"><span data-stu-id="d746b-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**ERROR\_DEPENDENCY\_TREE\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-850">5929 (0x1729)</span><span class="sxs-lookup"><span data-stu-id="d746b-850">5929 (0x1729)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-851">As dependências para esse recurso estão aninhadas muito profundamente.</span><span class="sxs-lookup"><span data-stu-id="d746b-851">The dependencies for this resource are nested too deeply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**\_exceção \_ de erro \_ na \_ chamada de recurso**</span><span class="sxs-lookup"><span data-stu-id="d746b-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**ERROR\_EXCEPTION\_IN\_RESOURCE\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-853">5930 (0x172A)</span><span class="sxs-lookup"><span data-stu-id="d746b-853">5930 (0x172A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-854">A chamada para a DLL de recurso gerou uma exceção sem tratamento.</span><span class="sxs-lookup"><span data-stu-id="d746b-854">The call into the resource DLL raised an unhandled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**ERRO \_ \_ \_ na inicialização do RHS do cluster de erros \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**ERROR\_CLUSTER\_RHS\_FAILED\_INITIALIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-856">5931 (0x172B)</span><span class="sxs-lookup"><span data-stu-id="d746b-856">5931 (0x172B)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-857">Falha ao inicializar o processo de RHS.</span><span class="sxs-lookup"><span data-stu-id="d746b-857">The RHS process failed to initialize.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**CLUSTER de erros \_ \_ não \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="d746b-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**ERROR\_CLUSTER\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-859">5932 (0x172C)</span><span class="sxs-lookup"><span data-stu-id="d746b-859">5932 (0x172C)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-860">O recurso de clustering de failover não está instalado neste nó.</span><span class="sxs-lookup"><span data-stu-id="d746b-860">The Failover Clustering feature is not installed on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**\_ \_ os recursos de cluster de erros \_ devem \_ estar \_ online \_ no \_ \_ mesmo \_ nó**</span><span class="sxs-lookup"><span data-stu-id="d746b-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**ERROR\_CLUSTER\_RESOURCES\_MUST\_BE\_ONLINE\_ON\_THE\_SAME\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-862">5933 (0x172D)</span><span class="sxs-lookup"><span data-stu-id="d746b-862">5933 (0x172D)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-863">Os recursos devem estar online no mesmo nó para esta operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-863">The resources must be online on the same node for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**ERRO \_ \_ no máximo \_ \_ de nós do cluster no \_ cluster**</span><span class="sxs-lookup"><span data-stu-id="d746b-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**ERROR\_CLUSTER\_MAX\_NODES\_IN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-865">5934 (0x172E)</span><span class="sxs-lookup"><span data-stu-id="d746b-865">5934 (0x172E)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-866">Não é possível adicionar um novo nó, pois esse cluster já está em seu número máximo de nós.</span><span class="sxs-lookup"><span data-stu-id="d746b-866">A new node can not be added since this cluster is already at its maximum number of nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERRO de \_ cluster em \_ excesso de \_ \_ nós**</span><span class="sxs-lookup"><span data-stu-id="d746b-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERROR\_CLUSTER\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-868">5935 (0x172F)</span><span class="sxs-lookup"><span data-stu-id="d746b-868">5935 (0x172F)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-869">Este cluster não pode ser criado porque o número especificado de nós excede o limite máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="d746b-869">This cluster can not be created since the specified number of nodes exceeds the maximum allowed limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**ERRO \_ de \_ objeto de cluster \_ já \_ usado**</span><span class="sxs-lookup"><span data-stu-id="d746b-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**ERROR\_CLUSTER\_OBJECT\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-871">5936 (0x1730)</span><span class="sxs-lookup"><span data-stu-id="d746b-871">5936 (0x1730)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-872">Falha ao tentar usar o nome de cluster especificado porque já existe um objeto de computador habilitado com o nome fornecido no domínio.</span><span class="sxs-lookup"><span data-stu-id="d746b-872">An attempt to use the specified cluster name failed because an enabled computer object with the given name already exists in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERRO de \_ grupos não principais \_ \_ encontrados**</span><span class="sxs-lookup"><span data-stu-id="d746b-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERROR\_NONCORE\_GROUPS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-874">5937 (0x1731)</span><span class="sxs-lookup"><span data-stu-id="d746b-874">5937 (0x1731)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-875">Este cluster não pode ser destruído.</span><span class="sxs-lookup"><span data-stu-id="d746b-875">This cluster cannot be destroyed.</span></span> <span data-ttu-id="d746b-876">Ele tem grupos de aplicativos não principais que devem ser excluídos antes que o cluster possa ser destruído.</span><span class="sxs-lookup"><span data-stu-id="d746b-876">It has non-core application groups which must be deleted before the cluster can be destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**\_conflito de \_ recurso de compartilhamento de arquivo de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**ERROR\_FILE\_SHARE\_RESOURCE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-878">5938 (0x1732)</span><span class="sxs-lookup"><span data-stu-id="d746b-878">5938 (0x1732)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-879">O compartilhamento de arquivos associado ao recurso de testemunha de compartilhamento de arquivos não pode ser hospedado por este cluster ou por qualquer um de seus nós.</span><span class="sxs-lookup"><span data-stu-id="d746b-879">File share associated with file share witness resource cannot be hosted by this cluster or any of its nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERRO \_ ao \_ Remover \_ solicitação inválida de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERROR\_CLUSTER\_EVICT\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-881">5939 (0x1733)</span><span class="sxs-lookup"><span data-stu-id="d746b-881">5939 (0x1733)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-882">A remoção deste nó é inválida no momento.</span><span class="sxs-lookup"><span data-stu-id="d746b-882">Eviction of this node is invalid at this time.</span></span> <span data-ttu-id="d746b-883">Devido a requisitos de quorum, a remoção do nó resultará no desligamento do cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-883">Due to quorum requirements node eviction will result in cluster shutdown.</span></span> <span data-ttu-id="d746b-884">Se for o último nó no cluster, o comando destruir cluster deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="d746b-884">If it is the last node in the cluster, destroy cluster command should be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**\_ \_ recurso singleton do cluster de erros \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**ERROR\_CLUSTER\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-886">5940 (0x1734)</span><span class="sxs-lookup"><span data-stu-id="d746b-886">5940 (0x1734)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-887">Somente uma instância desse tipo de recurso é permitida no cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-887">Only one instance of this resource type is allowed in the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**ERRO \_ de \_ \_ recurso singleton do grupo de clusters \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**ERROR\_CLUSTER\_GROUP\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-889">5941 (0x1735)</span><span class="sxs-lookup"><span data-stu-id="d746b-889">5941 (0x1735)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-890">Somente uma instância desse tipo de recurso é permitida por grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d746b-890">Only one instance of this resource type is allowed per resource group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERRO \_ \_ \_ falha no provedor de recursos de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERROR\_CLUSTER\_RESOURCE\_PROVIDER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-892">5942 (0x1736)</span><span class="sxs-lookup"><span data-stu-id="d746b-892">5942 (0x1736)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-893">O recurso não pôde ficar online devido à falha de um ou mais recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="d746b-893">The resource failed to come online due to the failure of one or more provider resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**erro \_ de \_ \_ erro de configuração de recurso de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**ERROR\_CLUSTER\_RESOURCE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-895">5943 (0x1737)</span><span class="sxs-lookup"><span data-stu-id="d746b-895">5943 (0x1737)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-896">O recurso indicou que ele não pode ficar online em nenhum nó.</span><span class="sxs-lookup"><span data-stu-id="d746b-896">The resource has indicated that it cannot come online on any node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**ERRO no \_ grupo de clusters \_ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="d746b-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**ERROR\_CLUSTER\_GROUP\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-898">5944 (0x1738)</span><span class="sxs-lookup"><span data-stu-id="d746b-898">5944 (0x1738)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-899">A operação atual não pode ser executada neste grupo no momento.</span><span class="sxs-lookup"><span data-stu-id="d746b-899">The current operation cannot be performed on this group at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERRO \_ de \_ \_ volume não \_ compartilhado de cluster**</span><span class="sxs-lookup"><span data-stu-id="d746b-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERROR\_CLUSTER\_NOT\_SHARED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-901">5945 (0x1739)</span><span class="sxs-lookup"><span data-stu-id="d746b-901">5945 (0x1739)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-902">O diretório ou arquivo não está localizado em um volume compartilhado clusterizado.</span><span class="sxs-lookup"><span data-stu-id="d746b-902">The directory or file is not located on a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**ERRO \_ \_ \_ descritor de segurança inválido do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**ERROR\_CLUSTER\_INVALID\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-904">5946 (0x173A)</span><span class="sxs-lookup"><span data-stu-id="d746b-904">5946 (0x173A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-905">O descritor de segurança não atende aos requisitos de um cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-905">The Security Descriptor does not meet the requirements for a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**ERRO \_ \_ de volumes compartilhados clusterizados \_ \_ em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="d746b-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**ERROR\_CLUSTER\_SHARED\_VOLUMES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-907">5947 (0x173B)</span><span class="sxs-lookup"><span data-stu-id="d746b-907">5947 (0x173B)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-908">Há um ou mais recursos de volumes compartilhados configurados no cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-908">There is one or more shared volumes resources configured in the cluster.</span></span> <span data-ttu-id="d746b-909">Esses recursos devem ser movidos para o armazenamento disponível para que a operação tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="d746b-909">Those resources must be moved to available storage in order for operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**CLUSTER de erros \_ \_ usar a \_ API de \_ volumes compartilhados \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**ERROR\_CLUSTER\_USE\_SHARED\_VOLUMES\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-911">5948 (0x173C)</span><span class="sxs-lookup"><span data-stu-id="d746b-911">5948 (0x173C)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-912">Este grupo ou recurso não pode ser manipulado diretamente.</span><span class="sxs-lookup"><span data-stu-id="d746b-912">This group or resource cannot be directly manipulated.</span></span> <span data-ttu-id="d746b-913">Use APIs de volume compartilhado para executar a operação desejada.</span><span class="sxs-lookup"><span data-stu-id="d746b-913">Use shared volume APIs to perform desired operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERRO \_ \_ de backup \_ do cluster em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="d746b-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERROR\_CLUSTER\_BACKUP\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-915">5949 (0x173D)</span><span class="sxs-lookup"><span data-stu-id="d746b-915">5949 (0x173D)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-916">O backup está em andamento.</span><span class="sxs-lookup"><span data-stu-id="d746b-916">Back up is in progress.</span></span> <span data-ttu-id="d746b-917">Aguarde a conclusão do backup antes de tentar esta operação novamente.</span><span class="sxs-lookup"><span data-stu-id="d746b-917">Please wait for backup completion before trying this operation again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERRO \_ de \_ caminho não CSV \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERROR\_NON\_CSV\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-919">5950 (0x173E)</span><span class="sxs-lookup"><span data-stu-id="d746b-919">5950 (0x173E)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-920">O caminho não pertence a um volume compartilhado clusterizado.</span><span class="sxs-lookup"><span data-stu-id="d746b-920">The path does not belong to a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERRO \_ CSV \_ volume \_ não \_ local**</span><span class="sxs-lookup"><span data-stu-id="d746b-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERROR\_CSV\_VOLUME\_NOT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-922">5951 (0x173F)</span><span class="sxs-lookup"><span data-stu-id="d746b-922">5951 (0x173F)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-923">O volume compartilhado clusterizado não está montado localmente neste nó.</span><span class="sxs-lookup"><span data-stu-id="d746b-923">The cluster shared volume is not locally mounted on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**ERRO \_ ao \_ encerrar o WATCHDOG do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**ERROR\_CLUSTER\_WATCHDOG\_TERMINATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-925">5952 (0x1740)</span><span class="sxs-lookup"><span data-stu-id="d746b-925">5952 (0x1740)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-926">O Watchdog do cluster está sendo encerrado.</span><span class="sxs-lookup"><span data-stu-id="d746b-926">The cluster watchdog is terminating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERRO de \_ cluster de \_ recursos \_ vetado \_ mover \_ nós incompatíveis \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_INCOMPATIBLE\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-928">5953 (0x1741)</span><span class="sxs-lookup"><span data-stu-id="d746b-928">5953 (0x1741)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-929">Um recurso proibiu uma movimentação entre dois nós porque eles são incompatíveis.</span><span class="sxs-lookup"><span data-stu-id="d746b-929">A resource vetoed a move between two nodes because they are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**ERRO \_ de \_ \_ peso de nó inválido do cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**ERROR\_CLUSTER\_INVALID\_NODE\_WEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-931">5954 (0x1742)</span><span class="sxs-lookup"><span data-stu-id="d746b-931">5954 (0x1742)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-932">A solicitação é inválida porque o peso do nó não pode ser alterado enquanto o cluster estiver no modo de quorum somente de disco ou porque a alteração do peso do nó violaria os requisitos mínimos de quorum do cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-932">The request is invalid either because node weight cannot be changed while the cluster is in disk-only quorum mode, or because changing the node weight would violate the minimum cluster quorum requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERRO \_ de \_ \_ chamada vetada de recurso de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-934">5955 (0x1743)</span><span class="sxs-lookup"><span data-stu-id="d746b-934">5955 (0x1743)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-935">O recurso vetou a chamada.</span><span class="sxs-lookup"><span data-stu-id="d746b-935">The resource vetoed the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERRO \_ resmon \_ recursos do sistema \_ ausentes \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERROR\_RESMON\_SYSTEM\_RESOURCES\_LACKING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-937">5956 (0x1744)</span><span class="sxs-lookup"><span data-stu-id="d746b-937">5956 (0x1744)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-938">O recurso não pôde ser iniciado ou executado porque não pôde reservar recursos de sistema suficientes.</span><span class="sxs-lookup"><span data-stu-id="d746b-938">Resource could not start or run because it could not reserve sufficient system resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**ERRO \_ \_ de cluster \_ vetado \_ de recurso mover \_ não \_ há \_ recursos suficientes \_ no \_ destino**</span><span class="sxs-lookup"><span data-stu-id="d746b-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_DESTINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-940">5957 (0x1745)</span><span class="sxs-lookup"><span data-stu-id="d746b-940">5957 (0x1745)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-941">Um recurso proibiu uma movimentação entre dois nós porque o destino atualmente não tem recursos suficientes para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-941">A resource vetoed a move between two nodes because the destination currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERRO \_ \_ de cluster \_ vetado \_ de recurso mover \_ não \_ há \_ recursos suficientes \_ na \_ origem**</span><span class="sxs-lookup"><span data-stu-id="d746b-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-943">5958 (0x1746)</span><span class="sxs-lookup"><span data-stu-id="d746b-943">5958 (0x1746)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-944">Um recurso proibiu uma movimentação entre dois nós porque a origem atualmente não tem recursos suficientes para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-944">A resource vetoed a move between two nodes because the source currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERRO no \_ grupo de clusters \_ \_ na fila**</span><span class="sxs-lookup"><span data-stu-id="d746b-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERROR\_CLUSTER\_GROUP\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-946">5959 (0x1747)</span><span class="sxs-lookup"><span data-stu-id="d746b-946">5959 (0x1747)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-947">A operação solicitada não pode ser concluída porque o grupo está na fila para uma operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-947">The requested operation can not be completed because the group is queued for an operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERRO \_ de \_ \_ status bloqueado do recurso de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERROR\_CLUSTER\_RESOURCE\_LOCKED\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-949">5960 (0x1748)</span><span class="sxs-lookup"><span data-stu-id="d746b-949">5960 (0x1748)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-950">A operação solicitada não pode ser concluída porque um recurso tem status bloqueado.</span><span class="sxs-lookup"><span data-stu-id="d746b-950">The requested operation can not be completed because a resource has locked status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERRO \_ de \_ failover de volume compartilhado clusterizado \_ \_ \_ não \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="d746b-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_FAILOVER\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-952">5961 (0x1749)</span><span class="sxs-lookup"><span data-stu-id="d746b-952">5961 (0x1749)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-953">O recurso não pode ser movido para outro nó porque um volume compartilhado clusterizado vetou a operação.</span><span class="sxs-lookup"><span data-stu-id="d746b-953">The resource cannot move to another node because a cluster shared volume vetoed the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERRO \_ \_ \_ no descarregamento \_ do nó de cluster em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="d746b-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERROR\_CLUSTER\_NODE\_DRAIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-955">5962 (0x174A)</span><span class="sxs-lookup"><span data-stu-id="d746b-955">5962 (0x174A)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-956">Um descarregamento de nó já está em andamento.</span><span class="sxs-lookup"><span data-stu-id="d746b-956">A node drain is already in progress.</span></span>

<span data-ttu-id="d746b-957">Esse valor também foi chamado **\_ \_ \_ de evacuação de nó \_ de cluster de erro em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="d746b-957">This value was also named **ERROR\_CLUSTER\_NODE\_EVACUATION\_IN\_PROGRESS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERRO \_ disco de cluster \_ \_ não \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="d746b-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERROR\_CLUSTER\_DISK\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-959">5963 (0x174B)</span><span class="sxs-lookup"><span data-stu-id="d746b-959">5963 (0x174B)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-960">O armazenamento clusterizado não está conectado ao nó.</span><span class="sxs-lookup"><span data-stu-id="d746b-960">Clustered storage is not connected to the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**disco de erro \_ \_ sem \_ capacidade de CSV \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**ERROR\_DISK\_NOT\_CSV\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-962">5964 (0x174C)</span><span class="sxs-lookup"><span data-stu-id="d746b-962">5964 (0x174C)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-963">O disco não está configurado de forma a ser usado com CSV.</span><span class="sxs-lookup"><span data-stu-id="d746b-963">The disk is not configured in a way to be used with CSV.</span></span> <span data-ttu-id="d746b-964">Os discos CSV devem ter pelo menos uma partição formatada com NTFS.</span><span class="sxs-lookup"><span data-stu-id="d746b-964">CSV disks must have at least one partition that is formatted with NTFS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**o \_ recurso \_ de erro não \_ \_ está no \_ armazenamento disponível**</span><span class="sxs-lookup"><span data-stu-id="d746b-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**ERROR\_RESOURCE\_NOT\_IN\_AVAILABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-966">5965 (0x174D)</span><span class="sxs-lookup"><span data-stu-id="d746b-966">5965 (0x174D)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-967">O recurso deve fazer parte do grupo de armazenamento disponível para concluir esta ação.</span><span class="sxs-lookup"><span data-stu-id="d746b-967">The resource must be part of the Available Storage group to complete this action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERRO \_ de \_ volume compartilhado clusterizado \_ \_ Redirecionado**</span><span class="sxs-lookup"><span data-stu-id="d746b-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-969">5966 (0x174E)</span><span class="sxs-lookup"><span data-stu-id="d746b-969">5966 (0x174E)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-970">A operação CSVFS com falha como volume está no modo Redirecionado.</span><span class="sxs-lookup"><span data-stu-id="d746b-970">CSVFS failed operation as volume is in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERRO \_ de \_ volume compartilhado clusterizado \_ \_ não \_ Redirecionado**</span><span class="sxs-lookup"><span data-stu-id="d746b-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-972">5967 (0x174F)</span><span class="sxs-lookup"><span data-stu-id="d746b-972">5967 (0x174F)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-973">A operação CSVFS com falha porque o volume não está no modo Redirecionado.</span><span class="sxs-lookup"><span data-stu-id="d746b-973">CSVFS failed operation as volume is not in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**o \_ cluster de erros \_ não pode \_ retornar \_ Propriedades**</span><span class="sxs-lookup"><span data-stu-id="d746b-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**ERROR\_CLUSTER\_CANNOT\_RETURN\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-975">5968 (0x1750)</span><span class="sxs-lookup"><span data-stu-id="d746b-975">5968 (0x1750)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-976">As propriedades do cluster não podem ser retornadas neste momento.</span><span class="sxs-lookup"><span data-stu-id="d746b-976">Cluster properties cannot be returned at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**o \_ \_ recurso \_ de cluster de erros contém uma \_ \_ área de comparação sem suporte \_ \_ para \_ \_ volumes compartilhados**</span><span class="sxs-lookup"><span data-stu-id="d746b-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**ERROR\_CLUSTER\_RESOURCE\_CONTAINS\_UNSUPPORTED\_DIFF\_AREA\_FOR\_SHARED\_VOLUMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-978">5969 (0x1751)</span><span class="sxs-lookup"><span data-stu-id="d746b-978">5969 (0x1751)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-979">O recurso de disco clusterizado contém uma área de comparação de instantâneo de software que não tem suporte para volumes compartilhados clusterizados.</span><span class="sxs-lookup"><span data-stu-id="d746b-979">The clustered disk resource contains software snapshot diff area that are not supported for Cluster Shared Volumes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**ERRO \_ o \_ recurso \_ de cluster está \_ no \_ modo de manutenção \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_IN\_MAINTENANCE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-981">5970 (0x1752)</span><span class="sxs-lookup"><span data-stu-id="d746b-981">5970 (0x1752)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-982">A operação não pode ser concluída porque o recurso está no modo de manutenção.</span><span class="sxs-lookup"><span data-stu-id="d746b-982">The operation cannot be completed because the resource is in maintenance mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERRO \_ de \_ conflito de afinidade de cluster \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERROR\_CLUSTER\_AFFINITY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-984">5971 (0x1753)</span><span class="sxs-lookup"><span data-stu-id="d746b-984">5971 (0x1753)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-985">A operação não pode ser concluída devido a conflitos de afinidade de cluster.</span><span class="sxs-lookup"><span data-stu-id="d746b-985">The operation cannot be completed because of cluster affinity conflicts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d746b-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**o \_ recurso de cluster de erros \_ é uma \_ \_ \_ máquina virtual de réplica \_**</span><span class="sxs-lookup"><span data-stu-id="d746b-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_REPLICA\_VIRTUAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d746b-987">5972 (0x1754)</span><span class="sxs-lookup"><span data-stu-id="d746b-987">5972 (0x1754)</span></span>
</dt> <dt>



<span data-ttu-id="d746b-988">A operação não pode ser concluída porque o recurso é uma máquina virtual de réplica.</span><span class="sxs-lookup"><span data-stu-id="d746b-988">The operation cannot be completed because the resource is a replica virtual machine.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="d746b-989">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d746b-989">Requirements</span></span>



| <span data-ttu-id="d746b-990">Requisito</span><span class="sxs-lookup"><span data-stu-id="d746b-990">Requirement</span></span> | <span data-ttu-id="d746b-991">Valor</span><span class="sxs-lookup"><span data-stu-id="d746b-991">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d746b-992">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d746b-992">Minimum supported client</span></span><br/> | <span data-ttu-id="d746b-993">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d746b-993">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d746b-994">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d746b-994">Minimum supported server</span></span><br/> | <span data-ttu-id="d746b-995">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d746b-995">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d746b-996">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d746b-996">Header</span></span><br/>                   | <dl> <span data-ttu-id="d746b-997"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="d746b-997"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d746b-998">Confira também</span><span class="sxs-lookup"><span data-stu-id="d746b-998">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d746b-999">Códigos de erro do sistema</span><span class="sxs-lookup"><span data-stu-id="d746b-999">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




