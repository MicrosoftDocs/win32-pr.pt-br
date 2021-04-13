---
description: As constantes a seguir são usadas pela API de proteção de dados CNG.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: Constantes CNG DPAPI (NCryptprotect. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457267"
---
# <a name="cng-dpapi-constants"></a><span data-ttu-id="ffcef-103">Constantes CNG DPAPI</span><span class="sxs-lookup"><span data-stu-id="ffcef-103">CNG DPAPI Constants</span></span>

<span data-ttu-id="ffcef-104">As constantes a seguir são usadas pela API de proteção de dados CNG.</span><span class="sxs-lookup"><span data-stu-id="ffcef-104">The following constants are used by the CNG Data Protection API.</span></span>

<dl> <dt>

<span data-ttu-id="ffcef-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**\_ \_ delimitador de decrescente \_ de NCRYPT e**</span><span class="sxs-lookup"><span data-stu-id="ffcef-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**NCRYPT\_DESCR\_DELIMITER\_AND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-106">L "E"</span><span class="sxs-lookup"><span data-stu-id="ffcef-106">L" AND "</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-107">Pode ser usado para testar uma cadeia de caracteres de descritor de proteção para um delimitador AND.</span><span class="sxs-lookup"><span data-stu-id="ffcef-107">Can be used to test a protection descriptor string for an AND delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffcef-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**é \_ igual a decrescente de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT\_DESCR\_EQUAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-109">L "="</span><span class="sxs-lookup"><span data-stu-id="ffcef-109">L"="</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-110">Pode ser usado para testar uma cadeia de caracteres de descritor de proteção para um sinal de igual.</span><span class="sxs-lookup"><span data-stu-id="ffcef-110">Can be used to test a protection descriptor string for an equals sign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffcef-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**\_ \_ delimitador de decrescente \_ de NCRYPT ou**</span><span class="sxs-lookup"><span data-stu-id="ffcef-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**NCRYPT\_DESCR\_DELIMITER\_OR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-112">L "OU"</span><span class="sxs-lookup"><span data-stu-id="ffcef-112">L" OR "</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-113">Pode ser usado para testar uma cadeia de caracteres de descritor de proteção para um delimitador ou.</span><span class="sxs-lookup"><span data-stu-id="ffcef-113">Can be used to test a protection descriptor string for an OR delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffcef-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**\_algoritmo de proteção de chave NCRYPT \_ \_ \_ local**</span><span class="sxs-lookup"><span data-stu-id="ffcef-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-115">"LOCAL"</span><span class="sxs-lookup"><span data-stu-id="ffcef-115">"LOCAL"</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-116">O descritor de proteção LOCAL protege o conteúdo para a sessão de logon, o usuário atual ou o computador local, conforme identificado pelas seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="ffcef-116">The LOCAL protection descriptor protects content to the logon session, the current user, or the local machine as identified by the following constants:</span></span>

-   <span data-ttu-id="ffcef-117">**\_ \_ logon local de proteção de chave NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-117">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
-   <span data-ttu-id="ffcef-118">**\_ \_ usuário local de proteção de chave NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-118">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
-   <span data-ttu-id="ffcef-119">**\_ \_ máquina local de proteção de chave NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-119">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffcef-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**\_SDDL de \_ algoritmo de proteção de chave NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-121">SDDL</span><span class="sxs-lookup"><span data-stu-id="ffcef-121">"SDDL"</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-122">Protege o conteúdo a uma cadeia de caracteres SDDL (linguagem de definição de descritor de segurança) que contém informações de descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="ffcef-122">Protects content to an SDDL (Security Descriptor Definition Language) string that contains security descriptor information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffcef-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**\_SID do \_ algoritmo de proteção de chave NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-124">SIDs</span><span class="sxs-lookup"><span data-stu-id="ffcef-124">"SID"</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-125">O descritor de proteção SID contém um grupo ou uma identidade principal.</span><span class="sxs-lookup"><span data-stu-id="ffcef-125">The SID protection descriptor contains a group or principal identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffcef-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**\_WEBcredentials do algoritmo de proteção de chave NCRYPT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-127">"Webcredentials"</span><span class="sxs-lookup"><span data-stu-id="ffcef-127">"WEBCREDENTIALS"</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-128">Protege as credenciais da conta da Web de um usuário.</span><span class="sxs-lookup"><span data-stu-id="ffcef-128">Protects to a user's web account credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffcef-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**\_ \_ logon local de proteção de chave NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-130">logon</span><span class="sxs-lookup"><span data-stu-id="ffcef-130">"logon"</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-131">Protege o conteúdo à sessão de logon atual.</span><span class="sxs-lookup"><span data-stu-id="ffcef-131">Protects content to the current logon session.</span></span> <span data-ttu-id="ffcef-132">Os usuários não poderão descriptografar o conteúdo protegido após o logoff ou a reinicialização.</span><span class="sxs-lookup"><span data-stu-id="ffcef-132">Users will not be able to decrypt the protected content after logoff or reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffcef-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**\_ \_ máquina local de proteção de chave NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-134">Tradução</span><span class="sxs-lookup"><span data-stu-id="ffcef-134">"machine"</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-135">Protege o conteúdo para o computador local.</span><span class="sxs-lookup"><span data-stu-id="ffcef-135">Protects content to the local computer.</span></span> <span data-ttu-id="ffcef-136">Todos os usuários no computador local podem descriptografar o conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="ffcef-136">All users on the local computer can decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffcef-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**\_ \_ usuário local de proteção de chave NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-138">usuário</span><span class="sxs-lookup"><span data-stu-id="ffcef-138">"user"</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-139">Protege o conteúdo à sessão atual do usuário.</span><span class="sxs-lookup"><span data-stu-id="ffcef-139">Protects content to the current user session.</span></span> <span data-ttu-id="ffcef-140">Somente esse usuário no computador local poderá descriptografar o conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="ffcef-140">Only this user on the local computer will be able to decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffcef-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**\_provedor de \_ proteção de chave MS \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**MS\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-142">"Provedor de proteção de chave da Microsoft"</span><span class="sxs-lookup"><span data-stu-id="ffcef-142">"Microsoft Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-143">Representa o provedor de proteção de chave da Microsoft que dá suporte a formatos representados pelas seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="ffcef-143">Represents the Microsoft key protection provider which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="ffcef-144">**\_SID do \_ algoritmo de proteção de chave NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-144">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
-   <span data-ttu-id="ffcef-145">**\_algoritmo de proteção de chave NCRYPT \_ \_ \_ local**</span><span class="sxs-lookup"><span data-stu-id="ffcef-145">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
-   <span data-ttu-id="ffcef-146">**\_SDDL de \_ algoritmo de proteção de chave NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-146">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffcef-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**\_provedor de \_ proteção de chave do cliente do Windows \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**WINDOWS\_CLIENT\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffcef-148">"Provedor de proteção de chave do cliente do Windows"</span><span class="sxs-lookup"><span data-stu-id="ffcef-148">"Windows Client Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="ffcef-149">Representa o provedor de proteção de chave da Microsoft que está disponível somente no cliente e que oferece suporte a formatos representados pelas seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="ffcef-149">Represents the Microsoft key protection provider that is available only on the client and which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="ffcef-150">**\_WEBcredentials do algoritmo de proteção de chave NCRYPT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ffcef-150">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffcef-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffcef-151">Requirements</span></span>



| <span data-ttu-id="ffcef-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffcef-152">Requirement</span></span> | <span data-ttu-id="ffcef-153">Valor</span><span class="sxs-lookup"><span data-stu-id="ffcef-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffcef-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffcef-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ffcef-155">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ffcef-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ffcef-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffcef-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ffcef-157">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ffcef-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ffcef-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ffcef-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffcef-159"><dt>NCryptprotect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffcef-159"><dt>NCryptprotect.h</dt></span></span> </dl> |



 

 




