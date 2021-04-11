---
description: Defina para aplicativos recursos bem conhecidos usando a função AllocateAndInitializeSid.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Constantes de SID de recurso (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172317"
---
# <a name="capability-sid-constants"></a><span data-ttu-id="16e93-103">Constantes de SID de recurso</span><span class="sxs-lookup"><span data-stu-id="16e93-103">Capability SID Constants</span></span>

<span data-ttu-id="16e93-104">As constantes de SID de funcionalidade definem os recursos bem conhecidos do para aplicativos usando a função [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .</span><span class="sxs-lookup"><span data-stu-id="16e93-104">The capability SID constants define for applications well-known capabilities by using the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span>

<dl> <dt>

<span data-ttu-id="16e93-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**recurso de segurança de \_ \_ cliente de Internet \_**</span><span class="sxs-lookup"><span data-stu-id="16e93-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e93-106">(0x00000001l)</span><span class="sxs-lookup"><span data-stu-id="16e93-106">(0x00000001L)</span></span>
</dt> <dt>



<span data-ttu-id="16e93-107">Uma conta tem acesso à Internet de um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="16e93-107">An account has access to the Internet from a client computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16e93-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**funcionalidade de segurança \_ \_ servidor de cliente de Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="16e93-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e93-109">(0x00000002L)</span><span class="sxs-lookup"><span data-stu-id="16e93-109">(0x00000002L)</span></span>
</dt> <dt>



<span data-ttu-id="16e93-110">Uma conta tem acesso à Internet a partir dos computadores cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="16e93-110">An account has access to the Internet from the client and server computers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16e93-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**\_ \_ \_ servidor cliente de rede \_ privada \_ do recurso de segurança**</span><span class="sxs-lookup"><span data-stu-id="16e93-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**SECURITY\_CAPABILITY\_PRIVATE\_NETWORK\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e93-112">(0x00000003L)</span><span class="sxs-lookup"><span data-stu-id="16e93-112">(0x00000003L)</span></span>
</dt> <dt>



<span data-ttu-id="16e93-113">Uma conta tem acesso à Internet de uma rede privada.</span><span class="sxs-lookup"><span data-stu-id="16e93-113">An account has access to the Internet from a private network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16e93-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**\_biblioteca de \_ imagens de recursos de segurança \_**</span><span class="sxs-lookup"><span data-stu-id="16e93-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**SECURITY\_CAPABILITY\_PICTURES\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e93-115">(0x00000004L)</span><span class="sxs-lookup"><span data-stu-id="16e93-115">(0x00000004L)</span></span>
</dt> <dt>



<span data-ttu-id="16e93-116">Uma conta tem acesso à biblioteca de imagens.</span><span class="sxs-lookup"><span data-stu-id="16e93-116">An account has access to the pictures library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16e93-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**\_biblioteca de \_ vídeos de recursos de segurança \_**</span><span class="sxs-lookup"><span data-stu-id="16e93-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**SECURITY\_CAPABILITY\_VIDEOS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e93-118">(0x00000005L)</span><span class="sxs-lookup"><span data-stu-id="16e93-118">(0x00000005L)</span></span>
</dt> <dt>



<span data-ttu-id="16e93-119">Uma conta tem acesso à biblioteca de vídeos.</span><span class="sxs-lookup"><span data-stu-id="16e93-119">An account has access to the videos library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16e93-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**\_biblioteca de \_ música do recurso de segurança \_**</span><span class="sxs-lookup"><span data-stu-id="16e93-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**SECURITY\_CAPABILITY\_MUSIC\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e93-121">(0x00000006L)</span><span class="sxs-lookup"><span data-stu-id="16e93-121">(0x00000006L)</span></span>
</dt> <dt>



<span data-ttu-id="16e93-122">Uma conta tem acesso à biblioteca de músicas.</span><span class="sxs-lookup"><span data-stu-id="16e93-122">An account has access to the music library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16e93-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**\_biblioteca de \_ documentos de recursos de segurança \_**</span><span class="sxs-lookup"><span data-stu-id="16e93-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**SECURITY\_CAPABILITY\_DOCUMENTS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e93-124">(0x00000007L)</span><span class="sxs-lookup"><span data-stu-id="16e93-124">(0x00000007L)</span></span>
</dt> <dt>



<span data-ttu-id="16e93-125">Uma conta tem acesso à biblioteca de documentação.</span><span class="sxs-lookup"><span data-stu-id="16e93-125">An account has access to the documentation library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16e93-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**\_ \_ autenticação corporativa do recurso de segurança \_**</span><span class="sxs-lookup"><span data-stu-id="16e93-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**SECURITY\_CAPABILITY\_ENTERPRISE\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e93-127">(0x00000008L)</span><span class="sxs-lookup"><span data-stu-id="16e93-127">(0x00000008L)</span></span>
</dt> <dt>



<span data-ttu-id="16e93-128">Uma conta tem acesso às credenciais padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="16e93-128">An account has access to the default Windows credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16e93-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**recursos de segurança \_ \_ compartilhados \_ certificados de usuário \_**</span><span class="sxs-lookup"><span data-stu-id="16e93-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**SECURITY\_CAPABILITY\_SHARED\_USER\_CERTIFICATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e93-130">(0x00000009L)</span><span class="sxs-lookup"><span data-stu-id="16e93-130">(0x00000009L)</span></span>
</dt> <dt>



<span data-ttu-id="16e93-131">Uma conta tem acesso aos certificados de usuário compartilhados.</span><span class="sxs-lookup"><span data-stu-id="16e93-131">An account has access to the shared user certificates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16e93-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**\_ \_ armazenamento removível do recurso de segurança \_**</span><span class="sxs-lookup"><span data-stu-id="16e93-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**SECURITY\_CAPABILITY\_REMOVABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e93-133">(0x0000000AL)</span><span class="sxs-lookup"><span data-stu-id="16e93-133">(0x0000000AL)</span></span>
</dt> <dt>



<span data-ttu-id="16e93-134">Uma conta tem acesso ao armazenamento removível.</span><span class="sxs-lookup"><span data-stu-id="16e93-134">An account has access to removable storage.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16e93-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="16e93-135">Remarks</span></span>

<span data-ttu-id="16e93-136">Ao construir um SID de recurso, você precisa incluir a autoridade do pacote, a \_ \_ autoridade do pacote do aplicativo de segurança \_ {0,0,0,0,0,15} , na chamada para a função [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .</span><span class="sxs-lookup"><span data-stu-id="16e93-136">When constructing a capability SID, you need to include the package authority, SECURITY\_APP\_PACKAGE\_AUTHORITY {0,0,0,0,0,15}, in the call to the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span> <span data-ttu-id="16e93-137">Além disso, você precisa da contagem base RID e RID para os recursos internos, o \_ \_ RID base de recurso de segurança \_ (0x00000003L) e a \_ contagem de RID de recurso interno de segurança \_ \_ \_ (2L).</span><span class="sxs-lookup"><span data-stu-id="16e93-137">Additionally, you need the base RID and RID count for the built-in capabilities, SECURITY\_CAPABILITY\_BASE\_RID (0x00000003L) and SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT (2L).</span></span>

## <a name="requirements"></a><span data-ttu-id="16e93-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16e93-138">Requirements</span></span>



| <span data-ttu-id="16e93-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="16e93-139">Requirement</span></span> | <span data-ttu-id="16e93-140">Valor</span><span class="sxs-lookup"><span data-stu-id="16e93-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16e93-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16e93-141">Minimum supported client</span></span><br/> | <span data-ttu-id="16e93-142">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="16e93-142">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="16e93-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16e93-143">Minimum supported server</span></span><br/> | <span data-ttu-id="16e93-144">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="16e93-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="16e93-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16e93-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="16e93-146"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="16e93-146"><dt>Winnt.h</dt></span></span> </dl> |



 

