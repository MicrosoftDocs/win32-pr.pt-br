---
title: Modelo de objeto ADSI para provedores LDAP
description: Uma ilustração que mostra objetos ADSI usados para o provedor LDAP e interfaces usadas para acessar esses objetos.
ms.assetid: 109fd42e-201e-4b84-a213-2695d81f005b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ee06c6bbcfc96a84cc3e7f679d7a13988a78b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915921"
---
# <a name="adsi-object-model-for-ldap-providers"></a>Modelo de objeto ADSI para provedores LDAP

A ilustração a seguir mostra os objetos ADSI usados para o provedor LDAP e as interfaces usadas para acessar esses objetos.

![modelo de objeto para o provedor LDAP](images/adsiobjmodldap-gif-1.png)

| Objeto                        | Interface                                                                                                                                                                                                                                                                                      |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Classe<br/>              | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                                                                                                                                                                                                                           |
| Propriedade<br/>           | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                                                                                                                                                                                                                                     |
| GenObject<br/>          | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops), [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) |
| Namespace<br/>          | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                                                                                                                                                                                     |
| RootDSE<br/>            | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                                                                                                                                                                                                                             |
| Nome<br/>           | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)                                                                                                                                                                                                                                     |
| Esquema<br/>             | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                                                                                                                                                                                                                                   |
| Syntax<br/>             | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                                                                                                                                                                                                                                         |
| Organização<br/>       | [**IADso**](/windows/desktop/api/Iads/nn-iads-iadso)                                                                                                                                                                                                                                                                         |
| OrganizationalUnit<br/> | [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                                                                                                                                                                                                                                                       |
| GroupCollection<br/>    | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Agrupar<br/>              | [**IADs**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                                                                                                                                                                                                                                                 |
| UserCollection<br/>     | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Usuário<br/>               | [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                                                                                                                                                                                                                                                   |
| Localidade<br/>           | [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                                                                                                                                                                                                                                                           |
| NameTranslate<br/>      | [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)                                                                                                                                                                                                                                                 |
| PrintQueue<br/>         | [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue), [ **IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)                                                                                                                                                                                         |



 

 

 





