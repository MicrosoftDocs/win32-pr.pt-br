---
description: O controle de registro de certificado pode ser usado por um aplicativo que deve solicitar que um certificado seja emitido para um assunto nomeado.
ms.assetid: ce6661b0-7ed2-452f-a54c-6705d14f3298
title: Controle de registro de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e417a9db7984cbb58b7c2e3b51d828b6d61a97b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753228"
---
# <a name="certificate-enrollment-control"></a>Controle de registro de certificado

O controle de registro de certificado pode ser usado por um aplicativo que deve solicitar que um certificado seja emitido para um assunto nomeado. Ele foi projetado para aceitar dados na forma de uma cadeia de caracteres binária (BSTR). Os dados podem vir de uma página da Web ou da interface do usuário do Visual Basic ou Visual C++ sistema de desenvolvimento. A saída do controle de registro de certificado é uma \# solicitação de certificado PKCS 10 que pode ser enviada para uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA).

![controle de registro de certificado](images/xen-arch.png)

As informações necessárias sobre o usuário, a entidade do certificado, são coletadas pela interface do usuário. Essas informações são fornecidas como uma entrada BSTR para o controle de registro de certificado. O controle de registro de certificado gera a chave de assinatura apropriada, chave de troca de chave ou ambos os pares de chaves. Em seguida, o controle gera e assina \# uma [*solicitação de certificado*](../secgloss/c-gly.md) PKCS 10 usando a [*chave privada*](../secgloss/p-gly.md)gerada. Em seguida, o controle de registro de certificado vincula o par de chaves a um certificado fictício temporário que é armazenado no repositório de solicitações até que o certificado emitido seja retornado de uma autoridade de certificação. Por fim, o aplicativo envia a \# solicitação de certificado PKCS 10 para uma CA.

Se a autoridade de certificação aprovar a solicitação de certificado, a autoridade de certificação criará um certificado contendo a chave pública. A CA também assina e retorna o certificado.

Quando o certificado solicitado é retornado da autoridade de certificação, o aplicativo passa a \# mensagem PKCS 7 de volta para o controle de registro de certificado em que o certificado ou a cadeia de certificados é extraída da \# mensagem PKCS 7. O certificado e quaisquer outros certificados na cadeia de confiança são armazenados em um [*repositório de certificados*](../secgloss/c-gly.md). O certificado retornado não é modificado de forma alguma. Qualquer aplicativo com reconhecimento de certificado agora pode acessar esse certificado do repositório.

O controle de registro de cartão inteligente é usado por um administrador para se registrar em nome de usuários de cartão inteligente. O processo de registro resulta em um certificado emitido que é armazenado no cartão inteligente de um usuário.

O controle de registro de cartão inteligente está contido em Scrdenrl.dll e consiste em um objeto, **SCrdEnr**. Nenhum outro objeto está incluído no Scrdenrl.dll. Esse objeto de registro de cartão inteligente pode ser usado com uma linguagem de script, como Visual Basic Scripting Edition (VBScript).

Um [*leitor de cartão inteligente*](../secgloss/r-gly.md) deve ser instalado no computador que executa o controle de registro de cartão inteligente.

Além disso, o emissor do cartão inteligente deve ter obtido um certificado de autenticação baseado no modelo de certificado "EnrollmentAgent". Esse certificado de autenticação será usado para assinar a solicitação de certificado gerada em nome do destinatário do cartão inteligente. Por padrão, os administradores de domínio recebem permissão para solicitar um certificado com base no modelo "agente de registro". Outro usuário pode receber permissão para se registrar para um certificado "EnrollmentAgent" (por meio do snap-in Active Directory sites e serviços do MMC); isso, no entanto, permite que esse usuário emita por conta própria um cartão inteligente com privilégios de administrador de domínio.

 

 
