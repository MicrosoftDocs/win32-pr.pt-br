---
title: APIs para trabalhar com descritores de segurança
description: APIs para trabalhar com descritores de segurança
ms.assetid: eb5ee183-949c-41f5-9f74-f9c418fdf0a2
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de descritores de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb798e036d5e30ba58a83499b92340bf30ee3cb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917151"
---
# <a name="apis-for-working-with-security-descriptors"></a>APIs para trabalhar com descritores de segurança

Cada objeto no Active Directory Domain Services tem um atributo **nTSecurityDescriptor** que contém o descritor de segurança do objeto. Há duas maneiras principais de ler e manipular um descritor de segurança de objeto de diretório:

-   Use o método [**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar o descritor de segurança como um objeto com ADSI com uma interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . As interfaces **IADsSecurityDescriptor**, [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) podem ser usadas para lidar com o descritor de segurança e seus componentes (ACLs, Aces e assim por diante). Para obter mais informações e um exemplo de código, consulte [usando IADs para obter um descritor de segurança](using-iads-to-get-a-security-descriptor.md).
-   Use o método [**IDirectoryObject:: Getobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) para recuperar um descritor de segurança de objeto como um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . Use esse ponteiro com uma função de controle de acesso do Win32, como [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) ou [**BuildSecurityDescriptor**](/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora). Para obter mais informações e um exemplo de código, consulte [usando IDirectoryObject para obter um descritor de segurança](using-idirectoryobject-to-get-a-security-descriptor.md).

A técnica recomendada, e a usada pela maioria dos exemplos de código neste guia, é usar as interfaces **IADs \*** porque elas simplificam a manipulação de descritores de segurança, ACLs e ACEs. Para os programadores de Visual Basic, as interfaces **IADs \*** são a maneira mais eficiente de lidar com descritores de segurança.

A técnica [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) é útil quando uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) é necessária. Por exemplo, o exemplo de código na [verificação de um direito de acesso de controle na ACL de um objeto](checking-a-control-access-right-in-an-objectampaposs-acl.md) usa esse método para recuperar um descritor de segurança a ser passado para a função [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) .

Para obter mais informações, consulte:

-   [Usando IADs para obter um descritor de segurança](using-iads-to-get-a-security-descriptor.md)
-   [Usando IDirectoryObject para obter um descritor de segurança](using-idirectoryobject-to-get-a-security-descriptor.md)
-   [Componentes do descritor de segurança](security-descriptor-components.md)
-   [Recuperando a DACL de um objeto](retrieving-an-objectampaposs-dacl.md)
-   [Recuperando a SACL de um objeto](retrieving-an-objectampaposs-sacl.md)
-   [Lendo o descritor de segurança de um objeto](reading-an-objectampaposs-security-descriptor.md)
-   [Exemplo de código para criar um descritor de segurança](example-code-for-creating-a-security-descriptor.md)
-   [Código de exemplo para enumerar a ACL de um objeto no Active Directory Domain Services](example-code-for-enumerating-the-acl-of-an-active-directory-object.md)

 

 