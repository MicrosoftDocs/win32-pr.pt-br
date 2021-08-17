---
description: O Active Directory fornece o banco de dados de conta que centro de distribuição de chaves (KDC) usa para obter informações sobre entidades de segurança no domínio.
ms.assetid: 560ef22c-dd4f-49f8-9e15-a45dbf17df01
title: Banco de dados de conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4d5e41c959a8c546ef36a5e4014b14ffc949e1670e2b32b199a8c9368bfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141589"
---
# <a name="account-database"></a>Banco de dados de conta

O Active Directory fornece o banco de dados de conta [*que centro de distribuição de chaves*](/windows/desktop/SecGloss/k-gly) (KDC) usa para obter informações sobre [*entidades de segurança*](/windows/desktop/SecGloss/s-gly) no domínio. Cada entidade de entidade é representada por um objeto de conta no diretório . A [*chave*](/windows/desktop/SecGloss/e-gly) de criptografia usada na comunicação com um usuário, computador ou serviço é armazenada como um atributo do objeto de conta dessa entidade de segurança.

Somente controladores de domínio são servidores do Active Directory. Cada controlador de domínio mantém uma cópia que pode ser escrita do diretório para que as contas possam ser criadas, redefinição de senhas e associação de grupo modificada em qualquer controlador de domínio. As alterações feitas em uma réplica do diretório são propagadas automaticamente para todas as outras réplicas. Windows replica o armazenamento de informações para o Active Directory usando um protocolo proprietário de replicação de vários mestres que usa uma conexão de chamada de procedimento remoto segura entre parceiros de replicação. A conexão usa o protocolo [*de autenticação Kerberos*](/windows/desktop/SecGloss/k-gly) para fornecer [*autenticação mútua e*](/windows/desktop/SecGloss/a-gly) criptografia.

O armazenamento físico de dados da conta é gerenciado pelo Agente do Sistema de [Diretório,](/windows/desktop/AD/directory-system-agent)um processo protegido integrado à LSA (Autoridade de Segurança [*Local)*](/windows/desktop/SecGloss/l-gly) no controlador de domínio. Os clientes do serviço de diretório nunca têm acesso direto ao armazenamento de dados. Qualquer cliente que queira acesso às informações de diretório deve se conectar ao Agente do Sistema de Diretório e, em seguida, pesquisar, ler e gravar objetos de diretório e seus atributos.

As solicitações para acessar um objeto ou atributo no diretório estão sujeitas à validação Windows de controle de acesso. Como objetos de arquivo e pasta no sistema de arquivos NTFS, os objetos no Active Directory são protegidos por ACLs [*(listas*](/windows/desktop/SecGloss/a-gly) de controle de acesso) que especificam quem pode acessar o objeto e de que maneira. Ao contrário de arquivos e pastas, no entanto, os objetos do Active Directory têm uma ACL para cada um de seus atributos. Portanto, os atributos para informações confidenciais da conta podem ser protegidos por permissões mais restritivas do que aquelas concedidas para outros atributos da conta.

As informações mais confidenciais sobre uma conta são, obviamente, sua senha. Embora o atributo de senha de um objeto de conta armazene uma chave de criptografia derivada de uma senha, não a senha em si, essa chave é tão útil para um invasor. Portanto, o acesso ao atributo de senha de um objeto de conta é concedido somente ao titular da conta, nunca a ninguém, nem mesmo aos administradores. Somente processos com privilégio base de computação [](/windows/desktop/SecGloss/c-gly) confiável – processos em execução no contexto de segurança do LSA – têm permissão para ler ou alterar informações de senha.

Para impedir um ataque offline por alguém com acesso à fita de backup de um controlador de domínio, o atributo de senha de um objeto de conta é protegido por uma segunda criptografia usando uma chave do sistema. Essa chave de criptografia pode ser armazenada em mídia removível para que ela possa ser protegida separadamente ou pode ser armazenada no controlador de domínio, mas protegida por um mecanismo disperso. Os administradores têm a opção de escolher onde a chave do sistema está armazenada e qual dos vários algoritmos é usado para criptografar atributos de senha.

 

 
