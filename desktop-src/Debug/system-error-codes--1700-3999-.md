---
description: Descreve os códigos de erro 1700-3999 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: Códigos de erro do sistema (1700-3999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 23b90db71a6e2e84b28f4aafc94475e9e82e3e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826166"
---
# <a name="system-error-codes-1700-3999"></a><span data-ttu-id="4651e-103">Códigos de erro do sistema (1700-3999)</span><span class="sxs-lookup"><span data-stu-id="4651e-103">System Error Codes (1700-3999)</span></span>

> [!NOTE]
> <span data-ttu-id="4651e-104">Essas informações destinam-se a desenvolvedores Depurando erros do sistema.</span><span class="sxs-lookup"><span data-stu-id="4651e-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="4651e-105">Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4651e-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="4651e-106">A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) para erros 1700 a 3999.</span><span class="sxs-lookup"><span data-stu-id="4651e-106">The following list describes [system error codes](system-error-codes.md) for errors 1700 to 3999.</span></span> <span data-ttu-id="4651e-107">Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham.</span><span class="sxs-lookup"><span data-stu-id="4651e-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="4651e-108">Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="4651e-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="4651e-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**Associação de cadeia de caracteres de RPC \_ S \_ inválida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC\_S\_INVALID\_STRING\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-110">1700 (0x6A4)</span><span class="sxs-lookup"><span data-stu-id="4651e-110">1700 (0x6A4)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-111">A associação de cadeia de caracteres é inválida.</span><span class="sxs-lookup"><span data-stu-id="4651e-111">The string binding is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**\_ \_ \_ tipo \_ de \_ Associação RPC S incorreto**</span><span class="sxs-lookup"><span data-stu-id="4651e-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**RPC\_S\_WRONG\_KIND\_OF\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-113">1701 (0x6A5)</span><span class="sxs-lookup"><span data-stu-id="4651e-113">1701 (0x6A5)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-114">O identificador de associação não é do tipo correto.</span><span class="sxs-lookup"><span data-stu-id="4651e-114">The binding handle is not the correct type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**Associação de RPC \_ S \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-116">1702 (0x6A6)</span><span class="sxs-lookup"><span data-stu-id="4651e-116">1702 (0x6A6)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-117">O identificador de associação é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-117">The binding handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**\_ \_ \_ não \_ há suporte para RPC S PROTSEQ**</span><span class="sxs-lookup"><span data-stu-id="4651e-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC\_S\_PROTSEQ\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-119">1703 (0x6A7)</span><span class="sxs-lookup"><span data-stu-id="4651e-119">1703 (0x6A7)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-120">Não há suporte para a sequência de protocolo RPC.</span><span class="sxs-lookup"><span data-stu-id="4651e-120">The RPC protocol sequence is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC \_ S \_ \_ PROTSEQ de RPC inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC\_S\_INVALID\_RPC\_PROTSEQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-122">1704 (0x6A8)</span><span class="sxs-lookup"><span data-stu-id="4651e-122">1704 (0x6A8)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-123">A sequência do Protocolo RPC é inválida.</span><span class="sxs-lookup"><span data-stu-id="4651e-123">The RPC protocol sequence is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**\_UUID de \_ cadeia de \_ caracteres inválido \_ do RPC S**</span><span class="sxs-lookup"><span data-stu-id="4651e-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC\_S\_INVALID\_STRING\_UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-125">1705 (0x6A9)</span><span class="sxs-lookup"><span data-stu-id="4651e-125">1705 (0x6A9)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-126">O UUID (identificador exclusivo universal) da cadeia de caracteres é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-126">The string universal unique identifier (UUID) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**\_formato de \_ ponto de \_ extremidade inválido \_ RPC S**</span><span class="sxs-lookup"><span data-stu-id="4651e-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**RPC\_S\_INVALID\_ENDPOINT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-128">1706 (0x6AA)</span><span class="sxs-lookup"><span data-stu-id="4651e-128">1706 (0x6AA)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-129">O formato do ponto de extremidade é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-129">The endpoint format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC \_ S \_ \_ endereço de rede inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC\_S\_INVALID\_NET\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-131">1707 (0x6AB)</span><span class="sxs-lookup"><span data-stu-id="4651e-131">1707 (0x6AB)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-132">O endereço de rede é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-132">The network address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC \_ S \_ nenhum \_ ponto de extremidade \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC\_S\_NO\_ENDPOINT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-134">1708 (0x6AC)</span><span class="sxs-lookup"><span data-stu-id="4651e-134">1708 (0x6AC)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-135">Nenhum ponto de extremidade foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="4651e-135">No endpoint was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**\_tempo limite de RPC S \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**RPC\_S\_INVALID\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-137">1709 (0x6AD)</span><span class="sxs-lookup"><span data-stu-id="4651e-137">1709 (0x6AD)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-138">O valor de tempo limite é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-138">The timeout value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**\_objeto RPC \_ S \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**RPC\_S\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-140">1710 (0x6AE)</span><span class="sxs-lookup"><span data-stu-id="4651e-140">1710 (0x6AE)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-141">O UUID (identificador exclusivo universal) do objeto não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="4651e-141">The object universal unique identifier (UUID) was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC \_ S \_ já \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC\_S\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-143">1711 (0x6AF)</span><span class="sxs-lookup"><span data-stu-id="4651e-143">1711 (0x6AF)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-144">O UUID (identificador exclusivo universal) do objeto já foi registrado.</span><span class="sxs-lookup"><span data-stu-id="4651e-144">The object universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**tipo de RPC \_ S \_ \_ já \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**RPC\_S\_TYPE\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-146">1712 (0x6B0)</span><span class="sxs-lookup"><span data-stu-id="4651e-146">1712 (0x6B0)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-147">O identificador exclusivo universal (UUID) do tipo já foi registrado.</span><span class="sxs-lookup"><span data-stu-id="4651e-147">The type universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ S \_ já \_ escutando**</span><span class="sxs-lookup"><span data-stu-id="4651e-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC\_S\_ALREADY\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-149">1713 (0x6B1)</span><span class="sxs-lookup"><span data-stu-id="4651e-149">1713 (0x6B1)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-150">O servidor RPC já está escutando.</span><span class="sxs-lookup"><span data-stu-id="4651e-150">The RPC server is already listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S \_ nenhum \_ PROTSEQS \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC\_S\_NO\_PROTSEQS\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-152">1714 (0x6B2)</span><span class="sxs-lookup"><span data-stu-id="4651e-152">1714 (0x6B2)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-153">Nenhuma sequência de protocolo foi registrada.</span><span class="sxs-lookup"><span data-stu-id="4651e-153">No protocol sequences have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ S \_ não \_ escutando**</span><span class="sxs-lookup"><span data-stu-id="4651e-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC\_S\_NOT\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-155">1715 (0x6B3)</span><span class="sxs-lookup"><span data-stu-id="4651e-155">1715 (0x6B3)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-156">O servidor RPC não está escutando.</span><span class="sxs-lookup"><span data-stu-id="4651e-156">The RPC server is not listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**\_tipo de \_ \_ Gerenciador desconhecido RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**RPC\_S\_UNKNOWN\_MGR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-158">1716 (0x6B4)</span><span class="sxs-lookup"><span data-stu-id="4651e-158">1716 (0x6B4)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-159">O tipo de Gerenciador é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4651e-159">The manager type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ S \_ desconhecido \_ se**</span><span class="sxs-lookup"><span data-stu-id="4651e-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC\_S\_UNKNOWN\_IF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-161">1717 (0x6B5)</span><span class="sxs-lookup"><span data-stu-id="4651e-161">1717 (0x6B5)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-162">A interface é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="4651e-162">The interface is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC \_ S \_ sem \_ associações**</span><span class="sxs-lookup"><span data-stu-id="4651e-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC\_S\_NO\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-164">1718 (0x6B6)</span><span class="sxs-lookup"><span data-stu-id="4651e-164">1718 (0x6B6)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-165">Não há associações.</span><span class="sxs-lookup"><span data-stu-id="4651e-165">There are no bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**\_ \_ não \_ PROTSEQS de RPC**</span><span class="sxs-lookup"><span data-stu-id="4651e-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC\_S\_NO\_PROTSEQS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-167">1719 (0x6B7)</span><span class="sxs-lookup"><span data-stu-id="4651e-167">1719 (0x6B7)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-168">Não há sequências de protocolo.</span><span class="sxs-lookup"><span data-stu-id="4651e-168">There are no protocol sequences.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ S não \_ consegue \_ criar ponto de \_ extremidade**</span><span class="sxs-lookup"><span data-stu-id="4651e-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC\_S\_CANT\_CREATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-170">1720 (0x6B8)</span><span class="sxs-lookup"><span data-stu-id="4651e-170">1720 (0x6B8)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-171">Não é possível criar o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="4651e-171">The endpoint cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC \_ S \_ \_ de \_ recursos**</span><span class="sxs-lookup"><span data-stu-id="4651e-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC\_S\_OUT\_OF\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-173">1721 (0x6B9)</span><span class="sxs-lookup"><span data-stu-id="4651e-173">1721 (0x6B9)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-174">Não há recursos suficientes disponíveis para concluir esta operação.</span><span class="sxs-lookup"><span data-stu-id="4651e-174">Not enough resources are available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**\_servidor RPC \_ S \_ não disponível**</span><span class="sxs-lookup"><span data-stu-id="4651e-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC\_S\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-176">1722 (0x6BA)</span><span class="sxs-lookup"><span data-stu-id="4651e-176">1722 (0x6BA)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-177">O servidor RPC não está disponível.</span><span class="sxs-lookup"><span data-stu-id="4651e-177">The RPC server is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**\_servidor RPC \_ S \_ muito \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="4651e-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC\_S\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-179">1723 (0x6BB)</span><span class="sxs-lookup"><span data-stu-id="4651e-179">1723 (0x6BB)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-180">O servidor RPC está muito ocupado para concluir esta operação.</span><span class="sxs-lookup"><span data-stu-id="4651e-180">The RPC server is too busy to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**opções de rede de RPC \_ S \_ inválidas \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**RPC\_S\_INVALID\_NETWORK\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-182">1724 (0x6BC)</span><span class="sxs-lookup"><span data-stu-id="4651e-182">1724 (0x6BC)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-183">As opções de rede são inválidas.</span><span class="sxs-lookup"><span data-stu-id="4651e-183">The network options are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ \_ sem \_ chamada \_ ativa**</span><span class="sxs-lookup"><span data-stu-id="4651e-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC\_S\_NO\_CALL\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-185">1725 (0x6BD)</span><span class="sxs-lookup"><span data-stu-id="4651e-185">1725 (0x6BD)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-186">Não há chamadas de procedimento remoto ativas neste thread.</span><span class="sxs-lookup"><span data-stu-id="4651e-186">There are no remote procedure calls active on this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**\_ \_ falha na chamada RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**RPC\_S\_CALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-188">1726 (0x6BE)</span><span class="sxs-lookup"><span data-stu-id="4651e-188">1726 (0x6BE)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-189">Falha na chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4651e-189">The remote procedure call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**\_ \_ falha na chamada de RPC S \_ \_ DNE**</span><span class="sxs-lookup"><span data-stu-id="4651e-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**RPC\_S\_CALL\_FAILED\_DNE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-191">1727 (0x6BF)</span><span class="sxs-lookup"><span data-stu-id="4651e-191">1727 (0x6BF)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-192">A chamada de procedimento remoto falhou e não foi executada.</span><span class="sxs-lookup"><span data-stu-id="4651e-192">The remote procedure call failed and did not execute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**\_erro de \_ protocolo RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**RPC\_S\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-194">1728 (0x6C0)</span><span class="sxs-lookup"><span data-stu-id="4651e-194">1728 (0x6C0)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-195">Ocorreu um erro de protocolo RPC (chamada de procedimento remoto).</span><span class="sxs-lookup"><span data-stu-id="4651e-195">A remote procedure call (RPC) protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**\_acesso ao proxy RPC S \_ \_ \_ negado**</span><span class="sxs-lookup"><span data-stu-id="4651e-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**RPC\_S\_PROXY\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-197">1729 (0x6C1)</span><span class="sxs-lookup"><span data-stu-id="4651e-197">1729 (0x6C1)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-198">O acesso ao proxy HTTP foi negado.</span><span class="sxs-lookup"><span data-stu-id="4651e-198">Access to the HTTP proxy is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**\_ \_ \_ Transações SYN sem suporte de RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="4651e-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC\_S\_UNSUPPORTED\_TRANS\_SYN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-200">1730 (0x6C2)</span><span class="sxs-lookup"><span data-stu-id="4651e-200">1730 (0x6C2)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-201">A sintaxe de transferência não é suportada pelo servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="4651e-201">The transfer syntax is not supported by the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**tipo de RPC \_ S \_ sem suporte \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**RPC\_S\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-203">1732 (0x6C4)</span><span class="sxs-lookup"><span data-stu-id="4651e-203">1732 (0x6C4)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-204">Não há suporte para o tipo de identificador exclusivo universal (UUID).</span><span class="sxs-lookup"><span data-stu-id="4651e-204">The universal unique identifier (UUID) type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**marca de RPC \_ S \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**RPC\_S\_INVALID\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-206">1733 (0x6C5)</span><span class="sxs-lookup"><span data-stu-id="4651e-206">1733 (0x6C5)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-207">A marca é inválida.</span><span class="sxs-lookup"><span data-stu-id="4651e-207">The tag is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**Associação de RPC \_ S \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC\_S\_INVALID\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-209">1734 (0x6C6)</span><span class="sxs-lookup"><span data-stu-id="4651e-209">1734 (0x6C6)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-210">Os limites de matriz são inválidos.</span><span class="sxs-lookup"><span data-stu-id="4651e-210">The array bounds are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**\_ \_ nenhum nome de \_ entrada \_ do RPC**</span><span class="sxs-lookup"><span data-stu-id="4651e-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC\_S\_NO\_ENTRY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-212">1735 (0x6C7)</span><span class="sxs-lookup"><span data-stu-id="4651e-212">1735 (0x6C7)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-213">A associação não contém um nome de entrada.</span><span class="sxs-lookup"><span data-stu-id="4651e-213">The binding does not contain an entry name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**\_sintaxe de \_ \_ nome inválido \_ de RPC S**</span><span class="sxs-lookup"><span data-stu-id="4651e-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**RPC\_S\_INVALID\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-215">1736 (0x6C8)</span><span class="sxs-lookup"><span data-stu-id="4651e-215">1736 (0x6C8)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-216">A sintaxe do nome é inválida.</span><span class="sxs-lookup"><span data-stu-id="4651e-216">The name syntax is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**\_sintaxe de \_ nome não suportada RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC\_S\_UNSUPPORTED\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-218">1737 (0x6C9)</span><span class="sxs-lookup"><span data-stu-id="4651e-218">1737 (0x6C9)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-219">Não há suporte para a sintaxe de nome.</span><span class="sxs-lookup"><span data-stu-id="4651e-219">The name syntax is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC \_ S \_ UUID \_ sem \_ Endereço**</span><span class="sxs-lookup"><span data-stu-id="4651e-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC\_S\_UUID\_NO\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-221">1739 (0x6CB)</span><span class="sxs-lookup"><span data-stu-id="4651e-221">1739 (0x6CB)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-222">Nenhum endereço de rede está disponível para ser usado para construir um identificador exclusivo universal (UUID).</span><span class="sxs-lookup"><span data-stu-id="4651e-222">No network address is available to use to construct a universal unique identifier (UUID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_ponto de \_ extremidade duplicado \_ de RPC**</span><span class="sxs-lookup"><span data-stu-id="4651e-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**RPC\_S\_DUPLICATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-224">1740 (0x6CC)</span><span class="sxs-lookup"><span data-stu-id="4651e-224">1740 (0x6CC)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-225">O ponto de extremidade é uma duplicata.</span><span class="sxs-lookup"><span data-stu-id="4651e-225">The endpoint is a duplicate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**\_tipo de \_ \_ autenticação desconhecido RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="4651e-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**RPC\_S\_UNKNOWN\_AUTHN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-227">1741 (0x6CD)</span><span class="sxs-lookup"><span data-stu-id="4651e-227">1741 (0x6CD)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-228">O tipo de autenticação é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4651e-228">The authentication type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**\_ \_ chamadas máximas RPC S \_ \_ muito \_ pequenas**</span><span class="sxs-lookup"><span data-stu-id="4651e-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**RPC\_S\_MAX\_CALLS\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-230">1742 (0x6CE)</span><span class="sxs-lookup"><span data-stu-id="4651e-230">1742 (0x6CE)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-231">O número máximo de chamadas é muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="4651e-231">The maximum number of calls is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**\_cadeia de caracteres RPC S \_ \_ muito \_ longa**</span><span class="sxs-lookup"><span data-stu-id="4651e-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC\_S\_STRING\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-233">1743 (0x6CF)</span><span class="sxs-lookup"><span data-stu-id="4651e-233">1743 (0x6CF)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-234">A cadeia de caracteres é longa demais.</span><span class="sxs-lookup"><span data-stu-id="4651e-234">The string is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**PROTSEQ de RPC \_ S \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC\_S\_PROTSEQ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-236">1744 (0x6D0)</span><span class="sxs-lookup"><span data-stu-id="4651e-236">1744 (0x6D0)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-237">A sequência do Protocolo RPC não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4651e-237">The RPC protocol sequence was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC \_ S \_ PROCNUM \_ fora \_ do \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="4651e-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC\_S\_PROCNUM\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-239">1745 (0x6D1)</span><span class="sxs-lookup"><span data-stu-id="4651e-239">1745 (0x6D1)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-240">O número do procedimento está fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="4651e-240">The procedure number is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**a \_ Associação RPC S \_ \_ \_ não tem \_ autenticação**</span><span class="sxs-lookup"><span data-stu-id="4651e-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**RPC\_S\_BINDING\_HAS\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-242">1746 (0x6D2)</span><span class="sxs-lookup"><span data-stu-id="4651e-242">1746 (0x6D2)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-243">A associação não contém nenhuma informação de autenticação.</span><span class="sxs-lookup"><span data-stu-id="4651e-243">The binding does not contain any authentication information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**\_serviço de \_ \_ autenticação desconhecido RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="4651e-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**RPC\_S\_UNKNOWN\_AUTHN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-245">1747 (0x6D3)</span><span class="sxs-lookup"><span data-stu-id="4651e-245">1747 (0x6D3)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-246">O serviço de autenticação é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4651e-246">The authentication service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**\_nível de \_ \_ autenticação desconhecido \_ de RPC S**</span><span class="sxs-lookup"><span data-stu-id="4651e-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**RPC\_S\_UNKNOWN\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-248">1748 (0x6D4)</span><span class="sxs-lookup"><span data-stu-id="4651e-248">1748 (0x6D4)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-249">O nível de autenticação é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4651e-249">The authentication level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**identidade de autenticação de RPC \_ S \_ inválida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**RPC\_S\_INVALID\_AUTH\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-251">1749 (0x6D5)</span><span class="sxs-lookup"><span data-stu-id="4651e-251">1749 (0x6D5)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-252">O contexto de segurança é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-252">The security context is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**\_serviço de \_ \_ AUTHZ desconhecido \_ do RPC**</span><span class="sxs-lookup"><span data-stu-id="4651e-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC\_S\_UNKNOWN\_AUTHZ\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-254">1750 (0x6D6)</span><span class="sxs-lookup"><span data-stu-id="4651e-254">1750 (0x6D6)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-255">O serviço de autorização é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4651e-255">The authorization service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT \_ S \_ entrada inválida \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT\_S\_INVALID\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-257">1751 (0x6D7)</span><span class="sxs-lookup"><span data-stu-id="4651e-257">1751 (0x6D7)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-258">A entrada é inválida.</span><span class="sxs-lookup"><span data-stu-id="4651e-258">The entry is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S não \_ consegue \_ executar \_ op**</span><span class="sxs-lookup"><span data-stu-id="4651e-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT\_S\_CANT\_PERFORM\_OP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-260">1752 (0x6D8)</span><span class="sxs-lookup"><span data-stu-id="4651e-260">1752 (0x6D8)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-261">O ponto de extremidade do servidor não pode executar a operação.</span><span class="sxs-lookup"><span data-stu-id="4651e-261">The server endpoint cannot perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ não \_ registrados**</span><span class="sxs-lookup"><span data-stu-id="4651e-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT\_S\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-263">1753 (0x6D9)</span><span class="sxs-lookup"><span data-stu-id="4651e-263">1753 (0x6D9)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-264">Não há mais pontos de extremidade disponíveis no mapeador de pontos de extremidades.</span><span class="sxs-lookup"><span data-stu-id="4651e-264">There are no more endpoints available from the endpoint mapper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**\_ \_ nada \_ para \_ Exportar RPC**</span><span class="sxs-lookup"><span data-stu-id="4651e-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC\_S\_NOTHING\_TO\_EXPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-266">1754 (0x6DA)</span><span class="sxs-lookup"><span data-stu-id="4651e-266">1754 (0x6DA)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-267">Nenhuma interface foi exportada.</span><span class="sxs-lookup"><span data-stu-id="4651e-267">No interfaces have been exported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_ \_ nome incompleto de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**RPC\_S\_INCOMPLETE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-269">1755 (0x6DB)</span><span class="sxs-lookup"><span data-stu-id="4651e-269">1755 (0x6DB)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-270">O nome da entrada está incompleto.</span><span class="sxs-lookup"><span data-stu-id="4651e-270">The entry name is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**\_opção de \_ \_ inversão de RPC S inválida \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC\_S\_INVALID\_VERS\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-272">1756 (0x6DC)</span><span class="sxs-lookup"><span data-stu-id="4651e-272">1756 (0x6DC)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-273">A opção de versão é inválida.</span><span class="sxs-lookup"><span data-stu-id="4651e-273">The version option is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ S \_ não \_ mais \_ Membros**</span><span class="sxs-lookup"><span data-stu-id="4651e-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC\_S\_NO\_MORE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-275">1757 (0x6DD)</span><span class="sxs-lookup"><span data-stu-id="4651e-275">1757 (0x6DD)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-276">Não há mais membros.</span><span class="sxs-lookup"><span data-stu-id="4651e-276">There are no more members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ S \_ nem \_ todos os \_ objs tivessem não \_ exportados**</span><span class="sxs-lookup"><span data-stu-id="4651e-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_UNEXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-278">1758 (0x6DE)</span><span class="sxs-lookup"><span data-stu-id="4651e-278">1758 (0x6DE)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-279">Não há nada para não exportar.</span><span class="sxs-lookup"><span data-stu-id="4651e-279">There is nothing to unexport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_interface RPC \_ S \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="4651e-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**RPC\_S\_INTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-281">1759 (0x6DF)</span><span class="sxs-lookup"><span data-stu-id="4651e-281">1759 (0x6DF)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-282">A interface não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4651e-282">The interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**a \_ entrada de RPC S \_ \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="4651e-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**RPC\_S\_ENTRY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-284">1760 (0x6E0)</span><span class="sxs-lookup"><span data-stu-id="4651e-284">1760 (0x6E0)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-285">A entrada já existe.</span><span class="sxs-lookup"><span data-stu-id="4651e-285">The entry already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**\_entrada RPC \_ S \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="4651e-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**RPC\_S\_ENTRY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-287">1761 (0x6E1)</span><span class="sxs-lookup"><span data-stu-id="4651e-287">1761 (0x6E1)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-288">A entrada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4651e-288">The entry is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**\_serviço de nome RPC S \_ \_ \_ indisponível**</span><span class="sxs-lookup"><span data-stu-id="4651e-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC\_S\_NAME\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-290">1762 (0x6E2)</span><span class="sxs-lookup"><span data-stu-id="4651e-290">1762 (0x6E2)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-291">O serviço de nome não está disponível.</span><span class="sxs-lookup"><span data-stu-id="4651e-291">The name service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**\_ \_ \_ ID NAF inválido do RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**RPC\_S\_INVALID\_NAF\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-293">1763 (0x6E3)</span><span class="sxs-lookup"><span data-stu-id="4651e-293">1763 (0x6E3)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-294">A família de endereços de rede é inválida.</span><span class="sxs-lookup"><span data-stu-id="4651e-294">The network address family is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**\_ \_ não é possível \_ dar suporte a RPC S**</span><span class="sxs-lookup"><span data-stu-id="4651e-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC\_S\_CANNOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-296">1764 (0x6E4)</span><span class="sxs-lookup"><span data-stu-id="4651e-296">1764 (0x6E4)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-297">Não há suporte para a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="4651e-297">The requested operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC \_ S \_ nenhum \_ contexto \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="4651e-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC\_S\_NO\_CONTEXT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-299">1765 (0x6E5)</span><span class="sxs-lookup"><span data-stu-id="4651e-299">1765 (0x6E5)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-300">Nenhum contexto de segurança está disponível para permitir a representação.</span><span class="sxs-lookup"><span data-stu-id="4651e-300">No security context is available to allow impersonation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**\_ \_ erro interno de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**RPC\_S\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-302">1766 (0x6E6)</span><span class="sxs-lookup"><span data-stu-id="4651e-302">1766 (0x6E6)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-303">Ocorreu um erro interno em uma chamada de procedimento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="4651e-303">An internal error occurred in a remote procedure call (RPC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**Divisão de RPC \_ S \_ zero \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC\_S\_ZERO\_DIVIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-305">1767 (0x6E7)</span><span class="sxs-lookup"><span data-stu-id="4651e-305">1767 (0x6E7)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-306">O servidor RPC tentou uma divisão de número inteiro por zero.</span><span class="sxs-lookup"><span data-stu-id="4651e-306">The RPC server attempted an integer division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**\_erro de \_ endereço RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**RPC\_S\_ADDRESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-308">1768 (0x6E8)</span><span class="sxs-lookup"><span data-stu-id="4651e-308">1768 (0x6E8)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-309">Ocorreu um erro de endereçamento no servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="4651e-309">An addressing error occurred in the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC \_ S \_ FP \_ div \_ zero**</span><span class="sxs-lookup"><span data-stu-id="4651e-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC\_S\_FP\_DIV\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-311">1769 (0x6E9)</span><span class="sxs-lookup"><span data-stu-id="4651e-311">1769 (0x6E9)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-312">Uma operação de ponto flutuante no servidor RPC causou uma divisão por zero.</span><span class="sxs-lookup"><span data-stu-id="4651e-312">A floating-point operation at the RPC server caused a division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**\_ \_ \_ estouro negativo do RPC S**</span><span class="sxs-lookup"><span data-stu-id="4651e-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**RPC\_S\_FP\_UNDERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-314">1770 (0x6EA)</span><span class="sxs-lookup"><span data-stu-id="4651e-314">1770 (0x6EA)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-315">Um estouro negativo de ponto flutuante ocorreu no servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="4651e-315">A floating-point underflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**estouro de FP de RPC \_ S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC\_S\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-317">1771 (0x6EB)</span><span class="sxs-lookup"><span data-stu-id="4651e-317">1771 (0x6EB)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-318">Ocorreu um estouro de ponto flutuante no servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="4651e-318">A floating-point overflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ não há \_ mais \_ entradas**</span><span class="sxs-lookup"><span data-stu-id="4651e-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC\_X\_NO\_MORE\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-320">1772 (0x6EC)</span><span class="sxs-lookup"><span data-stu-id="4651e-320">1772 (0x6EC)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-321">A lista de servidores RPC disponíveis para a associação de identificadores automáticos foi esgotada.</span><span class="sxs-lookup"><span data-stu-id="4651e-321">The list of RPC servers available for the binding of auto handles has been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**\_falha ao \_ \_ \_ \_ abrir trans \_ . de car de RPC X SS**</span><span class="sxs-lookup"><span data-stu-id="4651e-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC\_X\_SS\_CHAR\_TRANS\_OPEN\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-323">1773 (0x6ED)</span><span class="sxs-lookup"><span data-stu-id="4651e-323">1773 (0x6ED)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-324">Não é possível abrir o arquivo da tabela de conversão de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4651e-324">Unable to open the character translation table file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC \_ X \_ SS \_ Char \_ Trans \_ \_ arquivo curto**</span><span class="sxs-lookup"><span data-stu-id="4651e-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC\_X\_SS\_CHAR\_TRANS\_SHORT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-326">1774 (0x6EE)</span><span class="sxs-lookup"><span data-stu-id="4651e-326">1774 (0x6EE)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-327">O arquivo que contém a tabela de conversão de caracteres tem menos de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="4651e-327">The file containing the character translation table has fewer than 512 bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS \_ em \_ \_ contexto nulo**</span><span class="sxs-lookup"><span data-stu-id="4651e-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC\_X\_SS\_IN\_NULL\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-329">1775 (0x6EF)</span><span class="sxs-lookup"><span data-stu-id="4651e-329">1775 (0x6EF)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-330">Um identificador de contexto nulo foi passado do cliente para o host durante uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4651e-330">A null context handle was passed from the client to the host during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**contexto de RPC \_ X \_ SS \_ \_ danificado**</span><span class="sxs-lookup"><span data-stu-id="4651e-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC\_X\_SS\_CONTEXT\_DAMAGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-332">1777 (0x6F1)</span><span class="sxs-lookup"><span data-stu-id="4651e-332">1777 (0x6F1)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-333">O identificador de contexto foi alterado durante uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4651e-333">The context handle changed during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**\_ \_ identificadores RPC X SS \_ \_ incompatíveis**</span><span class="sxs-lookup"><span data-stu-id="4651e-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC\_X\_SS\_HANDLES\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-335">1778 (0x6F2)</span><span class="sxs-lookup"><span data-stu-id="4651e-335">1778 (0x6F2)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-336">Os identificadores de associação passados para uma chamada de procedimento remoto não correspondem.</span><span class="sxs-lookup"><span data-stu-id="4651e-336">The binding handles passed to a remote procedure call do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ não \_ pode \_ obter \_ identificador de chamada**</span><span class="sxs-lookup"><span data-stu-id="4651e-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC\_X\_SS\_CANNOT\_GET\_CALL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-338">1779 (0x6F3)</span><span class="sxs-lookup"><span data-stu-id="4651e-338">1779 (0x6F3)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-339">O stub não pode obter o identificador de chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4651e-339">The stub is unable to get the remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**ponteiro de referência de RPC \_ X \_ nulo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC\_X\_NULL\_REF\_POINTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-341">1780 (0x6F4)</span><span class="sxs-lookup"><span data-stu-id="4651e-341">1780 (0x6F4)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-342">Um ponteiro de referência nulo foi passado para o stub.</span><span class="sxs-lookup"><span data-stu-id="4651e-342">A null reference pointer was passed to the stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**\_ \_ \_ valor de enumeração de RPC X \_ fora \_ do \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="4651e-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-344">1781 (0x6F5)</span><span class="sxs-lookup"><span data-stu-id="4651e-344">1781 (0x6F5)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-345">O valor da enumeração está fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="4651e-345">The enumeration value is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**contagem de bytes de RPC \_ X \_ \_ \_ muito \_ pequena**</span><span class="sxs-lookup"><span data-stu-id="4651e-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC\_X\_BYTE\_COUNT\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-347">1782 (0x6F6)</span><span class="sxs-lookup"><span data-stu-id="4651e-347">1782 (0x6F6)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-348">A contagem de bytes é muito pequena.</span><span class="sxs-lookup"><span data-stu-id="4651e-348">The byte count is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**\_dados de \_ stub inválidos RPC X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC\_X\_BAD\_STUB\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-350">1783 (0x6F7)</span><span class="sxs-lookup"><span data-stu-id="4651e-350">1783 (0x6F7)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-351">O stub recebeu dados inválidos.</span><span class="sxs-lookup"><span data-stu-id="4651e-351">The stub received bad data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERRO \_ de \_ buffer de usuário inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERROR\_INVALID\_USER\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-353">1784 (0x6F8)</span><span class="sxs-lookup"><span data-stu-id="4651e-353">1784 (0x6F8)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-354">O buffer de usuário fornecido não é válido para a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="4651e-354">The supplied user buffer is not valid for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERRO de \_ mídia não reconhecida \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERROR\_UNRECOGNIZED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-356">1785 (0x6F9)</span><span class="sxs-lookup"><span data-stu-id="4651e-356">1785 (0x6F9)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-357">A mídia de disco não é reconhecida.</span><span class="sxs-lookup"><span data-stu-id="4651e-357">The disk media is not recognized.</span></span> <span data-ttu-id="4651e-358">Ele não pode ser formatado.</span><span class="sxs-lookup"><span data-stu-id="4651e-358">It may not be formatted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERRO \_ sem \_ confiança \_ no \_ segredo LSA**</span><span class="sxs-lookup"><span data-stu-id="4651e-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERROR\_NO\_TRUST\_LSA\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-360">1786 (0x6FA)</span><span class="sxs-lookup"><span data-stu-id="4651e-360">1786 (0x6FA)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-361">A estação de trabalho não tem um segredo de confiança.</span><span class="sxs-lookup"><span data-stu-id="4651e-361">The workstation does not have a trust secret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERRO \_ sem \_ confiança \_ na \_ conta Sam**</span><span class="sxs-lookup"><span data-stu-id="4651e-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERROR\_NO\_TRUST\_SAM\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-363">1787 (0x6FB)</span><span class="sxs-lookup"><span data-stu-id="4651e-363">1787 (0x6FB)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-364">O banco de dados de segurança no servidor não tem uma conta de computador para essa relação de confiança de estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4651e-364">The security database on the server does not have a computer account for this workstation trust relationship.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERRO \_ de \_ falha de domínio confiável \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERROR\_TRUSTED\_DOMAIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-366">1788 (0x6FC)</span><span class="sxs-lookup"><span data-stu-id="4651e-366">1788 (0x6FC)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-367">Falha na relação de confiança entre o domínio primário e o domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="4651e-367">The trust relationship between the primary domain and the trusted domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERRO \_ de \_ falha de relação confiável \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERROR\_TRUSTED\_RELATIONSHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-369">1789 (0x6FD)</span><span class="sxs-lookup"><span data-stu-id="4651e-369">1789 (0x6FD)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-370">A relação de confiança entre esta estação de trabalho e o domínio primário falhou.</span><span class="sxs-lookup"><span data-stu-id="4651e-370">The trust relationship between this workstation and the primary domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**\_falha de confiança de erro \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-372">1790 (0x6FE)</span><span class="sxs-lookup"><span data-stu-id="4651e-372">1790 (0x6FE)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-373">Falha no logon de rede.</span><span class="sxs-lookup"><span data-stu-id="4651e-373">The network logon failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**\_chamada RPC \_ S \_ em \_ andamento**</span><span class="sxs-lookup"><span data-stu-id="4651e-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**RPC\_S\_CALL\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-375">1791 (0x6FF)</span><span class="sxs-lookup"><span data-stu-id="4651e-375">1791 (0x6FF)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-376">Uma chamada de procedimento remoto já está em andamento para este thread.</span><span class="sxs-lookup"><span data-stu-id="4651e-376">A remote procedure call is already in progress for this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERRO \_ Netlogon \_ não \_ iniciado**</span><span class="sxs-lookup"><span data-stu-id="4651e-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERROR\_NETLOGON\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-378">1792 (0x700)</span><span class="sxs-lookup"><span data-stu-id="4651e-378">1792 (0x700)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-379">Foi feita uma tentativa de logon, mas o serviço de logon de rede não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="4651e-379">An attempt was made to logon, but the network logon service was not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**conta de erro \_ \_ expirada**</span><span class="sxs-lookup"><span data-stu-id="4651e-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**ERROR\_ACCOUNT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-381">1793 (0x701)</span><span class="sxs-lookup"><span data-stu-id="4651e-381">1793 (0x701)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-382">A conta do usuário expirou.</span><span class="sxs-lookup"><span data-stu-id="4651e-382">The user's account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**o \_ REdirecionador de erros \_ tem \_ \_ identificadores abertos**</span><span class="sxs-lookup"><span data-stu-id="4651e-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**ERROR\_REDIRECTOR\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-384">1794 (0x702)</span><span class="sxs-lookup"><span data-stu-id="4651e-384">1794 (0x702)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-385">O redirecionador está em uso e não pode ser descarregado.</span><span class="sxs-lookup"><span data-stu-id="4651e-385">The redirector is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**o \_ Driver de impressora de erro \_ \_ já está \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="4651e-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**ERROR\_PRINTER\_DRIVER\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-387">1795 (0x703)</span><span class="sxs-lookup"><span data-stu-id="4651e-387">1795 (0x703)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-388">O driver de impressora especificado já está instalado.</span><span class="sxs-lookup"><span data-stu-id="4651e-388">The specified printer driver is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**porta de erro \_ desconhecida \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERROR\_UNKNOWN\_PORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-390">1796 (0x704)</span><span class="sxs-lookup"><span data-stu-id="4651e-390">1796 (0x704)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-391">A porta especificada é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="4651e-391">The specified port is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERRO \_ de \_ Driver de impressora desconhecido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERROR\_UNKNOWN\_PRINTER\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-393">1797 (0x705)</span><span class="sxs-lookup"><span data-stu-id="4651e-393">1797 (0x705)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-394">O driver de impressora é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4651e-394">The printer driver is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERRO \_ de \_ multiprocessador desconhecido**</span><span class="sxs-lookup"><span data-stu-id="4651e-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERROR\_UNKNOWN\_PRINTPROCESSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-396">1798 (0x706)</span><span class="sxs-lookup"><span data-stu-id="4651e-396">1798 (0x706)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-397">O processador de impressão é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4651e-397">The print processor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERRO \_ de \_ arquivo separador inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERROR\_INVALID\_SEPARATOR\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-399">1799 (0x707)</span><span class="sxs-lookup"><span data-stu-id="4651e-399">1799 (0x707)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-400">O arquivo separador especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-400">The specified separator file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERRO \_ de \_ prioridade inválida**</span><span class="sxs-lookup"><span data-stu-id="4651e-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERROR\_INVALID\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-402">1800 (0x708)</span><span class="sxs-lookup"><span data-stu-id="4651e-402">1800 (0x708)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-403">A prioridade especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="4651e-403">The specified priority is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**\_nome de \_ impressora \_ inválido do erro**</span><span class="sxs-lookup"><span data-stu-id="4651e-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERROR\_INVALID\_PRINTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-405">1801 (0x709)</span><span class="sxs-lookup"><span data-stu-id="4651e-405">1801 (0x709)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-406">O nome da impressora é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-406">The printer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**a \_ impressora de erro \_ já \_ existe**</span><span class="sxs-lookup"><span data-stu-id="4651e-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**ERROR\_PRINTER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-408">1802 (0x70A)</span><span class="sxs-lookup"><span data-stu-id="4651e-408">1802 (0x70A)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-409">A impressora já existe.</span><span class="sxs-lookup"><span data-stu-id="4651e-409">The printer already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERRO \_ de \_ comando de impressora inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERROR\_INVALID\_PRINTER\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-411">1803 (0x70B)</span><span class="sxs-lookup"><span data-stu-id="4651e-411">1803 (0x70B)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-412">O comando de impressora é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-412">The printer command is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERRO \_ de \_ tipo de dados inválido**</span><span class="sxs-lookup"><span data-stu-id="4651e-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERROR\_INVALID\_DATATYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-414">1804 (0x70C)</span><span class="sxs-lookup"><span data-stu-id="4651e-414">1804 (0x70C)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-415">O tipo de dados especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-415">The specified datatype is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERRO \_ de \_ ambiente inválido**</span><span class="sxs-lookup"><span data-stu-id="4651e-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERROR\_INVALID\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-417">1805 (0x70D)</span><span class="sxs-lookup"><span data-stu-id="4651e-417">1805 (0x70D)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-418">O ambiente especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-418">The environment specified is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**\_ \_ não há \_ mais \_ associações de RPC**</span><span class="sxs-lookup"><span data-stu-id="4651e-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC\_S\_NO\_MORE\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-420">1806 (0x70E)</span><span class="sxs-lookup"><span data-stu-id="4651e-420">1806 (0x70E)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-421">Não há mais associações.</span><span class="sxs-lookup"><span data-stu-id="4651e-421">There are no more bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERRO \_ NOlogon da \_ conta de \_ confiança entre domínios \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERROR\_NOLOGON\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-423">1807 (0x70F)</span><span class="sxs-lookup"><span data-stu-id="4651e-423">1807 (0x70F)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-424">A conta usada é uma conta de confiança entre domínios.</span><span class="sxs-lookup"><span data-stu-id="4651e-424">The account used is an interdomain trust account.</span></span> <span data-ttu-id="4651e-425">Use sua conta de usuário global ou conta de usuário local para acessar este servidor.</span><span class="sxs-lookup"><span data-stu-id="4651e-425">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERRO \_ NOlogon da \_ \_ conta de confiança da estação de trabalho \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERROR\_NOLOGON\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-427">1808 (0x710)</span><span class="sxs-lookup"><span data-stu-id="4651e-427">1808 (0x710)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-428">A conta usada é uma conta de computador.</span><span class="sxs-lookup"><span data-stu-id="4651e-428">The account used is a computer account.</span></span> <span data-ttu-id="4651e-429">Use sua conta de usuário global ou conta de usuário local para acessar este servidor.</span><span class="sxs-lookup"><span data-stu-id="4651e-429">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERRO \_ NOlogon da \_ \_ conta de confiança do servidor \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERROR\_NOLOGON\_SERVER\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-431">1809 (0x711)</span><span class="sxs-lookup"><span data-stu-id="4651e-431">1809 (0x711)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-432">A conta usada é uma conta de confiança do servidor.</span><span class="sxs-lookup"><span data-stu-id="4651e-432">The account used is a server trust account.</span></span> <span data-ttu-id="4651e-433">Use sua conta de usuário global ou conta de usuário local para acessar este servidor.</span><span class="sxs-lookup"><span data-stu-id="4651e-433">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**ERRO \_ de \_ confiança de domínio \_ inconsistente**</span><span class="sxs-lookup"><span data-stu-id="4651e-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**ERROR\_DOMAIN\_TRUST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-435">1810 (0x712)</span><span class="sxs-lookup"><span data-stu-id="4651e-435">1810 (0x712)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-436">O nome ou a ID de segurança (SID) do domínio especificado é inconsistente com as informações de confiança para esse domínio.</span><span class="sxs-lookup"><span data-stu-id="4651e-436">The name or security ID (SID) of the domain specified is inconsistent with the trust information for that domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**o \_ servidor de erro \_ tem \_ \_ identificadores abertos**</span><span class="sxs-lookup"><span data-stu-id="4651e-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**ERROR\_SERVER\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-438">1811 (0x713)</span><span class="sxs-lookup"><span data-stu-id="4651e-438">1811 (0x713)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-439">O servidor está em uso e não pode ser descarregado.</span><span class="sxs-lookup"><span data-stu-id="4651e-439">The server is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**dados de recurso de erro \_ \_ \_ não \_ encontrados**</span><span class="sxs-lookup"><span data-stu-id="4651e-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**ERROR\_RESOURCE\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-441">1812 (0x714)</span><span class="sxs-lookup"><span data-stu-id="4651e-441">1812 (0x714)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-442">O arquivo de imagem especificado não continha uma seção de recursos.</span><span class="sxs-lookup"><span data-stu-id="4651e-442">The specified image file did not contain a resource section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**tipo de recurso de erro \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**ERROR\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-444">1813 (0x715)</span><span class="sxs-lookup"><span data-stu-id="4651e-444">1813 (0x715)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-445">O tipo de recurso especificado não pode ser encontrado no arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="4651e-445">The specified resource type cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**nome do recurso de erro \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**ERROR\_RESOURCE\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-447">1814 (0x716)</span><span class="sxs-lookup"><span data-stu-id="4651e-447">1814 (0x716)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-448">O nome do recurso especificado não pode ser encontrado no arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="4651e-448">The specified resource name cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**LANG de recurso de erro \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**ERROR\_RESOURCE\_LANG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-450">1815 (0x717)</span><span class="sxs-lookup"><span data-stu-id="4651e-450">1815 (0x717)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-451">A ID do idioma do recurso especificado não pode ser encontrada no arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="4651e-451">The specified resource language ID cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERRO \_ sem \_ \_ cota suficiente**</span><span class="sxs-lookup"><span data-stu-id="4651e-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERROR\_NOT\_ENOUGH\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-453">1816 (0x718)</span><span class="sxs-lookup"><span data-stu-id="4651e-453">1816 (0x718)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-454">Não há cota suficiente para processar este comando.</span><span class="sxs-lookup"><span data-stu-id="4651e-454">Not enough quota is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC \_ S \_ sem \_ interfaces**</span><span class="sxs-lookup"><span data-stu-id="4651e-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC\_S\_NO\_INTERFACES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-456">1817 (0x719)</span><span class="sxs-lookup"><span data-stu-id="4651e-456">1817 (0x719)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-457">Nenhuma interface foi registrada.</span><span class="sxs-lookup"><span data-stu-id="4651e-457">No interfaces have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**\_chamada RPC \_ S \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="4651e-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC\_S\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-459">1818 (0x71A)</span><span class="sxs-lookup"><span data-stu-id="4651e-459">1818 (0x71A)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-460">A chamada de procedimento remoto foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="4651e-460">The remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**Associação de RPC \_ S \_ \_ incompleta**</span><span class="sxs-lookup"><span data-stu-id="4651e-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**RPC\_S\_BINDING\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-462">1819 (0x71B)</span><span class="sxs-lookup"><span data-stu-id="4651e-462">1819 (0x71B)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-463">O identificador de associação não contém todas as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="4651e-463">The binding handle does not contain all required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**falha de comunicação de RPC \_ S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC\_S\_COMM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-465">1820 (0x71C)</span><span class="sxs-lookup"><span data-stu-id="4651e-465">1820 (0x71C)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-466">Ocorreu uma falha de comunicação durante uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4651e-466">A communications failure occurred during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**nível de autenticação do RPC \_ S \_ sem suporte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**RPC\_S\_UNSUPPORTED\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-468">1821 (0x71D)</span><span class="sxs-lookup"><span data-stu-id="4651e-468">1821 (0x71D)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-469">Não há suporte para o nível de autenticação solicitado.</span><span class="sxs-lookup"><span data-stu-id="4651e-469">The requested authentication level is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**\_ \_ não \_ princ \_ nome do RPC**</span><span class="sxs-lookup"><span data-stu-id="4651e-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC\_S\_NO\_PRINC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-471">1822 (0x71E)</span><span class="sxs-lookup"><span data-stu-id="4651e-471">1822 (0x71E)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-472">Nenhum nome de entidade de segurança registrado.</span><span class="sxs-lookup"><span data-stu-id="4651e-472">No principal name registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**\_erro RPC S \_ not \_ RPC \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC\_S\_NOT\_RPC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-474">1823 (0x71F)</span><span class="sxs-lookup"><span data-stu-id="4651e-474">1823 (0x71F)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-475">O erro especificado não é um código de erro de RPC do Windows válido.</span><span class="sxs-lookup"><span data-stu-id="4651e-475">The error specified is not a valid Windows RPC error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**\_ \_ \_ somente local do UUID \_ de RPC S**</span><span class="sxs-lookup"><span data-stu-id="4651e-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**RPC\_S\_UUID\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-477">1824 (0x720)</span><span class="sxs-lookup"><span data-stu-id="4651e-477">1824 (0x720)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-478">Um UUID que é válido somente neste computador foi alocado.</span><span class="sxs-lookup"><span data-stu-id="4651e-478">A UUID that is valid only on this computer has been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**\_erro de pacote RPC s \_ seg \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**RPC\_S\_SEC\_PKG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-480">1825 (0x721)</span><span class="sxs-lookup"><span data-stu-id="4651e-480">1825 (0x721)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-481">Ocorreu um erro específico do pacote de segurança.</span><span class="sxs-lookup"><span data-stu-id="4651e-481">A security package specific error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ S \_ não \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="4651e-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC\_S\_NOT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-483">1826 (0x722)</span><span class="sxs-lookup"><span data-stu-id="4651e-483">1826 (0x722)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-484">O thread não foi cancelado.</span><span class="sxs-lookup"><span data-stu-id="4651e-484">Thread is not canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**ação de es de RPC \_ X \_ inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**RPC\_X\_INVALID\_ES\_ACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-486">1827 (0x723)</span><span class="sxs-lookup"><span data-stu-id="4651e-486">1827 (0x723)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-487">Operação inválida no identificador de codificação/decodificação.</span><span class="sxs-lookup"><span data-stu-id="4651e-487">Invalid operation on the encoding/decoding handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**versão de es de RPC \_ X \_ incorreta \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC\_X\_WRONG\_ES\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-489">1828 (0x724)</span><span class="sxs-lookup"><span data-stu-id="4651e-489">1828 (0x724)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-490">Versão incompatível do pacote de serialização.</span><span class="sxs-lookup"><span data-stu-id="4651e-490">Incompatible version of the serializing package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**versão de stub de RPC \_ X \_ incorreta \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**RPC\_X\_WRONG\_STUB\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-492">1829 (0x725)</span><span class="sxs-lookup"><span data-stu-id="4651e-492">1829 (0x725)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-493">Versão incompatível do stub RPC.</span><span class="sxs-lookup"><span data-stu-id="4651e-493">Incompatible version of the RPC stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**\_objeto de \_ \_ pipe inválido RPC X \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC\_X\_INVALID\_PIPE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-495">1830 (0x726)</span><span class="sxs-lookup"><span data-stu-id="4651e-495">1830 (0x726)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-496">O objeto de pipe de RPC é inválido ou está corrompido.</span><span class="sxs-lookup"><span data-stu-id="4651e-496">The RPC pipe object is invalid or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**ordem de pipe de RPC \_ X \_ incorreta \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC\_X\_WRONG\_PIPE\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-498">1831 (0x727)</span><span class="sxs-lookup"><span data-stu-id="4651e-498">1831 (0x727)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-499">Tentativa de operação inválida em um objeto de pipe RPC.</span><span class="sxs-lookup"><span data-stu-id="4651e-499">An invalid operation was attempted on an RPC pipe object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**\_versão de \_ pipe incorreta de RPC X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC\_X\_WRONG\_PIPE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-501">1832 (0x728)</span><span class="sxs-lookup"><span data-stu-id="4651e-501">1832 (0x728)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-502">Versão de pipe de RPC sem suporte.</span><span class="sxs-lookup"><span data-stu-id="4651e-502">Unsupported RPC pipe version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**\_ \_ \_ falha na autenticação do cookie RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**RPC\_S\_COOKIE\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-504">1833 (0x729)</span><span class="sxs-lookup"><span data-stu-id="4651e-504">1833 (0x729)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-505">O servidor proxy HTTP rejeitou a conexão porque houve falha na autenticação do cookie.</span><span class="sxs-lookup"><span data-stu-id="4651e-505">HTTP proxy server rejected the connection because the cookie authentication failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**\_membro do grupo RPC S \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**RPC\_S\_GROUP\_MEMBER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-507">1898 (0x76A)</span><span class="sxs-lookup"><span data-stu-id="4651e-507">1898 (0x76A)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-508">O membro do grupo não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="4651e-508">The group member was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S não \_ consegue \_ criar**</span><span class="sxs-lookup"><span data-stu-id="4651e-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT\_S\_CANT\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-510">1899 (0x76B)</span><span class="sxs-lookup"><span data-stu-id="4651e-510">1899 (0x76B)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-511">Não foi possível criar a entrada do banco de dados mapeador de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="4651e-511">The endpoint mapper database entry could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**objeto de RPC \_ S \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**RPC\_S\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-513">1900 (0x76C)</span><span class="sxs-lookup"><span data-stu-id="4651e-513">1900 (0x76C)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-514">O UUID (identificador exclusivo universal) do objeto é o UUID nil.</span><span class="sxs-lookup"><span data-stu-id="4651e-514">The object universal unique identifier (UUID) is the nil UUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**tempo de erro \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**ERROR\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-516">1901 (0x76D)</span><span class="sxs-lookup"><span data-stu-id="4651e-516">1901 (0x76D)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-517">A hora especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="4651e-517">The specified time is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERRO \_ de \_ nome de formulário inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERROR\_INVALID\_FORM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-519">1902 (0x76E)</span><span class="sxs-lookup"><span data-stu-id="4651e-519">1902 (0x76E)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-520">O nome do formulário especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-520">The specified form name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERRO \_ de \_ tamanho de formulário inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERROR\_INVALID\_FORM\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-522">1903 (0x76F)</span><span class="sxs-lookup"><span data-stu-id="4651e-522">1903 (0x76F)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-523">O tamanho do formulário especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-523">The specified form size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERRO \_ já \_ aguardando**</span><span class="sxs-lookup"><span data-stu-id="4651e-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERROR\_ALREADY\_WAITING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-525">1904 (0x770)</span><span class="sxs-lookup"><span data-stu-id="4651e-525">1904 (0x770)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-526">O identificador de impressora especificado já está sendo aguardado.</span><span class="sxs-lookup"><span data-stu-id="4651e-526">The specified printer handle is already being waited on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**impressora de erro \_ \_ excluída**</span><span class="sxs-lookup"><span data-stu-id="4651e-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**ERROR\_PRINTER\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-528">1905 (0x771)</span><span class="sxs-lookup"><span data-stu-id="4651e-528">1905 (0x771)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-529">A impressora especificada foi excluída.</span><span class="sxs-lookup"><span data-stu-id="4651e-529">The specified printer has been deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERRO \_ de \_ estado de impressora inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERROR\_INVALID\_PRINTER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-531">1906 (0x772)</span><span class="sxs-lookup"><span data-stu-id="4651e-531">1906 (0x772)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-532">O estado da impressora é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-532">The state of the printer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**a \_ senha do erro \_ deve ser \_ alterada**</span><span class="sxs-lookup"><span data-stu-id="4651e-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**ERROR\_PASSWORD\_MUST\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-534">1907 (0x773)</span><span class="sxs-lookup"><span data-stu-id="4651e-534">1907 (0x773)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-535">A senha do usuário deve ser alterada antes de entrar.</span><span class="sxs-lookup"><span data-stu-id="4651e-535">The user's password must be changed before signing in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**ERRO \_ de \_ controlador de domínio \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**ERROR\_DOMAIN\_CONTROLLER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-537">1908 (0x774)</span><span class="sxs-lookup"><span data-stu-id="4651e-537">1908 (0x774)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-538">Não foi possível localizar o controlador de domínio para este domínio.</span><span class="sxs-lookup"><span data-stu-id="4651e-538">Could not find the domain controller for this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**conta de erro \_ \_ bloqueada \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**ERROR\_ACCOUNT\_LOCKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-540">1909 (0x775)</span><span class="sxs-lookup"><span data-stu-id="4651e-540">1909 (0x775)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-541">A conta referenciada está bloqueada no momento e pode não estar conectada ao.</span><span class="sxs-lookup"><span data-stu-id="4651e-541">The referenced account is currently locked out and may not be logged on to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**OU \_ \_ oxid inválido**</span><span class="sxs-lookup"><span data-stu-id="4651e-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**OR\_INVALID\_OXID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-543">1910 (0x776)</span><span class="sxs-lookup"><span data-stu-id="4651e-543">1910 (0x776)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-544">O exportador de objeto especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="4651e-544">The object exporter specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**OU \_ \_ OID inválido**</span><span class="sxs-lookup"><span data-stu-id="4651e-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**OR\_INVALID\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-546">1911 (0x777)</span><span class="sxs-lookup"><span data-stu-id="4651e-546">1911 (0x777)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-547">O objeto especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="4651e-547">The object specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**OU \_ \_ conjunto inválido**</span><span class="sxs-lookup"><span data-stu-id="4651e-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**OR\_INVALID\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-549">1912 (0x778)</span><span class="sxs-lookup"><span data-stu-id="4651e-549">1912 (0x778)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-550">O conjunto de resolvedores de objetos especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="4651e-550">The object resolver set specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**envio de RPC \_ S \_ \_ incompleto**</span><span class="sxs-lookup"><span data-stu-id="4651e-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC\_S\_SEND\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-552">1913 (0x779)</span><span class="sxs-lookup"><span data-stu-id="4651e-552">1913 (0x779)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-553">Alguns dados continuam a ser enviados no buffer de solicitação.</span><span class="sxs-lookup"><span data-stu-id="4651e-553">Some data remains to be sent in the request buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**\_ \_ \_ identificador assíncrono inválido de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC\_S\_INVALID\_ASYNC\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-555">1914 (0x77A)</span><span class="sxs-lookup"><span data-stu-id="4651e-555">1914 (0x77A)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-556">Identificador de chamada de procedimento remoto assíncrono inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-556">Invalid asynchronous remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**\_ \_ \_ chamada assíncrona inválida de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC\_S\_INVALID\_ASYNC\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-558">1915 (0x77B)</span><span class="sxs-lookup"><span data-stu-id="4651e-558">1915 (0x77B)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-559">Identificador de chamada RPC assíncrona inválido para esta operação.</span><span class="sxs-lookup"><span data-stu-id="4651e-559">Invalid asynchronous RPC call handle for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**\_pipe RPC \_ X \_ fechado**</span><span class="sxs-lookup"><span data-stu-id="4651e-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC\_X\_PIPE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-561">1916 (0x77C)</span><span class="sxs-lookup"><span data-stu-id="4651e-561">1916 (0x77C)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-562">O objeto de pipe de RPC já foi fechado.</span><span class="sxs-lookup"><span data-stu-id="4651e-562">The RPC pipe object has already been closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**\_erro de \_ disciplina de pipe \_ \_ de RPC X**</span><span class="sxs-lookup"><span data-stu-id="4651e-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC\_X\_PIPE\_DISCIPLINE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-564">1917 (0x77D)</span><span class="sxs-lookup"><span data-stu-id="4651e-564">1917 (0x77D)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-565">A chamada RPC foi concluída antes de todos os pipes serem processados.</span><span class="sxs-lookup"><span data-stu-id="4651e-565">The RPC call completed before all pipes were processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**PIPE de RPC \_ X \_ \_ vazio**</span><span class="sxs-lookup"><span data-stu-id="4651e-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC\_X\_PIPE\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-567">1918 (0x77E)</span><span class="sxs-lookup"><span data-stu-id="4651e-567">1918 (0x77E)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-568">Não há mais dados disponíveis no pipe de RPC.</span><span class="sxs-lookup"><span data-stu-id="4651e-568">No more data is available from the RPC pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERRO \_ no \_ SiteName**</span><span class="sxs-lookup"><span data-stu-id="4651e-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERROR\_NO\_SITENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-570">1919 (0x77F)</span><span class="sxs-lookup"><span data-stu-id="4651e-570">1919 (0x77F)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-571">Nenhum nome de site está disponível para este computador.</span><span class="sxs-lookup"><span data-stu-id="4651e-571">No site name is available for this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERRO não é possível \_ \_ acessar o \_ arquivo**</span><span class="sxs-lookup"><span data-stu-id="4651e-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERROR\_CANT\_ACCESS\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-573">1920 (0x780)</span><span class="sxs-lookup"><span data-stu-id="4651e-573">1920 (0x780)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-574">O arquivo não pode ser acessado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="4651e-574">The file cannot be accessed by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERRO não é possível \_ \_ resolver o nome do \_ arquivo**</span><span class="sxs-lookup"><span data-stu-id="4651e-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERROR\_CANT\_RESOLVE\_FILENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-576">1921 (0x781)</span><span class="sxs-lookup"><span data-stu-id="4651e-576">1921 (0x781)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-577">O nome do arquivo não pode ser resolvido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="4651e-577">The name of the file cannot be resolved by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**\_tipo de entrada RPC S \_ \_ \_ incompatível**</span><span class="sxs-lookup"><span data-stu-id="4651e-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**RPC\_S\_ENTRY\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-579">1922 (0x782)</span><span class="sxs-lookup"><span data-stu-id="4651e-579">1922 (0x782)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-580">A entrada não é do tipo esperado.</span><span class="sxs-lookup"><span data-stu-id="4651e-580">The entry is not of the expected type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ S \_ nem \_ todos os \_ objs tivessem \_ exportados**</span><span class="sxs-lookup"><span data-stu-id="4651e-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-582">1923 (0x783)</span><span class="sxs-lookup"><span data-stu-id="4651e-582">1923 (0x783)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-583">Nem todos os UUIDs de objeto puderam ser exportados para a entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="4651e-583">Not all object UUIDs could be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**\_interface RPC \_ S \_ não \_ exportada**</span><span class="sxs-lookup"><span data-stu-id="4651e-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**RPC\_S\_INTERFACE\_NOT\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-585">1924 (0x784)</span><span class="sxs-lookup"><span data-stu-id="4651e-585">1924 (0x784)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-586">A interface não pôde ser exportada para a entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="4651e-586">Interface could not be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**\_perfil RPC \_ S \_ não \_ adicionado**</span><span class="sxs-lookup"><span data-stu-id="4651e-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**RPC\_S\_PROFILE\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-588">1925 (0x785)</span><span class="sxs-lookup"><span data-stu-id="4651e-588">1925 (0x785)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-589">Não foi possível adicionar a entrada de perfil especificada.</span><span class="sxs-lookup"><span data-stu-id="4651e-589">The specified profile entry could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC \_ S \_ Prf \_ ELT \_ não \_ adicionado**</span><span class="sxs-lookup"><span data-stu-id="4651e-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC\_S\_PRF\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-591">1926 (0x786)</span><span class="sxs-lookup"><span data-stu-id="4651e-591">1926 (0x786)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-592">Não foi possível adicionar o elemento de perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="4651e-592">The specified profile element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC \_ S \_ Prf \_ ELT \_ não \_ removido**</span><span class="sxs-lookup"><span data-stu-id="4651e-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC\_S\_PRF\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-594">1927 (0x787)</span><span class="sxs-lookup"><span data-stu-id="4651e-594">1927 (0x787)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-595">O elemento de perfil especificado não pôde ser removido.</span><span class="sxs-lookup"><span data-stu-id="4651e-595">The specified profile element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC \_ S \_ GRP \_ ELT \_ não \_ adicionado**</span><span class="sxs-lookup"><span data-stu-id="4651e-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC\_S\_GRP\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-597">1928 (0x788)</span><span class="sxs-lookup"><span data-stu-id="4651e-597">1928 (0x788)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-598">Não foi possível adicionar o elemento de grupo.</span><span class="sxs-lookup"><span data-stu-id="4651e-598">The group element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC \_ S \_ GRP \_ \_ não \_ removido**</span><span class="sxs-lookup"><span data-stu-id="4651e-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC\_S\_GRP\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-600">1929 (0x789)</span><span class="sxs-lookup"><span data-stu-id="4651e-600">1929 (0x789)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-601">Não foi possível remover o elemento de grupo.</span><span class="sxs-lookup"><span data-stu-id="4651e-601">The group element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**\_Driver km de erro \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="4651e-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERROR\_KM\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-603">1930 (0x78A)</span><span class="sxs-lookup"><span data-stu-id="4651e-603">1930 (0x78A)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-604">O driver de impressora não é compatível com uma política habilitada em seu computador que bloqueia drivers NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="4651e-604">The printer driver is not compatible with a policy enabled on your computer that blocks NT 4.0 drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**contexto de erro \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="4651e-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**ERROR\_CONTEXT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-606">1931 (0x78B)</span><span class="sxs-lookup"><span data-stu-id="4651e-606">1931 (0x78B)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-607">O contexto expirou e não pode mais ser usado.</span><span class="sxs-lookup"><span data-stu-id="4651e-607">The context has expired and can no longer be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERRO \_ por \_ cota de confiança de usuário \_ \_ \_ excedida**</span><span class="sxs-lookup"><span data-stu-id="4651e-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERROR\_PER\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-609">1932 (0x78C)</span><span class="sxs-lookup"><span data-stu-id="4651e-609">1932 (0x78C)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-610">A cota de criação de confiança delegada do usuário atual foi excedida.</span><span class="sxs-lookup"><span data-stu-id="4651e-610">The current user's delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERRO de \_ todas as \_ \_ cotas de confiança de usuário \_ \_ excedidas**</span><span class="sxs-lookup"><span data-stu-id="4651e-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERROR\_ALL\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-612">1933 (0x78D)</span><span class="sxs-lookup"><span data-stu-id="4651e-612">1933 (0x78D)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-613">A cota de criação de confiança delegada total foi excedida.</span><span class="sxs-lookup"><span data-stu-id="4651e-613">The total delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERRO ao \_ excluir a cota de confiança do usuário \_ \_ \_ \_ excedida**</span><span class="sxs-lookup"><span data-stu-id="4651e-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERROR\_USER\_DELETE\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-615">1934 (0x78E)</span><span class="sxs-lookup"><span data-stu-id="4651e-615">1934 (0x78E)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-616">A cota de exclusão de confiança delegada do usuário atual foi excedida.</span><span class="sxs-lookup"><span data-stu-id="4651e-616">The current user's delegated trust deletion quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**\_ \_ falha no firewall de autenticação de erro \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERROR\_AUTHENTICATION\_FIREWALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-618">1935 (0x78F)</span><span class="sxs-lookup"><span data-stu-id="4651e-618">1935 (0x78F)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-619">O computador no qual você está se conectando é protegido por um firewall de autenticação.</span><span class="sxs-lookup"><span data-stu-id="4651e-619">The computer you are signing into is protected by an authentication firewall.</span></span> <span data-ttu-id="4651e-620">A conta especificada não tem permissão para se autenticar no computador.</span><span class="sxs-lookup"><span data-stu-id="4651e-620">The specified account is not allowed to authenticate to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERRO \_ de \_ conexões de impressão remota \_ \_ bloqueadas**</span><span class="sxs-lookup"><span data-stu-id="4651e-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERROR\_REMOTE\_PRINT\_CONNECTIONS\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-622">1936 (0x790)</span><span class="sxs-lookup"><span data-stu-id="4651e-622">1936 (0x790)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-623">As conexões remotas com o spooler de impressão são bloqueadas por uma política definida em seu computador.</span><span class="sxs-lookup"><span data-stu-id="4651e-623">Remote connections to the Print Spooler are blocked by a policy set on your machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERRO \_ NTLM \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="4651e-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERROR\_NTLM\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-625">1937 (0x791)</span><span class="sxs-lookup"><span data-stu-id="4651e-625">1937 (0x791)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-626">A autenticação falhou porque a autenticação NTLM foi desabilitada.</span><span class="sxs-lookup"><span data-stu-id="4651e-626">Authentication failed because NTLM authentication has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**ERRO \_ de \_ alteração de senha \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="4651e-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**ERROR\_PASSWORD\_CHANGE\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-628">1938 (0x792)</span><span class="sxs-lookup"><span data-stu-id="4651e-628">1938 (0x792)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-629">Falha de logon: a política de EAS requer que o usuário altere sua senha antes que essa operação possa ser executada.</span><span class="sxs-lookup"><span data-stu-id="4651e-629">Logon Failure: EAS policy requires that the user change their password before this operation can be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERRO \_ de \_ formato de pixel inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERROR\_INVALID\_PIXEL\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-631">2000 (0x7D0)</span><span class="sxs-lookup"><span data-stu-id="4651e-631">2000 (0x7D0)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-632">O formato de pixel é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-632">The pixel format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERRO \_ de \_ Driver insatisfatório**</span><span class="sxs-lookup"><span data-stu-id="4651e-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERROR\_BAD\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-634">2001 (0x7D1)</span><span class="sxs-lookup"><span data-stu-id="4651e-634">2001 (0x7D1)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-635">O driver especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-635">The specified driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERRO \_ de \_ estilo de janela inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERROR\_INVALID\_WINDOW\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-637">2002 (0x7D2)</span><span class="sxs-lookup"><span data-stu-id="4651e-637">2002 (0x7D2)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-638">O estilo de janela ou o atributo de classe é inválido para esta operação.</span><span class="sxs-lookup"><span data-stu-id="4651e-638">The window style or class attribute is invalid for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**metarquivo de erro \_ \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="4651e-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**ERROR\_METAFILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-640">2003 (0x7D3)</span><span class="sxs-lookup"><span data-stu-id="4651e-640">2003 (0x7D3)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-641">Não há suporte para a operação de metarquivo solicitada.</span><span class="sxs-lookup"><span data-stu-id="4651e-641">The requested metafile operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**transformação de erro \_ \_ sem \_ suporte**</span><span class="sxs-lookup"><span data-stu-id="4651e-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**ERROR\_TRANSFORM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-643">2004 (0x7D4)</span><span class="sxs-lookup"><span data-stu-id="4651e-643">2004 (0x7D4)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-644">Não há suporte para a operação de transformação solicitada.</span><span class="sxs-lookup"><span data-stu-id="4651e-644">The requested transformation operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**\_ \_ não \_ há suporte para REcorte de erro**</span><span class="sxs-lookup"><span data-stu-id="4651e-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**ERROR\_CLIPPING\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-646">2005 (0x7D5)</span><span class="sxs-lookup"><span data-stu-id="4651e-646">2005 (0x7D5)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-647">Não há suporte para a operação de recorte solicitada.</span><span class="sxs-lookup"><span data-stu-id="4651e-647">The requested clipping operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERRO \_ \_ CMM inválido**</span><span class="sxs-lookup"><span data-stu-id="4651e-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERROR\_INVALID\_CMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-649">2010 (0x7DA)</span><span class="sxs-lookup"><span data-stu-id="4651e-649">2010 (0x7DA)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-650">O módulo de gerenciamento de cores especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-650">The specified color management module is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERRO \_ de \_ perfil inválido**</span><span class="sxs-lookup"><span data-stu-id="4651e-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERROR\_INVALID\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-652">2011 (0x7DB)</span><span class="sxs-lookup"><span data-stu-id="4651e-652">2011 (0x7DB)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-653">O perfil de cor especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-653">The specified color profile is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**marca de erro \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="4651e-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**ERROR\_TAG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-655">2012 (0x7DC)</span><span class="sxs-lookup"><span data-stu-id="4651e-655">2012 (0x7DC)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-656">A marca especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="4651e-656">The specified tag was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**marca de erro \_ \_ não \_ presente**</span><span class="sxs-lookup"><span data-stu-id="4651e-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**ERROR\_TAG\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-658">2013 (0x7DD)</span><span class="sxs-lookup"><span data-stu-id="4651e-658">2013 (0x7DD)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-659">Uma marca necessária não está presente.</span><span class="sxs-lookup"><span data-stu-id="4651e-659">A required tag is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERRO \_ de \_ marca duplicada**</span><span class="sxs-lookup"><span data-stu-id="4651e-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERROR\_DUPLICATE\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-661">2014 (0x7DE)</span><span class="sxs-lookup"><span data-stu-id="4651e-661">2014 (0x7DE)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-662">A marca especificada já está presente.</span><span class="sxs-lookup"><span data-stu-id="4651e-662">The specified tag is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**\_perfil \_ de erro não \_ associado \_ ao \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="4651e-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**ERROR\_PROFILE\_NOT\_ASSOCIATED\_WITH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-664">2015 (0x7DF)</span><span class="sxs-lookup"><span data-stu-id="4651e-664">2015 (0x7DF)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-665">O perfil de cor especificado não está associado ao dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="4651e-665">The specified color profile is not associated with the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**Perfil de erro \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**ERROR\_PROFILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-667">2016 (0x7E0)</span><span class="sxs-lookup"><span data-stu-id="4651e-667">2016 (0x7E0)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-668">O perfil de cor especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="4651e-668">The specified color profile was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERRO \_ \_ COLORSPACE inválido**</span><span class="sxs-lookup"><span data-stu-id="4651e-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERROR\_INVALID\_COLORSPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-670">2017 (0x7E1)</span><span class="sxs-lookup"><span data-stu-id="4651e-670">2017 (0x7E1)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-671">O espaço de cores especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-671">The specified color space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERRO \_ ICM \_ não \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="4651e-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERROR\_ICM\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-673">2018 (0x7E2)</span><span class="sxs-lookup"><span data-stu-id="4651e-673">2018 (0x7E2)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-674">O gerenciamento de cores de imagem não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="4651e-674">Image Color Management is not enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERRO ao \_ excluir o \_ XFORM de ICM \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERROR\_DELETING\_ICM\_XFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-676">2019 (0x7E3)</span><span class="sxs-lookup"><span data-stu-id="4651e-676">2019 (0x7E3)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-677">Ocorreu um erro ao excluir a transformação de cor.</span><span class="sxs-lookup"><span data-stu-id="4651e-677">There was an error while deleting the color transform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**\_transformação inválida de erro \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERROR\_INVALID\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-679">2020 (0x7E4)</span><span class="sxs-lookup"><span data-stu-id="4651e-679">2020 (0x7E4)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-680">A transformação de cor especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="4651e-680">The specified color transform is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**incompatibilidade de COLORSPACE de erro \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERROR\_COLORSPACE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-682">2021 (0x7E5)</span><span class="sxs-lookup"><span data-stu-id="4651e-682">2021 (0x7E5)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-683">A transformação especificada não corresponde ao espaço de cores do bitmap.</span><span class="sxs-lookup"><span data-stu-id="4651e-683">The specified transform does not match the bitmap's color space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERRO \_ de \_ COLORINDEX inválido**</span><span class="sxs-lookup"><span data-stu-id="4651e-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERROR\_INVALID\_COLORINDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-685">2022 (0x7E6)</span><span class="sxs-lookup"><span data-stu-id="4651e-685">2022 (0x7E6)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-686">O índice de cores nomeados especificado não está presente no perfil.</span><span class="sxs-lookup"><span data-stu-id="4651e-686">The specified named color index is not present in the profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**\_o perfil de erro \_ \_ não \_ corresponde ao \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="4651e-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**ERROR\_PROFILE\_DOES\_NOT\_MATCH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-688">2023 (0x7E7)</span><span class="sxs-lookup"><span data-stu-id="4651e-688">2023 (0x7E7)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-689">O perfil especificado destina-se a um dispositivo de um tipo diferente do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="4651e-689">The specified profile is intended for a device of a different type than the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERRO \_ conectado a \_ outra \_ senha**</span><span class="sxs-lookup"><span data-stu-id="4651e-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-691">2108 (0x83C)</span><span class="sxs-lookup"><span data-stu-id="4651e-691">2108 (0x83C)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-692">A conexão de rede foi feita com êxito, mas o usuário precisava ser solicitado a fornecer uma senha diferente da especificada originalmente.</span><span class="sxs-lookup"><span data-stu-id="4651e-692">The network connection was made successfully, but the user had to be prompted for a password other than the one originally specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERRO \_ conectado \_ outro \_ padrão de senha \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-694">2109 (0x83D)</span><span class="sxs-lookup"><span data-stu-id="4651e-694">2109 (0x83D)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-695">A conexão de rede foi feita com êxito usando as credenciais padrão.</span><span class="sxs-lookup"><span data-stu-id="4651e-695">The network connection was made successfully using default credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERRO \_ de \_ nome de usuário insatisfatório**</span><span class="sxs-lookup"><span data-stu-id="4651e-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERROR\_BAD\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-697">2202 (0x89A)</span><span class="sxs-lookup"><span data-stu-id="4651e-697">2202 (0x89A)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-698">O nome de usuário especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="4651e-698">The specified username is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERRO \_ não \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="4651e-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERROR\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-700">2250 (0x8CA)</span><span class="sxs-lookup"><span data-stu-id="4651e-700">2250 (0x8CA)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-701">Esta conexão de rede não existe.</span><span class="sxs-lookup"><span data-stu-id="4651e-701">This network connection does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERRO ao \_ abrir \_ arquivos**</span><span class="sxs-lookup"><span data-stu-id="4651e-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERROR\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-703">2401 (0x961)</span><span class="sxs-lookup"><span data-stu-id="4651e-703">2401 (0x961)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-704">Esta conexão de rede tem arquivos abertos ou solicitações pendentes.</span><span class="sxs-lookup"><span data-stu-id="4651e-704">This network connection has files open or requests pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**\_conexões ativas de erro \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ERROR\_ACTIVE\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-706">2402 (0x962)</span><span class="sxs-lookup"><span data-stu-id="4651e-706">2402 (0x962)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-707">As conexões ativas ainda existem.</span><span class="sxs-lookup"><span data-stu-id="4651e-707">Active connections still exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_dispositivo \_ de erro em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="4651e-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**ERROR\_DEVICE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-709">2404 (0x964)</span><span class="sxs-lookup"><span data-stu-id="4651e-709">2404 (0x964)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-710">O dispositivo está em uso por um processo ativo e não pode ser desconectado.</span><span class="sxs-lookup"><span data-stu-id="4651e-710">The device is in use by an active process and cannot be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**MONITOR de impressão de erro \_ desconhecido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERROR\_UNKNOWN\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-712">3000 (0xBB8)</span><span class="sxs-lookup"><span data-stu-id="4651e-712">3000 (0xBB8)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-713">O monitor de impressão especificado é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="4651e-713">The specified print monitor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERRO \_ \_ de driver \_ de impressora em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="4651e-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERROR\_PRINTER\_DRIVER\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-715">3001 (0xBB9)</span><span class="sxs-lookup"><span data-stu-id="4651e-715">3001 (0xBB9)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-716">O driver de impressora especificado está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="4651e-716">The specified printer driver is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**ERRO \_ de \_ arquivo de spool \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**ERROR\_SPOOL\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-718">3002 (0xBBA)</span><span class="sxs-lookup"><span data-stu-id="4651e-718">3002 (0xBBA)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-719">O arquivo de spool não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="4651e-719">The spool file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERRO \_ SPL \_ \_ StartDoc**</span><span class="sxs-lookup"><span data-stu-id="4651e-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERROR\_SPL\_NO\_STARTDOC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-721">3003 (0xBBB)</span><span class="sxs-lookup"><span data-stu-id="4651e-721">3003 (0xBBB)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-722">Uma chamada StartDocPrinter não foi emitida.</span><span class="sxs-lookup"><span data-stu-id="4651e-722">A StartDocPrinter call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERRO \_ SPL \_ \_ ADDJOB**</span><span class="sxs-lookup"><span data-stu-id="4651e-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERROR\_SPL\_NO\_ADDJOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-724">3004 (0xBBC)</span><span class="sxs-lookup"><span data-stu-id="4651e-724">3004 (0xBBC)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-725">Uma chamada AddJob não foi emitida.</span><span class="sxs-lookup"><span data-stu-id="4651e-725">An AddJob call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**ERRO \_ o \_ processador de impressão \_ já está \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="4651e-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**ERROR\_PRINT\_PROCESSOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-727">3005 (0xBBD)</span><span class="sxs-lookup"><span data-stu-id="4651e-727">3005 (0xBBD)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-728">O processador de impressão especificado já foi instalado.</span><span class="sxs-lookup"><span data-stu-id="4651e-728">The specified print processor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**o \_ Monitor de impressão de erro \_ \_ já está \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="4651e-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**ERROR\_PRINT\_MONITOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-730">3006 (0xBBE)</span><span class="sxs-lookup"><span data-stu-id="4651e-730">3006 (0xBBE)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-731">O monitor de impressão especificado já foi instalado.</span><span class="sxs-lookup"><span data-stu-id="4651e-731">The specified print monitor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERRO \_ de \_ Monitor de impressão inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERROR\_INVALID\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-733">3007 (0xBBF)</span><span class="sxs-lookup"><span data-stu-id="4651e-733">3007 (0xBBF)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-734">O monitor de impressão especificado não tem as funções necessárias.</span><span class="sxs-lookup"><span data-stu-id="4651e-734">The specified print monitor does not have the required functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERRO \_ \_ no monitor \_ de impressão em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="4651e-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERROR\_PRINT\_MONITOR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-736">3008 (0xBC0)</span><span class="sxs-lookup"><span data-stu-id="4651e-736">3008 (0xBC0)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-737">O monitor de impressão especificado está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="4651e-737">The specified print monitor is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**a \_ impressora de erro \_ tem \_ trabalhos em \_ fila**</span><span class="sxs-lookup"><span data-stu-id="4651e-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**ERROR\_PRINTER\_HAS\_JOBS\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-739">3009 (0xBC1)</span><span class="sxs-lookup"><span data-stu-id="4651e-739">3009 (0xBC1)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-740">A operação solicitada não é permitida quando há trabalhos na fila para a impressora.</span><span class="sxs-lookup"><span data-stu-id="4651e-740">The requested operation is not allowed when there are jobs queued to the printer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERRO \_ de \_ reinicialização bem-sucedida \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="4651e-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERROR\_SUCCESS\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-742">3010 (0xBC2)</span><span class="sxs-lookup"><span data-stu-id="4651e-742">3010 (0xBC2)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-743">A operação solicitada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4651e-743">The requested operation is successful.</span></span> <span data-ttu-id="4651e-744">As alterações não entrarão em vigor até que o sistema seja reinicializado.</span><span class="sxs-lookup"><span data-stu-id="4651e-744">Changes will not be effective until the system is rebooted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERRO \_ de \_ reinicialização bem-sucedida \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="4651e-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERROR\_SUCCESS\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-746">3011 (0xBC3)</span><span class="sxs-lookup"><span data-stu-id="4651e-746">3011 (0xBC3)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-747">A operação solicitada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4651e-747">The requested operation is successful.</span></span> <span data-ttu-id="4651e-748">As alterações não entrarão em vigor até que o serviço seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="4651e-748">Changes will not be effective until the service is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**impressora de erro \_ \_ não \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="4651e-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**ERROR\_PRINTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-750">3012 (0xBC4)</span><span class="sxs-lookup"><span data-stu-id="4651e-750">3012 (0xBC4)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-751">Nenhuma impressora encontrada.</span><span class="sxs-lookup"><span data-stu-id="4651e-751">No printers were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERRO \_ de \_ Driver de impressora \_ avisado**</span><span class="sxs-lookup"><span data-stu-id="4651e-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERROR\_PRINTER\_DRIVER\_WARNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-753">3013 (0xBC5)</span><span class="sxs-lookup"><span data-stu-id="4651e-753">3013 (0xBC5)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-754">O driver de impressora é conhecido como não confiável.</span><span class="sxs-lookup"><span data-stu-id="4651e-754">The printer driver is known to be unreliable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**Driver de impressora de erro \_ \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="4651e-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**ERROR\_PRINTER\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-756">3014 (0xBC6)</span><span class="sxs-lookup"><span data-stu-id="4651e-756">3014 (0xBC6)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-757">O driver de impressora é conhecido por prejudicar o sistema.</span><span class="sxs-lookup"><span data-stu-id="4651e-757">The printer driver is known to harm the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERRO \_ \_ \_ \_ de pacote de driver de impressora em \_ uso**</span><span class="sxs-lookup"><span data-stu-id="4651e-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERROR\_PRINTER\_DRIVER\_PACKAGE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-759">3015 (0xBC7)</span><span class="sxs-lookup"><span data-stu-id="4651e-759">3015 (0xBC7)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-760">O pacote de driver de impressora especificado está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="4651e-760">The specified printer driver package is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**pacote de driver de núcleo de erro \_ \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="4651e-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**ERROR\_CORE\_DRIVER\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-762">3016 (0xBC8)</span><span class="sxs-lookup"><span data-stu-id="4651e-762">3016 (0xBC8)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-763">Não é possível encontrar um pacote de driver principal exigido pelo pacote de driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="4651e-763">Unable to find a core driver package that is required by the printer driver package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERRO \_ falha na \_ reinicialização \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="4651e-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERROR\_FAIL\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-765">3017 (0xBC9)</span><span class="sxs-lookup"><span data-stu-id="4651e-765">3017 (0xBC9)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-766">A operação solicitada falhou.</span><span class="sxs-lookup"><span data-stu-id="4651e-766">The requested operation failed.</span></span> <span data-ttu-id="4651e-767">Uma reinicialização do sistema é necessária para reverter as alterações feitas.</span><span class="sxs-lookup"><span data-stu-id="4651e-767">A system reboot is required to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERRO \_ de \_ reinicialização \_ iniciada**</span><span class="sxs-lookup"><span data-stu-id="4651e-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERROR\_FAIL\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-769">3018 (0xBCA)</span><span class="sxs-lookup"><span data-stu-id="4651e-769">3018 (0xBCA)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-770">A operação solicitada falhou.</span><span class="sxs-lookup"><span data-stu-id="4651e-770">The requested operation failed.</span></span> <span data-ttu-id="4651e-771">Uma reinicialização do sistema foi iniciada para reverter as alterações feitas.</span><span class="sxs-lookup"><span data-stu-id="4651e-771">A system reboot has been initiated to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERRO \_ de \_ download de driver de impressora \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="4651e-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERROR\_PRINTER\_DRIVER\_DOWNLOAD\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-773">3019 (0xBCB)</span><span class="sxs-lookup"><span data-stu-id="4651e-773">3019 (0xBCB)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-774">O driver de impressora especificado não foi encontrado no sistema e precisa ser baixado.</span><span class="sxs-lookup"><span data-stu-id="4651e-774">The specified printer driver was not found on the system and needs to be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERRO \_ de \_ reinicialização do trabalho de impressão \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="4651e-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERROR\_PRINT\_JOB\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-776">3020 (0xBCC)</span><span class="sxs-lookup"><span data-stu-id="4651e-776">3020 (0xBCC)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-777">Falha ao imprimir o trabalho de impressão solicitado.</span><span class="sxs-lookup"><span data-stu-id="4651e-777">The requested print job has failed to print.</span></span> <span data-ttu-id="4651e-778">Uma atualização do sistema de impressão requer que o trabalho seja reenviado.</span><span class="sxs-lookup"><span data-stu-id="4651e-778">A print system update requires the job to be resubmitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERRO \_ de \_ \_ manifesto de driver de impressora inválido \_**</span><span class="sxs-lookup"><span data-stu-id="4651e-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERROR\_INVALID\_PRINTER\_DRIVER\_MANIFEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-780">3021 (0xBCD)</span><span class="sxs-lookup"><span data-stu-id="4651e-780">3021 (0xBCD)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-781">O driver de impressora não contém um manifesto válido ou contém muitos manifestos.</span><span class="sxs-lookup"><span data-stu-id="4651e-781">The printer driver does not contain a valid manifest, or contains too many manifests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERRO de \_ impressora \_ não \_ compartilhável**</span><span class="sxs-lookup"><span data-stu-id="4651e-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERROR\_PRINTER\_NOT\_SHAREABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-783">3022 (0xBCE)</span><span class="sxs-lookup"><span data-stu-id="4651e-783">3022 (0xBCE)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-784">A impressora especificada não pode ser compartilhada.</span><span class="sxs-lookup"><span data-stu-id="4651e-784">The specified printer cannot be shared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**solicitação de erro \_ \_ pausada**</span><span class="sxs-lookup"><span data-stu-id="4651e-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**ERROR\_REQUEST\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-786">3050 (0xBEA)</span><span class="sxs-lookup"><span data-stu-id="4651e-786">3050 (0xBEA)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-787">A operação foi pausada.</span><span class="sxs-lookup"><span data-stu-id="4651e-787">The operation was paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4651e-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERRO \_ \_ de reemissão de e/s \_ como \_ em cache**</span><span class="sxs-lookup"><span data-stu-id="4651e-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERROR\_IO\_REISSUE\_AS\_CACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4651e-789">3950 (0xF6E)</span><span class="sxs-lookup"><span data-stu-id="4651e-789">3950 (0xF6E)</span></span>
</dt> <dt>



<span data-ttu-id="4651e-790">Emita novamente a operação especificada como uma operação de e/s em cache.</span><span class="sxs-lookup"><span data-stu-id="4651e-790">Reissue the given operation as a cached IO operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="4651e-791">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4651e-791">Requirements</span></span>



| <span data-ttu-id="4651e-792">Requisito</span><span class="sxs-lookup"><span data-stu-id="4651e-792">Requirement</span></span> | <span data-ttu-id="4651e-793">Valor</span><span class="sxs-lookup"><span data-stu-id="4651e-793">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4651e-794">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4651e-794">Minimum supported client</span></span><br/> | <span data-ttu-id="4651e-795">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4651e-795">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4651e-796">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4651e-796">Minimum supported server</span></span><br/> | <span data-ttu-id="4651e-797">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4651e-797">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4651e-798">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4651e-798">Header</span></span><br/>                   | <dl> <span data-ttu-id="4651e-799"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="4651e-799"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4651e-800">Confira também</span><span class="sxs-lookup"><span data-stu-id="4651e-800">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4651e-801">Códigos de erro do sistema</span><span class="sxs-lookup"><span data-stu-id="4651e-801">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




