---
title: Lendo o defaultSecurityDescriptor para uma classe de objeto
description: Usando ADSI, você pode obter o atributo defaultSecurityDescriptor para uma classe de objeto com a interface IADs.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Exemplos do Active Directory do Active Directory , lendo o defaultSecurityDescriptor para uma classe de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26204ebe31155363a1be8bf30bd1c0495d16a939b58789f421a0772d6d90a9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184687"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a>Lendo o defaultSecurityDescriptor para uma classe de objeto

Usando ADSI, você pode obter o **atributo defaultSecurityDescriptor** para uma classe de objeto com a interface [**IADs.**](/windows/desktop/api/iads/nn-iads-iads) Para obter o **atributo defaultSecurityDescriptor para** uma classe de objeto, execute as etapas a seguir.

1.  Obter um ponteiro de interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) para o **objeto classSchema** para a classe de objeto.
2.  Use o [**método IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) para obter o descritor de segurança padrão do objeto . O nome da propriedade que contém o descritor de segurança é "defaultSecurityDescriptor". A propriedade será retornada como [**uma VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) que contém um BSTR com o descritor de segurança padrão no formato de cadeia de caracteres SDDL.
3.  Use a [**função ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para converter o formulário de cadeia de caracteres SDDL em um descritor de segurança.
4.  Use as APIs de Segurança [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl,**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)e [**GetSecurityDescriptorControl para**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) ler as partes do descritor de segurança.

Para ver um exemplo de código que demonstra como fazer isso, consulte [Código de exemplo para leitura defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).

 

 