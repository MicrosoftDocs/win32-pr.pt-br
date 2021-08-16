---
title: Objetos ADSI implementados na camada do roteador
description: A tabela a seguir apresenta uma breve descrição dos objetos COM implementados no roteador ADSI.
ms.assetid: bd446e05-a15d-4354-9204-1df4e360497c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cc96eac8a2d680cb83622e01d94f8ef7a1d236726ab6b6fef9b2e6c5c40f50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692813"
---
# <a name="adsi-objects-implemented-in-the-router-layer"></a>Objetos ADSI implementados na camada do roteador

A tabela a seguir apresenta uma breve descrição dos objetos COM implementados no roteador ADSI.



| Objeto ADSI            | Descrição                                                         | Interfaces com suporte                                                                                                                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Accesscontrolentry** | Um objeto ADSI que representa uma ACE (entrada de controle de acesso).       | [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)                                                                                                                                                                                                                                  |
| **AccessControlList**  | Um objeto ADSI que representa uma ACL (lista de controle de acesso).        | [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                                                                                                                                                                                                                                    |
| **ADsNamespaces**      | Um objeto ADSI que representa o contêiner de vários namespaces. | <dl> <dt>[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)</dt> <dt>[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)</dt> <dt>[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)</dt> </dl> |
| **LargeInteger**       | Um objeto ADSI que representa um inteiro grande.                     | [**Iadslargeinteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                                                                                                                                                                                                                                              |
| **Propertyentry**      | Um objeto ADSI que representa uma entrada de propriedade.                    | [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                                                                                                                                                                                                                                            |
| **PropertyValue**      | Um objeto ADSI que representa um valor da propriedade.                    | [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                                                                                                                                                                                                                                            |
| **PropertyValue2**     | Um objeto ADSI que representa um valor da propriedade.                    | [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)                                                                                                                                                                                                                                          |
| **SecurityDescriptor** | Um objeto ADSI que representa um descritor de segurança.               | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                                                                                                                                                                                                                  |



 

 

 




