---
title: Estruturas RPC
description: Esta seção explica as estruturas definidas e usadas pelo Microsoft RPC.
ms.assetid: 8d2f31f6-21d3-402c-b84b-960a2d03ff40
keywords:
- RPC, referência, estruturas de chamada de procedimento remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94d03209af8b14f87cd8b15929389b6eb524833
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641625"
---
# <a name="rpc-structures"></a><span data-ttu-id="dee31-104">Estruturas RPC</span><span class="sxs-lookup"><span data-stu-id="dee31-104">RPC Structures</span></span>

<span data-ttu-id="dee31-105">Esta seção explica as estruturas definidas e usadas pelo Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="dee31-105">This section explains the structures defined and used by Microsoft RPC.</span></span>

-   <span data-ttu-id="dee31-106">[**\_SCONTEXT NDR**](/previous-versions/aa374336(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="dee31-106">[**NDR\_SCONTEXT**](/previous-versions/aa374336(v=vs.80))</span></span>
-   [<span data-ttu-id="dee31-107">**VOLUME**</span><span class="sxs-lookup"><span data-stu-id="dee31-107">**GUID**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
-   [<span data-ttu-id="dee31-108">**\_informações de \_ marshaling do usuário de NDR \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-108">**NDR\_USER\_MARSHAL\_INFO**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info)
-   [<span data-ttu-id="dee31-109">**\_Informações de marshaling do usuário de NDR \_ \_ \_ LEVEL1**</span><span class="sxs-lookup"><span data-stu-id="dee31-109">**NDR\_USER\_MARSHAL\_INFO\_LEVEL1**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info_level1)
-   [<span data-ttu-id="dee31-110">**\_informações de \_ notificação assíncrona de RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-110">**RPC\_ASYNC\_NOTIFICATION\_INFO**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_notification_info)
-   [<span data-ttu-id="dee31-111">**\_estado assíncrono de RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-111">**RPC\_ASYNC\_STATE**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_state)
-   [<span data-ttu-id="dee31-112">**\_Opções de identificador de ligação RPC \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="dee31-112">**RPC\_BINDING\_HANDLE\_OPTIONS\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_options_v1)
-   [<span data-ttu-id="dee31-113">**\_Segurança de identificador de ligação RPC \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="dee31-113">**RPC\_BINDING\_HANDLE\_SECURITY\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a)
-   [<span data-ttu-id="dee31-114">**\_Modelo de associação RPC \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="dee31-114">**RPC\_BINDING\_HANDLE\_TEMPLATE\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a)
-   [<span data-ttu-id="dee31-115">**\_vetor de associação RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-115">**RPC\_BINDING\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_vector)
-   [<span data-ttu-id="dee31-116">**\_ \_ \_ \_ descritor de autenticação do cookie de consentimento RPC C \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-116">**RPC\_C\_OPT\_COOKIE\_AUTH\_DESCRIPTOR**</span></span>](/windows/win32/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)
-   [<span data-ttu-id="dee31-117">**\_Atributos de chamada RPC \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="dee31-117">**RPC\_CALL\_ATTRIBUTES\_V1**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v1_a)
-   [<span data-ttu-id="dee31-118">**\_Atributos de chamada RPC \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="dee31-118">**RPC\_CALL\_ATTRIBUTES\_V2**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a)
-   [<span data-ttu-id="dee31-119">**\_Endereço local da chamada RPC \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="dee31-119">**RPC\_CALL\_LOCAL\_ADDRESS\_V1**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_call_local_address_v1)
-   [<span data-ttu-id="dee31-120">**\_interface de cliente RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-120">**RPC\_CLIENT\_INTERFACE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_client_interface)
-   [<span data-ttu-id="dee31-121">**\_tabela de expedição de RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-121">**RPC\_DISPATCH\_TABLE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_dispatch_table)
-   [<span data-ttu-id="dee31-122">**parâmetro de informações de RPC \_ EE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-122">**RPC\_EE\_INFO\_PARAM**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_ee_info_param)
-   [<span data-ttu-id="dee31-123">**\_modelo de ponto de extremidade RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-123">**RPC\_ENDPOINT\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_endpoint_template)
-   [<span data-ttu-id="dee31-124">**\_identificador de \_ enumeração de erro RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-124">**RPC\_ERROR\_ENUM\_HANDLE**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_error_enum_handle)
-   [<span data-ttu-id="dee31-125">**\_informações de \_ erro ESTENDIdo RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-125">**RPC\_EXTENDED\_ERROR\_INFO**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)
-   [<span data-ttu-id="dee31-126">**\_credenciais de \_ transporte \_ http RPC**</span><span class="sxs-lookup"><span data-stu-id="dee31-126">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_a)
-   [<span data-ttu-id="dee31-127">**\_Credenciais de \_ transporte http RPC \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="dee31-127">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a)
-   [<span data-ttu-id="dee31-128">**\_Credenciais de transporte HTTP de RPC \_ \_ \_ v3**</span><span class="sxs-lookup"><span data-stu-id="dee31-128">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v3_a)
-   [<span data-ttu-id="dee31-129">**RPC \_ se \_ ID**</span><span class="sxs-lookup"><span data-stu-id="dee31-129">**RPC\_IF\_ID**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id)
-   [<span data-ttu-id="dee31-130">**RPC \_ se \_ o \_ vetor de ID**</span><span class="sxs-lookup"><span data-stu-id="dee31-130">**RPC\_IF\_ID\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id_vector)
-   [<span data-ttu-id="dee31-131">**\_modelo de interface RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-131">**RPC\_INTERFACE\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_interface_template)
-   [<span data-ttu-id="dee31-132">**\_política RPC**</span><span class="sxs-lookup"><span data-stu-id="dee31-132">**RPC\_POLICY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_policy)
-   [<span data-ttu-id="dee31-133">**\_vetor PROTSEQ de RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-133">**RPC\_PROTSEQ\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_protseq_vector)
-   [<span data-ttu-id="dee31-134">**\_QoS de segurança RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-134">**RPC\_SECURITY\_QOS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos)
-   [<span data-ttu-id="dee31-135">**\_QoS de segurança RPC \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="dee31-135">**RPC\_SECURITY\_QOS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v2_a)
-   [<span data-ttu-id="dee31-136">**\_QoS de segurança RPC \_ \_ v3**</span><span class="sxs-lookup"><span data-stu-id="dee31-136">**RPC\_SECURITY\_QOS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v3_a)
-   [<span data-ttu-id="dee31-137">**\_QoS de segurança RPC \_ \_ v4**</span><span class="sxs-lookup"><span data-stu-id="dee31-137">**RPC\_SECURITY\_QOS\_V4**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v4_a)
-   [<span data-ttu-id="dee31-138">**\_QoS de segurança RPC \_ \_ V5**</span><span class="sxs-lookup"><span data-stu-id="dee31-138">**RPC\_SECURITY\_QOS\_V5**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v5_a)
-   [<span data-ttu-id="dee31-139">**\_vetor de estatísticas de RPC \_**</span><span class="sxs-lookup"><span data-stu-id="dee31-139">**RPC\_STATS\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_stats_vector)
-   [<span data-ttu-id="dee31-140">**\_identidade de \_ autenticação \_ WinNT de s**</span><span class="sxs-lookup"><span data-stu-id="dee31-140">**SEC\_WINNT\_AUTH\_IDENTITY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a)
-   [<span data-ttu-id="dee31-141">**UUID**</span><span class="sxs-lookup"><span data-stu-id="dee31-141">**UUID**</span></span>](./rpcdce/ns-rpcdce-uuid.md)
-   [<span data-ttu-id="dee31-142">**\_vetor UUID**</span><span class="sxs-lookup"><span data-stu-id="dee31-142">**UUID\_VECTOR**</span></span>](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)

 

 