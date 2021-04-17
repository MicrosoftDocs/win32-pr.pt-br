---
description: Lista os tipos de ACE definidos atualmente.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (WinNT. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d06b3457e4df6aea38d3e35acf4f7aaa4e2f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751326"
---
# <a name="ace"></a>PERFEITA

Uma **Ace** é uma [*entrada de controle de acesso*](/windows/desktop/SecGloss/a-gly) em uma ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ).

A tabela a seguir lista os tipos de **Ace** definidos atualmente.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de ACE</th>
<th>Estrutura</th>
<th>Tipo de ACL</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Acesso permitido</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></td>
<td>DACL</td>
</tr>
<tr class="even">
<td><ul>
<li>Acesso permitido</li>
<li>Permite o retorno de chamada durante a verificação de acesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></td>
<td>DACL</td>
</tr>
<tr class="odd">
<td><ul>
<li>Acesso permitido</li>
<li>Específico do objeto</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></td>
<td>DACL</td>
</tr>
<tr class="even">
<td><ul>
<li>Acesso permitido</li>
<li>Específico do objeto</li>
<li>Permite o retorno de chamada durante a verificação de acesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>DACL</td>
</tr>
<tr class="odd">
<td><ul>
<li>Acesso negado</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></td>
<td>DACL</td>
</tr>
<tr class="even">
<td><ul>
<li>Acesso negado</li>
<li>Permite o retorno de chamada durante a verificação de acesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></td>
<td>DACL</td>
</tr>
<tr class="odd">
<td><ul>
<li>Acesso negado</li>
<li>Específico do objeto</li>
<li>Permite o retorno de chamada durante a verificação de acesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>DACL</td>
</tr>
<tr class="even">
<td><ul>
<li>Acesso negado</li>
<li>Específico do objeto</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></td>
<td>DACL</td>
</tr>
<tr class="odd">
<td><ul>
<li>Alarme do sistema</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="even">
<td><ul>
<li>Alarme do sistema</li>
<li>Permite o retorno de chamada durante a verificação de acesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="odd">
<td><ul>
<li>Alarme do sistema</li>
<li>Específico do objeto</li>
<li>Permite o retorno de chamada durante a verificação de acesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="even">
<td><ul>
<li>Alarme do sistema</li>
<li>Específico do objeto</li>
</ul></td>
<td><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="odd">
<td><ul>
<li>Auditoria do sistema</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="even">
<td><ul>
<li>Auditoria do sistema</li>
<li>Permite o retorno de chamada durante a verificação de acesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="odd">
<td><ul>
<li>Auditoria do sistema</li>
<li>Específico do objeto</li>
<li>Permite o retorno de chamada durante a verificação de acesso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
<tr class="even">
<td><ul>
<li>Auditoria do sistema</li>
<li>Específico do objeto</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></td>
<td>Sistema</td>
</tr>
</tbody>
</table>



 

Não há suporte para as ACEs System-Alarm específicas do sistema e do objeto.

> [!Note]  
> Cada ACE começa com uma estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . O formato dos dados que seguem o cabeçalho varia de acordo com o tipo de ACE especificado no cabeçalho.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>Winnt. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**Ace de acesso \_ permitido \_**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**Ace de acesso \_ negado \_**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**LCA**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**\_Ace do alarme do sistema \_**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**\_ACE de auditoria do sistema \_**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

