---
description: Durante uma atualização do computador ou uma migração de computador a computador, os certificados em determinados repositórios de certificados serão migrados.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Migração do repositório de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de694fc24433ce8db039dd677f52935da70cbf07d0a719b0871bd1e8f4b2d35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771092"
---
# <a name="certificate-store-migration"></a>Migração do repositório de certificados

Durante uma atualização do computador ou uma migração de computador a computador, os certificados em determinados repositórios de certificados serão migrados. A tabela a seguir lista os repositórios de certificados que são migrados por padrão. para o repositório ACRS (Configurações solicitação de certificado automática) do sistema, somente as [*listas de certificados confiáveis*](../secgloss/c-gly.md) (CTLs) são migradas. Para todas as outras lojas listadas abaixo, somente os certificados são migrados.

<table>
<thead>
<tr class="header">
<th>Sistema/usuário</th>
<th>Repositório</th>
<th>Local de armazenamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$ {ROWSPAN8} $System $ {remover} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Raiz</strong> \ do <strong>Certificados</strong> do<br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Meu</strong> \ <strong>Certificados</strong> do<br/></td>

</tr>
<tr class="odd">
<td>REQUEST</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Solicitação</strong> \ do <strong>Certificados</strong> do<br/></td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificados</strong> do<br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificados</strong> do<br/></td>

</tr>
<tr class="even">
<td>Não permitido</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Não <strong>permitido</strong> \ <strong>Certificados</strong> do<br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>AC</strong> \ <strong>Certificados</strong> do<br/></td>

</tr>
<tr class="even">
<td>ACRS</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>ACRS</strong> \ <strong>CTLs</strong><br/></td>

</tr>
<tr class="odd">
<td rowspan="7">Usuário $ {REMOVE} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Raiz</strong> \ do <strong>Certificados</strong> do<br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td>arquivo: \\ %AppData%\Microsoft\SystemCertificates\My\Certificates</td>

</tr>
<tr class="odd">
<td>REQUEST</td>
<td>arquivo: \\ %AppData%\Microsoft\SystemCertificates\Request\Certificates</td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Certificados</strong> do<br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Certificados</strong> do<br/></td>

</tr>
<tr class="even">
<td>Não permitido</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ Não <strong>permitido</strong> \ <strong>Certificados</strong> do<br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>AC</strong> \ <strong>Certificados</strong> do<br/></td>

</tr>
</tbody>
</table>



 

Outros repositórios de certificados criados por aplicativos não são migrados por padrão. Os aplicativos que criam suas próprias lojas são responsáveis pela migração das lojas que eles criam. Para criar lojas, recomendamos que você defina uma chave do registro nas configurações do aplicativo e crie um repositório dentro das configurações do registro usando o provedor de repositório de **certificados \_ \_ Prov \_ reg** Store. Para obter mais informações sobre como migrar configurações de aplicativo, consulte o tópico *como criar um arquivo de .xml personalizado* no guia *usando o USMT 3,0* em [ferramenta de migração do usuário 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx). (Esse recurso pode não estar disponível em alguns idiomas e países ou regiões.)

 

 
