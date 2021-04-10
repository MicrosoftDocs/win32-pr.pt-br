---
description: Permissões nativas da API WiFi
ms.assetid: cfea9f7d-a069-497b-8138-b3949002fa5d
title: Permissões nativas da API WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afafec7619e0920a17e3769a430c8c79aeff3828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169388"
---
# <a name="native-wifi-api-permissions"></a><span data-ttu-id="e6954-103">Permissões nativas da API WiFi</span><span class="sxs-lookup"><span data-stu-id="e6954-103">Native Wifi API Permissions</span></span>

<span data-ttu-id="e6954-104">Uma chamada nativa à API wifi pode falhar com quando um chamador não tiver as permissões adequadas para executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="e6954-104">A Native Wifi API call may fail with when a caller does not have adequate permissions to perform the requested operation.</span></span>

<span data-ttu-id="e6954-105">As permissões são armazenadas em uma [DACL (listas de controle de acesso discricionário)](../secauthz/access-control-lists.md) associadas a um [**\_ \_ objeto protegível de WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span><span class="sxs-lookup"><span data-stu-id="e6954-105">Permissions are stored in a [discretionary access control lists (DACL)](../secauthz/access-control-lists.md) associated with a [**WLAN\_SECURABLE\_OBJECT**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object).</span></span> <span data-ttu-id="e6954-106">Para obter mais informações sobre DACLs e objetos protegíveis, consulte [como as DACLs controlam o acesso a um objeto](../secauthz/how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="e6954-106">For more information about DACLs and securable objects, see [How DACLs Control Access to an Object](../secauthz/how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="e6954-107">A tabela a seguir mostra as funções WiFi nativas que usam objetos protegíveis para determinar se o chamador tem permissões suficientes para executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="e6954-107">The following table shows the Native Wifi functions that use securable objects to determine if the caller has sufficient permissions to perform the requested operation.</span></span> <span data-ttu-id="e6954-108">Ele também mostra os objetos protegíveis usados por cada função.</span><span class="sxs-lookup"><span data-stu-id="e6954-108">It also shows the securable objects used by each function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6954-109">Função</span><span class="sxs-lookup"><span data-stu-id="e6954-109">Function</span></span></th>
<th><span data-ttu-id="e6954-110">Objeto protegível</span><span class="sxs-lookup"><span data-stu-id="e6954-110">Securable object</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6954-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6954-111"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"><strong>WlanSetFilterList</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="e6954-112">wlan_secure_deny_list</span><span class="sxs-lookup"><span data-stu-id="e6954-112">wlan_secure_deny_list</span></span></li>
<li><span data-ttu-id="e6954-113">wlan_secure_permit_list</span><span class="sxs-lookup"><span data-stu-id="e6954-113">wlan_secure_permit_list</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6954-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6954-114"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="e6954-115">wlan_secure_ihv_control</span><span class="sxs-lookup"><span data-stu-id="e6954-115">wlan_secure_ihv_control</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6954-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6954-116"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"><strong>WlanSetAutoConfigParameter</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="e6954-117">wlan_secure_show_denied</span><span class="sxs-lookup"><span data-stu-id="e6954-117">wlan_secure_show_denied</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6954-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6954-118"><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"><strong>WlanSetInterface</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="e6954-119">wlan_secure_ac_enabled</span><span class="sxs-lookup"><span data-stu-id="e6954-119">wlan_secure_ac_enabled</span></span></li>
<li><span data-ttu-id="e6954-120">wlan_secure_bc_scan_enabled</span><span class="sxs-lookup"><span data-stu-id="e6954-120">wlan_secure_bc_scan_enabled</span></span></li>
<li><span data-ttu-id="e6954-121">wlan_secure_bss_type</span><span class="sxs-lookup"><span data-stu-id="e6954-121">wlan_secure_bss_type</span></span></li>
<li><span data-ttu-id="e6954-122">wlan_secure_current_operation_mode</span><span class="sxs-lookup"><span data-stu-id="e6954-122">wlan_secure_current_operation_mode</span></span></li>
<li><span data-ttu-id="e6954-123">wlan_secure_interface_properties</span><span class="sxs-lookup"><span data-stu-id="e6954-123">wlan_secure_interface_properties</span></span></li>
<li><span data-ttu-id="e6954-124">wlan_secure_media_streaming_mode_enabled</span><span class="sxs-lookup"><span data-stu-id="e6954-124">wlan_secure_media_streaming_mode_enabled</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6954-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6954-125"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="e6954-126">wlan_secure_add_new_all_user_profiles</span><span class="sxs-lookup"><span data-stu-id="e6954-126">wlan_secure_add_new_all_user_profiles</span></span></li>
<li><span data-ttu-id="e6954-127">wlan_secure_add_new_per_user_profiles</span><span class="sxs-lookup"><span data-stu-id="e6954-127">wlan_secure_add_new_per_user_profiles</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6954-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6954-128"><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"><strong>WlanSetProfilePosition</strong></a></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="e6954-129">wlan_secure_all_user_profiles_order</span><span class="sxs-lookup"><span data-stu-id="e6954-129">wlan_secure_all_user_profiles_order</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e6954-130">Antes que uma das funções nomeadas acima conclua sua operação, a função recupera a DACL armazenada no objeto protegível apropriado.</span><span class="sxs-lookup"><span data-stu-id="e6954-130">Before one of the above-named functions completes its operation, the function retrieves the DACL stored in the appropriate securable object.</span></span> <span data-ttu-id="e6954-131">Em seguida, a função verifica a DACL para ver se o chamador tem permissões suficientes.</span><span class="sxs-lookup"><span data-stu-id="e6954-131">The function then checks the DACL to see if the caller has sufficient permissions.</span></span> <span data-ttu-id="e6954-132">As \* funções WlanGet e WlanQuery \* exigem que a DACL contenha uma [ACE (entrada de controle de acesso)](../secauthz/access-control-entries.md) que conceda o [token de acesso](../secauthz/access-tokens.md) do acesso de leitura da WLAN do thread de chamada \_ \_ à função.</span><span class="sxs-lookup"><span data-stu-id="e6954-132">The WlanGet\* and WlanQuery\* functions require that the DACL contains an [access control entry (ACE)](../secauthz/access-control-entries.md) that grants the [access token](../secauthz/access-tokens.md) of the calling thread WLAN\_READ\_ACCESS to the function.</span></span> <span data-ttu-id="e6954-133">As funções de Wlanset \* exigem uma ACE que concede o token de acesso do acesso de gravação de WLAN do thread de chamada \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e6954-133">The WlanSet\* functions require an ACE that grants the access token of the calling thread WLAN\_WRITE\_ACCESS.</span></span> <span data-ttu-id="e6954-134">Se o chamador não tiver permissões suficientes, a chamada de função falhará com o erro de \_ acesso \_ negado.</span><span class="sxs-lookup"><span data-stu-id="e6954-134">If the caller does not have sufficient permissions, the function call fails with the error ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="e6954-135">Cada objeto protegível tem uma DACL associada a ele por padrão.</span><span class="sxs-lookup"><span data-stu-id="e6954-135">Each securable object has a DACL associated with it by default.</span></span> <span data-ttu-id="e6954-136">As permissões padrão armazenadas na DACL podem ser alteradas usando a função [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) .</span><span class="sxs-lookup"><span data-stu-id="e6954-136">The default permissions stored in the DACL can be changed using the [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) function.</span></span> <span data-ttu-id="e6954-137">Para determinar os direitos de usuário efetivos necessários para executar uma operação em um sistema específico, chame [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span><span class="sxs-lookup"><span data-stu-id="e6954-137">To determine the effective user rights required to perform an operation on a particular system, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="e6954-138">Todos os perfis de usuário têm permissões adicionais associadas ao próprio perfil.</span><span class="sxs-lookup"><span data-stu-id="e6954-138">All-user profiles have additional permissions associated with the profile itself.</span></span> <span data-ttu-id="e6954-139">As permissões em um perfil de todos os usuários são estabelecidas quando o perfil é criado ou modificado usando [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) ou [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span><span class="sxs-lookup"><span data-stu-id="e6954-139">The permissions on an all-user profile are established when the profile is created or modified using [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) or [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile).</span></span> <span data-ttu-id="e6954-140">O parâmetro *strAllUserProfileSecurity* especifica as permissões necessárias para modificar um perfil, excluir um perfil ou conectar-se a uma rede usando um perfil.</span><span class="sxs-lookup"><span data-stu-id="e6954-140">The *strAllUserProfileSecurity* parameter specifies the required permissions for modifying a profile, deleting a profile, or connecting to a network using a profile.</span></span> <span data-ttu-id="e6954-141">Excluir ou modificar um perfil requer permissão de acesso de gravação de WLAN \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e6954-141">Deleting or modifying a profile requires WLAN\_WRITE\_ACCESS permission.</span></span> <span data-ttu-id="e6954-142">Conectar-se a uma rede usando um perfil requer permissão de acesso de execução de WLAN \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e6954-142">Connecting to a network using a profile requires WLAN\_EXECUTE\_ACCESS permission.</span></span>

<span data-ttu-id="e6954-143">\* \* Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2: \* \* não há suporte para as funções [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) e [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) .</span><span class="sxs-lookup"><span data-stu-id="e6954-143">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* The [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) and [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) functions are not supported.</span></span> <span data-ttu-id="e6954-144">O parâmetro *strAllUserProfileSecurity* não é usado.</span><span class="sxs-lookup"><span data-stu-id="e6954-144">The *strAllUserProfileSecurity* parameter is not used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6954-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6954-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6954-146">Como as DACLs controlam o acesso a um objeto</span><span class="sxs-lookup"><span data-stu-id="e6954-146">How DACLs Control Access to an Object</span></span>](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="e6954-147">**\_objeto PROTEGÍVEL \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="e6954-147">**WLAN\_SECURABLE\_OBJECT**</span></span>](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
