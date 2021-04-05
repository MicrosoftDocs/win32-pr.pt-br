---
description: Active Directory fornece o banco de dados de conta que o centro de distribuição de chaves (KDC) usa para obter informações sobre entidades de segurança no domínio.
ms.assetid: 560ef22c-dd4f-49f8-9e15-a45dbf17df01
title: Banco de dados da conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0713d8f7b4336f43172fcd5cda18aa9d25c702fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921902"
---
# <a name="account-database"></a>Banco de dados da conta

Active Directory fornece o banco de dados de conta que o [*centro de distribuição de chaves*](/windows/desktop/SecGloss/k-gly) (KDC) usa para obter informações sobre [*entidades de segurança*](/windows/desktop/SecGloss/s-gly) no domínio. Cada entidade de segurança é representada por um objeto de conta no diretório. A chave de [*criptografia*](/windows/desktop/SecGloss/e-gly) usada na comunicação com um usuário, computador ou serviço é armazenada como um atributo do objeto de conta dessa entidade de segurança.

Somente os controladores de domínio são Active Directory servidores. Cada controlador de domínio mantém uma cópia gravável do diretório, de modo que as contas podem ser criadas, redefinição de senhas e Associação de grupo modificada em qualquer controlador de domínio. As alterações feitas em uma réplica do diretório são propagadas automaticamente para todas as outras réplicas. O Windows Replica o armazenamento de informações para o Active Directory usando um protocolo de replicação de vários mestres proprietário que usa uma conexão de chamada de procedimento remoto segura entre parceiros de replicação. A conexão usa o [*protocolo de autenticação Kerberos*](/windows/desktop/SecGloss/k-gly) para fornecer [*autenticação*](/windows/desktop/SecGloss/a-gly) e criptografia mútuas.

O armazenamento físico de dados de conta é gerenciado pelo [agente do sistema de diretório](/windows/desktop/AD/directory-system-agent), um processo protegido integrado à LSA (autoridade de [*segurança local*](/windows/desktop/SecGloss/l-gly) ) no controlador de domínio. Os clientes do serviço de diretório nunca recebem acesso direto ao armazenamento de dados. Qualquer cliente que queira acesso às informações de diretório deve se conectar ao agente do sistema de diretório e, em seguida, Pesquisar, ler e gravar objetos de diretório e seus atributos.

As solicitações para acessar um objeto ou atributo no diretório estão sujeitas à validação por mecanismos de controle de acesso do Windows. Como os objetos de arquivo e pasta no sistema de arquivos NTFS, os objetos no Active Directory são protegidos por [*listas de controle de acesso*](/windows/desktop/SecGloss/a-gly) (ACLs) que especificam quem pode acessar o objeto e de que maneira. Ao contrário de arquivos e pastas, no entanto, Active Directory objetos têm uma ACL para cada um de seus atributos. Portanto, os atributos para informações confidenciais da conta podem ser protegidos por permissões mais restritivas do que aquelas concedidas para outros atributos da conta.

A informação mais confidencial sobre uma conta é, naturalmente, sua senha. Embora o atributo de senha de um objeto de conta armazene uma chave de criptografia derivada de uma senha, não a senha propriamente dita, essa chave é tão útil para um invasor. Portanto, o acesso ao atributo de senha de um objeto de conta é concedido somente ao titular da conta, nunca a outras pessoas, nem mesmo aos administradores. Somente processos com privilégio de base de computação confiável — processos em execução no [*contexto*](/windows/desktop/SecGloss/c-gly) de segurança da LSA — têm permissão para ler ou alterar informações de senha.

Para impedir um ataque offline por alguém com acesso à fita de backup de um controlador de domínio, o atributo de senha de um objeto de conta é protegido por uma segunda criptografia usando uma chave do sistema. Essa chave de criptografia pode ser armazenada em mídia removível para que possa ser protegida separadamente, ou pode ser armazenada no controlador de domínio, mas protegido por um mecanismo disperso. Os administradores recebem a opção de escolher onde a chave do sistema está armazenada e quais dos vários algoritmos são usados para criptografar atributos de senha.

 

 
