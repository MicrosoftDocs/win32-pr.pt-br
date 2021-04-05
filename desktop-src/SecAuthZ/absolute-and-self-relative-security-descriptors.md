---
description: Para determinar se um descritor de segurança é auto-relativo ou absoluto, chame a função GetSecurityDescriptorControl e verifique o \_ sinalizador se \_ relativo individual do parâmetro de \_ controle do descritor de segurança \_ .
ms.assetid: dab2844b-7df9-446c-aacf-380a0a805cbc
title: Descritores de segurança absolutos e Self-Relative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57406e194a31e79594394913055609e2981e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921944"
---
# <a name="absolute-and-self-relative-security-descriptors"></a>Descritores de segurança absolutos e Self-Relative

Um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) pode estar em um formato [*absoluto*](/windows/desktop/SecGloss/a-gly) ou [*autônomo*](/windows/desktop/SecGloss/s-gly) . No formato absoluto, um descritor de segurança contém ponteiros para suas informações, não as informações em si. No formato auto-relativo, um descritor de segurança armazena uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e informações de segurança associadas em um bloco contíguo de memória. Para determinar se um descritor de segurança é auto-relativo ou absoluto, chame a função [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) e verifique o \_ sinalizador se \_ relativo individual do parâmetro [**de \_ \_ controle do descritor de segurança**](security-descriptor-control.md) . Você pode usar as funções [**makeselfrelativesd devia**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeselfrelativesd) e [**makeabsolutesd devia**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd) para converter entre esses dois formatos.

O formato absoluto é útil quando você está criando um descritor de segurança e tem ponteiros para todos os componentes, por exemplo, quando as configurações padrão para o proprietário, o grupo e a ACL discricionária estão disponíveis. Nesse caso, você pode chamar a função [**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor) para inicializar uma estrutura [**de \_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e, em seguida, chamar funções como [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) para atribuir ACLs e ponteiros de Sid ao descritor de segurança.

Em formato auto-relativo, um descritor de segurança sempre começa com uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) , mas os outros componentes do descritor de segurança podem seguir a estrutura em qualquer ordem. Em vez de usar endereços de memória, os componentes do descritor de segurança são identificados por deslocamentos do início do descritor. Esse formato é útil quando um descritor de segurança deve ser armazenado em disco, transmitido por meio de um protocolo de comunicação ou copiado na memória.

Exceto para [**makeabsolutesd devia**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd), todas as funções que retornam um descritor de segurança fazem isso usando o formato auto-relativo. Os descritores de segurança passados como argumentos para uma função podem ser formados automaticamente ou absolutos. Para obter mais informações, consulte a documentação da função.

 

 
