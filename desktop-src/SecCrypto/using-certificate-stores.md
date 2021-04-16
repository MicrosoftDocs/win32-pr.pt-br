---
description: O capicot usa certificados digitais para criar assinaturas, criptografar chaves de criptografia de sessão ao criar mensagens envelopadas e descriptografar chaves de sessão criptografadas quando uma mensagem envelopada é recebida.
ms.assetid: 018fc41a-19fd-4e4c-bfed-e0215afb5150
title: Usando repositórios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682068ba8f2f88d0fedabeef7ccee676f092e52e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750739"
---
# <a name="using-certificate-stores"></a>Usando repositórios de certificados

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

O capicot usa [*certificados digitais*](../secgloss/d-gly.md) para criar assinaturas, criptografar chaves de criptografia de sessão ao criar mensagens envelopadas e descriptografar chaves de sessão criptografadas quando uma mensagem envelopada é recebida. Por padrão, o capicot usa certificados no meu repositório que têm uma chave privada associada para a criação de [*assinaturas digitais*](../secgloss/d-gly.md) e a descriptografia de chave de sessão. Na maioria dos casos, um aplicativo nunca precisaria abrir ou, de outra forma, lidar diretamente com um repositório de certificados.

No entanto, os aplicativos que criam mensagens envelopadas usam a [*chave pública*](../secgloss/p-gly.md) de cada destinatário pretendido de uma mensagem envelopada. Essas chaves são recuperadas dos certificados dos destinatários pretendidos. Portanto, para criar mensagens envelopadas para um grupo de destinatários pretendidos, os certificados desses destinatários seriam coletados em um repositório de certificados.

A tabela a seguir lista os repositórios de certificados padrão normalmente persistidos em uma estação de usuário.



| Repositório        | Descrição                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Meu           | Contém certificados pessoais. Esses certificados geralmente terão uma chave privada associada.                                                                                                                                                                                                                                                                             |
| Outras pessoas | Contém os certificados daqueles para os quais o usuário normalmente envia mensagens envelopadas ou recebe mensagens assinadas do.                                                                                                                                                                                                                                                     |
| CA e raiz  | Contém os [*certificados*](../secgloss/r-gly.md) de autoridades de certificação que o usuário confia para emitir certificados para outras pessoas. Os certificados nesses armazenamentos normalmente são fornecidos com o sistema operacional ou o administrador de rede do usuário. Os certificados no repositório raiz normalmente são autoassinados. |



 

\_ \_ Os armazenamentos de usuário atuais do CAPICOM podem ser criados, abertos e persistidos fornecendo um nome de repositório diferente como uma cadeia de caracteres. Se um repositório com esse nome não existir, um repositório vazio será criado e aberto. Se houver uma loja, ela será aberta e todos os certificados atualmente no armazenamento serão disponibilizados.

As seções a seguir mostram exemplos de tarefas de repositório de certificados:

-   [Abrir o armazenamento de Active Directory e recuperar certificados](opening-the-active-directory-store-and-retrieving-certificates.md)
-   [Adicionando certificados a um repositório de certificados](adding-certificates-to-a-certificate-store.md)
-   [Usando lojas em locais diferentes](using-stores-in-different-locations.md)
-   [Coletando e verificando certificados](collecting-and-verifying-certificates.md)

 

 
