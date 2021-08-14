---
description: A primeira função CryptoAPI chamada por um aplicativo que usa qualquer APIs criptográficas é a função CryptAcquireContext.
ms.assetid: ad1ff45c-7d02-431b-a287-e9db765476ce
title: Contextos do provedor de serviços criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ad2e77178ade8cc286dae1ff7334c89d33e46a63af227503f8e163f7d81cec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768628"
---
# <a name="cryptographic-service-provider-contexts"></a>Contextos do provedor de serviços criptográficos

A primeira [*função CryptoAPI*](../secgloss/c-gly.md) chamada por um aplicativo que usa qualquer APIs criptográficas é a [**função CryptAcquireContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) Essa função retorna um handle para um CSP específico que inclui a especificação de um contêiner [*de chave específico*](../secgloss/k-gly.md) dentro do CSP. Esse contêiner de chave é um contêiner de chave especificamente solicitado ou é o contêiner de chave padrão para o usuário conectado no momento.

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) também pode criar um novo contêiner de chave. Para obter mais informações, consulte Programa C de [exemplo: criando](example-c-program-creating-a-key-container-and-generating-keys.md) um contêiner de chave e gerando chaves e Programa C de [exemplo: usando CryptAcquireContext](example-c-program-using-cryptacquirecontext.md).

Um [*CSP (provedor de serviços de*](../secgloss/c-gly.md) criptografia) tem um nome e um tipo. Por exemplo, o nome de um dos CSPs atualmente fornecidos com o sistema operacional é [Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md). É um provedor [de tipo \_ PROV RSA \_ FULL.](prov-rsa-full.md) O nome de cada provedor é exclusivo; o tipo de provedor não é.

Quando um aplicativo chama [**CryptAcquireContext para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) obter um identificador CSP, ele especifica um tipo de provedor e, opcionalmente, um nome de provedor. Se um tipo e um nome são especificados, a função carrega o CSP com o tipo de provedor e o nome do provedor correspondentes. A função retorna o handle do CSP, que fornece acesso ao CSP e a um contêiner [*de chave*](../secgloss/k-gly.md) dentro do CSP.

Quando um aplicativo chama [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) e especifica um tipo de provedor, mas nenhum nome de provedor, a função procura um provedor nomeado, primeiro verificando uma lista de provedores nomeados padrão associados ao usuário conectado e, se isso falhar, em uma lista de provedores nomeados padrão associados ao computador. Depois que o nome do provedor for determinado, a função **CryptAcquireContext** pesquisa o CSP para esse provedor, carrega-o e retorna seu handle.

Quando terminar de usar um alça CSP, libere-o chamando a [**função CryptReleaseContext.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)

 

 
