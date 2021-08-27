---
title: Objetos ADSI do WinNT
description: O provedor WinNT ADSI implementa os seguintes objetos COM para dar suporte a recursos e serviços de várias interfaces ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- Objetos ADSI e ADSI do provedor de serviços WinNT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f3d2cb845e7fa6c754198abbb9a274987f69a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467383"
---
# <a name="adsi-objects-of-winnt"></a>Objetos ADSI do WinNT

O provedor WinNT ADSI implementa os seguintes objetos COM para dar suporte a recursos e serviços de várias interfaces ADSI.




| Objeto ADSI | Descrição | Interfaces com suporte | 
|-------------|-------------|----------------------|
| <strong>Classe</strong> | Um objeto ADSI que representa uma definição de classe. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>IADsClass</strong></a></dt></dl> | 
| <strong>Computador</strong> | Um objeto ADSI que representa um computador. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>Domínio</strong> | Um objeto ADSI que representa um domínio pela rede. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FileService</strong> | Um objeto ADSI que representa um serviço de arquivo. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FileShare</strong> | Um objeto ADSI que representa um compartilhamento de arquivo. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWFileService</strong> | Um objeto ADSI que representa um serviço de arquivo. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt></dl> | 
| <strong>FPNWFileShare</strong> | Um objeto ADSI que representa um compartilhamento de arquivo. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWResource</strong> | Um objeto ADSI que representa um recurso. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWResourcesCollection</strong> | Um objeto ADSI que representa uma coleção de recursos. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>FPNWSession</strong> | Um objeto ADSI que representa uma sessão. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWSessionsCollection</strong> | Um objeto ADSI que representa uma coleção de sessões. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>Grupo</strong> | Um objeto ADSI que representa um grupo. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl><blockquote>[!Note]<br />GetInfo não pode ser usado para grupos que contêm membros que são entidades de segurança wellKnown no escopo do WinNT.</blockquote><br /> | 
| <strong>Groupcollection</strong> | Um objeto ADSI que representa uma coleção de grupos. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt></dl> | 
| <strong>Localgroup</strong> | Um objeto ADSI que representa um grupo local. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>LocalgroupCollection</strong> | Um objeto ADSI que representa uma coleção de grupos locais. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt></dl> | 
| <strong>Namespace</strong> | Um objeto ADSI que representa o namespace do WinNT. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt></dl> | 
| <strong>PrintJob</strong> | Um objeto ADSI que representa um trabalho de impressão. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>PrintJobsCollection</strong> | Um objeto ADSI que representa uma coleção de trabalhos de impressão. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>PrintQueue</strong> | Um objeto ADSI que representa uma fila de impressão. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>Propriedade</strong> | Um objeto ADSI que representa uma definição de atributo. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>IADsProperty</strong></a></dt></dl> | 
| <strong>Recurso</strong> | Um objeto ADSI que representa um recurso. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>ResourcesCollection</strong> | Um objeto ADSI que representa uma coleção de recursos. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>Esquema</strong> | Um objeto ADSI que representa o contêiner de esquema. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt></dl> | 
| <strong>Serviço</strong> | Um objeto ADSI que representa um serviço. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>Sessão</strong> | Um objeto ADSI que representa uma sessão. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>SessionsCollection</strong> | Um objeto ADSI que representa uma coleção de sessões. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>Sintaxe</strong> | Um objeto ADSI que representa a sintaxe de um atributo. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>IADsSyntax</strong></a></dt></dl> | 
| <strong>Usuário</strong> | Um objeto ADSI que representa uma conta de usuário. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>UserGroupCollection</strong> | Um objeto ADSI que representa uma coleção de grupos de usuários. | <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a> | 




 

 

 





