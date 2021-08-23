---
title: Modelo de objeto ADSI para provedores LDAP
description: Uma ilustração que mostra os objetos ADSI usados para o provedor LDAP e as interfaces usadas para acessar esses objetos.
ms.assetid: 109fd42e-201e-4b84-a213-2695d81f005b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c7c520793f6095bc9d4d9c6379f8ff6f09766f39ae6102f7e0a82d3a3de7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023784"
---
# <a name="adsi-object-model-for-ldap-providers"></a>Modelo de objeto ADSI para provedores LDAP

A ilustração a seguir mostra os objetos ADSI usados para o provedor LDAP e as interfaces usadas para acessar esses objetos.

![modelo de objeto para o provedor ldap](images/adsiobjmodldap-gif-1.png)

| Objeto                        | Interface                                                                                                                                                                                                                                                                                      |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Classe<br/>              | [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) [ **IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                                                                                                                                                                                                                           |
| Propriedade<br/>           | [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) [ **IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                                                                                                                                                                                                                                     |
| GenObject<br/>          | [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) [**IADsContainer,**](/windows/desktop/api/Iads/nn-iads-iadscontainer) [**IADsDeleteOps,**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) [**IADsObjectOptions,**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) [**IADsPropertyList,**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) [**IDirectoryObject,**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) |
| Namespace<br/>          | [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) [**IADsContainer,**](/windows/desktop/api/Iads/nn-iads-iadscontainer) [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                                                                                                                                                                                     |
| Rootdse<br/>            | [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) [ **IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                                                                                                                                                                                                                             |
| Caminho<br/>           | [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) [ **IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)                                                                                                                                                                                                                                     |
| Esquema<br/>             | [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) [ **IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                                                                                                                                                                                                                                   |
| Syntax<br/>             | [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) [ **IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                                                                                                                                                                                                                                         |
| Organização<br/>       | [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)                                                                                                                                                                                                                                                                         |
| OrganizationalUnit<br/> | [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                                                                                                                                                                                                                                                       |
| Groupcollection<br/>    | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Agrupar<br/>              | [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                                                                                                                                                                                                                                                 |
| Usercollection<br/>     | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Usuário<br/>               | [**Iadsuser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                                                                                                                                                                                                                                                   |
| Localidade<br/>           | [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                                                                                                                                                                                                                                                           |
| NameTranslate<br/>      | [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)                                                                                                                                                                                                                                                 |
| PrintQueue<br/>         | [**IADsPrintQueue,**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) [ **IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)                                                                                                                                                                                         |



 

 

 





