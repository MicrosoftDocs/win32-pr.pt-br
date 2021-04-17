---
description: Funções para configurar e recuperar um descritor de segurança de objetos.
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: 'Funções de descritor de segurança de nível inferior '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72406dc2481e4671d8d535327f416a2d003c3a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755565"
---
# <a name="low-level-security-descriptor-functions"></a>Funções de descritor de segurança de nível inferior 

Há vários pares de funções de nível baixo para configurar e recuperar o [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)de um objeto. Cada um desses pares funciona apenas com um conjunto limitado de objetos do Windows. Por exemplo, um par funciona com objetos de arquivo e outro funciona com chaves do registro. A tabela a seguir mostra as funções de nível baixo a serem usadas com os diferentes tipos de objetos protegíveis.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de objeto</th>
<th>Funções de nível baixo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Arquivos</a></li>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Listas</a></li>
<li>Processadores</li>
<li><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Pipes nomeados</a></li>
</ul></td>
<td>Use as funções <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>GetFileSecurity</strong></a> e <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>SetFileSecurity</strong></a> . Essas funções usam cadeias de caracteres para identificar o objeto protegível, em vez de usar identificadores.</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Processos</a></li>
<li><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></li>
<li><a href="access-rights-for-access-token-objects.md">Tokens de acesso</a></li>
<li><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Objetos de mapeamento de arquivos</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semáforos</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Eventos</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexes</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Temporizadores esperados</a></li>
</ul></td>
<td>Use as funções <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>GetKernelObjectSecurity</strong></a> e <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>SetKernelObjectSecurity</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Estações de janela</a></li>
<li><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktops</a></li>
</ul></td>
<td>Use as funções <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>GetUserObjectSecurity</strong></a> e <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>SetUserObjectSecurity</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Chaves do Registro</a></li>
</ul></td>
<td>Use as funções <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>RegGetKeySecurity</strong></a> e <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>RegSetKeySecurity</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/Services/service-security-and-access-rights">Objetos de serviço do Windows</a></li>
</ul></td>
<td>Use as funções <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> e <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li>Objetos de impressora</li>
</ul></td>
<td>Use a estrutura de <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> com as funções <a href="/windows/desktop/printdocs/getprinter"><strong>getimpressor</strong></a> e <a href="/windows/desktop/printdocs/setprinter"><strong>setprinter</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Compartilhamentos de rede</a></li>
</ul></td>
<td>Use o nível 502 com as funções <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> e <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="acl-based-access-control.md">Objetos privados (objetos privados ao aplicativo de criação)</a></li>
</ul></td>
<td>Use as funções <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>CreatePrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> e <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>SetPrivateObjectSecurity</strong></a> .</td>
</tr>
</tbody>
</table>



 

 

 
