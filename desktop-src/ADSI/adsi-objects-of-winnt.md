---
title: Objetos ADSI do WinNT
description: O provedor do ADSI WinNT implementa os seguintes objetos COM para dar suporte a recursos e serviços de várias interfaces ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- ADSI do provedor de serviços do WinNT, objetos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d0c9e5c486d07e1e392a9f307ecd9af4509ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084013"
---
# <a name="adsi-objects-of-winnt"></a>Objetos ADSI do WinNT

O provedor do ADSI WinNT implementa os seguintes objetos COM para dar suporte a recursos e serviços de várias interfaces ADSI.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Objeto ADSI</th>
<th>Descrição</th>
<th>Interfaces com suporte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Classe</strong></td>
<td>Um objeto ADSI que representa uma definição de classe.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong>IADsClass</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Computador</strong></td>
<td>Um objeto ADSI que representa um computador.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Domínio</strong></td>
<td>Um objeto ADSI que representa um domínio pela rede.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FileService</strong></td>
<td>Um objeto ADSI que representa um serviço de arquivo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FileShare</strong></td>
<td>Um objeto ADSI que representa um compartilhamento de arquivos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FPNWFileService</strong></td>
<td>Um objeto ADSI que representa um serviço de arquivo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWFileShare</strong></td>
<td>Um objeto ADSI que representa um compartilhamento de arquivos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FPNWResource</strong></td>
<td>Um objeto ADSI que representa um recurso.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWResourcesCollection</strong></td>
<td>Um objeto ADSI que representa uma coleção de recursos.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADscollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>FPNWSession</strong></td>
<td>Um objeto ADSI que representa uma sessão.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWSessionsCollection</strong></td>
<td>Um objeto ADSI que representa uma coleção de sessões.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADscollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>Grupo</strong></td>
<td>Um objeto ADSI que representa um grupo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl>
<blockquote>
[!Note]<br />
GetInfo não pode ser usada para grupos que contêm membros que são entidades de segurança wellKnown no escopo WinNT.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>GroupCollection</strong></td>
<td>Um objeto ADSI que representa uma coleção de grupos.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Localgroup</strong></td>
<td>Um objeto ADSI que representa um grupo local.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>LocalgroupCollection</strong></td>
<td>Um objeto ADSI que representa uma coleção de grupos locais.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Namespace</strong></td>
<td>Um objeto ADSI que representa o namespace WinNT.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>PrintJob</strong></td>
<td>Um objeto ADSI que representa um trabalho de impressão.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Trabalhos de trabalho</strong></td>
<td>Um objeto ADSI que representa uma coleção de trabalhos de impressão.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADscollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>PrintQueue</strong></td>
<td>Um objeto ADSI que representa uma fila de impressão.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Propriedade</strong></td>
<td>Um objeto ADSI que representa uma definição de atributo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>iadsproperty</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Recurso</strong></td>
<td>Um objeto ADSI que representa um recurso.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Recursos</strong></td>
<td>Um objeto ADSI que representa uma coleção de recursos.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADscollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Esquema</strong></td>
<td>Um objeto ADSI que representa o contêiner de esquema.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Serviço</strong></td>
<td>Um objeto ADSI que representa um serviço.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Sessão</strong></td>
<td>Um objeto ADSI que representa uma sessão.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Sessõescollection</strong></td>
<td>Um objeto ADSI que representa uma coleção de sessões.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADscollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Sintaxe</strong></td>
<td>Um objeto ADSI que representa a sintaxe de um atributo.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>IADsSyntax</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Usuário</strong></td>
<td>Um objeto ADSI que representa uma conta de usuário.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Usergroupcollection</strong></td>
<td>Um objeto ADSI que representa uma coleção de grupos de usuários.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></td>
</tr>
</tbody>
</table>



 

 

 





