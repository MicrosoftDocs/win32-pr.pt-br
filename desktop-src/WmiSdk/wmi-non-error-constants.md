---
description: Códigos de retorno do WMI que indicam o status e não indicam um erro.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Constantes de não erro do WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165322"
---
# <a name="wmi-non-error-constants"></a><span data-ttu-id="4c215-103">Constantes de não erro do WMI</span><span class="sxs-lookup"><span data-stu-id="4c215-103">WMI Non-Error Constants</span></span>

<span data-ttu-id="4c215-104">Códigos de retorno do WMI que indicam o status e não indicam um erro.</span><span class="sxs-lookup"><span data-stu-id="4c215-104">WMI return codes that indicate status and do not indicate an error.</span></span>

<span data-ttu-id="4c215-105">Se uma operação não resultar em um erro, o WMI retornará um dos códigos a seguir como um **HRESULT** que indica o status da operação.</span><span class="sxs-lookup"><span data-stu-id="4c215-105">If an operation does not result in an error, WMI returns one of the following codes as an **HRESULT** that indicates the status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="4c215-106">Alguns métodos em classes WMI podem retornar códigos de erro de sistema e rede (64, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="4c215-106">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="4c215-107">Você pode verificar a definição desses tipos de códigos de erro usando o comando **net helpmsg** na janela do prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="4c215-107">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="4c215-108">Por exemplo, o comando **net helpmsg 64** retorna a mensagem: o nome de rede especificado não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="4c215-108">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="4c215-109">Em C++, você pode chamar [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e especificar **C: \\ Windows \\ System32 \\ WBEM \\wmiutils.dll** como o módulo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="4c215-109">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="4c215-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**\_ \_ não há erro no WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="4c215-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM\_S\_NO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-111">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="4c215-111">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-112">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4c215-112">The operation was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ falso**</span><span class="sxs-lookup"><span data-stu-id="4c215-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM\_S\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-114">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4c215-114">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-115">Não há mais objetos disponíveis, o número de objetos retornados é menor que o número solicitado ou este é o final de uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="4c215-115">No more objects are available, the number of objects returned is less than the number requested, or this is the end of an enumeration.</span></span> <span data-ttu-id="4c215-116">Esse valor também é retornado quando esse método é chamado com um valor de 0 para o parâmetro *uCount* .</span><span class="sxs-lookup"><span data-stu-id="4c215-116">This value is also returned when this method is called with a value of 0 for the *uCount* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**o WBEM \_ S \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="4c215-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM\_S\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-118">262145 (0x40001)</span><span class="sxs-lookup"><span data-stu-id="4c215-118">262145 (0x40001)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-119">Foi feita uma tentativa de criar um objeto ou classe que já existe.</span><span class="sxs-lookup"><span data-stu-id="4c215-119">An attempt was made to create an object or class that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM \_ S \_ Redefinir \_ para \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="4c215-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM\_S\_RESET\_TO\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-121">262146 (0x40002)</span><span class="sxs-lookup"><span data-stu-id="4c215-121">262146 (0x40002)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-122">Uma propriedade substituída foi excluída.</span><span class="sxs-lookup"><span data-stu-id="4c215-122">An overridden property was deleted.</span></span> <span data-ttu-id="4c215-123">Esse valor é retornado para sinalizar que o valor original não substituído foi restaurado como resultado da exclusão.</span><span class="sxs-lookup"><span data-stu-id="4c215-123">This value is returned to signal that the original non-overridden value has been restored as a result of the deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ diferentes**</span><span class="sxs-lookup"><span data-stu-id="4c215-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM\_S\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-125">262147 (0x40003)</span><span class="sxs-lookup"><span data-stu-id="4c215-125">262147 (0x40003)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-126">Os itens (objetos, classes e assim por diante) que estão sendo comparados não são idênticos.</span><span class="sxs-lookup"><span data-stu-id="4c215-126">The items (objects, classes, and so on) that are being compared are not identical.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM \_ S \_ TIMEDOUT**</span><span class="sxs-lookup"><span data-stu-id="4c215-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM\_S\_TIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-128">262148 (0x40004)</span><span class="sxs-lookup"><span data-stu-id="4c215-128">262148 (0x40004)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-129">Uma chamada atingiu o tempo limite. Essa não é uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="4c215-129">A call timed out. This is not an error condition.</span></span> <span data-ttu-id="4c215-130">Portanto, alguns resultados também podem ter sido retornados.</span><span class="sxs-lookup"><span data-stu-id="4c215-130">Therefore, some results may have also been returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ S \_ não \_ mais \_ dados**</span><span class="sxs-lookup"><span data-stu-id="4c215-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM\_S\_NO\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-132">262149 (0x40005)</span><span class="sxs-lookup"><span data-stu-id="4c215-132">262149 (0x40005)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-133">Não há mais dados disponíveis na enumeração e o usuário deve encerrar a enumeração.</span><span class="sxs-lookup"><span data-stu-id="4c215-133">No more data is available from the enumeration, and the user must terminate the enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**\_operação do \_ WBEM \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="4c215-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**WBEM\_S\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-135">262150 (0x40006)</span><span class="sxs-lookup"><span data-stu-id="4c215-135">262150 (0x40006)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-136">A operação foi cancelada intencional ou não intencionalmente.</span><span class="sxs-lookup"><span data-stu-id="4c215-136">The operation was intentionally or unintentionally canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ pendentes**</span><span class="sxs-lookup"><span data-stu-id="4c215-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM\_S\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-138">262151 (0x40007)</span><span class="sxs-lookup"><span data-stu-id="4c215-138">262151 (0x40007)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-139">Uma solicitação ainda está em andamento e os resultados ainda não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4c215-139">A request is still in progress, and the results are not yet available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**\_ \_ objetos duplicados do WBEM S \_**</span><span class="sxs-lookup"><span data-stu-id="4c215-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**WBEM\_S\_DUPLICATE\_OBJECTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-141">262152 (0x40008)</span><span class="sxs-lookup"><span data-stu-id="4c215-141">262152 (0x40008)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-142">Foi detectada mais de uma cópia do mesmo objeto no conjunto de resultados de uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="4c215-142">More than one copy of the same object was detected in the result set of an enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**\_ \_ acesso \_ NEGAdo a WBEM**</span><span class="sxs-lookup"><span data-stu-id="4c215-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**WBEM\_S\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-144">262153 (0x40009)</span><span class="sxs-lookup"><span data-stu-id="4c215-144">262153 (0x40009)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-145">O usuário teve o acesso negado a alguns, mas não a todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="4c215-145">The user was denied access to some but not all resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_ \_ resultados parciais do WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="4c215-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**WBEM\_S\_PARTIAL\_RESULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-147">262160 (0x40010)</span><span class="sxs-lookup"><span data-stu-id="4c215-147">262160 (0x40010)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-148">O usuário não recebeu todos os objetos solicitados devido a recursos inacessíveis (que não sejam violações de segurança).</span><span class="sxs-lookup"><span data-stu-id="4c215-148">The user did not receive all of the objects requested due to inaccessible resources (other than security violations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**\_ \_ serviço limitado do \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="4c215-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**WBEM\_S\_LIMITED\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-150">274433 (0x43001)</span><span class="sxs-lookup"><span data-stu-id="4c215-150">274433 (0x43001)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-151">O provedor é capaz de serviço limitado.</span><span class="sxs-lookup"><span data-stu-id="4c215-151">The provider is capable of limited service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4c215-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**o WBEM \_ S foi \_ atualizado indiretamente \_**</span><span class="sxs-lookup"><span data-stu-id="4c215-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM\_S\_INDIRECTLY\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c215-153">274434 (0x43002)</span><span class="sxs-lookup"><span data-stu-id="4c215-153">274434 (0x43002)</span></span>
</dt> <dt>



<span data-ttu-id="4c215-154">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4c215-154">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c215-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c215-155">Requirements</span></span>



| <span data-ttu-id="4c215-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c215-156">Requirement</span></span> | <span data-ttu-id="4c215-157">Valor</span><span class="sxs-lookup"><span data-stu-id="4c215-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c215-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c215-158">Minimum supported client</span></span><br/> | <span data-ttu-id="4c215-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c215-159">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4c215-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c215-160">Minimum supported server</span></span><br/> | <span data-ttu-id="4c215-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c215-161">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4c215-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c215-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c215-163"><dt>WbemCli. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c215-163"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c215-164">INSERI</span><span class="sxs-lookup"><span data-stu-id="4c215-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c215-165"><dt>WbemCli. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c215-165"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c215-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c215-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c215-167">Códigos de retorno do WMI</span><span class="sxs-lookup"><span data-stu-id="4c215-167">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

