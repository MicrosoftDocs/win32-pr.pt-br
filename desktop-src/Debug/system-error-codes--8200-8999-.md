---
description: Descreve os códigos de erro 8200-8999 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Códigos de erro do sistema (8200-8999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164035"
---
# <a name="system-error-codes-8200-8999"></a><span data-ttu-id="2d00a-103">Códigos de erro do sistema (8200-8999)</span><span class="sxs-lookup"><span data-stu-id="2d00a-103">System Error Codes (8200-8999)</span></span>

> [!NOTE]
> <span data-ttu-id="2d00a-104">Essas informações destinam-se a desenvolvedores Depurando erros do sistema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="2d00a-105">Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2d00a-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="2d00a-106">A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) para erros 8200 a 8999.</span><span class="sxs-lookup"><span data-stu-id="2d00a-106">The following list describes [system error codes](system-error-codes.md) for errors 8200 to 8999.</span></span> <span data-ttu-id="2d00a-107">Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham.</span><span class="sxs-lookup"><span data-stu-id="2d00a-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="2d00a-108">Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="2d00a-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="2d00a-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERRO \_ DS \_ não \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERROR\_DS\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-110">8200 (0x2008)</span><span class="sxs-lookup"><span data-stu-id="2d00a-110">8200 (0x2008)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-111">Ocorreu um erro ao instalar o serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="2d00a-111">An error occurred while installing the directory service.</span></span> <span data-ttu-id="2d00a-112">Para obter mais informações, consulte o log de eventos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-112">For more information, see the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERRO \_ de \_ Associação DS \_ avaliada \_ localmente**</span><span class="sxs-lookup"><span data-stu-id="2d00a-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERROR\_DS\_MEMBERSHIP\_EVALUATED\_LOCALLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-114">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="2d00a-114">8201 (0x2009)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-115">O serviço de diretório avaliou associações de grupo localmente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-115">The directory service evaluated group memberships locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERRO \_ DS \_ sem \_ atributo \_ ou \_ valor**</span><span class="sxs-lookup"><span data-stu-id="2d00a-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERROR\_DS\_NO\_ATTRIBUTE\_OR\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-117">8202 (0x200A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-117">8202 (0x200A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-118">O atributo ou o valor do serviço de diretório especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-118">The specified directory service attribute or value does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERRO \_ de \_ \_ sintaxe de atributo inválido DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERROR\_DS\_INVALID\_ATTRIBUTE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-120">8203 (0x200B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-120">8203 (0x200B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-121">A sintaxe de atributo especificada para o serviço de diretório é inválida.</span><span class="sxs-lookup"><span data-stu-id="2d00a-121">The attribute syntax specified to the directory service is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERRO \_ de \_ tipo de atributo DS \_ \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERROR\_DS\_ATTRIBUTE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-123">8204 (0x200C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-123">8204 (0x200C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-124">O tipo de atributo especificado para o serviço de diretório não está definido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-124">The attribute type specified to the directory service is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERRO \_ o \_ atributo \_ ou o valor do DS \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="2d00a-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERROR\_DS\_ATTRIBUTE\_OR\_VALUE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-126">8205 (0x200D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-126">8205 (0x200D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-127">O atributo ou o valor do serviço de diretório especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-127">The specified directory service attribute or value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERRO \_ DS \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERROR\_DS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-129">8206 (0x200E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-129">8206 (0x200E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-130">O serviço de diretório está ocupado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-130">The directory service is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERRO \_ DS \_ não disponível**</span><span class="sxs-lookup"><span data-stu-id="2d00a-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-132">8207 (0x200F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-132">8207 (0x200F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-133">O serviço de diretório não está disponível.</span><span class="sxs-lookup"><span data-stu-id="2d00a-133">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERRO \_ DS \_ nenhum \_ RIDs \_ alocado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERROR\_DS\_NO\_RIDS\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-135">8208 (0x2010)</span><span class="sxs-lookup"><span data-stu-id="2d00a-135">8208 (0x2010)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-136">O serviço de diretório não pôde alocar um identificador relativo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-136">The directory service was unable to allocate a relative identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERRO \_ DS \_ não \_ mais \_ RIDs**</span><span class="sxs-lookup"><span data-stu-id="2d00a-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERROR\_DS\_NO\_MORE\_RIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-138">8209 (0x2011)</span><span class="sxs-lookup"><span data-stu-id="2d00a-138">8209 (0x2011)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-139">O serviço de diretório esgotou o pool de identificadores relativos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-139">The directory service has exhausted the pool of relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERRO \_ \_ proprietário da \_ função incorreta do DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERROR\_DS\_INCORRECT\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-141">8210 (0x2012)</span><span class="sxs-lookup"><span data-stu-id="2d00a-141">8210 (0x2012)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-142">A operação solicitada não pôde ser executada porque o serviço de diretório não é o mestre para esse tipo de operação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-142">The requested operation could not be performed because the directory service is not the master for that type of operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**ERRO \_ DS \_ RIDMGR \_ erro de inicialização \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**ERROR\_DS\_RIDMGR\_INIT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-144">8211 (0x2013)</span><span class="sxs-lookup"><span data-stu-id="2d00a-144">8211 (0x2013)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-145">O serviço de diretório não pôde inicializar o subsistema que aloca identificadores relativos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-145">The directory service was unable to initialize the subsystem that allocates relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERRO \_ de \_ \_ violação de classe DS obj \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERROR\_DS\_OBJ\_CLASS\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-147">8212 (0x2014)</span><span class="sxs-lookup"><span data-stu-id="2d00a-147">8212 (0x2014)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-148">A operação solicitada não satisfez uma ou mais restrições associadas à classe do objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-148">The requested operation did not satisfy one or more constraints associated with the class of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERRO \_ DS \_ \_ não consegue \_ em \_ folha**</span><span class="sxs-lookup"><span data-stu-id="2d00a-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERROR\_DS\_CANT\_ON\_NON\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-150">8213 (0x2015)</span><span class="sxs-lookup"><span data-stu-id="2d00a-150">8213 (0x2015)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-151">O serviço de diretório pode executar a operação solicitada somente em um objeto folha.</span><span class="sxs-lookup"><span data-stu-id="2d00a-151">The directory service can perform the requested operation only on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERRO \_ DS não \_ consegue \_ no \_ RDN**</span><span class="sxs-lookup"><span data-stu-id="2d00a-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERROR\_DS\_CANT\_ON\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-153">8214 (0x2016)</span><span class="sxs-lookup"><span data-stu-id="2d00a-153">8214 (0x2016)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-154">O serviço de diretório não pode executar a operação solicitada no atributo RDN de um objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-154">The directory service cannot perform the requested operation on the RDN attribute of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERRO DS não é possível \_ \_ \_ \_ \_ classe obj**</span><span class="sxs-lookup"><span data-stu-id="2d00a-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERROR\_DS\_CANT\_MOD\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-156">8215 (0x2017)</span><span class="sxs-lookup"><span data-stu-id="2d00a-156">8215 (0x2017)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-157">O serviço de diretório detectou uma tentativa de modificar a classe de objeto de um objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-157">The directory service detected an attempt to modify the object class of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**erro ao mover o erro \_ \_ entre \_ dom do \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**ERROR\_DS\_CROSS\_DOM\_MOVE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-159">8216 (0x2018)</span><span class="sxs-lookup"><span data-stu-id="2d00a-159">8216 (0x2018)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-160">Não foi possível executar a operação de movimentação entre domínios solicitada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-160">The requested cross-domain move operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERRO \_ DS \_ GC \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="2d00a-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERROR\_DS\_GC\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-162">8217 (0x2019)</span><span class="sxs-lookup"><span data-stu-id="2d00a-162">8217 (0x2019)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-163">Não é possível contatar o servidor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="2d00a-163">Unable to contact the global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERRO \_ de \_ política compartilhada**</span><span class="sxs-lookup"><span data-stu-id="2d00a-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERROR\_SHARED\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-165">8218 (0x201A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-165">8218 (0x201A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-166">O objeto de política é compartilhado e só pode ser modificado na raiz.</span><span class="sxs-lookup"><span data-stu-id="2d00a-166">The policy object is shared and can only be modified at the root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**objeto de política de erro \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**ERROR\_POLICY\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-168">8219 (0x201B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-168">8219 (0x201B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-169">O objeto de política não existe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-169">The policy object does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_política \_ de erro somente \_ no \_ DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**ERROR\_POLICY\_ONLY\_IN\_DS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-171">8220 (0x201C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-171">8220 (0x201C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-172">As informações de política solicitadas só estão no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="2d00a-172">The requested policy information is only in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**promoção de erros \_ \_ ativa**</span><span class="sxs-lookup"><span data-stu-id="2d00a-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**ERROR\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-174">8221 (0x201D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-174">8221 (0x201D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-175">Uma promoção do controlador de domínio está ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="2d00a-175">A domain controller promotion is currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERRO \_ sem \_ promoção \_ ativa**</span><span class="sxs-lookup"><span data-stu-id="2d00a-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERROR\_NO\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-177">8222 (0x201E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-177">8222 (0x201E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-178">Uma promoção do controlador de domínio não está ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="2d00a-178">A domain controller promotion is not currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**erro \_ de \_ operações \_ DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**ERROR\_DS\_OPERATIONS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-180">8224 (0x2020)</span><span class="sxs-lookup"><span data-stu-id="2d00a-180">8224 (0x2020)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-181">Ocorreu um erro de operação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-181">An operations error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**erro \_ de \_ erro de protocolo DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**ERROR\_DS\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-183">8225 (0x2021)</span><span class="sxs-lookup"><span data-stu-id="2d00a-183">8225 (0x2021)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-184">Erro de protocolo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-184">A protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERRO \_ de \_ limite de DS \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERROR\_DS\_TIMELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-186">8226 (0x2022)</span><span class="sxs-lookup"><span data-stu-id="2d00a-186">8226 (0x2022)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-187">O limite de tempo para esta solicitação foi excedido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-187">The time limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERRO \_ \_ SIZELIMIT DS \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERROR\_DS\_SIZELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-189">8227 (0x2023)</span><span class="sxs-lookup"><span data-stu-id="2d00a-189">8227 (0x2023)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-190">O limite de tamanho para esta solicitação foi excedido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-190">The size limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERRO \_ de \_ limite de administrador DS \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERROR\_DS\_ADMIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-192">8228 (0x2024)</span><span class="sxs-lookup"><span data-stu-id="2d00a-192">8228 (0x2024)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-193">O limite administrativo para esta solicitação foi excedido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-193">The administrative limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERRO \_ de \_ comparação de DS \_ falso**</span><span class="sxs-lookup"><span data-stu-id="2d00a-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERROR\_DS\_COMPARE\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-195">8229 (0x2025)</span><span class="sxs-lookup"><span data-stu-id="2d00a-195">8229 (0x2025)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-196">A resposta de comparação foi falsa.</span><span class="sxs-lookup"><span data-stu-id="2d00a-196">The compare response was false.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERRO \_ de \_ comparação de DS \_ verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="2d00a-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERROR\_DS\_COMPARE\_TRUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-198">8230 (0x2026)</span><span class="sxs-lookup"><span data-stu-id="2d00a-198">8230 (0x2026)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-199">A resposta de comparação foi verdadeira.</span><span class="sxs-lookup"><span data-stu-id="2d00a-199">The compare response was true.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERRO \_ \_ \_ \_ não \_ há suporte para o método de autenticação DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERROR\_DS\_AUTH\_METHOD\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-201">8231 (0x2027)</span><span class="sxs-lookup"><span data-stu-id="2d00a-201">8231 (0x2027)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-202">O servidor não dá suporte ao método de autenticação solicitado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-202">The requested authentication method is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERRO \_ de \_ autenticação forte de DS \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="2d00a-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERROR\_DS\_STRONG\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-204">8232 (0x2028)</span><span class="sxs-lookup"><span data-stu-id="2d00a-204">8232 (0x2028)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-205">Um método de autenticação mais seguro é necessário para este servidor.</span><span class="sxs-lookup"><span data-stu-id="2d00a-205">A more secure authentication method is required for this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERRO \_ de \_ autenticação inadequada de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERROR\_DS\_INAPPROPRIATE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-207">8233 (0x2029)</span><span class="sxs-lookup"><span data-stu-id="2d00a-207">8233 (0x2029)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-208">Autenticação inadequada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-208">Inappropriate authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERRO \_ de \_ autenticação DS \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERROR\_DS\_AUTH\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-210">8234 (0x202A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-210">8234 (0x202A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-211">O mecanismo de autenticação é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-211">The authentication mechanism is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**ERRO \_ de \_ referência DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**ERROR\_DS\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-213">8235 (0x202B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-213">8235 (0x202B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-214">Uma referência foi retornada do servidor.</span><span class="sxs-lookup"><span data-stu-id="2d00a-214">A referral was returned from the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERRO \_ de \_ extensão de crit não disponível DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERROR\_DS\_UNAVAILABLE\_CRIT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-216">8236 (0x202C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-216">8236 (0x202C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-217">O servidor não oferece suporte à extensão crítica solicitada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-217">The server does not support the requested critical extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERRO \_ de \_ confidencialidade de DS \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="2d00a-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERROR\_DS\_CONFIDENTIALITY\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-219">8237 (0x202D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-219">8237 (0x202D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-220">Essa solicitação requer uma conexão segura.</span><span class="sxs-lookup"><span data-stu-id="2d00a-220">This request requires a secure connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERRO \_ de \_ correspondência inadequada ao DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERROR\_DS\_INAPPROPRIATE\_MATCHING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-222">8238 (0x202E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-222">8238 (0x202E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-223">Correspondência inadequada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-223">Inappropriate matching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERRO \_ de \_ violação de restrição DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERROR\_DS\_CONSTRAINT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-225">8239 (0x202F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-225">8239 (0x202F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-226">Ocorreu uma violação de restrição.</span><span class="sxs-lookup"><span data-stu-id="2d00a-226">A constraint violation occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERRO \_ DS \_ não é \_ tal \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="2d00a-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERROR\_DS\_NO\_SUCH\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-228">8240 (0x2030)</span><span class="sxs-lookup"><span data-stu-id="2d00a-228">8240 (0x2030)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-229">Esse objeto não existe no servidor.</span><span class="sxs-lookup"><span data-stu-id="2d00a-229">There is no such object on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERRO \_ de \_ alias de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERROR\_DS\_ALIAS\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-231">8241 (0x2031)</span><span class="sxs-lookup"><span data-stu-id="2d00a-231">8241 (0x2031)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-232">Há um problema de alias.</span><span class="sxs-lookup"><span data-stu-id="2d00a-232">There is an alias problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERRO \_ de \_ \_ sintaxe DN inválida DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERROR\_DS\_INVALID\_DN\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-234">8242 (0x2032)</span><span class="sxs-lookup"><span data-stu-id="2d00a-234">8242 (0x2032)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-235">Uma sintaxe de DN inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-235">An invalid dn syntax has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**ERRO \_ DS \_ é \_ folha**</span><span class="sxs-lookup"><span data-stu-id="2d00a-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**ERROR\_DS\_IS\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-237">8243 (0x2033)</span><span class="sxs-lookup"><span data-stu-id="2d00a-237">8243 (0x2033)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-238">O objeto é um objeto folha.</span><span class="sxs-lookup"><span data-stu-id="2d00a-238">The object is a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERRO \_ do \_ alias DS \_ DEREF \_ problema**</span><span class="sxs-lookup"><span data-stu-id="2d00a-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERROR\_DS\_ALIAS\_DEREF\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-240">8244 (0x2034)</span><span class="sxs-lookup"><span data-stu-id="2d00a-240">8244 (0x2034)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-241">Há um problema de desreferenciamento de alias.</span><span class="sxs-lookup"><span data-stu-id="2d00a-241">There is an alias dereferencing problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERRO \_ DS não \_ funcionado \_ para \_ executar**</span><span class="sxs-lookup"><span data-stu-id="2d00a-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERROR\_DS\_UNWILLING\_TO\_PERFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-243">8245 (0x2035)</span><span class="sxs-lookup"><span data-stu-id="2d00a-243">8245 (0x2035)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-244">O servidor não vai processar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-244">The server is unwilling to process the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERRO \_ de \_ detecção de loop DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERROR\_DS\_LOOP\_DETECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-246">8246 (0x2036)</span><span class="sxs-lookup"><span data-stu-id="2d00a-246">8246 (0x2036)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-247">Um loop foi detectado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-247">A loop has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERRO \_ de \_ violação de nomenclatura de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERROR\_DS\_NAMING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-249">8247 (0x2037)</span><span class="sxs-lookup"><span data-stu-id="2d00a-249">8247 (0x2037)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-250">Há uma violação de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="2d00a-250">There is a naming violation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERRO \_ de \_ objeto \_ DS \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="2d00a-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERROR\_DS\_OBJECT\_RESULTS\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-252">8248 (0x2038)</span><span class="sxs-lookup"><span data-stu-id="2d00a-252">8248 (0x2038)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-253">O conjunto de resultados é muito grande.</span><span class="sxs-lookup"><span data-stu-id="2d00a-253">The result set is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERRO o \_ DS \_ afeta \_ vários \_ DSAs**</span><span class="sxs-lookup"><span data-stu-id="2d00a-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERROR\_DS\_AFFECTS\_MULTIPLE\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-255">8249 (0x2039)</span><span class="sxs-lookup"><span data-stu-id="2d00a-255">8249 (0x2039)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-256">A operação afeta vários DSAs.</span><span class="sxs-lookup"><span data-stu-id="2d00a-256">The operation affects multiple DSAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERRO \_ de \_ servidor DS \_ inoperante**</span><span class="sxs-lookup"><span data-stu-id="2d00a-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERROR\_DS\_SERVER\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-258">8250 (0x203A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-258">8250 (0x203A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-259">O servidor não está operacional.</span><span class="sxs-lookup"><span data-stu-id="2d00a-259">The server is not operational.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**erro \_ de \_ local \_ DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**ERROR\_DS\_LOCAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-261">8251 (0x203B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-261">8251 (0x203B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-262">Ocorreu um erro local.</span><span class="sxs-lookup"><span data-stu-id="2d00a-262">A local error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**erro \_ de \_ codificação \_ DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**ERROR\_DS\_ENCODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-264">8252 (0x203C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-264">8252 (0x203C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-265">Ocorreu um erro de codificação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-265">An encoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**erro \_ ao \_ decodificar \_ DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**ERROR\_DS\_DECODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-267">8253 (0x203D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-267">8253 (0x203D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-268">Ocorreu um erro de decodificação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-268">A decoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERRO \_ de \_ filtro DS \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERROR\_DS\_FILTER\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-270">8254 (0x203E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-270">8254 (0x203E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-271">Não é possível reconhecer o filtro de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="2d00a-271">The search filter cannot be recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**erro \_ de \_ erro de parâmetro DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**ERROR\_DS\_PARAM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-273">8255 (0x203F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-273">8255 (0x203F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-274">Um ou mais parâmetros são ilegais.</span><span class="sxs-lookup"><span data-stu-id="2d00a-274">One or more parameters are illegal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERRO \_ DS \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="2d00a-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERROR\_DS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-276">8256 (0x2040)</span><span class="sxs-lookup"><span data-stu-id="2d00a-276">8256 (0x2040)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-277">Não há suporte para o método especificado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-277">The specified method is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERRO \_ DS \_ nenhum \_ resultado \_ retornado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERROR\_DS\_NO\_RESULTS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-279">8257 (0x2041)</span><span class="sxs-lookup"><span data-stu-id="2d00a-279">8257 (0x2041)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-280">Nenhum resultado foi retornado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-280">No results were returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERRO \_ de \_ controle DS \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERROR\_DS\_CONTROL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-282">8258 (0x2042)</span><span class="sxs-lookup"><span data-stu-id="2d00a-282">8258 (0x2042)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-283">O servidor não dá suporte ao controle especificado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-283">The specified control is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERRO \_ de \_ loop de cliente DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERROR\_DS\_CLIENT\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-285">8259 (0x2043)</span><span class="sxs-lookup"><span data-stu-id="2d00a-285">8259 (0x2043)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-286">Um loop de referência foi detectado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-286">A referral loop was detected by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERRO \_ \_ limite de referências DS \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERROR\_DS\_REFERRAL\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-288">8260 (0x2044)</span><span class="sxs-lookup"><span data-stu-id="2d00a-288">8260 (0x2044)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-289">O limite de referência predefinido foi excedido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-289">The preset referral limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERRO \_ de \_ controle de classificação DS \_ \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="2d00a-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERROR\_DS\_SORT\_CONTROL\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-291">8261 (0x2045)</span><span class="sxs-lookup"><span data-stu-id="2d00a-291">8261 (0x2045)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-292">A pesquisa requer um controle SORT.</span><span class="sxs-lookup"><span data-stu-id="2d00a-292">The search requires a SORT control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**erro \_ \_ ao intervalo de deslocamento DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**ERROR\_DS\_OFFSET\_RANGE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-294">8262 (0x2046)</span><span class="sxs-lookup"><span data-stu-id="2d00a-294">8262 (0x2046)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-295">Os resultados da pesquisa excedem o intervalo de deslocamento especificado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-295">The search results exceed the offset range specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERRO \_ \_ RIDMGR DS \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERROR\_DS\_RIDMGR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-297">8263 (0x2047)</span><span class="sxs-lookup"><span data-stu-id="2d00a-297">8263 (0x2047)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-298">O serviço de diretório detectou que o subsistema que aloca identificadores relativos está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-298">The directory service detected the subsystem that allocates relative identifiers is disabled.</span></span> <span data-ttu-id="2d00a-299">Isso pode ocorrer como um mecanismo de proteção quando o sistema determina que uma parte significativa de RIDs (identificadores relativos) foi esgotada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-299">This can occur as a protective mechanism when the system determines a significant portion of relative identifiers (RIDs) have been exhausted.</span></span> <span data-ttu-id="2d00a-300">Consulte <https://go.microsoft.com/fwlink/p/?linkid=228610> para obter as etapas de diagnóstico recomendadas e o procedimento para reabilitar a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-300">Please see <https://go.microsoft.com/fwlink/p/?linkid=228610> for recommended diagnostic steps and the procedure to re-enable account creation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**ERRO \_ a \_ raiz DS \_ deve \_ ser \_ NC**</span><span class="sxs-lookup"><span data-stu-id="2d00a-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**ERROR\_DS\_ROOT\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-302">8301 (0x206D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-302">8301 (0x206D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-303">O objeto raiz deve ser o cabeçalho de um contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="2d00a-303">The root object must be the head of a naming context.</span></span> <span data-ttu-id="2d00a-304">O objeto raiz não pode ter um pai instanciado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-304">The root object cannot have an instantiated parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERRO \_ DS \_ Adicionar \_ réplica \_ inibido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERROR\_DS\_ADD\_REPLICA\_INHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-306">8302 (0x206E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-306">8302 (0x206E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-307">Não é possível executar a operação de adição de réplica.</span><span class="sxs-lookup"><span data-stu-id="2d00a-307">The add replica operation cannot be performed.</span></span> <span data-ttu-id="2d00a-308">O contexto de nomenclatura deve ser gravável para criar a réplica.</span><span class="sxs-lookup"><span data-stu-id="2d00a-308">The naming context must be writeable in order to create the replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERRO \_ DS \_ ATT \_ não \_ Def \_ no \_ esquema**</span><span class="sxs-lookup"><span data-stu-id="2d00a-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-310">8303 (0x206F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-310">8303 (0x206F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-311">Ocorreu uma referência a um atributo que não está definido no esquema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-311">A reference to an attribute that is not defined in the schema occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERRO \_ de \_ tamanho máximo de obj de DS \_ \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERROR\_DS\_MAX\_OBJ\_SIZE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-313">8304 (0x2070)</span><span class="sxs-lookup"><span data-stu-id="2d00a-313">8304 (0x2070)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-314">O tamanho máximo de um objeto foi excedido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-314">The maximum size of an object has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERRO \_ o \_ nome da cadeia de caracteres DS obj \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="2d00a-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERROR\_DS\_OBJ\_STRING\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-316">8305 (0x2071)</span><span class="sxs-lookup"><span data-stu-id="2d00a-316">8305 (0x2071)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-317">Foi feita uma tentativa de adicionar um objeto ao diretório com um nome que já está em uso.</span><span class="sxs-lookup"><span data-stu-id="2d00a-317">An attempt was made to add an object to the directory with a name that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERRO \_ DS \_ nenhum \_ RDN \_ definido \_ no \_ esquema**</span><span class="sxs-lookup"><span data-stu-id="2d00a-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERROR\_DS\_NO\_RDN\_DEFINED\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-319">8306 (0x2072)</span><span class="sxs-lookup"><span data-stu-id="2d00a-319">8306 (0x2072)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-320">Foi feita uma tentativa de adicionar um objeto de uma classe que não tem um RDN definido no esquema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-320">An attempt was made to add an object of a class that does not have an RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERRO o \_ RDN de DS não \_ \_ \_ corresponde ao \_ esquema**</span><span class="sxs-lookup"><span data-stu-id="2d00a-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERROR\_DS\_RDN\_DOESNT\_MATCH\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-322">8307 (0x2073)</span><span class="sxs-lookup"><span data-stu-id="2d00a-322">8307 (0x2073)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-323">Foi feita uma tentativa de adicionar um objeto usando um RDN que não é o RDN definido no esquema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-323">An attempt was made to add an object using an RDN that is not the RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERRO \_ DS \_ nenhum \_ \_ atts solicitado \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERROR\_DS\_NO\_REQUESTED\_ATTS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-325">8308 (0x2074)</span><span class="sxs-lookup"><span data-stu-id="2d00a-325">8308 (0x2074)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-326">Nenhum dos atributos solicitados foi encontrado nos objetos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-326">None of the requested attributes were found on the objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERRO \_ \_ \_ de buffer de usuário DS \_ para \_ pequeno**</span><span class="sxs-lookup"><span data-stu-id="2d00a-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERROR\_DS\_USER\_BUFFER\_TO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-328">8309 (0x2075)</span><span class="sxs-lookup"><span data-stu-id="2d00a-328">8309 (0x2075)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-329">O buffer do usuário é muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="2d00a-329">The user buffer is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERRO \_ DS \_ ATT \_ \_ não está \_ em \_ obj**</span><span class="sxs-lookup"><span data-stu-id="2d00a-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERROR\_DS\_ATT\_IS\_NOT\_ON\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-331">8310 (0x2076)</span><span class="sxs-lookup"><span data-stu-id="2d00a-331">8310 (0x2076)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-332">O atributo especificado na operação não está presente no objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-332">The attribute specified in the operation is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERRO \_ DS \_ de \_ operação mod ilegal \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERROR\_DS\_ILLEGAL\_MOD\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-334">8311 (0x2077)</span><span class="sxs-lookup"><span data-stu-id="2d00a-334">8311 (0x2077)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-335">Operação de modificação inválida.</span><span class="sxs-lookup"><span data-stu-id="2d00a-335">Illegal modify operation.</span></span> <span data-ttu-id="2d00a-336">Não é permitido algum aspecto da modificação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-336">Some aspect of the modification is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERRO \_ DS \_ obj \_ muito \_ grande**</span><span class="sxs-lookup"><span data-stu-id="2d00a-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERROR\_DS\_OBJ\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-338">8312 (0x2078)</span><span class="sxs-lookup"><span data-stu-id="2d00a-338">8312 (0x2078)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-339">O objeto especificado é muito grande.</span><span class="sxs-lookup"><span data-stu-id="2d00a-339">The specified object is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERRO \_ \_ tipo de \_ instância inválido DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERROR\_DS\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-341">8313 (0x2079)</span><span class="sxs-lookup"><span data-stu-id="2d00a-341">8313 (0x2079)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-342">O tipo de instância especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-342">The specified instance type is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERRO \_ \_ MASTERDSA DS \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="2d00a-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERROR\_DS\_MASTERDSA\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-344">8314 (0x207A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-344">8314 (0x207A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-345">A operação deve ser executada em um DSA mestre.</span><span class="sxs-lookup"><span data-stu-id="2d00a-345">The operation must be performed at a master DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**ERRO \_ de \_ classe de objeto DS \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="2d00a-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**ERROR\_DS\_OBJECT\_CLASS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-347">8315 (0x207B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-347">8315 (0x207B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-348">O atributo de classe de objeto deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-348">The object class attribute must be specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERRO \_ DS \_ ausente \_ na \_ ATT necessária**</span><span class="sxs-lookup"><span data-stu-id="2d00a-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERROR\_DS\_MISSING\_REQUIRED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-350">8316 (0x207C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-350">8316 (0x207C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-351">Um atributo necessário está ausente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-351">A required attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERRO \_ DS \_ ATT \_ não \_ Def \_ para \_ classe**</span><span class="sxs-lookup"><span data-stu-id="2d00a-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_FOR\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-353">8317 (0x207D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-353">8317 (0x207D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-354">Foi feita uma tentativa de modificar um objeto para incluir um atributo que não é válido para sua classe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-354">An attempt was made to modify an object to include an attribute that is not legal for its class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERRO o \_ DS \_ ATT \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="2d00a-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERROR\_DS\_ATT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-356">8318 (0x207E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-356">8318 (0x207E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-357">O atributo especificado já está presente no objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-357">The specified attribute is already present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERRO \_ DS \_ não \_ consegue \_ Adicionar \_ valores de ATT**</span><span class="sxs-lookup"><span data-stu-id="2d00a-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERROR\_DS\_CANT\_ADD\_ATT\_VALUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-359">8320 (0x2080)</span><span class="sxs-lookup"><span data-stu-id="2d00a-359">8320 (0x2080)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-360">O atributo especificado não está presente ou não tem nenhum valor.</span><span class="sxs-lookup"><span data-stu-id="2d00a-360">The specified attribute is not present, or has no values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERRO \_ de \_ \_ restrição de valor único DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR\_DS\_SINGLE\_VALUE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-362">8321 (0x2081)</span><span class="sxs-lookup"><span data-stu-id="2d00a-362">8321 (0x2081)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-363">Vários valores foram especificados para um atributo que pode ter apenas um valor.</span><span class="sxs-lookup"><span data-stu-id="2d00a-363">Multiple values were specified for an attribute that can have only one value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERRO \_ de \_ restrição de intervalo DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERROR\_DS\_RANGE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-365">8322 (0x2082)</span><span class="sxs-lookup"><span data-stu-id="2d00a-365">8322 (0x2082)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-366">Um valor para o atributo não estava no intervalo de valores aceitável.</span><span class="sxs-lookup"><span data-stu-id="2d00a-366">A value for the attribute was not in the acceptable range of values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERRO o \_ Val de ATT de DS \_ \_ \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="2d00a-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERROR\_DS\_ATT\_VAL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-368">8323 (0x2083)</span><span class="sxs-lookup"><span data-stu-id="2d00a-368">8323 (0x2083)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-369">O valor especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-369">The specified value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERRO \_ DS \_ \_ não consegue REM \_ faltando \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="2d00a-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-371">8324 (0x2084)</span><span class="sxs-lookup"><span data-stu-id="2d00a-371">8324 (0x2084)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-372">O atributo não pode ser removido porque não está presente no objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-372">The attribute cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERRO \_ DS \_ \_ não consegue REM \_ falta de \_ ATT \_ Val**</span><span class="sxs-lookup"><span data-stu-id="2d00a-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT\_VAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-374">8325 (0x2085)</span><span class="sxs-lookup"><span data-stu-id="2d00a-374">8325 (0x2085)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-375">O valor do atributo não pode ser removido porque ele não está presente no objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-375">The attribute value cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**o \_ erro \_ raiz \_ DS \_ não é \_ SUBREF**</span><span class="sxs-lookup"><span data-stu-id="2d00a-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERROR\_DS\_ROOT\_CANT\_BE\_SUBREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-377">8326 (0x2086)</span><span class="sxs-lookup"><span data-stu-id="2d00a-377">8326 (0x2086)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-378">O objeto raiz especificado não pode ser um subref.</span><span class="sxs-lookup"><span data-stu-id="2d00a-378">The specified root object cannot be a subref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERRO \_ DS \_ sem \_ encadeamento**</span><span class="sxs-lookup"><span data-stu-id="2d00a-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERROR\_DS\_NO\_CHAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-380">8327 (0x2087)</span><span class="sxs-lookup"><span data-stu-id="2d00a-380">8327 (0x2087)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-381">O encadeamento não é permitido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-381">Chaining is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERRO \_ DS \_ sem \_ avaliação encadeada \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERROR\_DS\_NO\_CHAINED\_EVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-383">8328 (0x2088)</span><span class="sxs-lookup"><span data-stu-id="2d00a-383">8328 (0x2088)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-384">A avaliação encadeada não é permitida.</span><span class="sxs-lookup"><span data-stu-id="2d00a-384">Chained evaluation is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERRO \_ DS \_ sem \_ \_ objeto pai**</span><span class="sxs-lookup"><span data-stu-id="2d00a-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERROR\_DS\_NO\_PARENT\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-386">8329 (0x2089)</span><span class="sxs-lookup"><span data-stu-id="2d00a-386">8329 (0x2089)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-387">A operação não pôde ser executada porque o pai do objeto está não instanciado ou foi excluído.</span><span class="sxs-lookup"><span data-stu-id="2d00a-387">The operation could not be performed because the object's parent is either uninstantiated or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERRO \_ \_ o pai do DS \_ é \_ um \_ alias**</span><span class="sxs-lookup"><span data-stu-id="2d00a-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERROR\_DS\_PARENT\_IS\_AN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-389">8330 (0x208A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-389">8330 (0x208A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-390">Não é permitido ter um pai que seja um alias.</span><span class="sxs-lookup"><span data-stu-id="2d00a-390">Having a parent that is an alias is not permitted.</span></span> <span data-ttu-id="2d00a-391">Os aliases são objetos folha.</span><span class="sxs-lookup"><span data-stu-id="2d00a-391">Aliases are leaf objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERRO \_ DS não \_ consegue \_ misturar \_ mestre \_ e \_ representantes**</span><span class="sxs-lookup"><span data-stu-id="2d00a-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERROR\_DS\_CANT\_MIX\_MASTER\_AND\_REPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-393">8331 (0x208B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-393">8331 (0x208B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-394">O objeto e o pai devem ser do mesmo tipo, tanto os mestres quanto as duas réplicas.</span><span class="sxs-lookup"><span data-stu-id="2d00a-394">The object and parent must be of the same type, either both masters or both replicas.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERRO \_ os \_ filhos do DS \_ existem**</span><span class="sxs-lookup"><span data-stu-id="2d00a-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERROR\_DS\_CHILDREN\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-396">8332 (0x208C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-396">8332 (0x208C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-397">A operação não pode ser executada porque existem objetos filho.</span><span class="sxs-lookup"><span data-stu-id="2d00a-397">The operation cannot be performed because child objects exist.</span></span> <span data-ttu-id="2d00a-398">Esta operação só pode ser executada em um objeto folha.</span><span class="sxs-lookup"><span data-stu-id="2d00a-398">This operation can only be performed on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERRO \_ \_ obj DS \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERROR\_DS\_OBJ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-400">8333 (0x208D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-400">8333 (0x208D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-401">Objeto de diretório não encontrado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-401">Directory object not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERRO \_ \_ obj. alias \_ DS \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="2d00a-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERROR\_DS\_ALIASED\_OBJ\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-403">8334 (0x208E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-403">8334 (0x208E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-404">O objeto com alias está ausente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-404">The aliased object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERRO \_ de \_ \_ sintaxe de nome insatisfatório DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERROR\_DS\_BAD\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-406">8335 (0x208F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-406">8335 (0x208F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-407">O nome do objeto tem uma sintaxe inadequada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-407">The object name has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**ERRO \_ \_ \_ de pontos de alias DS \_ para \_ alias**</span><span class="sxs-lookup"><span data-stu-id="2d00a-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**ERROR\_DS\_ALIAS\_POINTS\_TO\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-409">8336 (0x2090)</span><span class="sxs-lookup"><span data-stu-id="2d00a-409">8336 (0x2090)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-410">Não é permitido que um alias faça referência a outro alias.</span><span class="sxs-lookup"><span data-stu-id="2d00a-410">It is not permitted for an alias to refer to another alias.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERRO DS não é possível \_ \_ \_ DEREF \_ alias**</span><span class="sxs-lookup"><span data-stu-id="2d00a-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERROR\_DS\_CANT\_DEREF\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-412">8337 (0x2091)</span><span class="sxs-lookup"><span data-stu-id="2d00a-412">8337 (0x2091)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-413">Não é possível desreferenciar o alias.</span><span class="sxs-lookup"><span data-stu-id="2d00a-413">The alias cannot be dereferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERRO \_ DS \_ fora \_ do \_ escopo**</span><span class="sxs-lookup"><span data-stu-id="2d00a-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERROR\_DS\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-415">8338 (0x2092)</span><span class="sxs-lookup"><span data-stu-id="2d00a-415">8338 (0x2092)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-416">A operação está fora do escopo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-416">The operation is out of scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERRO \_ de \_ objeto DS \_ sendo \_ removido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERROR\_DS\_OBJECT\_BEING\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-418">8339 (0x2093)</span><span class="sxs-lookup"><span data-stu-id="2d00a-418">8339 (0x2093)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-419">A operação não pode continuar porque o objeto está no processo de ser removido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-419">The operation cannot continue because the object is in the process of being removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERRO \_ DS não \_ consegue \_ excluir \_ DSA \_ obj**</span><span class="sxs-lookup"><span data-stu-id="2d00a-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERROR\_DS\_CANT\_DELETE\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-421">8340 (0x2094)</span><span class="sxs-lookup"><span data-stu-id="2d00a-421">8340 (0x2094)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-422">O objeto DSA não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2d00a-422">The DSA object cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**erro \_ genérico erro de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**ERROR\_DS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-424">8341 (0x2095)</span><span class="sxs-lookup"><span data-stu-id="2d00a-424">8341 (0x2095)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-425">Ocorreu um erro de serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="2d00a-425">A directory service error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERRO \_ DSA de DS \_ \_ deve \_ ser um \_ \_ mestre int**</span><span class="sxs-lookup"><span data-stu-id="2d00a-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERROR\_DS\_DSA\_MUST\_BE\_INT\_MASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-427">8342 (0x2096)</span><span class="sxs-lookup"><span data-stu-id="2d00a-427">8342 (0x2096)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-428">A operação só pode ser executada em um objeto DSA mestre interno.</span><span class="sxs-lookup"><span data-stu-id="2d00a-428">The operation can only be performed on an internal master DSA object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERRO \_ de \_ classe DS \_ não \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="2d00a-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERROR\_DS\_CLASS\_NOT\_DSA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-430">8343 (0x2097)</span><span class="sxs-lookup"><span data-stu-id="2d00a-430">8343 (0x2097)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-431">O objeto deve ser da classe DSA.</span><span class="sxs-lookup"><span data-stu-id="2d00a-431">The object must be of class DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**ERRO \_ ao \_ DS \_ INSUFF \_ direitos de acesso**</span><span class="sxs-lookup"><span data-stu-id="2d00a-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**ERROR\_DS\_INSUFF\_ACCESS\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-433">8344 (0x2098)</span><span class="sxs-lookup"><span data-stu-id="2d00a-433">8344 (0x2098)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-434">Direitos de acesso insuficientes para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-434">Insufficient access rights to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERRO \_ DS \_ inválido \_ superior**</span><span class="sxs-lookup"><span data-stu-id="2d00a-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERROR\_DS\_ILLEGAL\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-436">8345 (0x2099)</span><span class="sxs-lookup"><span data-stu-id="2d00a-436">8345 (0x2099)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-437">O objeto não pode ser adicionado porque o pai não está na lista de superiores possíveis.</span><span class="sxs-lookup"><span data-stu-id="2d00a-437">The object cannot be added because the parent is not on the list of possible superiors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERRO \_ \_ de atributo DS \_ pertencente \_ a \_ Sam**</span><span class="sxs-lookup"><span data-stu-id="2d00a-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERROR\_DS\_ATTRIBUTE\_OWNED\_BY\_SAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-439">8346 (0x209A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-439">8346 (0x209A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-440">O acesso ao atributo não é permitido porque o atributo pertence ao SAM (Gerenciador de contas de segurança).</span><span class="sxs-lookup"><span data-stu-id="2d00a-440">Access to the attribute is not permitted because the attribute is owned by the Security Accounts Manager (SAM).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERRO o nome DS é um número \_ \_ excessivo de \_ \_ \_ partes**</span><span class="sxs-lookup"><span data-stu-id="2d00a-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERROR\_DS\_NAME\_TOO\_MANY\_PARTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-442">8347 (0x209B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-442">8347 (0x209B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-443">O nome tem muitas partes.</span><span class="sxs-lookup"><span data-stu-id="2d00a-443">The name has too many parts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERRO \_ de \_ nome DS \_ muito \_ longo**</span><span class="sxs-lookup"><span data-stu-id="2d00a-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERROR\_DS\_NAME\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-445">8348 (0x209C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-445">8348 (0x209C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-446">O nome é muito longo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-446">The name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERRO \_ \_ nome DS \_ valor \_ muito \_ longo**</span><span class="sxs-lookup"><span data-stu-id="2d00a-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERROR\_DS\_NAME\_VALUE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-448">8349 (0x209D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-448">8349 (0x209D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-449">O valor do nome é muito longo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-449">The name value is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERRO \_ de \_ nome DS não \_ analisável**</span><span class="sxs-lookup"><span data-stu-id="2d00a-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERROR\_DS\_NAME\_UNPARSEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-451">8350 (0x209E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-451">8350 (0x209E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-452">O serviço de diretório encontrou um erro ao analisar um nome.</span><span class="sxs-lookup"><span data-stu-id="2d00a-452">The directory service encountered an error parsing a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERRO \_ \_ tipo de nome DS \_ \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERROR\_DS\_NAME\_TYPE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-454">8351 (0x209F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-454">8351 (0x209F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-455">O serviço de diretório não pode obter o tipo de atributo para um nome.</span><span class="sxs-lookup"><span data-stu-id="2d00a-455">The directory service cannot get the attribute type for a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERRO \_ DS \_ não é \_ um \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="2d00a-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERROR\_DS\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-457">8352 (0x20A0)</span><span class="sxs-lookup"><span data-stu-id="2d00a-457">8352 (0x20A0)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-458">O nome não identifica um objeto; o nome identifica um fantasma.</span><span class="sxs-lookup"><span data-stu-id="2d00a-458">The name does not identify an object; the name identifies a phantom.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERRO \_ DS \_ s \_ desc \_ muito \_ curto**</span><span class="sxs-lookup"><span data-stu-id="2d00a-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR\_DS\_SEC\_DESC\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-460">8353 (0x20A1)</span><span class="sxs-lookup"><span data-stu-id="2d00a-460">8353 (0x20A1)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-461">O descritor de segurança é muito curto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-461">The security descriptor is too short.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERRO \_ DS \_ SEC \_ desc \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR\_DS\_SEC\_DESC\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-463">8354 (0x20A2)</span><span class="sxs-lookup"><span data-stu-id="2d00a-463">8354 (0x20A2)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-464">O descritor de segurança é inválido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-464">The security descriptor is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERRO \_ DS \_ sem \_ \_ nome excluído**</span><span class="sxs-lookup"><span data-stu-id="2d00a-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERROR\_DS\_NO\_DELETED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-466">8355 (0x20A3)</span><span class="sxs-lookup"><span data-stu-id="2d00a-466">8355 (0x20A3)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-467">Falha ao criar o nome para o objeto excluído.</span><span class="sxs-lookup"><span data-stu-id="2d00a-467">Failed to create name for deleted object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERRO \_ \_ SUBREF DS \_ deve \_ ter \_ pai**</span><span class="sxs-lookup"><span data-stu-id="2d00a-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERROR\_DS\_SUBREF\_MUST\_HAVE\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-469">8356 (0x20A4)</span><span class="sxs-lookup"><span data-stu-id="2d00a-469">8356 (0x20A4)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-470">O pai de um novo subref deve existir.</span><span class="sxs-lookup"><span data-stu-id="2d00a-470">The parent of a new subref must exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERRO \_ o \_ NCName do DS \_ deve \_ ser \_ NC**</span><span class="sxs-lookup"><span data-stu-id="2d00a-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERROR\_DS\_NCNAME\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-472">8357 (0x20A5)</span><span class="sxs-lookup"><span data-stu-id="2d00a-472">8357 (0x20A5)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-473">O objeto deve ser um contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="2d00a-473">The object must be a naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERRO \_ DS \_ não \_ consegue \_ Adicionar \_ somente sistema**</span><span class="sxs-lookup"><span data-stu-id="2d00a-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERROR\_DS\_CANT\_ADD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-475">8358 (0x20A6)</span><span class="sxs-lookup"><span data-stu-id="2d00a-475">8358 (0x20A6)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-476">Não é permitido adicionar um atributo que pertence ao sistema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-476">It is not permitted to add an attribute which is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**a \_ classe DS de erro \_ \_ deve \_ ser \_ concreta**</span><span class="sxs-lookup"><span data-stu-id="2d00a-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**ERROR\_DS\_CLASS\_MUST\_BE\_CONCRETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-478">8359 (0x20A7)</span><span class="sxs-lookup"><span data-stu-id="2d00a-478">8359 (0x20A7)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-479">A classe do objeto deve ser estrutural; Não é possível criar uma instância de uma classe abstrata.</span><span class="sxs-lookup"><span data-stu-id="2d00a-479">The class of the object must be structural; you cannot instantiate an abstract class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERRO \_ DS \_ \_ DMD inválido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERROR\_DS\_INVALID\_DMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-481">8360 (0x20A8)</span><span class="sxs-lookup"><span data-stu-id="2d00a-481">8360 (0x20A8)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-482">O objeto de esquema não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-482">The schema object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERRO \_ o \_ GUID do obj DS \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="2d00a-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERROR\_DS\_OBJ\_GUID\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-484">8361 (0x20A9)</span><span class="sxs-lookup"><span data-stu-id="2d00a-484">8361 (0x20A9)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-485">Já existe um objeto local com este GUID (Dead ou vivo).</span><span class="sxs-lookup"><span data-stu-id="2d00a-485">A local object with this GUID (dead or alive) already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERRO \_ DS \_ não \_ em \_ BACKLINK**</span><span class="sxs-lookup"><span data-stu-id="2d00a-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERROR\_DS\_NOT\_ON\_BACKLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-487">8362 (0x20AA)</span><span class="sxs-lookup"><span data-stu-id="2d00a-487">8362 (0x20AA)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-488">A operação não pode ser executada em um vínculo regressivo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-488">The operation cannot be performed on a back link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERRO \_ DS \_ sem \_ CROSSREF \_ para \_ NC**</span><span class="sxs-lookup"><span data-stu-id="2d00a-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERROR\_DS\_NO\_CROSSREF\_FOR\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-490">8363 (0x20AB)</span><span class="sxs-lookup"><span data-stu-id="2d00a-490">8363 (0x20AB)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-491">Não foi possível encontrar a referência cruzada para o contexto de nomenclatura especificado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-491">The cross reference for the specified naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERRO \_ ao \_ desligar \_ DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERROR\_DS\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-493">8364 (0x20AC)</span><span class="sxs-lookup"><span data-stu-id="2d00a-493">8364 (0x20AC)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-494">A operação não pôde ser executada porque o serviço de diretório está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-494">The operation could not be performed because the directory service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERRO \_ de \_ operação desconhecida de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERROR\_DS\_UNKNOWN\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-496">8365 (0x20AD)</span><span class="sxs-lookup"><span data-stu-id="2d00a-496">8365 (0x20AD)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-497">A solicitação de serviço de diretório é inválida.</span><span class="sxs-lookup"><span data-stu-id="2d00a-497">The directory service request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERRO \_ \_ proprietário da \_ função \_ inválido DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERROR\_DS\_INVALID\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-499">8366 (0x20AE)</span><span class="sxs-lookup"><span data-stu-id="2d00a-499">8366 (0x20AE)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-500">Não foi possível ler o atributo proprietário da função.</span><span class="sxs-lookup"><span data-stu-id="2d00a-500">The role owner attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERRO \_ DS \_ não foi possível \_ contatar \_ FSMO**</span><span class="sxs-lookup"><span data-stu-id="2d00a-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERROR\_DS\_COULDNT\_CONTACT\_FSMO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-502">8367 (0x20AF)</span><span class="sxs-lookup"><span data-stu-id="2d00a-502">8367 (0x20AF)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-503">Falha na operação FSMO solicitada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-503">The requested FSMO operation failed.</span></span> <span data-ttu-id="2d00a-504">O atual titular do FSMO não pôde ser contatado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-504">The current FSMO holder could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERRO \_ DS \_ Cross \_ NC \_ DN \_ renomear**</span><span class="sxs-lookup"><span data-stu-id="2d00a-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERROR\_DS\_CROSS\_NC\_DN\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-506">8368 (0x20B0)</span><span class="sxs-lookup"><span data-stu-id="2d00a-506">8368 (0x20B0)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-507">Não é permitido modificar um DN em um contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="2d00a-507">Modification of a DN across a naming context is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERRO \_ DS \_ \_ somente no \_ sistema \_ mod**</span><span class="sxs-lookup"><span data-stu-id="2d00a-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERROR\_DS\_CANT\_MOD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-509">8369 (0x20B1)</span><span class="sxs-lookup"><span data-stu-id="2d00a-509">8369 (0x20B1)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-510">O atributo não pode ser modificado porque pertence ao sistema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-510">The attribute cannot be modified because it is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERRO \_ \_ somente replicador \_ DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERROR\_DS\_REPLICATOR\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-512">8370 (0x20B2)</span><span class="sxs-lookup"><span data-stu-id="2d00a-512">8370 (0x20B2)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-513">Somente o replicador pode executar essa função.</span><span class="sxs-lookup"><span data-stu-id="2d00a-513">Only the replicator can perform this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERRO \_ de \_ classe de obj DS \_ \_ não \_ definida**</span><span class="sxs-lookup"><span data-stu-id="2d00a-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-515">8371 (0x20B3)</span><span class="sxs-lookup"><span data-stu-id="2d00a-515">8371 (0x20B3)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-516">A classe especificada não está definida.</span><span class="sxs-lookup"><span data-stu-id="2d00a-516">The specified class is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERRO \_ de \_ classe DS obj \_ \_ não \_ subclasse**</span><span class="sxs-lookup"><span data-stu-id="2d00a-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_SUBCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-518">8372 (0x20B4)</span><span class="sxs-lookup"><span data-stu-id="2d00a-518">8372 (0x20B4)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-519">A classe especificada não é uma subclasse.</span><span class="sxs-lookup"><span data-stu-id="2d00a-519">The specified class is not a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERRO \_ de \_ referência de nome DS \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERROR\_DS\_NAME\_REFERENCE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-521">8373 (0x20B5)</span><span class="sxs-lookup"><span data-stu-id="2d00a-521">8373 (0x20B5)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-522">A referência de nome é inválida.</span><span class="sxs-lookup"><span data-stu-id="2d00a-522">The name reference is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERRO \_ de \_ referência cruzada de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERROR\_DS\_CROSS\_REF\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-524">8374 (0x20B6)</span><span class="sxs-lookup"><span data-stu-id="2d00a-524">8374 (0x20B6)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-525">Já existe uma referência cruzada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-525">A cross reference already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERRO DS não é possível \_ \_ excluir o \_ \_ \_ CROSSREF mestre**</span><span class="sxs-lookup"><span data-stu-id="2d00a-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERROR\_DS\_CANT\_DEL\_MASTER\_CROSSREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-527">8375 (0x20B7)</span><span class="sxs-lookup"><span data-stu-id="2d00a-527">8375 (0x20B7)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-528">Não é permitido excluir uma referência cruzada mestre.</span><span class="sxs-lookup"><span data-stu-id="2d00a-528">It is not permitted to delete a master cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERRO \_ na \_ subárvore DS de \_ notificação \_ não \_ NC \_ cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="2d00a-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERROR\_DS\_SUBTREE\_NOTIFY\_NOT\_NC\_HEAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-530">8376 (0x20B8)</span><span class="sxs-lookup"><span data-stu-id="2d00a-530">8376 (0x20B8)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-531">As notificações de subárvore só têm suporte em cabeçalhos NC.</span><span class="sxs-lookup"><span data-stu-id="2d00a-531">Subtree notifications are only supported on NC heads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERRO \_ do \_ filtro de notificação DS \_ \_ muito \_ complexo**</span><span class="sxs-lookup"><span data-stu-id="2d00a-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERROR\_DS\_NOTIFY\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-533">8377 (0x20B9)</span><span class="sxs-lookup"><span data-stu-id="2d00a-533">8377 (0x20B9)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-534">O filtro de notificação é muito complexo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-534">Notification filter is too complex.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERRO \_ \_ RDN de Dup de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR\_DS\_DUP\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-536">8378 (0x20BA)</span><span class="sxs-lookup"><span data-stu-id="2d00a-536">8378 (0x20BA)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-537">Falha na atualização do esquema: RDN duplicado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-537">Schema update failed: duplicate RDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERRO \_ \_ OID de Dup de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERROR\_DS\_DUP\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-539">8379 (0x20BB)</span><span class="sxs-lookup"><span data-stu-id="2d00a-539">8379 (0x20BB)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-540">Falha na atualização do esquema: OID duplicado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-540">Schema update failed: duplicate OID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERRO \_ de \_ \_ ID MAPI do Dup de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERROR\_DS\_DUP\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-542">8380 (0x20BC)</span><span class="sxs-lookup"><span data-stu-id="2d00a-542">8380 (0x20BC)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-543">Falha na atualização do esquema: identificador MAPI duplicado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-543">Schema update failed: duplicate MAPI identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERRO \_ \_ GUID de \_ ID de esquema do DUP \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERROR\_DS\_DUP\_SCHEMA\_ID\_GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-545">8381 (0x20BD)</span><span class="sxs-lookup"><span data-stu-id="2d00a-545">8381 (0x20BD)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-546">Falha na atualização do esquema: GUID de ID de esquema duplicado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-546">Schema update failed: duplicate schema-id GUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERRO \_ \_ nome de \_ exibição LDAP de DUP \_ de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR\_DS\_DUP\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-548">8382 (0x20BE)</span><span class="sxs-lookup"><span data-stu-id="2d00a-548">8382 (0x20BE)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-549">Falha na atualização do esquema: nome de exibição LDAP duplicado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-549">Schema update failed: duplicate LDAP display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERRO \_ de \_ teste semântico de \_ ATT de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERROR\_DS\_SEMANTIC\_ATT\_TEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-551">8383 (0x20BF)</span><span class="sxs-lookup"><span data-stu-id="2d00a-551">8383 (0x20BF)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-552">Falha na atualização do esquema: intervalo inferior menor que intervalo superior.</span><span class="sxs-lookup"><span data-stu-id="2d00a-552">Schema update failed: range-lower less than range upper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERRO \_ de \_ incompatibilidade de sintaxe DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERROR\_DS\_SYNTAX\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-554">8384 (0x20C0)</span><span class="sxs-lookup"><span data-stu-id="2d00a-554">8384 (0x20C0)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-555">Falha na atualização do esquema: incompatibilidade de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-555">Schema update failed: syntax mismatch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**o erro \_ DS \_ existe \_ em \_ deve \_ ter**</span><span class="sxs-lookup"><span data-stu-id="2d00a-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**ERROR\_DS\_EXISTS\_IN\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-557">8385 (0x20C1)</span><span class="sxs-lookup"><span data-stu-id="2d00a-557">8385 (0x20C1)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-558">Falha na exclusão do esquema: o atributo é usado em deve-conter.</span><span class="sxs-lookup"><span data-stu-id="2d00a-558">Schema deletion failed: attribute is used in must-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**o erro \_ DS \_ existe \_ em \_ pode \_ ter**</span><span class="sxs-lookup"><span data-stu-id="2d00a-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**ERROR\_DS\_EXISTS\_IN\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-560">8386 (0x20C2)</span><span class="sxs-lookup"><span data-stu-id="2d00a-560">8386 (0x20C2)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-561">Falha na exclusão do esquema: o atributo é usado em maio-conter.</span><span class="sxs-lookup"><span data-stu-id="2d00a-561">Schema deletion failed: attribute is used in may-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERRO o \_ DS não \_ existente \_ pode \_ ter**</span><span class="sxs-lookup"><span data-stu-id="2d00a-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERROR\_DS\_NONEXISTENT\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-563">8387 (0x20C3)</span><span class="sxs-lookup"><span data-stu-id="2d00a-563">8387 (0x20C3)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-564">Falha na atualização do esquema: o atributo em pode-conter não existe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-564">Schema update failed: attribute in may-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**o erro \_ DS não \_ existente \_ deve \_ ter**</span><span class="sxs-lookup"><span data-stu-id="2d00a-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**ERROR\_DS\_NONEXISTENT\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-566">8388 (0x20C4)</span><span class="sxs-lookup"><span data-stu-id="2d00a-566">8388 (0x20C4)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-567">Falha na atualização do esquema: o atributo em deve-conter não existe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-567">Schema update failed: attribute in must-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERRO \_ \_ falha no \_ teste de CLS auxiliar \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERROR\_DS\_AUX\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-569">8389 (0x20C5)</span><span class="sxs-lookup"><span data-stu-id="2d00a-569">8389 (0x20C5)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-570">Falha na atualização do esquema: a classe na lista de classes auxiliares não existe ou não é uma classe auxiliar.</span><span class="sxs-lookup"><span data-stu-id="2d00a-570">Schema update failed: class in aux-class list does not exist or is not an auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERRO \_ DS não \_ existente \_ poss \_ sup**</span><span class="sxs-lookup"><span data-stu-id="2d00a-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERROR\_DS\_NONEXISTENT\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-572">8390 (0x20C6)</span><span class="sxs-lookup"><span data-stu-id="2d00a-572">8390 (0x20C6)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-573">Falha na atualização do esquema: a classe em poss-superiors não existe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-573">Schema update failed: class in poss-superiors does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERRO \_ \_ falha no \_ teste de subcls do \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERROR\_DS\_SUB\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-575">8391 (0x20C7)</span><span class="sxs-lookup"><span data-stu-id="2d00a-575">8391 (0x20C7)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-576">Falha na atualização do esquema: a classe na lista listas SubClassOf não existe ou não satisfaz as regras de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="2d00a-576">Schema update failed: class in subclassof list does not exist or does not satisfy hierarchy rules.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERRO \_ DS \_ insatisfatório \_ \_ \_ ID de \_ sintaxe do RDN**</span><span class="sxs-lookup"><span data-stu-id="2d00a-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERROR\_DS\_BAD\_RDN\_ATT\_ID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-578">8392 (0x20C8)</span><span class="sxs-lookup"><span data-stu-id="2d00a-578">8392 (0x20C8)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-579">Falha na atualização do esquema: RDN-ATT-ID tem sintaxe incorreta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-579">Schema update failed: Rdn-Att-Id has wrong syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERRO \_ o \_ DS \_ existe \_ no \_ CLS auxiliar**</span><span class="sxs-lookup"><span data-stu-id="2d00a-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERROR\_DS\_EXISTS\_IN\_AUX\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-581">8393 (0x20C9)</span><span class="sxs-lookup"><span data-stu-id="2d00a-581">8393 (0x20C9)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-582">Falha na exclusão do esquema: a classe é usada como classe auxiliar.</span><span class="sxs-lookup"><span data-stu-id="2d00a-582">Schema deletion failed: class is used as auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERRO \_ DS \_ existe \_ em \_ sub \_ CLS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERROR\_DS\_EXISTS\_IN\_SUB\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-584">8394 (0x20CA)</span><span class="sxs-lookup"><span data-stu-id="2d00a-584">8394 (0x20CA)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-585">Falha na exclusão do esquema: a classe é usada como subclasse.</span><span class="sxs-lookup"><span data-stu-id="2d00a-585">Schema deletion failed: class is used as sub class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERRO o \_ DS \_ existe \_ no \_ poss \_ sup**</span><span class="sxs-lookup"><span data-stu-id="2d00a-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERROR\_DS\_EXISTS\_IN\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-587">8395 (0x20CB)</span><span class="sxs-lookup"><span data-stu-id="2d00a-587">8395 (0x20CB)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-588">Falha na exclusão do esquema: a classe é usada como poss superior.</span><span class="sxs-lookup"><span data-stu-id="2d00a-588">Schema deletion failed: class is used as poss superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERRO \_ \_ RECALCSCHEMA DS \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="2d00a-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERROR\_DS\_RECALCSCHEMA\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-590">8396 (0x20CC)</span><span class="sxs-lookup"><span data-stu-id="2d00a-590">8396 (0x20CC)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-591">Falha na atualização do esquema ao recalcular o cache de validação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-591">Schema update failed in recalculating validation cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERRO \_ ao \_ excluir árvore de DS \_ \_ não \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="2d00a-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERROR\_DS\_TREE\_DELETE\_NOT\_FINISHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-593">8397 (0x20CD)</span><span class="sxs-lookup"><span data-stu-id="2d00a-593">8397 (0x20CD)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-594">A exclusão de árvore não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="2d00a-594">The tree deletion is not finished.</span></span> <span data-ttu-id="2d00a-595">A solicitação deve ser feita novamente para continuar a excluir a árvore.</span><span class="sxs-lookup"><span data-stu-id="2d00a-595">The request must be made again to continue deleting the tree.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERRO o \_ DS não \_ consegue \_ excluir**</span><span class="sxs-lookup"><span data-stu-id="2d00a-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERROR\_DS\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-597">8398 (0x20CE)</span><span class="sxs-lookup"><span data-stu-id="2d00a-597">8398 (0x20CE)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-598">Não foi possível executar a operação de exclusão solicitada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-598">The requested delete operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERRO \_ ID de req. de \_ esquema DS ATT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-600">8399 (0x20CF)</span><span class="sxs-lookup"><span data-stu-id="2d00a-600">8399 (0x20CF)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-601">Não é possível ler o identificador de classe de controle para o registro de esquema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-601">Cannot read the governs class identifier for the schema record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERRO \_ de \_ \_ sintaxe de \_ esquema \_ ATT Bad insatisfatório**</span><span class="sxs-lookup"><span data-stu-id="2d00a-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERROR\_DS\_BAD\_ATT\_SCHEMA\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-603">8400 (0x20D0)</span><span class="sxs-lookup"><span data-stu-id="2d00a-603">8400 (0x20D0)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-604">O esquema de atributo tem uma sintaxe inadequada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-604">The attribute schema has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERRO \_ DS não \_ consegue \_ cache \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="2d00a-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERROR\_DS\_CANT\_CACHE\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-606">8401 (0x20D1)</span><span class="sxs-lookup"><span data-stu-id="2d00a-606">8401 (0x20D1)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-607">Não foi possível armazenar o atributo em cache.</span><span class="sxs-lookup"><span data-stu-id="2d00a-607">The attribute could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERRO \_ DS não \_ consegue \_ armazenar \_ classe**</span><span class="sxs-lookup"><span data-stu-id="2d00a-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERROR\_DS\_CANT\_CACHE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-609">8402 (0x20D2)</span><span class="sxs-lookup"><span data-stu-id="2d00a-609">8402 (0x20D2)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-610">Não foi possível armazenar a classe em cache.</span><span class="sxs-lookup"><span data-stu-id="2d00a-610">The class could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERRO \_ DS não \_ consegue \_ remover o \_ cache de ATT \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_ATT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-612">8403 (0x20D3)</span><span class="sxs-lookup"><span data-stu-id="2d00a-612">8403 (0x20D3)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-613">Não foi possível remover o atributo do cache.</span><span class="sxs-lookup"><span data-stu-id="2d00a-613">The attribute could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERRO \_ DS \_ não \_ consegue \_ Remover \_ cache de classe**</span><span class="sxs-lookup"><span data-stu-id="2d00a-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_CLASS\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-615">8404 (0x20D4)</span><span class="sxs-lookup"><span data-stu-id="2d00a-615">8404 (0x20D4)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-616">A classe não pôde ser removida do cache.</span><span class="sxs-lookup"><span data-stu-id="2d00a-616">The class could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERRO \_ DS não \_ consegue \_ recuperar \_ DN**</span><span class="sxs-lookup"><span data-stu-id="2d00a-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERROR\_DS\_CANT\_RETRIEVE\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-618">8405 (0x20D5)</span><span class="sxs-lookup"><span data-stu-id="2d00a-618">8405 (0x20D5)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-619">Não foi possível ler o atributo de nome distinto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-619">The distinguished name attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERRO \_ DS \_ ausente \_ SUPREF**</span><span class="sxs-lookup"><span data-stu-id="2d00a-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERROR\_DS\_MISSING\_SUPREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-621">8406 (0x20D6)</span><span class="sxs-lookup"><span data-stu-id="2d00a-621">8406 (0x20D6)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-622">Nenhuma referência superior foi configurada para o serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="2d00a-622">No superior reference has been configured for the directory service.</span></span> <span data-ttu-id="2d00a-623">Portanto, o serviço de diretório não pode emitir referências a objetos fora desta floresta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-623">The directory service is therefore unable to issue referrals to objects outside this forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERRO \_ DS não \_ consegue \_ recuperar \_ instância**</span><span class="sxs-lookup"><span data-stu-id="2d00a-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERROR\_DS\_CANT\_RETRIEVE\_INSTANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-625">8407 (0x20D7)</span><span class="sxs-lookup"><span data-stu-id="2d00a-625">8407 (0x20D7)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-626">Não foi possível recuperar o atributo de tipo de instância.</span><span class="sxs-lookup"><span data-stu-id="2d00a-626">The instance type attribute could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERRO \_ de \_ inconsistência de código DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERROR\_DS\_CODE\_INCONSISTENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-628">8408 (0x20D8)</span><span class="sxs-lookup"><span data-stu-id="2d00a-628">8408 (0x20D8)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-629">Ocorreu um erro interno.</span><span class="sxs-lookup"><span data-stu-id="2d00a-629">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**erro \_ de \_ banco de dados DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**ERROR\_DS\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-631">8409 (0x20D9)</span><span class="sxs-lookup"><span data-stu-id="2d00a-631">8409 (0x20D9)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-632">Ocorreu um erro de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2d00a-632">A database error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERRO \_ DS \_ GOVERNSID \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="2d00a-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERROR\_DS\_GOVERNSID\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-634">8410 (0x20DA)</span><span class="sxs-lookup"><span data-stu-id="2d00a-634">8410 (0x20DA)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-635">O atributo GOVERNSID está ausente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-635">The attribute GOVERNSID is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERRO \_ DS \_ faltando \_ \_ ATT esperado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERROR\_DS\_MISSING\_EXPECTED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-637">8411 (0x20DB)</span><span class="sxs-lookup"><span data-stu-id="2d00a-637">8411 (0x20DB)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-638">Um atributo esperado está ausente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-638">An expected attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERRO \_ de \_ NCName de DS ausente na \_ \_ referência de Cr \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERROR\_DS\_NCNAME\_MISSING\_CR\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-640">8412 (0x20DC)</span><span class="sxs-lookup"><span data-stu-id="2d00a-640">8412 (0x20DC)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-641">O contexto de nomenclatura especificado não tem uma referência cruzada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-641">The specified naming context is missing a cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**erro \_ \_ ao verificar a segurança do DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**ERROR\_DS\_SECURITY\_CHECKING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-643">8413 (0x20DD)</span><span class="sxs-lookup"><span data-stu-id="2d00a-643">8413 (0x20DD)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-644">Ocorreu um erro de verificação de segurança.</span><span class="sxs-lookup"><span data-stu-id="2d00a-644">A security checking error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERRO \_ de \_ esquema DS \_ não \_ carregado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERROR\_DS\_SCHEMA\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-646">8414 (0x20DE)</span><span class="sxs-lookup"><span data-stu-id="2d00a-646">8414 (0x20DE)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-647">O esquema não está carregado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-647">The schema is not loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERRO \_ \_ \_ falha na alocação de esquema DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERROR\_DS\_SCHEMA\_ALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-649">8415 (0x20DF)</span><span class="sxs-lookup"><span data-stu-id="2d00a-649">8415 (0x20DF)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-650">Falha na alocação de esquema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-650">Schema allocation failed.</span></span> <span data-ttu-id="2d00a-651">Verifique se o computador está com pouca memória.</span><span class="sxs-lookup"><span data-stu-id="2d00a-651">Please check if the machine is running low on memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERRO \_ de \_ \_ sintaxe de req de esquema DS ATT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-653">8416 (0x20E0)</span><span class="sxs-lookup"><span data-stu-id="2d00a-653">8416 (0x20E0)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-654">Falha ao obter a sintaxe necessária para o esquema de atributo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-654">Failed to obtain the required syntax for the attribute schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**erro erro de \_ \_ GCVERIFY DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**ERROR\_DS\_GCVERIFY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-656">8417 (0x20E1)</span><span class="sxs-lookup"><span data-stu-id="2d00a-656">8417 (0x20E1)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-657">Falha na verificação do catálogo global.</span><span class="sxs-lookup"><span data-stu-id="2d00a-657">The global catalog verification failed.</span></span> <span data-ttu-id="2d00a-658">O catálogo global não está disponível ou não oferece suporte à operação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-658">The global catalog is not available or does not support the operation.</span></span> <span data-ttu-id="2d00a-659">Parte do diretório não está disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="2d00a-659">Some part of the directory is currently not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de esquema Dra DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERROR\_DS\_DRA\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-661">8418 (0x20E2)</span><span class="sxs-lookup"><span data-stu-id="2d00a-661">8418 (0x20E2)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-662">A operação de replicação falhou devido a uma incompatibilidade de esquema entre os servidores envolvidos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-662">The replication operation failed because of a schema mismatch between the servers involved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERRO \_ DS não \_ consegue \_ encontrar \_ DSA \_ obj**</span><span class="sxs-lookup"><span data-stu-id="2d00a-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERROR\_DS\_CANT\_FIND\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-664">8419 (0x20E3)</span><span class="sxs-lookup"><span data-stu-id="2d00a-664">8419 (0x20E3)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-665">Não foi possível encontrar o objeto DSA.</span><span class="sxs-lookup"><span data-stu-id="2d00a-665">The DSA object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERRO \_ DS não \_ consegue \_ localizar o \_ \_ NC esperado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERROR\_DS\_CANT\_FIND\_EXPECTED\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-667">8420 (0x20E4)</span><span class="sxs-lookup"><span data-stu-id="2d00a-667">8420 (0x20E4)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-668">Não foi possível encontrar o contexto de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="2d00a-668">The naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERRO \_ DS não \_ consegue \_ localizar \_ NC \_ no \_ cache**</span><span class="sxs-lookup"><span data-stu-id="2d00a-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERROR\_DS\_CANT\_FIND\_NC\_IN\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-670">8421 (0x20E5)</span><span class="sxs-lookup"><span data-stu-id="2d00a-670">8421 (0x20E5)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-671">Não foi possível encontrar o contexto de nomenclatura no cache.</span><span class="sxs-lookup"><span data-stu-id="2d00a-671">The naming context could not be found in the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERRO \_ DS não \_ consegue \_ recuperar \_ filho**</span><span class="sxs-lookup"><span data-stu-id="2d00a-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERROR\_DS\_CANT\_RETRIEVE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-673">8422 (0x20E6)</span><span class="sxs-lookup"><span data-stu-id="2d00a-673">8422 (0x20E6)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-674">Não foi possível recuperar o objeto filho.</span><span class="sxs-lookup"><span data-stu-id="2d00a-674">The child object could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERRO \_ de \_ \_ modificação ilegal de segurança DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERROR\_DS\_SECURITY\_ILLEGAL\_MODIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-676">8423 (0x20E7)</span><span class="sxs-lookup"><span data-stu-id="2d00a-676">8423 (0x20E7)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-677">A modificação não foi permitida por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="2d00a-677">The modification was not permitted for security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERRO \_ DS não \_ consegue \_ substituir o \_ \_ REC oculto**</span><span class="sxs-lookup"><span data-stu-id="2d00a-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERROR\_DS\_CANT\_REPLACE\_HIDDEN\_REC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-679">8424 (0x20E8)</span><span class="sxs-lookup"><span data-stu-id="2d00a-679">8424 (0x20E8)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-680">A operação não pode substituir o registro oculto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-680">The operation cannot replace the hidden record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERRO \_ de \_ \_ arquivo de hierarquia insatisfatório DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERROR\_DS\_BAD\_HIERARCHY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-682">8425 (0x20E9)</span><span class="sxs-lookup"><span data-stu-id="2d00a-682">8425 (0x20E9)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-683">O arquivo de hierarquia é inválido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-683">The hierarchy file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERRO \_ \_ \_ \_ falha na tabela de hierarquia de compilação DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERROR\_DS\_BUILD\_HIERARCHY\_TABLE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-685">8426 (0x20EA)</span><span class="sxs-lookup"><span data-stu-id="2d00a-685">8426 (0x20EA)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-686">Falha na tentativa de criar a tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="2d00a-686">The attempt to build the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERRO \_ \_ parâmetro DS \_ config \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="2d00a-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERROR\_DS\_CONFIG\_PARAM\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-688">8427 (0x20EB)</span><span class="sxs-lookup"><span data-stu-id="2d00a-688">8427 (0x20EB)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-689">O parâmetro de configuração de diretório está ausente no registro.</span><span class="sxs-lookup"><span data-stu-id="2d00a-689">The directory configuration parameter is missing from the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERRO de \_ contagem de DS de \_ \_ \_ índices AB \_ com falha**</span><span class="sxs-lookup"><span data-stu-id="2d00a-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERROR\_DS\_COUNTING\_AB\_INDICES\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-691">8428 (0x20EC)</span><span class="sxs-lookup"><span data-stu-id="2d00a-691">8428 (0x20EC)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-692">Falha na tentativa de contagem dos índices do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="2d00a-692">The attempt to count the address book indices failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERRO \_ \_ \_ \_ falha ao alocar tabela de hierarquia DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_MALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-694">8429 (0x20ED)</span><span class="sxs-lookup"><span data-stu-id="2d00a-694">8429 (0x20ED)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-695">Falha na alocação da tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="2d00a-695">The allocation of the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERRO \_ interno de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERROR\_DS\_INTERNAL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-697">8430 (0x20EE)</span><span class="sxs-lookup"><span data-stu-id="2d00a-697">8430 (0x20EE)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-698">O serviço de diretório encontrou uma falha interna.</span><span class="sxs-lookup"><span data-stu-id="2d00a-698">The directory service encountered an internal failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**erro \_ desconhecido ao DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**ERROR\_DS\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-700">8431 (0x20EF)</span><span class="sxs-lookup"><span data-stu-id="2d00a-700">8431 (0x20EF)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-701">O serviço de diretório encontrou uma falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="2d00a-701">The directory service encountered an unknown failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**ERRO \_ a \_ raiz DS \_ requer a \_ classe \_ Top**</span><span class="sxs-lookup"><span data-stu-id="2d00a-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**ERROR\_DS\_ROOT\_REQUIRES\_CLASS\_TOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-703">8432 (0x20F0)</span><span class="sxs-lookup"><span data-stu-id="2d00a-703">8432 (0x20F0)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-704">Um objeto raiz requer uma classe de ' top '.</span><span class="sxs-lookup"><span data-stu-id="2d00a-704">A root object requires a class of 'top'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERRO \_ ao \_ recusar as \_ \_ funções FSMO do DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERROR\_DS\_REFUSING\_FSMO\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-706">8433 (0x20F1)</span><span class="sxs-lookup"><span data-stu-id="2d00a-706">8433 (0x20F1)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-707">Este servidor de diretório está sendo desligado e não é possível apropriar-se de novas funções de operação de mestre único flutuante.</span><span class="sxs-lookup"><span data-stu-id="2d00a-707">This directory server is shutting down, and cannot take ownership of new floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERRO \_ DS \_ ausente \_ \_ configurações FSMO**</span><span class="sxs-lookup"><span data-stu-id="2d00a-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERROR\_DS\_MISSING\_FSMO\_SETTINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-709">8434 (0x20F2)</span><span class="sxs-lookup"><span data-stu-id="2d00a-709">8434 (0x20F2)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-710">O serviço de diretório não tem informações de configuração obrigatórias e não é possível determinar a propriedade de funções de operação de mestre único flutuante.</span><span class="sxs-lookup"><span data-stu-id="2d00a-710">The directory service is missing mandatory configuration information, and is unable to determine the ownership of floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERRO \_ DS \_ incapaz \_ de despartir de \_ \_ funções**</span><span class="sxs-lookup"><span data-stu-id="2d00a-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERROR\_DS\_UNABLE\_TO\_SURRENDER\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-712">8435 (0x20F3)</span><span class="sxs-lookup"><span data-stu-id="2d00a-712">8435 (0x20F3)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-713">O serviço de diretório não pôde transferir a propriedade de uma ou mais funções de operação de mestre único flutuantes para outros servidores.</span><span class="sxs-lookup"><span data-stu-id="2d00a-713">The directory service was unable to transfer ownership of one or more floating single-master operation roles to other servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERRO \_ de \_ Dra \_ genérico de DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERROR\_DS\_DRA\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-715">8436 (0x20F4)</span><span class="sxs-lookup"><span data-stu-id="2d00a-715">8436 (0x20F4)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-716">Falha na operação de replicação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-716">The replication operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERRO \_ de \_ \_ parâmetro inválido de Dra DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERROR\_DS\_DRA\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-718">8437 (0x20F5)</span><span class="sxs-lookup"><span data-stu-id="2d00a-718">8437 (0x20F5)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-719">Um parâmetro inválido foi especificado para esta operação de replicação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-719">An invalid parameter was specified for this replication operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERRO \_ DS \_ Dra \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERROR\_DS\_DRA\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-721">8438 (0x20F6)</span><span class="sxs-lookup"><span data-stu-id="2d00a-721">8438 (0x20F6)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-722">O serviço de diretório está muito ocupado para concluir a operação de replicação no momento.</span><span class="sxs-lookup"><span data-stu-id="2d00a-722">The directory service is too busy to complete the replication operation at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERRO \_ \_ DN DS Dra \_ insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERROR\_DS\_DRA\_BAD\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-724">8439 (0x20F7)</span><span class="sxs-lookup"><span data-stu-id="2d00a-724">8439 (0x20F7)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-725">O nome distinto especificado para esta operação de replicação é inválido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-725">The distinguished name specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERRO \_ \_ NC DS Dra \_ insatisfatório \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERROR\_DS\_DRA\_BAD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-727">8440 (0x20F8)</span><span class="sxs-lookup"><span data-stu-id="2d00a-727">8440 (0x20F8)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-728">O contexto de nomenclatura especificado para esta operação de replicação é inválido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-728">The naming context specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERRO \_ o \_ DN DS Dra \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="2d00a-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERROR\_DS\_DRA\_DN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-730">8441 (0x20F9)</span><span class="sxs-lookup"><span data-stu-id="2d00a-730">8441 (0x20F9)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-731">O nome distinto especificado para esta operação de replicação já existe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-731">The distinguished name specified for this replication operation already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**erro \_ \_ interno de Dra DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**ERROR\_DS\_DRA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-733">8442 (0x20FA)</span><span class="sxs-lookup"><span data-stu-id="2d00a-733">8442 (0x20FA)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-734">O sistema de replicação encontrou um erro interno.</span><span class="sxs-lookup"><span data-stu-id="2d00a-734">The replication system encountered an internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERRO \_ de \_ dit de Dra \_ inconsistente DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERROR\_DS\_DRA\_INCONSISTENT\_DIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-736">8443 (0x20FB)</span><span class="sxs-lookup"><span data-stu-id="2d00a-736">8443 (0x20FB)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-737">A operação de replicação encontrou uma inconsistência de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2d00a-737">The replication operation encountered a database inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERRO \_ \_ \_ falha na conexão Dra DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERROR\_DS\_DRA\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-739">8444 (0x20FC)</span><span class="sxs-lookup"><span data-stu-id="2d00a-739">8444 (0x20FC)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-740">O servidor especificado para esta operação de replicação não pôde ser contatado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-740">The server specified for this replication operation could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERRO \_ de \_ \_ tipo de \_ instância inválido DS Dra \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERROR\_DS\_DRA\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-742">8445 (0x20FD)</span><span class="sxs-lookup"><span data-stu-id="2d00a-742">8445 (0x20FD)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-743">A operação de replicação encontrou um objeto com um tipo de instância inválido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-743">The replication operation encountered an object with an invalid instance type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERRO \_ DS \_ Dra \_ fora \_ do \_ mem**</span><span class="sxs-lookup"><span data-stu-id="2d00a-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERROR\_DS\_DRA\_OUT\_OF\_MEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-745">8446 (0x20FE)</span><span class="sxs-lookup"><span data-stu-id="2d00a-745">8446 (0x20FE)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-746">Falha na operação de replicação ao alocar memória.</span><span class="sxs-lookup"><span data-stu-id="2d00a-746">The replication operation failed to allocate memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERRO \_ de \_ email Dra DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERROR\_DS\_DRA\_MAIL\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-748">8447 (0x20FF)</span><span class="sxs-lookup"><span data-stu-id="2d00a-748">8447 (0x20FF)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-749">A operação de replicação encontrou um erro com o sistema de email.</span><span class="sxs-lookup"><span data-stu-id="2d00a-749">The replication operation encountered an error with the mail system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERRO o \_ DS \_ Dra \_ ref \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="2d00a-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERROR\_DS\_DRA\_REF\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-751">8448 (0x2100)</span><span class="sxs-lookup"><span data-stu-id="2d00a-751">8448 (0x2100)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-752">As informações de referência de replicação para o servidor de destino já existem.</span><span class="sxs-lookup"><span data-stu-id="2d00a-752">The replication reference information for the target server already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERRO \_ de \_ ref Dra DS \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERROR\_DS\_DRA\_REF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-754">8449 (0x2101)</span><span class="sxs-lookup"><span data-stu-id="2d00a-754">8449 (0x2101)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-755">As informações de referência de replicação para o servidor de destino não existem.</span><span class="sxs-lookup"><span data-stu-id="2d00a-755">The replication reference information for the target server does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERRO \_ DS \_ Dra \_ obj \_ is \_ origem do representante \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR\_DS\_DRA\_OBJ\_IS\_REP\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-757">8450 (0x2102)</span><span class="sxs-lookup"><span data-stu-id="2d00a-757">8450 (0x2102)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-758">Não é possível remover o contexto de nomenclatura porque ele é replicado em outro servidor.</span><span class="sxs-lookup"><span data-stu-id="2d00a-758">The naming context cannot be removed because it is replicated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**erro \_ erro de banco de domínio DS \_ Dra \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**ERROR\_DS\_DRA\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-760">8451 (0x2103)</span><span class="sxs-lookup"><span data-stu-id="2d00a-760">8451 (0x2103)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-761">A operação de replicação encontrou um erro de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2d00a-761">The replication operation encountered a database error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERRO \_ DS \_ Dra \_ sem \_ réplica**</span><span class="sxs-lookup"><span data-stu-id="2d00a-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERROR\_DS\_DRA\_NO\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-763">8452 (0x2104)</span><span class="sxs-lookup"><span data-stu-id="2d00a-763">8452 (0x2104)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-764">O contexto de nomenclatura está no processo de ser removido ou não é replicado do servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-764">The naming context is in the process of being removed or is not replicated from the specified server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERRO \_ \_ acesso ao Dra DS \_ \_ negado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERROR\_DS\_DRA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-766">8453 (0x2105)</span><span class="sxs-lookup"><span data-stu-id="2d00a-766">8453 (0x2105)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-767">O acesso à replicação foi negado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-767">Replication access was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERRO \_ DS \_ Dra \_ não \_ suportado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERROR\_DS\_DRA\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-769">8454 (0x2106)</span><span class="sxs-lookup"><span data-stu-id="2d00a-769">8454 (0x2106)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-770">Esta versão do serviço de diretório não dá suporte para a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-770">The requested operation is not supported by this version of the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERRO \_ \_ RPC de Dra DS \_ \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERROR\_DS\_DRA\_RPC\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-772">8455 (0x2107)</span><span class="sxs-lookup"><span data-stu-id="2d00a-772">8455 (0x2107)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-773">A chamada de procedimento remoto de replicação foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-773">The replication remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERRO \_ \_ origem de Dra DS \_ \_ desabilitada**</span><span class="sxs-lookup"><span data-stu-id="2d00a-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERROR\_DS\_DRA\_SOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-775">8456 (0x2108)</span><span class="sxs-lookup"><span data-stu-id="2d00a-775">8456 (0x2108)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-776">O servidor de origem está rejeitando solicitações de replicação no momento.</span><span class="sxs-lookup"><span data-stu-id="2d00a-776">The source server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERRO \_ de \_ coletor de Dra DS \_ \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERROR\_DS\_DRA\_SINK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-778">8457 (0x2109)</span><span class="sxs-lookup"><span data-stu-id="2d00a-778">8457 (0x2109)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-779">O servidor de destino está rejeitando solicitações de replicação no momento.</span><span class="sxs-lookup"><span data-stu-id="2d00a-779">The destination server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERRO \_ de \_ \_ colisão de nome Dra DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERROR\_DS\_DRA\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-781">8458 (0x210A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-781">8458 (0x210A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-782">Falha na operação de replicação devido a uma colisão de nomes de objetos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-782">The replication operation failed due to a collision of object names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERRO \_ de \_ origem de Dra DS \_ \_ reinstalado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERROR\_DS\_DRA\_SOURCE\_REINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-784">8459 (0x210B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-784">8459 (0x210B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-785">A origem da replicação foi reinstalada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-785">The replication source has been reinstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERRO \_ DS \_ Dra \_ ausente \_ pai**</span><span class="sxs-lookup"><span data-stu-id="2d00a-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERROR\_DS\_DRA\_MISSING\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-787">8460 (0x210C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-787">8460 (0x210C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-788">Falha na operação de replicação porque um objeto pai necessário está ausente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-788">The replication operation failed because a required parent object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERRO \_ de \_ Dra DS \_ preempção**</span><span class="sxs-lookup"><span data-stu-id="2d00a-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERROR\_DS\_DRA\_PREEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-790">8461 (0x210D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-790">8461 (0x210D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-791">A operação de replicação foi antecipada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-791">The replication operation was preempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERRO \_ DS \_ Dra \_ ABANDON \_ Sync**</span><span class="sxs-lookup"><span data-stu-id="2d00a-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERROR\_DS\_DRA\_ABANDON\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-793">8462 (0x210E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-793">8462 (0x210E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-794">A tentativa de sincronização de replicação foi abandonada devido à falta de atualizações.</span><span class="sxs-lookup"><span data-stu-id="2d00a-794">The replication synchronization attempt was abandoned because of a lack of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERRO \_ de \_ \_ desligamento de Dra DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERROR\_DS\_DRA\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-796">8463 (0x210F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-796">8463 (0x210F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-797">A operação de replicação foi encerrada porque o sistema está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-797">The replication operation was terminated because the system is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERRO \_ de \_ \_ \_ conjunto parcial incompatível de Dra DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERROR\_DS\_DRA\_INCOMPATIBLE\_PARTIAL\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-799">8464 (0x2110)</span><span class="sxs-lookup"><span data-stu-id="2d00a-799">8464 (0x2110)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-800">Falha na tentativa de sincronização porque o DC de destino está aguardando a sincronização de novos atributos parciais da origem no momento.</span><span class="sxs-lookup"><span data-stu-id="2d00a-800">Synchronization attempt failed because the destination DC is currently waiting to synchronize new partial attributes from source.</span></span> <span data-ttu-id="2d00a-801">Essa condição será normal se uma alteração de esquema recente tiver modificado o conjunto de atributos parciais.</span><span class="sxs-lookup"><span data-stu-id="2d00a-801">This condition is normal if a recent schema change modified the partial attribute set.</span></span> <span data-ttu-id="2d00a-802">O conjunto de atributos parciais de destino não é um subconjunto do conjunto de atributos parciais de origem.</span><span class="sxs-lookup"><span data-stu-id="2d00a-802">The destination partial attribute set is not a subset of source partial attribute set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERRO \_ a \_ origem do Dra DS \_ é uma \_ \_ \_ réplica parcial**</span><span class="sxs-lookup"><span data-stu-id="2d00a-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERROR\_DS\_DRA\_SOURCE\_IS\_PARTIAL\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-804">8465 (0x2111)</span><span class="sxs-lookup"><span data-stu-id="2d00a-804">8465 (0x2111)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-805">Falha na tentativa de sincronização de replicação porque uma réplica mestre tentou sincronizar a partir de uma réplica parcial.</span><span class="sxs-lookup"><span data-stu-id="2d00a-805">The replication synchronization attempt failed because a master replica attempted to sync from a partial replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERRO \_ \_ \_ \_ falha na conexão de EXTN Dra DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERROR\_DS\_DRA\_EXTN\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-807">8466 (0x2112)</span><span class="sxs-lookup"><span data-stu-id="2d00a-807">8466 (0x2112)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-808">O servidor especificado para esta operação de replicação foi contatado, mas esse servidor não pôde contatar um servidor adicional necessário para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-808">The server specified for this replication operation was contacted, but that server was unable to contact an additional server needed to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de esquema de instalação DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERROR\_DS\_INSTALL\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-810">8467 (0x2113)</span><span class="sxs-lookup"><span data-stu-id="2d00a-810">8467 (0x2113)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-811">A versão do esquema de serviço de diretório da floresta de origem não é compatível com a versão do serviço de diretório neste computador.</span><span class="sxs-lookup"><span data-stu-id="2d00a-811">The version of the directory service schema of the source forest is not compatible with the version of directory service on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**ERRO \_ \_ ID de \_ link de DUP DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**ERROR\_DS\_DUP\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-813">8468 (0x2114)</span><span class="sxs-lookup"><span data-stu-id="2d00a-813">8468 (0x2114)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-814">Falha na atualização do esquema: já existe um atributo com o mesmo identificador de link.</span><span class="sxs-lookup"><span data-stu-id="2d00a-814">Schema update failed: An attribute with the same link identifier already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERRO \_ ao \_ \_ resolver erro de nome DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERROR\_DS\_NAME\_ERROR\_RESOLVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-816">8469 (0x2115)</span><span class="sxs-lookup"><span data-stu-id="2d00a-816">8469 (0x2115)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-817">Conversão de nomes: erro de processamento genérico.</span><span class="sxs-lookup"><span data-stu-id="2d00a-817">Name translation: Generic processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**erro \_ de \_ nome \_ DS \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-819">8470 (0x2116)</span><span class="sxs-lookup"><span data-stu-id="2d00a-819">8470 (0x2116)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-820">Conversão de nomes: não foi possível encontrar o nome ou o direito insuficiente para ver o nome.</span><span class="sxs-lookup"><span data-stu-id="2d00a-820">Name translation: Could not find the name or insufficient right to see name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERRO \_ \_ nome DS \_ erro \_ não \_ exclusivo**</span><span class="sxs-lookup"><span data-stu-id="2d00a-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-822">8471 (0x2117)</span><span class="sxs-lookup"><span data-stu-id="2d00a-822">8471 (0x2117)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-823">Conversão de nomes: nome de entrada mapeado para mais de um nome de saída.</span><span class="sxs-lookup"><span data-stu-id="2d00a-823">Name translation: Input name mapped to more than one output name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**erro \_ \_ nome DS \_ erro \_ sem \_ mapeamento**</span><span class="sxs-lookup"><span data-stu-id="2d00a-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-825">8472 (0x2118)</span><span class="sxs-lookup"><span data-stu-id="2d00a-825">8472 (0x2118)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-826">Conversão de nomes: nome de entrada encontrado, mas não o formato de saída associado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-826">Name translation: Input name found, but not the associated output format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERRO \_ \_ nome DS \_ \_ somente domínio \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERROR\_DS\_NAME\_ERROR\_DOMAIN\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-828">8473 (0x2119)</span><span class="sxs-lookup"><span data-stu-id="2d00a-828">8473 (0x2119)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-829">Conversão de nomes: não é possível resolver completamente, somente o domínio foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-829">Name translation: Unable to resolve completely, only the domain was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**erro \_ de \_ nome DS \_ erro \_ sem \_ \_ mapeamento sintático**</span><span class="sxs-lookup"><span data-stu-id="2d00a-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_SYNTACTICAL\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-831">8474 (0x211A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-831">8474 (0x211A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-832">Conversão de nomes: não é possível executar um mapeamento puramente sintático no cliente sem sair da conexão.</span><span class="sxs-lookup"><span data-stu-id="2d00a-832">Name translation: Unable to perform purely syntactical mapping at the client without going out to the wire.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERRO \_ DS \_ construído \_ ATT \_ mod**</span><span class="sxs-lookup"><span data-stu-id="2d00a-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERROR\_DS\_CONSTRUCTED\_ATT\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-834">8475 (0x211B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-834">8475 (0x211B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-835">A modificação de um atributo construído não é permitida.</span><span class="sxs-lookup"><span data-stu-id="2d00a-835">Modification of a constructed attribute is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERRO \_ DS \_ de \_ classe do OM incorreto \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERROR\_DS\_WRONG\_OM\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-837">8476 (0x211C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-837">8476 (0x211C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-838">A classe de objeto OM especificada está incorreta para um atributo com a sintaxe especificada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-838">The OM-Object-Class specified is incorrect for an attribute with the specified syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERRO \_ de \_ replicação de Dra DS \_ \_ pendente**</span><span class="sxs-lookup"><span data-stu-id="2d00a-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERROR\_DS\_DRA\_REPL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-840">8477 (0x211D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-840">8477 (0x211D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-841">A solicitação de replicação foi postada; aguardando resposta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-841">The replication request has been posted; waiting for reply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERRO DS DS \_ \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="2d00a-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERROR\_DS\_DS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-843">8478 (0x211E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-843">8478 (0x211E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-844">A operação solicitada requer um serviço de diretório e nenhuma estava disponível.</span><span class="sxs-lookup"><span data-stu-id="2d00a-844">The requested operation requires a directory service, and none was available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERRO \_ \_ nome de \_ \_ exibição LDAP \_ inválido do DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERROR\_DS\_INVALID\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-846">8479 (0x211F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-846">8479 (0x211F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-847">O nome de exibição LDAP da classe ou do atributo contém caracteres não ASCII.</span><span class="sxs-lookup"><span data-stu-id="2d00a-847">The LDAP display name of the class or attribute contains non-ASCII characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERRO \_ de \_ \_ pesquisa não \_ básica de DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERROR\_DS\_NON\_BASE\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-849">8480 (0x2120)</span><span class="sxs-lookup"><span data-stu-id="2d00a-849">8480 (0x2120)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-850">A operação de pesquisa solicitada só tem suporte para pesquisas base.</span><span class="sxs-lookup"><span data-stu-id="2d00a-850">The requested search operation is only supported for base searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERRO \_ DS não \_ consegue \_ recuperar \_ atts**</span><span class="sxs-lookup"><span data-stu-id="2d00a-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERROR\_DS\_CANT\_RETRIEVE\_ATTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-852">8481 (0x2121)</span><span class="sxs-lookup"><span data-stu-id="2d00a-852">8481 (0x2121)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-853">A pesquisa não pôde recuperar os atributos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2d00a-853">The search failed to retrieve attributes from the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERRO \_ DS \_ BACKLINK \_ sem \_ link**</span><span class="sxs-lookup"><span data-stu-id="2d00a-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERROR\_DS\_BACKLINK\_WITHOUT\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-855">8482 (0x2122)</span><span class="sxs-lookup"><span data-stu-id="2d00a-855">8482 (0x2122)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-856">A operação de atualização de esquema tentou adicionar um atributo de vínculo regressivo que não tem nenhum link de encaminhamento correspondente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-856">The schema update operation tried to add a backward link attribute that has no corresponding forward link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERRO \_ de \_ incompatibilidade de época DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERROR\_DS\_EPOCH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-858">8483 (0x2123)</span><span class="sxs-lookup"><span data-stu-id="2d00a-858">8483 (0x2123)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-859">A origem e o destino de uma movimentação entre domínios não aceitam o número de época do objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-859">Source and destination of a cross-domain move do not agree on the object's epoch number.</span></span> <span data-ttu-id="2d00a-860">A origem ou o destino não tem a versão mais recente do objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-860">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de nome src DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERROR\_DS\_SRC\_NAME\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-862">8484 (0x2124)</span><span class="sxs-lookup"><span data-stu-id="2d00a-862">8484 (0x2124)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-863">A origem e o destino de uma movimentação entre domínios não aceitam o nome atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-863">Source and destination of a cross-domain move do not agree on the object's current name.</span></span> <span data-ttu-id="2d00a-864">A origem ou o destino não tem a versão mais recente do objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-864">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERRO \_ DS \_ src \_ e \_ DST \_ NC \_ idênticos**</span><span class="sxs-lookup"><span data-stu-id="2d00a-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERROR\_DS\_SRC\_AND\_DST\_NC\_IDENTICAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-866">8485 (0x2125)</span><span class="sxs-lookup"><span data-stu-id="2d00a-866">8485 (0x2125)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-867">A origem e o destino da operação de movimentação entre domínios são idênticos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-867">Source and destination for the cross-domain move operation are identical.</span></span> <span data-ttu-id="2d00a-868">O chamador deve usar a operação de movimentação local em vez da operação de movimentação entre domínios.</span><span class="sxs-lookup"><span data-stu-id="2d00a-868">Caller should use local move operation instead of cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de NC de DST de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERROR\_DS\_DST\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-870">8486 (0x2126)</span><span class="sxs-lookup"><span data-stu-id="2d00a-870">8486 (0x2126)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-871">A origem e o destino de uma movimentação entre domínios não estão em acordo com os contextos de nomenclatura na floresta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-871">Source and destination for a cross-domain move are not in agreement on the naming contexts in the forest.</span></span> <span data-ttu-id="2d00a-872">A origem ou o destino não tem a versão mais recente do contêiner de partições.</span><span class="sxs-lookup"><span data-stu-id="2d00a-872">Either source or destination does not have the latest version of the Partitions container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERRO \_ DS \_ não \_ AUTHORITIVE \_ para o \_ DST \_ NC**</span><span class="sxs-lookup"><span data-stu-id="2d00a-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERROR\_DS\_NOT\_AUTHORITIVE\_FOR\_DST\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-874">8487 (0x2127)</span><span class="sxs-lookup"><span data-stu-id="2d00a-874">8487 (0x2127)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-875">O destino de uma movimentação entre domínios não é autoritativo para o contexto de nomenclatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2d00a-875">Destination of a cross-domain move is not authoritative for the destination naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de GUID src DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERROR\_DS\_SRC\_GUID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-877">8488 (0x2128)</span><span class="sxs-lookup"><span data-stu-id="2d00a-877">8488 (0x2128)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-878">A origem e o destino de uma movimentação entre domínios não aceitam a identidade do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="2d00a-878">Source and destination of a cross-domain move do not agree on the identity of the source object.</span></span> <span data-ttu-id="2d00a-879">A origem ou o destino não tem a versão mais recente do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="2d00a-879">Either source or destination does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERRO \_ DS \_ impossível \_ mover \_ \_ objeto excluído**</span><span class="sxs-lookup"><span data-stu-id="2d00a-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERROR\_DS\_CANT\_MOVE\_DELETED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-881">8489 (0x2129)</span><span class="sxs-lookup"><span data-stu-id="2d00a-881">8489 (0x2129)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-882">O objeto que está sendo movido entre domínios já é conhecido como excluído pelo servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="2d00a-882">Object being moved across-domains is already known to be deleted by the destination server.</span></span> <span data-ttu-id="2d00a-883">O servidor de origem não tem a versão mais recente do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="2d00a-883">The source server does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERRO \_ \_ \_ \_ na operação de PDC do DS em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="2d00a-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERROR\_DS\_PDC\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-885">8490 (0x212A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-885">8490 (0x212A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-886">Outra operação que requer acesso exclusivo ao PDC FSMO já está em andamento.</span><span class="sxs-lookup"><span data-stu-id="2d00a-886">Another operation which requires exclusive access to the PDC FSMO is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERRO \_ \_ REQD de \_ limpeza entre domínios \_ \_ DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERROR\_DS\_CROSS\_DOMAIN\_CLEANUP\_REQD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-888">8491 (0x212B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-888">8491 (0x212B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-889">Uma operação de movimentação entre domínios falhou, de modo que duas versões do objeto movido existam-uma a cada nos domínios de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="2d00a-889">A cross-domain move operation failed such that two versions of the moved object exist - one each in the source and destination domains.</span></span> <span data-ttu-id="2d00a-890">O objeto de destino precisa ser removido para restaurar o sistema para um estado consistente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-890">The destination object needs to be removed to restore the system to a consistent state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERRO \_ DS \_ inválido \_ ao \_ mover \_ operação de XDOM**</span><span class="sxs-lookup"><span data-stu-id="2d00a-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERROR\_DS\_ILLEGAL\_XDOM\_MOVE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-892">8492 (0x212C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-892">8492 (0x212C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-893">Esse objeto não pode ser movido entre limites de domínio porque as movimentações entre domínios dessa classe não são permitidas ou o objeto tem algumas características especiais, por exemplo: conta de confiança ou RID restrito, o que impede sua movimentação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-893">This object may not be moved across domain boundaries either because cross-domain moves for this class are disallowed, or the object has some special characteristics, e.g.: trust account or restricted RID, which prevent its move.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERRO \_ DS não \_ consegue \_ com o \_ \_ grupo acct \_ MEMBERSHPS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERROR\_DS\_CANT\_WITH\_ACCT\_GROUP\_MEMBERSHPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-895">8493 (0x212D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-895">8493 (0x212D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-896">Não é possível mover objetos com associações entre limites de domínio assim que forem movidos, isso violaria as condições de associação do grupo de contas.</span><span class="sxs-lookup"><span data-stu-id="2d00a-896">Can't move objects with memberships across domain boundaries as once moved, this would violate the membership conditions of the account group.</span></span> <span data-ttu-id="2d00a-897">Remova o objeto de qualquer associação de grupo de conta e tente novamente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-897">Remove the object from any account group memberships and retry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERRO \_ o \_ NC DS \_ deve \_ ter o \_ NC \_ pai**</span><span class="sxs-lookup"><span data-stu-id="2d00a-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERROR\_DS\_NC\_MUST\_HAVE\_NC\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-899">8494 (0x212E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-899">8494 (0x212E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-900">Uma cabeça de contexto de nomenclatura deve ser o filho imediato de outro cabeçalho de contexto de nomenclatura, não de um nó interior.</span><span class="sxs-lookup"><span data-stu-id="2d00a-900">A naming context head must be the immediate child of another naming context head, not of an interior node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERRO \_ \_ de DS CR \_ impossível \_ de \_ validar**</span><span class="sxs-lookup"><span data-stu-id="2d00a-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-902">8495 (0x212F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-902">8495 (0x212F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-903">O diretório não pode validar o nome de contexto de nomenclatura proposto porque não contém uma réplica do contexto de nomenclatura acima do contexto de nomenclatura proposto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-903">The directory cannot validate the proposed naming context name because it does not hold a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="2d00a-904">Verifique se a função mestre de nomeação de domínio é mantida por um servidor configurado como um servidor de catálogo global e se o servidor está atualizado com seus parceiros de replicação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-904">Please ensure that the domain naming master role is held by a server that is configured as a global catalog server, and that the server is up to date with its replication partners.</span></span> <span data-ttu-id="2d00a-905">(Aplica-se somente aos mestres de nomenclatura de domínio do Windows 2000.)</span><span class="sxs-lookup"><span data-stu-id="2d00a-905">(Applies only to Windows 2000 Domain Naming masters.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERRO \_ DS \_ DST \_ Domain \_ não \_ nativo**</span><span class="sxs-lookup"><span data-stu-id="2d00a-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERROR\_DS\_DST\_DOMAIN\_NOT\_NATIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-907">8496 (0x2130)</span><span class="sxs-lookup"><span data-stu-id="2d00a-907">8496 (0x2130)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-908">O domínio de destino deve estar no modo nativo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-908">Destination domain must be in native mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERRO \_ DS \_ - \_ contêiner de infraestrutura ausente \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERROR\_DS\_MISSING\_INFRASTRUCTURE\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-910">8497 (0x2131)</span><span class="sxs-lookup"><span data-stu-id="2d00a-910">8497 (0x2131)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-911">A operação não pode ser executada porque o servidor não tem um contêiner de infraestrutura no domínio de interesse.</span><span class="sxs-lookup"><span data-stu-id="2d00a-911">The operation cannot be performed because the server does not have an infrastructure container in the domain of interest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERRO \_ DS \_ impossível \_ mover \_ grupo de contas \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERROR\_DS\_CANT\_MOVE\_ACCOUNT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-913">8498 (0x2132)</span><span class="sxs-lookup"><span data-stu-id="2d00a-913">8498 (0x2132)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-914">A movimentação entre domínios de grupos de contas não vazios não é permitida.</span><span class="sxs-lookup"><span data-stu-id="2d00a-914">Cross-domain move of non-empty account groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERRO \_ DS não \_ consegue \_ mover o \_ grupo de recursos \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERROR\_DS\_CANT\_MOVE\_RESOURCE\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-916">8499 (0x2133)</span><span class="sxs-lookup"><span data-stu-id="2d00a-916">8499 (0x2133)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-917">A movimentação entre domínios de grupos de recursos não vazios não é permitida.</span><span class="sxs-lookup"><span data-stu-id="2d00a-917">Cross-domain move of non-empty resource groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERRO \_ de \_ \_ sinalizador de pesquisa inválido de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-919">8500 (0x2134)</span><span class="sxs-lookup"><span data-stu-id="2d00a-919">8500 (0x2134)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-920">Os sinalizadores de pesquisa para o atributo são inválidos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-920">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="2d00a-921">O bit ANR é válido somente em atributos de cadeias de caracteres Unicode ou Teletex.</span><span class="sxs-lookup"><span data-stu-id="2d00a-921">The ANR bit is valid only on attributes of Unicode or Teletex strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERRO \_ DS \_ sem \_ exclusão de árvore \_ \_ acima do \_ NC**</span><span class="sxs-lookup"><span data-stu-id="2d00a-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERROR\_DS\_NO\_TREE\_DELETE\_ABOVE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-923">8501 (0x2135)</span><span class="sxs-lookup"><span data-stu-id="2d00a-923">8501 (0x2135)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-924">As exclusões de árvore que começam em um objeto que tem um cabeçalho NC como descendente não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="2d00a-924">Tree deletions starting at an object which has an NC head as a descendant are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERRO \_ \_ \_ \_ de árvore de bloqueio \_ de não foi possível DS para \_ exclusão**</span><span class="sxs-lookup"><span data-stu-id="2d00a-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERROR\_DS\_COULDNT\_LOCK\_TREE\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-926">8502 (0x2136)</span><span class="sxs-lookup"><span data-stu-id="2d00a-926">8502 (0x2136)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-927">O serviço de diretório não pôde bloquear uma árvore na preparação para uma exclusão de árvore porque a árvore estava em uso.</span><span class="sxs-lookup"><span data-stu-id="2d00a-927">The directory service failed to lock a tree in preparation for a tree deletion because the tree was in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERRO \_ DS \_ não foi possível \_ identificar \_ objetos \_ para \_ exclusão de árvore \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERROR\_DS\_COULDNT\_IDENTIFY\_OBJECTS\_FOR\_TREE\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-929">8503 (0x2137)</span><span class="sxs-lookup"><span data-stu-id="2d00a-929">8503 (0x2137)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-930">O serviço de diretório não identificou a lista de objetos a serem excluídos ao tentar uma exclusão de árvore.</span><span class="sxs-lookup"><span data-stu-id="2d00a-930">The directory service failed to identify the list of objects to delete while attempting a tree deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERRO \_ \_ \_ falha na inicialização de Sam do DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-932">8504 (0x2138)</span><span class="sxs-lookup"><span data-stu-id="2d00a-932">8504 (0x2138)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-933">Falha na inicialização do Gerenciador de contas de segurança devido ao seguinte erro: %1.</span><span class="sxs-lookup"><span data-stu-id="2d00a-933">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="2d00a-934">Status do erro: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="2d00a-934">Error Status: 0x%2.</span></span> <span data-ttu-id="2d00a-935">Desligue o sistema e reinicialize o Modo de Restauração dos Serviços de Diretório, verifique o log de eventos para obter informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="2d00a-935">Please shutdown this system and reboot into Directory Services Restore Mode, check the event log for more detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERRO \_ de \_ \_ violação de grupo confidencial de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERROR\_DS\_SENSITIVE\_GROUP\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-937">8505 (0x2139)</span><span class="sxs-lookup"><span data-stu-id="2d00a-937">8505 (0x2139)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-938">Somente um administrador pode modificar a lista de membros de um grupo administrativo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-938">Only an administrator can modify the membership list of an administrative group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERRO \_ DS não \_ puder \_ mod \_ PRIMARYGROUPID**</span><span class="sxs-lookup"><span data-stu-id="2d00a-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERROR\_DS\_CANT\_MOD\_PRIMARYGROUPID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-940">8506 (0x213A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-940">8506 (0x213A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-941">Não é possível alterar a ID do grupo primário de uma conta do controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="2d00a-941">Cannot change the primary group ID of a domain controller account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERRO \_ DS \_ do \_ esquema base ilegal \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERROR\_DS\_ILLEGAL\_BASE\_SCHEMA\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-943">8507 (0x213B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-943">8507 (0x213B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-944">É feita uma tentativa de modificar o esquema base.</span><span class="sxs-lookup"><span data-stu-id="2d00a-944">An attempt is made to modify the base schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERRO \_ de \_ alteração de esquema não confiável DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERROR\_DS\_NONSAFE\_SCHEMA\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-946">8508 (0x213C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-946">8508 (0x213C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-947">Adicionar um novo atributo obrigatório a uma classe existente, excluir um atributo obrigatório de uma classe existente ou adicionar um atributo opcional à classe especial Top que não é um atributo backlink (diretamente ou por meio de herança, por exemplo, adicionando ou excluindo uma classe auxiliar) não é permitido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-947">Adding a new mandatory attribute to an existing class, deleting a mandatory attribute from an existing class, or adding an optional attribute to the special class Top that is not a backlink attribute (directly or through inheritance, for example, by adding or deleting an auxiliary class) is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERRO \_ de \_ atualização do esquema DS não \_ \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERROR\_DS\_SCHEMA\_UPDATE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-949">8509 (0x213D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-949">8509 (0x213D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-950">A atualização do esquema não é permitida neste controlador de domínio porque o controlador de domínio não é o proprietário da função FSMO do esquema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-950">Schema update is not allowed on this DC because the DC is not the schema FSMO Role Owner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERRO \_ DS não \_ consegue \_ criar \_ em \_ esquema**</span><span class="sxs-lookup"><span data-stu-id="2d00a-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERROR\_DS\_CANT\_CREATE\_UNDER\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-952">8510 (0x213E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-952">8510 (0x213E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-953">Um objeto desta classe não pode ser criado no contêiner de esquema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-953">An object of this class cannot be created under the schema container.</span></span> <span data-ttu-id="2d00a-954">Você só pode criar objetos de esquema de atributo e de esquema de classe no contêiner de esquema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-954">You can only create attribute-schema and class-schema objects under the schema container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERRO \_ DS \_ instalação \_ sem \_ src \_ SCH \_ versão**</span><span class="sxs-lookup"><span data-stu-id="2d00a-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERROR\_DS\_INSTALL\_NO\_SRC\_SCH\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-956">8511 (0x213F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-956">8511 (0x213F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-957">A instalação de réplica/filho não pôde obter o atributo objectVersion no contêiner de esquema no controlador de domínio de origem.</span><span class="sxs-lookup"><span data-stu-id="2d00a-957">The replica/child install failed to get the objectVersion attribute on the schema container on the source DC.</span></span> <span data-ttu-id="2d00a-958">O atributo está ausente no contêiner de esquema ou as credenciais fornecidas não têm permissão para lê-lo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-958">Either the attribute is missing on the schema container or the credentials supplied do not have permission to read it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERRO \_ DS \_ instalar \_ nenhuma \_ \_ versão \_ do SCH no \_ inifile**</span><span class="sxs-lookup"><span data-stu-id="2d00a-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERROR\_DS\_INSTALL\_NO\_SCH\_VERSION\_IN\_INIFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-960">8512 (0x2140)</span><span class="sxs-lookup"><span data-stu-id="2d00a-960">8512 (0x2140)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-961">A instalação de réplica/filho não pôde ler o atributo objectVersion na seção de esquema do arquivo schema.ini no diretório system32.</span><span class="sxs-lookup"><span data-stu-id="2d00a-961">The replica/child install failed to read the objectVersion attribute in the SCHEMA section of the file schema.ini in the system32 directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERRO \_ DS \_ \_ tipo de grupo inválido \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERROR\_DS\_INVALID\_GROUP\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-963">8513 (0x2141)</span><span class="sxs-lookup"><span data-stu-id="2d00a-963">8513 (0x2141)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-964">O tipo de grupo especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-964">The specified group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERRO \_ DS \_ nenhum \_ aninhamento \_ global \_ em \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="2d00a-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_GLOBALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-966">8514 (0x2142)</span><span class="sxs-lookup"><span data-stu-id="2d00a-966">8514 (0x2142)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-967">Você não poderá aninhar grupos globais em um domínio misto se o grupo estiver habilitado para segurança.</span><span class="sxs-lookup"><span data-stu-id="2d00a-967">You cannot nest global groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERRO \_ DS \_ sem \_ aninhar \_ localgroup \_ em \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="2d00a-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_LOCALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-969">8515 (0x2143)</span><span class="sxs-lookup"><span data-stu-id="2d00a-969">8515 (0x2143)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-970">Você não poderá aninhar grupos locais em um domínio misto se o grupo estiver habilitado para segurança.</span><span class="sxs-lookup"><span data-stu-id="2d00a-970">You cannot nest local groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERRO \_ \_ global DS \_ não \_ tem \_ \_ membro local**</span><span class="sxs-lookup"><span data-stu-id="2d00a-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-972">8516 (0x2144)</span><span class="sxs-lookup"><span data-stu-id="2d00a-972">8516 (0x2144)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-973">Um grupo global não pode ter um grupo local como membro.</span><span class="sxs-lookup"><span data-stu-id="2d00a-973">A global group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERRO \_ \_ global DS \_ não \_ tem \_ \_ membro universal**</span><span class="sxs-lookup"><span data-stu-id="2d00a-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-975">8517 (0x2145)</span><span class="sxs-lookup"><span data-stu-id="2d00a-975">8517 (0x2145)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-976">Um grupo global não pode ter um grupo universal como membro.</span><span class="sxs-lookup"><span data-stu-id="2d00a-976">A global group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERRO \_ DS \_ Universal \_ não \_ tem \_ \_ membro local**</span><span class="sxs-lookup"><span data-stu-id="2d00a-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERROR\_DS\_UNIVERSAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-978">8518 (0x2146)</span><span class="sxs-lookup"><span data-stu-id="2d00a-978">8518 (0x2146)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-979">Um grupo universal não pode ter um grupo local como membro.</span><span class="sxs-lookup"><span data-stu-id="2d00a-979">A universal group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERRO \_ \_ global DS \_ não \_ tem \_ \_ membro CROSSDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="2d00a-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_CROSSDOMAIN\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-981">8519 (0x2147)</span><span class="sxs-lookup"><span data-stu-id="2d00a-981">8519 (0x2147)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-982">Um grupo global não pode ter um membro entre domínios.</span><span class="sxs-lookup"><span data-stu-id="2d00a-982">A global group cannot have a cross-domain member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERRO \_ \_ local DS \_ não \_ pode ter o \_ \_ membro local CROSSDOMAIN \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERROR\_DS\_LOCAL\_CANT\_HAVE\_CROSSDOMAIN\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-984">8520 (0x2148)</span><span class="sxs-lookup"><span data-stu-id="2d00a-984">8520 (0x2148)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-985">Um grupo local não pode ter outro grupo local entre domínios como um membro.</span><span class="sxs-lookup"><span data-stu-id="2d00a-985">A local group cannot have another cross domain local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERRO \_ DS \_ tem \_ Membros primários \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERROR\_DS\_HAVE\_PRIMARY\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-987">8521 (0x2149)</span><span class="sxs-lookup"><span data-stu-id="2d00a-987">8521 (0x2149)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-988">Um grupo com membros primários não pode ser alterado para um grupo desabilitado para segurança.</span><span class="sxs-lookup"><span data-stu-id="2d00a-988">A group with primary members cannot change to a security-disabled group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERRO \_ \_ \_ \_ na conversão SD da cadeia de caracteres DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERROR\_DS\_STRING\_SD\_CONVERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-990">8522 (0x214A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-990">8522 (0x214A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-991">O carregamento do cache de esquema falhou ao converter o SD padrão da cadeia de caracteres em um objeto de esquema de classe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-991">The schema cache load failed to convert the string default SD on a class-schema object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERRO \_ DS \_ do \_ mestre de nomeação \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERROR\_DS\_NAMING\_MASTER\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-993">8523 (0x214B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-993">8523 (0x214B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-994">Somente os DSAs configurados para serem servidores de catálogo global devem ter permissão para manter a função FSMO do mestre de nomeação de domínio.</span><span class="sxs-lookup"><span data-stu-id="2d00a-994">Only DSAs configured to be Global Catalog servers should be allowed to hold the Domain Naming Master FSMO role.</span></span> <span data-ttu-id="2d00a-995">(Aplica-se somente a servidores Windows 2000.)</span><span class="sxs-lookup"><span data-stu-id="2d00a-995">(Applies only to Windows 2000 servers.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERRO \_ de \_ \_ falha na pesquisa de DNS DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERROR\_DS\_DNS\_LOOKUP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-997">8524 (0x214C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-997">8524 (0x214C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-998">A operação DSA não pode continuar devido a uma falha de pesquisa de DNS.</span><span class="sxs-lookup"><span data-stu-id="2d00a-998">The DSA operation is unable to proceed because of a DNS lookup failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERRO \_ de \_ \_ SPNs de atualização de não foi possível DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERROR\_DS\_COULDNT\_UPDATE\_SPNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1000">8525 (0x214D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1000">8525 (0x214D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1001">Ao processar uma alteração no nome de host DNS de um objeto, os valores de nome da entidade de serviço não puderam ser mantidos em sincronia.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1001">While processing a change to the DNS Host Name for an object, the Service Principal Name values could not be kept in sync.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERRO \_ DS não \_ consegue \_ recuperar \_ SD**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERROR\_DS\_CANT\_RETRIEVE\_SD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1003">8526 (0x214E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1003">8526 (0x214E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1004">Não foi possível ler o atributo do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1004">The Security Descriptor attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERRO \_ de \_ chave DS \_ não \_ exclusiva**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERROR\_DS\_KEY\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1006">8527 (0x214F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1006">8527 (0x214F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1007">O objeto solicitado não foi encontrado, mas foi encontrado um objeto com essa chave.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1007">The object requested was not found, but an object with that key was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERRO \_ de \_ \_ sintaxe de \_ ATT vinculada incorreta de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERROR\_DS\_WRONG\_LINKED\_ATT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1009">8528 (0x2150)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1009">8528 (0x2150)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1010">A sintaxe do atributo vinculado que está sendo adicionado está incorreta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1010">The syntax of the linked attribute being added is incorrect.</span></span> <span data-ttu-id="2d00a-1011">Os links de encaminhamento só podem ter sintaxe 2.5.5.1, 2.5.5.7 e 2.5.5.14, e os backlinks só podem ter a sintaxe 2.5.5.1.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1011">Forward links can only have syntax 2.5.5.1, 2.5.5.7, and 2.5.5.14, and backlinks can only have syntax 2.5.5.1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERRO \_ DS \_ Sam \_ precisa de \_ BOOTKEY \_ senha**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1013">8529 (0x2151)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1013">8529 (0x2151)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1014">O Gerenciador de contas de segurança precisa obter a senha de inicialização.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1014">Security Account Manager needs to get the boot password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERRO \_ DS \_ Sam \_ necessário \_ \_ disquete BOOTKEY**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_FLOPPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1016">8530 (0x2152)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1016">8530 (0x2152)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1017">O Gerenciador de contas de segurança precisa obter a chave de inicialização do disquete.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1017">Security Account Manager needs to get the boot key from floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERRO o \_ DS não \_ consegue \_ Iniciar**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERROR\_DS\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1019">8531 (0x2153)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1019">8531 (0x2153)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1020">Não é possível iniciar o serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1020">Directory Service cannot start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERRO \_ de \_ falha de inicialização DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERROR\_DS\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1022">8532 (0x2154)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1022">8532 (0x2154)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1023">Os serviços de diretório não puderam ser iniciados.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1023">Directory Services could not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERRO \_ DS \_ sem \_ \_ privacidade \_ de PKT na \_ conexão**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERROR\_DS\_NO\_PKT\_PRIVACY\_ON\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1025">8533 (0x2155)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1025">8533 (0x2155)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1026">A conexão entre o cliente e o servidor requer a privacidade do pacote ou melhor.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1026">The connection between client and server requires packet privacy or better.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERRO \_ \_ \_ \_ de domínio de origem do DS na \_ floresta**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERROR\_DS\_SOURCE\_DOMAIN\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1028">8534 (0x2156)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1028">8534 (0x2156)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1029">O domínio de origem pode não estar na mesma floresta que o destino.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1029">The source domain may not be in the same forest as destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERRO \_ \_ \_ domínio de destino DS não está \_ \_ na \_ floresta**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERROR\_DS\_DESTINATION\_DOMAIN\_NOT\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1031">8535 (0x2157)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1031">8535 (0x2157)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1032">O domínio de destino deve estar na floresta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1032">The destination domain must be in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERRO \_ de \_ auditoria de destino DS \_ \_ não \_ habilitada**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERROR\_DS\_DESTINATION\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1034">8536 (0x2158)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1034">8536 (0x2158)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1035">A operação requer que a auditoria de domínio de destino esteja habilitada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1035">The operation requires that destination domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERRO \_ DS não \_ consegue \_ encontrar o \_ DC para o \_ \_ \_ domínio src**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERROR\_DS\_CANT\_FIND\_DC\_FOR\_SRC\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1037">8537 (0x2159)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1037">8537 (0x2159)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1038">A operação não pôde localizar um DC para o domínio de origem.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1038">The operation couldn't locate a DC for the source domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERRO \_ DS \_ src \_ obj \_ não \_ grupo \_ ou \_ usuário**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERROR\_DS\_SRC\_OBJ\_NOT\_GROUP\_OR\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1040">8538 (0x215A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1040">8538 (0x215A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1041">O objeto de origem deve ser um grupo ou um usuário.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1041">The source object must be a group or user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERRO \_ o \_ Sid src DS \_ \_ existe \_ na \_ floresta**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERROR\_DS\_SRC\_SID\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1043">8539 (0x215B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1043">8539 (0x215B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1044">O SID do objeto de origem já existe na floresta de destino.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1044">The source object's SID already exists in destination forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERRO \_ \_ \_ de \_ \_ \_ incompatibilidade de classe de objeto DS src e DST \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERROR\_DS\_SRC\_AND\_DST\_OBJECT\_CLASS\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1046">8540 (0x215C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1046">8540 (0x215C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1047">O objeto de origem e de destino deve ser do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1047">The source and destination object must be of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERRO \_ Sam \_ init \_ falha**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERROR\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1049">8541 (0x215D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1049">8541 (0x215D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1050">Falha na inicialização do Gerenciador de contas de segurança devido ao seguinte erro: %1.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1050">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="2d00a-1051">Status do erro: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1051">Error Status: 0x%2.</span></span> <span data-ttu-id="2d00a-1052">Clique em OK para desligar o sistema e reinicializar no modo de segurança.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1052">Click OK to shut down the system and reboot into Safe Mode.</span></span> <span data-ttu-id="2d00a-1053">Verifique o log de eventos para obter informações detalhadas.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1053">Check the event log for detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERRO \_ de \_ \_ remessa de informações de esquema Dra \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERROR\_DS\_DRA\_SCHEMA\_INFO\_SHIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1055">8542 (0x215E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1055">8542 (0x215E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1056">Não foi possível incluir as informações de esquema na solicitação de replicação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1056">Schema information could not be included in the replication request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERRO \_ de \_ \_ conflito de esquema Dra DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERROR\_DS\_DRA\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1058">8543 (0x215F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1058">8543 (0x215F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1059">A operação de replicação não pôde ser concluída devido a uma incompatibilidade de esquema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1059">The replication operation could not be completed due to a schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERRO \_ DS \_ Dra \_ anterior \_ conflito de esquema \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERROR\_DS\_DRA\_EARLIER\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1061">8544 (0x2160)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1061">8544 (0x2160)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1062">A operação de replicação não pôde ser concluída devido a uma incompatibilidade de esquema anterior.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1062">The replication operation could not be completed due to a previous schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERRO \_ DS \_ Dra \_ obj \_ NC \_ incompatível**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERROR\_DS\_DRA\_OBJ\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1064">8545 (0x2161)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1064">8545 (0x2161)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1065">Não foi possível aplicar a atualização de replicação porque a origem ou o destino ainda não recebeu informações sobre uma operação de movimentação entre domínios recente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1065">The replication update could not be applied because either the source or the destination has not yet received information regarding a recent cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**o \_ erro \_ NC DS \_ ainda \_ tem \_ DSAs**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**ERROR\_DS\_NC\_STILL\_HAS\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1067">8546 (0x2162)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1067">8546 (0x2162)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1068">Não foi possível excluir o domínio solicitado porque existem controladores de domínio que ainda hospedam esse domínio.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1068">The requested domain could not be deleted because there exist domain controllers that still host this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERRO \_ de \_ GC de DS \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERROR\_DS\_GC\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1070">8547 (0x2163)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1070">8547 (0x2163)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1071">A operação solicitada pode ser executada somente em um servidor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1071">The requested operation can be performed only on a global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERRO \_ \_ local \_ de membro \_ do \_ DS \_ somente local**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERROR\_DS\_LOCAL\_MEMBER\_OF\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1073">8548 (0x2164)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1073">8548 (0x2164)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1074">Um grupo local só pode ser um membro de outros grupos locais no mesmo domínio.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1074">A local group can only be a member of other local groups in the same domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERRO \_ DS \_ sem \_ FPO \_ em \_ grupos universais \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERROR\_DS\_NO\_FPO\_IN\_UNIVERSAL\_GROUPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1076">8549 (0x2165)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1076">8549 (0x2165)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1077">Entidades de segurança externas não podem ser membros de grupos universais.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1077">Foreign security principals cannot be members of universal groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERRO \_ DS não \_ consegue \_ Adicionar \_ ao \_ GC**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERROR\_DS\_CANT\_ADD\_TO\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1079">8550 (0x2166)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1079">8550 (0x2166)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1080">O atributo não pode ser replicado para o GC devido a motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1080">The attribute is not allowed to be replicated to the GC because of security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERRO \_ DS \_ sem \_ ponto \_ de verificação com \_ PDC**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERROR\_DS\_NO\_CHECKPOINT\_WITH\_PDC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1082">8551 (0x2167)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1082">8551 (0x2167)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1083">O ponto de verificação com o PDC não pôde ser obtido porque há muitas modificações sendo processadas no momento.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1083">The checkpoint with the PDC could not be taken because there too many modifications being processed currently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERRO \_ de \_ auditoria de origem DS \_ \_ não \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERROR\_DS\_SOURCE\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1085">8552 (0x2168)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1085">8552 (0x2168)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1086">A operação requer que a auditoria de domínio de origem esteja habilitada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1086">The operation requires that source domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERRO \_ DS não \_ consegue \_ criar \_ no \_ \_ NC não domínio**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERROR\_DS\_CANT\_CREATE\_IN\_NONDOMAIN\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1088">8553 (0x2169)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1088">8553 (0x2169)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1089">Os objetos de entidade de segurança só podem ser criados dentro de contextos de nomenclatura de domínio.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1089">Security principal objects can only be created inside domain naming contexts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERRO \_ \_ \_ nome de DS inválido \_ para \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERROR\_DS\_INVALID\_NAME\_FOR\_SPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1091">8554 (0x216A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1091">8554 (0x216A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1092">Não foi possível construir um SPN (nome da entidade de serviço) porque o nome do host fornecido não está no formato necessário.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1092">A Service Principal Name (SPN) could not be constructed because the provided hostname is not in the necessary format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERRO \_ o \_ filtro DS \_ usa \_ construído \_ ATTRS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERROR\_DS\_FILTER\_USES\_CONTRUCTED\_ATTRS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1094">8555 (0x216B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1094">8555 (0x216B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1095">Foi passado um filtro que usa atributos construídos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1095">A Filter was passed that uses constructed attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERRO o \_ DS \_ UNICODEPWD não está \_ \_ entre \_ aspas**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERROR\_DS\_UNICODEPWD\_NOT\_IN\_QUOTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1097">8556 (0x216C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1097">8556 (0x216C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1098">O valor do atributo unicodePwd deve ser colocado entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1098">The unicodePwd attribute value must be enclosed in double quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERRO \_ de \_ cota de conta de computador DS \_ \_ \_ excedida**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1100">8557 (0x216D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1100">8557 (0x216D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1101">Seu computador não pôde ingressar no domínio.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1101">Your computer could not be joined to the domain.</span></span> <span data-ttu-id="2d00a-1102">Você excedeu o número máximo de contas de computador que você tem permissão para criar nesse domínio.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1102">You have exceeded the maximum number of computer accounts you are allowed to create in this domain.</span></span> <span data-ttu-id="2d00a-1103">Contate o administrador do sistema para que esse limite seja redefinido ou aumentado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1103">Contact your system administrator to have this limit reset or increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**o erro \_ DS \_ deve \_ ser \_ executado \_ no \_ \_ DC do DST**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**ERROR\_DS\_MUST\_BE\_RUN\_ON\_DST\_DC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1105">8558 (0x216E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1105">8558 (0x216E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1106">Por motivos de segurança, a operação deve ser executada no DC de destino.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1106">For security reasons, the operation must be run on the destination DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERRO \_ DS \_ src \_ DC \_ deve \_ ser \_ SP4 \_ ou \_ superior**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERROR\_DS\_SRC\_DC\_MUST\_BE\_SP4\_OR\_GREATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1108">8559 (0x216F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1108">8559 (0x216F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1109">Por motivos de segurança, o DC de origem deve ser NT4SP4 ou superior.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1109">For security reasons, the source DC must be NT4SP4 or greater.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERRO DS não é possível \_ \_ excluir a \_ árvore \_ \_ crítica \_ obj**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERROR\_DS\_CANT\_TREE\_DELETE\_CRITICAL\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1111">8560 (0x2170)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1111">8560 (0x2170)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1112">Os objetos do sistema de serviço de diretório crítico não podem ser excluídos durante operações de exclusão de árvore.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1112">Critical Directory Service System objects cannot be deleted during tree delete operations.</span></span> <span data-ttu-id="2d00a-1113">A exclusão de árvore pode ter sido parcialmente executada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1113">The tree delete may have been partially performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERRO \_ do \_ \_ console de falha de inicialização DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERROR\_DS\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1115">8561 (0x2171)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1115">8561 (0x2171)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1116">Os serviços de diretório não puderam ser iniciados devido ao seguinte erro: %1.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1116">Directory Services could not start because of the following error: %1.</span></span> <span data-ttu-id="2d00a-1117">Status do erro: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1117">Error Status: 0x%2.</span></span> <span data-ttu-id="2d00a-1118">Clique em OK para desligar o sistema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1118">Please click OK to shutdown the system.</span></span> <span data-ttu-id="2d00a-1119">Você pode usar o console de recuperação para diagnosticar o sistema mais profundamente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1119">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERRO \_ DS \_ Sam \_ init \_ falha no \_ console**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1121">8562 (0x2172)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1121">8562 (0x2172)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1122">Falha na inicialização do Gerenciador de contas de segurança devido ao seguinte erro: %1.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1122">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="2d00a-1123">Status do erro: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1123">Error Status: 0x%2.</span></span> <span data-ttu-id="2d00a-1124">Clique em OK para desligar o sistema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1124">Please click OK to shutdown the system.</span></span> <span data-ttu-id="2d00a-1125">Você pode usar o console de recuperação para diagnosticar o sistema mais profundamente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1125">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERRO \_ de \_ versão de floresta DS \_ \_ muito \_ alta**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1127">8563 (0x2173)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1127">8563 (0x2173)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1128">A versão do sistema operacional é incompatível com o nível funcional da floresta AD DS atual ou AD LDS nível funcional do conjunto de configuração.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1128">The version of the operating system is incompatible with the current AD DS forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="2d00a-1129">Você deve atualizar para uma nova versão do sistema operacional antes que este servidor possa se tornar um AD DS controlador de domínio ou adicionar uma instância de AD LDS neste AD DS floresta ou AD LDS conjunto de configurações.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1129">You must upgrade to a new version of the operating system before this server can become an AD DS Domain Controller or add an AD LDS Instance in this AD DS Forest or AD LDS Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERRO \_ de \_ versão de domínio DS \_ \_ muito \_ alta**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1131">8564 (0x2174)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1131">8564 (0x2174)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1132">A versão do sistema operacional instalado é incompatível com o nível funcional do domínio atual.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1132">The version of the operating system installed is incompatible with the current domain functional level.</span></span> <span data-ttu-id="2d00a-1133">Você deve atualizar para uma nova versão do sistema operacional antes que este servidor possa se tornar um controlador de domínio nesse domínio.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1133">You must upgrade to a new version of the operating system before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERRO \_ de \_ versão de floresta DS \_ \_ muito \_ baixa**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1135">8565 (0x2175)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1135">8565 (0x2175)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1136">A versão do sistema operacional instalado neste servidor não dá mais suporte ao nível funcional da floresta AD DS atual ou AD LDS nível funcional do conjunto de configurações.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1136">The version of the operating system installed on this server no longer supports the current AD DS Forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="2d00a-1137">Você deve aumentar o nível funcional da floresta AD DS ou AD LDS o nível funcional do conjunto de configuração antes que este servidor possa se tornar um controlador de domínio AD DS ou uma instância de AD LDS nesta floresta ou conjunto de configuração.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1137">You must raise the AD DS Forest functional level or AD LDS Configuration Set functional level before this server can become an AD DS Domain Controller or an AD LDS Instance in this Forest or Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERRO \_ de \_ versão de domínio DS \_ \_ muito \_ baixo**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1139">8566 (0x2176)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1139">8566 (0x2176)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1140">A versão do sistema operacional instalado neste servidor não dá mais suporte ao nível funcional do domínio atual.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1140">The version of the operating system installed on this server no longer supports the current domain functional level.</span></span> <span data-ttu-id="2d00a-1141">Você deve aumentar o nível funcional do domínio para que este servidor possa se tornar um controlador de domínio nesse domínio.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1141">You must raise the domain functional level before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERRO \_ de \_ versão incompatível DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERROR\_DS\_INCOMPATIBLE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1143">8567 (0x2177)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1143">8567 (0x2177)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1144">A versão do sistema operacional instalado neste servidor é incompatível com o nível funcional do domínio ou da floresta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1144">The version of the operating system installed on this server is incompatible with the functional level of the domain or forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERRO \_ de \_ versão mínima de \_ DSA de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERROR\_DS\_LOW\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1146">8568 (0x2178)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1146">8568 (0x2178)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1147">O nível funcional do domínio (ou floresta) não pode ser gerado para o valor solicitado, pois existe um ou mais controladores de domínio no domínio (ou floresta) que estão em um nível funcional inferior incompatível.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1147">The functional level of the domain (or forest) cannot be raised to the requested value, because there exist one or more domain controllers in the domain (or forest) that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERRO \_ DS \_ sem \_ \_ versão \_ de comportamento em \_ MIXEDDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERROR\_DS\_NO\_BEHAVIOR\_VERSION\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1149">8569 (0x2179)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1149">8569 (0x2179)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1150">O nível funcional da floresta não pode ser aumentado para o valor solicitado, pois um ou mais domínios ainda estão no modo de domínio misto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1150">The forest functional level cannot be raised to the requested value since one or more domains are still in mixed domain mode.</span></span> <span data-ttu-id="2d00a-1151">Todos os domínios na floresta devem estar no modo nativo para que você aumente o nível funcional da floresta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1151">All domains in the forest must be in native mode, for you to raise the forest functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERRO \_ DS \_ sem \_ suporte \_ \_ para ordem de classificação**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERROR\_DS\_NOT\_SUPPORTED\_SORT\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1153">8570 (0x217A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1153">8570 (0x217A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1154">Não há suporte para a ordem de classificação solicitada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1154">The sort order requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERRO \_ \_ nome DS \_ não \_ exclusivo**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERROR\_DS\_NAME\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1156">8571 (0x217B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1156">8571 (0x217B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1157">O nome solicitado já existe como um identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1157">The requested name already exists as a unique identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERRO \_ \_ conta do computador DS \_ \_ criada \_ PRENT4**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_CREATED\_PRENT4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1159">8572 (0x217C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1159">8572 (0x217C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1160">A conta da máquina foi criada antes do NT4.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1160">The machine account was created pre-NT4.</span></span> <span data-ttu-id="2d00a-1161">A conta precisa ser recriada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1161">The account needs to be recreated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERRO \_ DS \_ fora \_ do \_ repositório de versão \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERROR\_DS\_OUT\_OF\_VERSION\_STORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1163">8573 (0x217D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1163">8573 (0x217D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1164">O banco de dados está fora do repositório de versão.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1164">The database is out of version store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERRO \_ de \_ controles incompatíveis DS \_ \_ usados**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERROR\_DS\_INCOMPATIBLE\_CONTROLS\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1166">8574 (0x217E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1166">8574 (0x217E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1167">Não é possível continuar a operação porque vários controles conflitantes foram usados.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1167">Unable to continue operation because multiple conflicting controls were used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERRO \_ DS \_ sem \_ referência de \_ domínio**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERROR\_DS\_NO\_REF\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1169">8575 (0x217F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1169">8575 (0x217F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1170">Não é possível localizar um domínio de referência de descritor de segurança válido para esta partição.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1170">Unable to find a valid security descriptor reference domain for this partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**ERRO \_ \_ ID de \_ link \_ reservado DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**ERROR\_DS\_RESERVED\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1172">8576 (0x2180)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1172">8576 (0x2180)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1173">Falha na atualização do esquema: o identificador de link está reservado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1173">Schema update failed: The link identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERRO \_ \_ ID de link DS \_ \_ não \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERROR\_DS\_LINK\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1175">8577 (0x2181)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1175">8577 (0x2181)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1176">Falha na atualização do esquema: não há identificadores de link disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1176">Schema update failed: There are no link identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERRO \_ AG do DS não \_ \_ \_ pode ter \_ \_ membro universal**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERROR\_DS\_AG\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1178">8578 (0x2182)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1178">8578 (0x2182)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1179">Um grupo de contas não pode ter um grupo universal como membro.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1179">An account group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERRO \_ MODIFYDN DS não \_ \_ permitido \_ por \_ tipo de instância \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1181">8579 (0x2183)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1181">8579 (0x2183)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1182">As operações de renomeação ou movimentação em cabeçalhos de contexto de nomenclatura ou objetos somente leitura não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1182">Rename or move operations on naming context heads or read-only objects are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERRO \_ DS \_ sem \_ \_ movimentação \_ de objeto \_ no \_ NC de esquema**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERROR\_DS\_NO\_OBJECT\_MOVE\_IN\_SCHEMA\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1184">8580 (0x2184)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1184">8580 (0x2184)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1185">As operações de movimentação em objetos no contexto de nomenclatura de esquema não são permitidas.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1185">Move operations on objects in the schema naming context are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERRO \_ MODIFYDN DS não \_ \_ permitido \_ por \_ sinalizador**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1187">8581 (0x2185)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1187">8581 (0x2185)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1188">Um sinalizador do sistema foi definido no objeto e não permite que o objeto seja movido ou renomeado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1188">A system flag has been set on the object and does not allow the object to be moved or renamed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERRO \_ DS \_ MODIFYDN \_ avô incorreto \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERROR\_DS\_MODIFYDN\_WRONG\_GRANDPARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1190">8582 (0x2186)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1190">8582 (0x2186)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1191">Este objeto não tem permissão para alterar seu contêiner avô.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1191">This object is not allowed to change its grandparent container.</span></span> <span data-ttu-id="2d00a-1192">As movimentações não são proibidas nesse objeto, mas são restritas a contêineres irmãos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1192">Moves are not forbidden on this object, but are restricted to sibling containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERRO \_ \_ nome DS \_ erro \_ referência de confiança \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERROR\_DS\_NAME\_ERROR\_TRUST\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1194">8583 (0x2187)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1194">8583 (0x2187)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1195">Não é possível resolver completamente, uma referência a outra floresta é gerada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1195">Unable to resolve completely, a referral to another forest is generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERRO \_ sem \_ suporte \_ no \_ \_ servidor Standard**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERROR\_NOT\_SUPPORTED\_ON\_STANDARD\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1197">8584 (0x2188)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1197">8584 (0x2188)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1198">Não há suporte para a ação solicitada no servidor padrão.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1198">The requested action is not supported on standard server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERRO \_ DS \_ não \_ consegue \_ acessar \_ parte remota \_ do \_ AD**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERROR\_DS\_CANT\_ACCESS\_REMOTE\_PART\_OF\_AD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1200">8585 (0x2189)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1200">8585 (0x2189)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1201">Não foi possível acessar uma partição do serviço de diretório localizado em um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1201">Could not access a partition of the directory service located on a remote server.</span></span> <span data-ttu-id="2d00a-1202">Verifique se pelo menos um servidor está em execução para a partição em questão.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1202">Make sure at least one server is running for the partition in question.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERRO \_ \_ de DS CR \_ impossível \_ para \_ validar \_ v2**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE\_V2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1204">8586 (0x218A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1204">8586 (0x218A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1205">O diretório não pode validar o nome de contexto (ou partição) de nomenclatura proposto porque ele não contém uma réplica nem pode entrar em contato com uma réplica do contexto de nomenclatura acima do contexto de nomenclatura proposto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1205">The directory cannot validate the proposed naming context (or partition) name because it does not hold a replica nor can it contact a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="2d00a-1206">Verifique se o contexto de nomenclatura pai está registrado corretamente no DNS e se pelo menos uma réplica desse contexto de nomenclatura pode ser acessada pelo mestre de nomeação de domínio.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1206">Please ensure that the parent naming context is properly registered in DNS, and at least one replica of this naming context is reachable by the Domain Naming master.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**ERRO \_ \_ limite de thread DS \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**ERROR\_DS\_THREAD\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1208">8587 (0x218B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1208">8587 (0x218B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1209">O limite de thread para esta solicitação foi excedido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1209">The thread limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERRO \_ DS \_ não \_ mais próximo**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERROR\_DS\_NOT\_CLOSEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1211">8588 (0x218C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1211">8588 (0x218C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1212">O servidor de catálogo global não está no site mais próximo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1212">The Global catalog server is not in the closest site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERRO \_ DS não \_ consegue \_ derivar \_ SPN \_ sem \_ ref do servidor \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_WITHOUT\_SERVER\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1214">8589 (0x218D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1214">8589 (0x218D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1215">O DS não pode derivar um SPN (nome da entidade de serviço) com o qual autenticar mutuamente o servidor de destino porque o objeto de servidor correspondente no banco de dados DS local não tem nenhum atributo serverReference.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1215">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the corresponding server object in the local DS database has no serverReference attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERRO \_ \_ \_ no modo de usuário único \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERROR\_DS\_SINGLE\_USER\_MODE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1217">8590 (0x218E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1217">8590 (0x218E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1218">O serviço de diretório não pôde entrar no modo de usuário único.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1218">The Directory Service failed to enter single user mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**erro \_ de \_ \_ erro de sintaxe DS NTDSCRIPT \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**ERROR\_DS\_NTDSCRIPT\_SYNTAX\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1220">8591 (0x218F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1220">8591 (0x218F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1221">O serviço de diretório não pode analisar o script devido a um erro de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1221">The Directory Service cannot parse the script because of a syntax error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**ERRO \_ de \_ processo de NTDSCRIPT DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**ERROR\_DS\_NTDSCRIPT\_PROCESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1223">8592 (0x2190)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1223">8592 (0x2190)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1224">O serviço de diretório não pode processar o script devido a um erro.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1224">The Directory Service cannot process the script because of an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERRO \_ de \_ \_ épocas de repl diferentes de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERROR\_DS\_DIFFERENT\_REPL\_EPOCHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1226">8593 (0x2191)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1226">8593 (0x2191)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1227">O serviço de diretório não pode executar a operação solicitada porque os servidores envolvidos são de épocas de replicação diferentes (que geralmente estão relacionadas a uma renomeação de domínio em andamento).</span><span class="sxs-lookup"><span data-stu-id="2d00a-1227">The directory service cannot perform the requested operation because the servers involved are of different replication epochs (which is usually related to a domain rename that is in progress).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERRO \_ nas \_ extensões DS DRS \_ \_ alteradas**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERROR\_DS\_DRS\_EXTENSIONS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1229">8594 (0x2192)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1229">8594 (0x2192)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1230">A associação de serviço de diretório deve ser renegociada devido a uma alteração nas informações de extensões de servidor.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1230">The directory service binding must be renegotiated due to a change in the server extensions information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERRO \_ \_ \_ \_ de alteração de conjunto \_ de réplica DS não \_ permitido \_ em \_ CR desabilitado \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERROR\_DS\_REPLICA\_SET\_CHANGE\_NOT\_ALLOWED\_ON\_DISABLED\_CR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1232">8595 (0x2193)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1232">8595 (0x2193)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1233">Operação não permitida em uma referência cruzada desabilitada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1233">Operation not allowed on a disabled cross ref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERRO \_ DS \_ sem \_ msDS \_ inicial**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERROR\_DS\_NO\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1235">8596 (0x2194)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1235">8596 (0x2194)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1236">Falha na atualização do esquema: nenhum valor para o msDS-inicial está disponível.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1236">Schema update failed: No values for msDS-IntId are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERRO de Dup de DS inicial de \_ \_ \_ msDS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERROR\_DS\_DUP\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1238">8597 (0x2195)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1238">8597 (0x2195)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1239">Falha na atualização do esquema: msDS-inicial duplicado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1239">Schema update failed: Duplicate msDS-INtId.</span></span> <span data-ttu-id="2d00a-1240">Repita a operação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1240">Retry the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERRO \_ DS \_ existente \_ em \_ RDNATTID**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERROR\_DS\_EXISTS\_IN\_RDNATTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1242">8598 (0x2196)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1242">8598 (0x2196)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1243">Falha na exclusão do esquema: o atributo é usado em rDNAttID.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1243">Schema deletion failed: attribute is used in rDNAttID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERRO \_ de \_ autorização DS \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERROR\_DS\_AUTHORIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1245">8599 (0x2197)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1245">8599 (0x2197)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1246">O serviço de diretório não pôde autorizar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1246">The directory service failed to authorize the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERRO \_ de \_ script DS inválido \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERROR\_DS\_INVALID\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1248">8600 (0x2198)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1248">8600 (0x2198)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1249">O serviço de diretório não pode processar o script porque ele é inválido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1249">The Directory Service cannot process the script because it is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERRO \_ \_ \_ \_ falha no operação do CROSSREF remoto do DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERROR\_DS\_REMOTE\_CROSSREF\_OP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1251">8601 (0x2199)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1251">8601 (0x2199)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1252">A operação de referência cruzada de criação remota falhou no mestre de nomeação de domínio FSMO.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1252">The remote create cross reference operation failed on the Domain Naming Master FSMO.</span></span> <span data-ttu-id="2d00a-1253">O erro da operação está nos dados estendidos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1253">The operation's error is in the extended data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERRO \_ de \_ referência cruzada DS \_ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERROR\_DS\_CROSS\_REF\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1255">8602 (0x219A)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1255">8602 (0x219A)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1256">Uma referência cruzada está em uso localmente com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1256">A cross reference is in use locally with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERRO \_ DS não \_ consegue \_ derivar \_ SPN \_ para \_ \_ domínio excluído**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_FOR\_DELETED\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1258">8603 (0x219B)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1258">8603 (0x219B)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1259">O DS não pode derivar um SPN (nome da entidade de serviço) com o qual autenticar mutuamente o servidor de destino porque o domínio do servidor foi excluído da floresta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1259">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the server's domain has been deleted from the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERRO \_ DS \_ impossível \_ rebaixar \_ com \_ NC gravável \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERROR\_DS\_CANT\_DEMOTE\_WITH\_WRITEABLE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1261">8604 (0x219C)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1261">8604 (0x219C)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1262">NCs graváveis impedem que este DC rebaixe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1262">Writeable NCs prevent this DC from demoting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERRO \_ \_ Id duplicada de DS \_ \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERROR\_DS\_DUPLICATE\_ID\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1264">8605 (0x219D)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1264">8605 (0x219D)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1265">O objeto solicitado tem um identificador não exclusivo e não pode ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1265">The requested object has a non-unique identifier and cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERRO \_ \_ \_ de attr insuficiente de DS \_ para \_ criar \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERROR\_DS\_INSUFFICIENT\_ATTR\_TO\_CREATE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1267">8606 (0x219E)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1267">8606 (0x219E)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1268">Atributos insuficientes foram fornecidos para criar um objeto.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1268">Insufficient attributes were given to create an object.</span></span> <span data-ttu-id="2d00a-1269">Este objeto pode não existir porque pode ter sido excluído e já ter sido coletado como lixo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1269">This object may not exist because it may have been deleted and already garbage collected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**erro \_ de \_ conversão de grupo DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**ERROR\_DS\_GROUP\_CONVERSION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1271">8607 (0x219F)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1271">8607 (0x219F)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1272">O grupo não pode ser convertido devido a restrições de atributo no tipo de grupo solicitado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1272">The group cannot be converted due to attribute restrictions on the requested group type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERRO \_ DS não \_ consegue \_ mover o \_ \_ grupo básico do aplicativo \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_BASIC\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1274">8608 (0x21A0)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1274">8608 (0x21A0)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1275">A movimentação entre domínios de grupos de aplicativos básicos não vazios não é permitida.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1275">Cross-domain move of non-empty basic application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERRO \_ DS não \_ consegue mover o grupo de \_ consultas de \_ aplicativo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_QUERY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1277">8609 (0x21A1)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1277">8609 (0x21A1)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1278">Não é permitida a movimentação entre domínios de grupos de aplicativos baseados em consultas não vazias.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1278">Cross-domain move of non-empty query based application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERRO \_ de \_ função DS \_ não \_ verificada**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERROR\_DS\_ROLE\_NOT\_VERIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1280">8610 (0x21A2)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1280">8610 (0x21A2)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1281">A propriedade da função FSMO não pôde ser verificada porque sua partição de diretório não foi replicada com êxito com pelo menos um parceiro de replicação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1281">The FSMO role ownership could not be verified because its directory partition has not replicated successfully with at least one replication partner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERRO \_ o \_ contêiner WKO DS \_ \_ não pode \_ ser \_ especial**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERROR\_DS\_WKO\_CONTAINER\_CANNOT\_BE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1283">8611 (0x21A3)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1283">8611 (0x21A3)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1284">O contêiner de destino para um redirecionamento de um contêiner de objeto bem conhecido não pode já ser um contêiner especial.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1284">The target container for a redirection of a well known object container cannot already be a special container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERRO \_ \_ \_ de renomeação de domínio DS \_ em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERROR\_DS\_DOMAIN\_RENAME\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1286">8612 (0x21A4)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1286">8612 (0x21A4)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1287">O serviço de diretório não pode executar a operação solicitada porque uma operação de renomeação de domínio está em andamento.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1287">The Directory Service cannot perform the requested operation because a domain rename operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERRO \_ \_ NC DS \_ filho do AD existente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERROR\_DS\_EXISTING\_AD\_CHILD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1289">8613 (0x21A5)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1289">8613 (0x21A5)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1290">O serviço de diretório detectou uma partição filho abaixo do nome da partição solicitada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1290">The directory service detected a child partition below the requested partition name.</span></span> <span data-ttu-id="2d00a-1291">A hierarquia de partição deve ser criada em um método de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1291">The partition hierarchy must be created in a top down method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERRO \_ de \_ tempo de vida de repl DS \_ \_ excedido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERROR\_DS\_REPL\_LIFETIME\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1293">8614 (0x21A6)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1293">8614 (0x21A6)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1294">O serviço de diretório não pode replicar com este servidor porque o tempo desde a última replicação com este servidor excedeu a vida útil da marca para exclusão.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1294">The directory service cannot replicate with this server because the time since the last replication with this server has exceeded the tombstone lifetime.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERRO \_ DS não \_ permitido \_ no \_ contêiner do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERROR\_DS\_DISALLOWED\_IN\_SYSTEM\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1296">8615 (0x21A7)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1296">8615 (0x21A7)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1297">A operação solicitada não é permitida em um objeto no contêiner do sistema.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1297">The requested operation is not allowed on an object under the system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERRO \_ de \_ fila de envio de LDAP DS \_ \_ \_ cheio**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERROR\_DS\_LDAP\_SEND\_QUEUE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1299">8616 (0x21A8)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1299">8616 (0x21A8)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1300">A fila de envio de rede dos servidores LDAP foi preenchida porque o cliente não está processando os resultados de suas solicitações com rapidez suficiente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1300">The LDAP servers network send queue has filled up because the client is not processing the results of its requests fast enough.</span></span> <span data-ttu-id="2d00a-1301">Nenhuma solicitação será processada até que o cliente seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1301">No more requests will be processed until the client catches up.</span></span> <span data-ttu-id="2d00a-1302">Se o cliente não for atualizado, ele será desconectado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1302">If the client does not catch up then it will be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERRO \_ na \_ \_ janela de \_ agendamento de saída \_ DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERROR\_DS\_DRA\_OUT\_SCHEDULE\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1304">8617 (0x21A9)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1304">8617 (0x21A9)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1305">A replicação agendada não foi realizada porque o sistema estava muito ocupado para executar a solicitação dentro da janela de agendamento.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1305">The scheduled replication did not take place because the system was too busy to execute the request within the schedule window.</span></span> <span data-ttu-id="2d00a-1306">A fila de replicação está sobrecarregada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1306">The replication queue is overloaded.</span></span> <span data-ttu-id="2d00a-1307">Considere a redução do número de parceiros ou a redução da frequência de replicação agendada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1307">Consider reducing the number of partners or decreasing the scheduled replication frequency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERRO \_ de \_ política DS \_ não \_ conhecida**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERROR\_DS\_POLICY\_NOT\_KNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1309">8618 (0x21AA)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1309">8618 (0x21AA)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1310">Neste momento, não será possível determinar se a política de replicação de ramificação está disponível no controlador de domínio do Hub.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1310">At this time, it cannot be determined if the branch replication policy is available on the hub domain controller.</span></span> <span data-ttu-id="2d00a-1311">Tente novamente mais tarde para considerar as latências de replicação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1311">Please retry at a later time to account for replication latencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERRO \_ nenhum \_ \_ objeto de configurações de site \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERROR\_NO\_SITE\_SETTINGS\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1313">8619 (0x21AB)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1313">8619 (0x21AB)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1314">O objeto de configurações de site para o site especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1314">The site settings object for the specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERRO \_ sem \_ segredos**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERROR\_NO\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1316">8620 (0x21AC)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1316">8620 (0x21AC)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1317">O repositório de conta local não contém material secreto para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1317">The local account store does not contain secret material for the specified account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERRO \_ nenhum \_ \_ DC gravável \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERROR\_NO\_WRITABLE\_DC\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1319">8621 (0x21AD)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1319">8621 (0x21AD)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1320">Não foi possível encontrar um controlador de domínio gravável no domínio.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1320">Could not find a writable domain controller in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERRO \_ DS \_ nenhum \_ objeto de servidor \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERROR\_DS\_NO\_SERVER\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1322">8622 (0x21AE)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1322">8622 (0x21AE)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1323">O objeto de servidor para o controlador de domínio não existe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1323">The server object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERRO \_ DS \_ sem \_ objeto NTDSA \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERROR\_DS\_NO\_NTDSA\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1325">8623 (0x21AF)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1325">8623 (0x21AF)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1326">O objeto de configurações NTDS para o controlador de domínio não existe.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1326">The NTDS Settings object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERRO \_ de \_ \_ pesquisa não \_ ASQ de DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERROR\_DS\_NON\_ASQ\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1328">8624 (0x21B0)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1328">8624 (0x21B0)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1329">A operação de pesquisa solicitada não tem suporte para pesquisas de ASQ.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1329">The requested search operation is not supported for ASQ searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERRO \_ de \_ falha de auditoria de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERROR\_DS\_AUDIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1331">8625 (0x21B1)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1331">8625 (0x21B1)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1332">Um evento de auditoria necessário não pôde ser gerado para a operação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1332">A required audit event could not be generated for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERRO \_ na \_ \_ \_ subárvore do sinalizador de pesquisa inválido do DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_SUBTREE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1334">8626 (0x21B2)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1334">8626 (0x21B2)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1335">Os sinalizadores de pesquisa para o atributo são inválidos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1335">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="2d00a-1336">O bit de índice de subárvore é válido somente em atributos com valor único.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1336">The subtree index bit is valid only on single valued attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERRO \_ de \_ \_ tupla de \_ sinalizador de pesquisa inválido \_ de DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_TUPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1338">8627 (0x21B3)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1338">8627 (0x21B3)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1339">Os sinalizadores de pesquisa para o atributo são inválidos.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1339">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="2d00a-1340">O bit de índice de tupla é válido somente em atributos de cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1340">The tuple index bit is valid only on attributes of Unicode strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERRO \_ na \_ tabela de hierarquia DS \_ \_ muito \_ profunda**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_TOO\_DEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1342">8628 (0x21B4)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1342">8628 (0x21B4)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1343">Os catálogos de endereços estão aninhados muito profundamente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1343">The address books are nested too deeply.</span></span> <span data-ttu-id="2d00a-1344">Falha ao criar a tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1344">Failed to build the hierarchy table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERRO \_ de \_ \_ vetor de \_ Utd corrompido de Dra DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERROR\_DS\_DRA\_CORRUPT\_UTD\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1346">8629 (0x21B5)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1346">8629 (0x21B5)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1347">O vetor de atualização de qualidade especificado está corrompido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1347">The specified up-to-date-ness vector is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERRO \_ de \_ segredos de Dra DS \_ \_ negado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERROR\_DS\_DRA\_SECRETS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1349">8630 (0x21B6)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1349">8630 (0x21B6)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1350">A solicitação para replicar segredos foi negada.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1350">The request to replicate secrets is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERRO \_ \_ ID de \_ MAPI reservada para DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERROR\_DS\_RESERVED\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1352">8631 (0x21B7)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1352">8631 (0x21B7)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1353">Falha na atualização do esquema: o identificador MAPI está reservado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1353">Schema update failed: The MAPI identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERRO a \_ ID de MAPI do DS \_ \_ \_ não \_ está disponível**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERROR\_DS\_MAPI\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1355">8632 (0x21B8)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1355">8632 (0x21B8)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1356">Falha na atualização do esquema: não há identificadores MAPI disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1356">Schema update failed: There are no MAPI identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERRO \_ DS \_ Dra \_ faltando \_ segredo de krbtgt \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERROR\_DS\_DRA\_MISSING\_KRBTGT\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1358">8633 (0x21B9)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1358">8633 (0x21B9)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1359">Falha na operação de replicação porque os atributos necessários do objeto krbtgt local estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1359">The replication operation failed because the required attributes of the local krbtgt object are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERRO \_ o \_ \_ nome de domínio DS \_ existe \_ na \_ floresta**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERROR\_DS\_DOMAIN\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1361">8634 (0x21BA)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1361">8634 (0x21BA)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1362">O nome de domínio do domínio confiável já existe na floresta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1362">The domain name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERRO \_ o \_ \_ nome simples \_ do DS existe \_ na \_ floresta**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERROR\_DS\_FLAT\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1364">8635 (0x21BB)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1364">8635 (0x21BB)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1365">O nome simples do domínio confiável já existe na floresta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1365">The flat name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**\_nome da \_ entidade de usuário \_ \_ do erro inválido**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERROR\_INVALID\_USER\_PRINCIPAL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1367">8636 (0x21BC)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1367">8636 (0x21BC)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1368">O UPN (nome principal do usuário) é inválido.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1368">The User Principal Name (UPN) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERRO \_ o \_ grupo mapeado de OID DS não \_ \_ \_ \_ pode ter \_ Membros**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERROR\_DS\_OID\_MAPPED\_GROUP\_CANT\_HAVE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1370">8637 (0x21BD)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1370">8637 (0x21BD)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1371">Os grupos mapeados por OID não podem ter membros.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1371">OID mapped groups cannot have members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERRO \_ de \_ OID DS \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERROR\_DS\_OID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1373">8638 (0x21BE)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1373">8638 (0x21BE)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1374">O OID especificado não pode ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1374">The specified OID cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERRO \_ de \_ \_ destino reciclado do Dra DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERROR\_DS\_DRA\_RECYCLED\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1376">8639 (0x21BF)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1376">8639 (0x21BF)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1377">Falha na operação de replicação porque o objeto de destino referenciado por um valor de link foi reciclado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1377">The replication operation failed because the target object referred by a link value is recycled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERRO \_ de \_ \_ redirecionamento NC não permitido de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERROR\_DS\_DISALLOWED\_NC\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1379">8640 (0x21C0)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1379">8640 (0x21C0)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1380">A operação de redirecionamento falhou porque o objeto de destino está em um NC diferente do NC de domínio do controlador de domínio atual.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1380">The redirect operation failed because the target object is in a NC different from the domain NC of the current domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERRO \_ DS \_ High \_ ADLDS \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR\_DS\_HIGH\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1382">8641 (0x21C1)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1382">8641 (0x21C1)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1383">O nível funcional do conjunto de configuração AD LDS não pode ser reduzido para o valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1383">The functional level of the AD LDS configuration set cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERRO \_ de \_ versão alta do \_ DSA de DS \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERROR\_DS\_HIGH\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1385">8642 (0x21C2)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1385">8642 (0x21C2)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1386">O nível funcional do domínio (ou floresta) não pode ser reduzido para o valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1386">The functional level of the domain (or forest) cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERRO \_ DS \_ baixo de \_ ADLDS \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERROR\_DS\_LOW\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1388">8643 (0x21C3)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1388">8643 (0x21C3)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1389">O nível funcional do conjunto de configuração AD LDS não pode ser gerado para o valor solicitado, pois existe uma ou mais instâncias do ADLDS que estão em um nível funcional inferior incompatível.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1389">The functional level of the AD LDS configuration set cannot be raised to the requested value, because there exist one or more ADLDS instances that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**ERRO \_ \_ de SID \_ de domínio \_ como \_ estação de \_ trabalho local**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**ERROR\_DOMAIN\_SID\_SAME\_AS\_LOCAL\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1391">8644 (0x21C4)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1391">8644 (0x21C4)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1392">O ingresso no domínio não pode ser concluído porque o SID do domínio que você tentou ingressar era idêntico ao SID deste computador.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1392">The domain join cannot be completed because the SID of the domain you attempted to join was identical to the SID of this machine.</span></span> <span data-ttu-id="2d00a-1393">Esse é um sintoma de uma instalação de sistema operacional clonado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1393">This is a symptom of an improperly cloned operating system install.</span></span> <span data-ttu-id="2d00a-1394">Você deve executar o Sysprep neste computador para gerar um novo SID de máquina.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1394">You should run sysprep on this machine in order to generate a new machine SID.</span></span> <span data-ttu-id="2d00a-1395">Consulte <https://go.microsoft.com/fwlink/p/?linkid=168895> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1395">Please see <https://go.microsoft.com/fwlink/p/?linkid=168895> for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERRO \_ \_ \_ \_ ao restaurar \_ falha na validação do Sam do DS**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERROR\_DS\_UNDELETE\_SAM\_VALIDATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1397">8645 (0x21C5)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1397">8645 (0x21C5)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1398">Falha na operação de reexclusão porque o nome da conta Sam ou o nome da conta Sam adicional do objeto que está sendo inexcluído está em conflito com um objeto dinâmico existente.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1398">The undelete operation failed because the Sam Account Name or Additional Sam Account Name of the object being undeleted conflicts with an existing live object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2d00a-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERRO \_ \_ tipo de conta incorreto \_**</span><span class="sxs-lookup"><span data-stu-id="2d00a-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERROR\_INCORRECT\_ACCOUNT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d00a-1400">8646 (0x21C6)</span><span class="sxs-lookup"><span data-stu-id="2d00a-1400">8646 (0x21C6)</span></span>
</dt> <dt>



<span data-ttu-id="2d00a-1401">O sistema não é autoritativo para a conta especificada e, portanto, não pode concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1401">The system is not authoritative for the specified account and therefore cannot complete the operation.</span></span> <span data-ttu-id="2d00a-1402">Repita a operação usando o provedor associado a esta conta.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1402">Please retry the operation using the provider associated with this account.</span></span> <span data-ttu-id="2d00a-1403">Se este for um provedor online, use o site online do provedor.</span><span class="sxs-lookup"><span data-stu-id="2d00a-1403">If this is an online provider please use the provider's online site.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="2d00a-1404">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d00a-1404">Requirements</span></span>



| <span data-ttu-id="2d00a-1405">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d00a-1405">Requirement</span></span> | <span data-ttu-id="2d00a-1406">Valor</span><span class="sxs-lookup"><span data-stu-id="2d00a-1406">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d00a-1407">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d00a-1407">Minimum supported client</span></span><br/> | <span data-ttu-id="2d00a-1408">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2d00a-1408">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2d00a-1409">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d00a-1409">Minimum supported server</span></span><br/> | <span data-ttu-id="2d00a-1410">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d00a-1410">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d00a-1411">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d00a-1411">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d00a-1412"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d00a-1412"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d00a-1413">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d00a-1413">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d00a-1414">Códigos de erro do sistema</span><span class="sxs-lookup"><span data-stu-id="2d00a-1414">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




