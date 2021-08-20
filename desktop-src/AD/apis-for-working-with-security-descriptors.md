---
title: APIs para trabalhar com descritores de segurança
description: APIs para trabalhar com descritores de segurança
ms.assetid: eb5ee183-949c-41f5-9f74-f9c418fdf0a2
ms.tgt_platform: multiple
keywords:
- AD de descritores de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78988a2c435f397f0030ebaaef4e6d06385e710bc3671995338052c220f852
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024568"
---
# <a name="apis-for-working-with-security-descriptors"></a>APIs para trabalhar com descritores de segurança

Cada objeto no Active Directory Domain Services tem um atributo **nTSecurityDescriptor** que contém o descritor de segurança do objeto. Há duas maneiras principais de ler e manipular um descritor de segurança de objeto de diretório:

-   Use o [**método IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar o descritor de segurança como um objeto COM ADSI com uma interface [**IADsSecurityDescriptor.**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) As interfaces **IADsSecurityDescriptor,** [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) podem ser usadas para lidar com o descritor de segurança e seus componentes (ACLs, ACEs e assim por diante). Para obter mais informações e um exemplo de código, consulte [Usando IADs para obter um descritor de segurança](using-iads-to-get-a-security-descriptor.md).
-   Use o [**método IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) para recuperar um descritor de segurança de objeto como um ponteiro para uma estrutura [**SECURITY \_ DESCRIPTOR.**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) Use esse ponteiro com uma função de controle de acesso Win32, como [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) ou [**BuildSecurityDescriptor**](/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora). Para obter mais informações e um exemplo de código, consulte [Using IDirectoryObject to Get a Security Descriptor](using-idirectoryobject-to-get-a-security-descriptor.md).

A técnica recomendada e a usada pela maioria dos exemplos de código neste guia é usar as interfaces IADs _ porque simplificam o tratamento de descritores de **\* *segurança, ACLs e ACEs. Para Visual Basic programadores, as interfaces* \* _ IADs** são a maneira mais eficiente de lidar com descritores de segurança.

A [**técnica IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) é útil quando uma [**estrutura SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) é necessária. Por exemplo, o exemplo de código em Verificando um direito de acesso de controle na [ACL](checking-a-control-access-right-in-an-objectampaposs-acl.md) de um objeto usa esse método para recuperar um descritor de segurança para passar para a [**função AccessCheckByTypeResultList.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist)

Para obter mais informações, consulte:

-   [Usando IADs para obter um descritor de segurança](using-iads-to-get-a-security-descriptor.md)
-   [Usando IDirectoryObject para obter um descritor de segurança](using-idirectoryobject-to-get-a-security-descriptor.md)
-   [Componentes do descritor de segurança](security-descriptor-components.md)
-   [Recuperando DACL de um objeto](retrieving-an-objectampaposs-dacl.md)
-   [Recuperando a SACL de um objeto](retrieving-an-objectampaposs-sacl.md)
-   [Lendo o descritor de segurança de um objeto](reading-an-objectampaposs-security-descriptor.md)
-   [Código de exemplo para criar um descritor de segurança](example-code-for-creating-a-security-descriptor.md)
-   [Código de exemplo para enumerar a ACL de um objeto em Active Directory Domain Services](example-code-for-enumerating-the-acl-of-an-active-directory-object.md)

 

 