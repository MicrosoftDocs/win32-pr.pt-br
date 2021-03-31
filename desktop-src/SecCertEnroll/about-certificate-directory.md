---
description: Uma PKI (infraestrutura de chave pública) do Windows salva certificados no servidor que hospeda a autoridade de certificação (CA) e no computador ou dispositivo local.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Certificar o diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172154"
---
# <a name="certificate-directory"></a>Certificar o diretório

Uma PKI (infraestrutura de chave pública) do Windows salva certificados no servidor que hospeda a autoridade de certificação (CA) e no computador ou dispositivo local. O armazenamento de CA é normalmente chamado de banco de dados de certificado, e o armazenamento local é conhecido como o repositório de certificados.

## <a name="certificate-database"></a>Banco de dados de certificados

Quando você adiciona os serviços de certificados em um servidor Windows e configura uma AC, um banco de dados de certificado é criado. Por padrão, o banco de dados está contido na pasta *% systemroot%* \\ System32 \\ Certlog e o nome é baseado no nome da autoridade de certificação com uma extensão. edb. O banco de dados pode conter:

-   Certificados emitidos
-   Certificados revogados
-   Chaves privadas arquivadas
-   Solicitações de certificado

Você não pode usar a API de registro de certificado para manipular o banco de dados. O processo de registro cria automaticamente as entradas necessárias.

## <a name="certificate-stores"></a>Repositórios de certificados

Os serviços de certificados da Microsoft copiam certificados emitidos e solicitações pendentes ou rejeitadas para computadores e dispositivos locais. O local de armazenamento é chamado de repositório de certificados e consiste nos repositórios lógicos a seguir.

| Repositório lógico                                         | Descrição                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Pessoal<br/>                                   | Contém certificados associados a uma chave privada controlada pelo usuário ou computador.<br/>                     |
| Autoridades de Certificação Confiáveis<br/>     | Contém certificados de CAs (autoridades de certificação) implicitamente confiáveis.<br/>                              |
| Confiabilidade Empresarial<br/>                           | Contém listas de certificados confiáveis normalmente usadas para confiar em certificados autoassinados de outras organizações.<br/> |
| Autoridades de Certificação Intermediárias<br/>     | Contém certificados emitidos para ACs subordinadas na hierarquia de certificação.<br/>                             |
| Objeto de Usuário do Active Directory<br/>               | Contém o certificado de objeto do usuário ou os certificados publicados no Active Directory.<br/>                         |
| Editores Confiáveis<br/>                         | Contém certificados de CAs confiáveis.<br/>                                                                     |
| Certificados Não Confiáveis<br/>                     | Contém certificados que foram identificados explicitamente como não confiáveis.<br/>                                    |
| Autoridades de Certificação Raiz de Terceiros<br/> | Contém certificados raiz confiáveis de CAs fora da hierarquia de certificados internos.<br/>                     |
| Pessoas de Confiança<br/>                             | Contém certificados emitidos para usuários ou entidades que foram explicitamente confiáveis.<br/>                        |
| Outras pessoas<br/>                               | Contém certificados emitidos para usuários ou entidades que foram implicitamente confiáveis.<br/>                        |
| Solicitações de registro de certificado<br/>            | Contém solicitações de certificado pendentes ou rejeitadas.<br/>                                                          |



 

Você não pode usar a API de registro de certificado para especificar ou recuperar propriedades de armazenamento ou copiar certificados para repositórios específicos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 




