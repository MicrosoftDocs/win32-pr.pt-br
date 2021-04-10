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
# <a name="native-wifi-api-permissions"></a>Permissões nativas da API WiFi

Uma chamada nativa à API wifi pode falhar com quando um chamador não tiver as permissões adequadas para executar a operação solicitada.

As permissões são armazenadas em uma [DACL (listas de controle de acesso discricionário)](../secauthz/access-control-lists.md) associadas a um [**\_ \_ objeto protegível de WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object). Para obter mais informações sobre DACLs e objetos protegíveis, consulte [como as DACLs controlam o acesso a um objeto](../secauthz/how-dacls-control-access-to-an-object.md).

A tabela a seguir mostra as funções WiFi nativas que usam objetos protegíveis para determinar se o chamador tem permissões suficientes para executar a operação solicitada. Ele também mostra os objetos protegíveis usados por cada função.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Objeto protegível</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlangetfilterlist"><strong>WlanGetFilterList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetfilterlist"> <strong>WlanSetFilterList</strong></a><br/></td>
<td><ul>
<li>wlan_secure_deny_list</li>
<li>wlan_secure_permit_list</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanihvcontrol"><strong>WlanIhvControl</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ihv_control</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryautoconfigparameter"><strong>WlanQueryAutoConfigParameter</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetautoconfigparameter"> <strong>WlanSetAutoConfigParameter</strong></a><br/></td>
<td><ul>
<li>wlan_secure_show_denied</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface"><strong>WlanQueryInterface</strong></a>, <a href="/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface"> <strong>WlanSetInterface</strong></a><br/></td>
<td><ul>
<li>wlan_secure_ac_enabled</li>
<li>wlan_secure_bc_scan_enabled</li>
<li>wlan_secure_bss_type</li>
<li>wlan_secure_current_operation_mode</li>
<li>wlan_secure_interface_properties</li>
<li>wlan_secure_media_streaming_mode_enabled</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile"><strong>WlanSetProfile</strong></a><br/></td>
<td><ul>
<li>wlan_secure_add_new_all_user_profiles</li>
<li>wlan_secure_add_new_per_user_profiles</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist"><strong>WlanSetProfileList</strong></a>, <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition"> <strong>WlanSetProfilePosition</strong></a><br/></td>
<td><ul>
<li>wlan_secure_all_user_profiles_order</li>
</ul></td>
</tr>
</tbody>
</table>



 

Antes que uma das funções nomeadas acima conclua sua operação, a função recupera a DACL armazenada no objeto protegível apropriado. Em seguida, a função verifica a DACL para ver se o chamador tem permissões suficientes. As \* funções WlanGet e WlanQuery \* exigem que a DACL contenha uma [ACE (entrada de controle de acesso)](../secauthz/access-control-entries.md) que conceda o [token de acesso](../secauthz/access-tokens.md) do acesso de leitura da WLAN do thread de chamada \_ \_ à função. As funções de Wlanset \* exigem uma ACE que concede o token de acesso do acesso de gravação de WLAN do thread de chamada \_ \_ . Se o chamador não tiver permissões suficientes, a chamada de função falhará com o erro de \_ acesso \_ negado.

Cada objeto protegível tem uma DACL associada a ele por padrão. As permissões padrão armazenadas na DACL podem ser alteradas usando a função [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) . Para determinar os direitos de usuário efetivos necessários para executar uma operação em um sistema específico, chame [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).

Todos os perfis de usuário têm permissões adicionais associadas ao próprio perfil. As permissões em um perfil de todos os usuários são estabelecidas quando o perfil é criado ou modificado usando [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile) ou [**WlanSaveTemporaryProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansavetemporaryprofile). O parâmetro *strAllUserProfileSecurity* especifica as permissões necessárias para modificar um perfil, excluir um perfil ou conectar-se a uma rede usando um perfil. Excluir ou modificar um perfil requer permissão de acesso de gravação de WLAN \_ \_ . Conectar-se a uma rede usando um perfil requer permissão de acesso de execução de WLAN \_ \_ .

* * Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2: * * não há suporte para as funções [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings) e [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings) . O parâmetro *strAllUserProfileSecurity* não é usado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como as DACLs controlam o acesso a um objeto](../secauthz/how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**\_objeto PROTEGÍVEL \_ WLAN**](/windows/desktop/api/wlanapi/ne-wlanapi-wlan_securable_object)
</dt> </dl>

 

 
