---
description: Para determinar se um descritor de segurança é auto-relativo ou absoluto, chame a função GetSecurityDescriptorControl e verifique o sinalizador ES SELF RELATIVE do parâmetro \_ \_ SECURITY \_ DESCRIPTOR \_ CONTROL.
ms.assetid: dab2844b-7df9-446c-aacf-380a0a805cbc
title: Descritores de segurança Self-Relative absolutos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a2639d1f17527b92116eabcaca96b637012253bbafc42198e37c9867fc585c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914718"
---
# <a name="absolute-and-self-relative-security-descriptors"></a>Descritores de segurança Self-Relative absolutos

Um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) pode estar no formato [*absoluto*](/windows/desktop/SecGloss/a-gly) ou [*auto-relativo.*](/windows/desktop/SecGloss/s-gly) Em formato absoluto, um descritor de segurança contém ponteiros para suas informações, não as informações em si. No formato auto-relativo, um descritor de segurança armazena uma estrutura [**SECURITY \_ DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e informações de segurança associadas em um bloco contíguo de memória. Para determinar se um descritor de segurança é auto-relativo ou absoluto, chame a função [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) e verifique o sinalizador ES SELF RELATIVE do parâmetro \_ \_ SECURITY [**\_ DESCRIPTOR \_ CONTROL.**](security-descriptor-control.md) Você pode usar as [**funções MakeSelfRelativeSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeselfrelativesd) e [**MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd) para converter entre esses dois formatos.

O formato absoluto é útil quando você está criando um descritor de segurança e tem ponteiros para todos os componentes, por exemplo, quando as configurações padrão para o proprietário, grupo e ACL discricionário estão disponíveis. Nesse caso, você pode chamar a função [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) para inicializar uma estrutura [**\_ SECURITY DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e, em seguida, chamar funções como [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) para atribuir ponteiros ACL e SID ao descritor de segurança.

No formato auto-relativo, um descritor de segurança sempre começa com uma estrutura [**SECURITY \_ DESCRIPTOR,**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) mas os outros componentes do descritor de segurança podem seguir a estrutura em qualquer ordem. Em vez de usar endereços de memória, os componentes do descritor de segurança são identificados por deslocamentos do início do descritor. Esse formato é útil quando um descritor de segurança deve ser armazenado em disco, transmitido por meio de um protocolo de comunicação ou copiado na memória.

Com [**exceção de MakeAbsoluteSD**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd), todas as funções que retornam um descritor de segurança fazem isso usando o formato auto-relativo. Os descritores de segurança passados como argumentos para uma função podem ser auto-relativos ou absolutos. Para obter mais informações, consulte a documentação da função.

 

 
