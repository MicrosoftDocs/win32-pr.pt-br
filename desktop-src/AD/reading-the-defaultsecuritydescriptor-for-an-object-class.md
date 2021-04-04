---
title: Lendo o defaultSecurityDescriptor para uma classe de objeto
description: Usando o ADSI, você pode obter o atributo defaultSecurityDescriptor para uma classe de objeto com a interface IADs.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, lendo o defaultSecurityDescriptor para uma classe de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e217ae42214c2c07867c2a57427d74fb7636736
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007296"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a>Lendo o defaultSecurityDescriptor para uma classe de objeto

Usando o ADSI, você pode obter o atributo **defaultSecurityDescriptor** para uma classe de objeto com a interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) . Para obter o atributo **defaultSecurityDescriptor** para uma classe de objeto, execute as etapas a seguir.

1.  Obtenha um ponteiro de interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) para o objeto **classSchema** da classe Object.
2.  Use o método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para obter o descritor de segurança padrão do objeto. O nome da propriedade que contém o descritor de segurança é "defaultSecurityDescriptor". A propriedade será retornada como uma [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) que contém um BSTR com o descritor de segurança padrão no formato de cadeia de caracteres SDDL.
3.  Use a função [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para converter o formulário de cadeia de caracteres SDDL em um descritor de segurança.
4.  Use as APIs de segurança [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)e [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) para ler as partes do descritor de segurança.

Para obter um exemplo de código que demonstra como fazer isso, consulte [exemplo de código para ler defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).

 

 