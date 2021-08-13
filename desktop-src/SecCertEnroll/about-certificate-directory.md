---
description: Uma Windows PKI (infraestrutura de chave pública) salva certificados no servidor que hospeda a AC (autoridade de certificação) e no computador ou dispositivo local.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Certificar o diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b77a7c63e234460394005aac416d41ff7845470139ba2cb8b700132bea0118c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904825"
---
# <a name="certificate-directory"></a>Certificar o diretório

Uma Windows PKI (infraestrutura de chave pública) salva certificados no servidor que hospeda a AC (autoridade de certificação) e no computador ou dispositivo local. O armazenamento de AC normalmente é chamado de banco de dados de certificado e o armazenamento local é conhecido como o armazenamento de certificados.

## <a name="certificate-database"></a>Banco de dados de certificado

Quando você adiciona Serviços de Certificados em um Windows e configura uma AC, um banco de dados de certificado é criado. Por padrão, o banco de dados está contido na pasta *%SystemRoot%* System32 Certlog e o nome é baseado no nome da AC com uma \\ \\ extensão .edb. O banco de dados pode conter:

-   Certificados emitidos
-   Certificados revogados
-   Chaves privadas arquivadas
-   Solicitações de certificado

Você não pode usar a API de Registro de Certificado para manipular o banco de dados. O processo de registro cria automaticamente as entradas necessárias.

## <a name="certificate-stores"></a>Repositórios de certificados

Os Serviços de Certificados da Microsoft copiam certificados emitidos e solicitações pendentes ou rejeitadas para computadores e dispositivos locais. O local de armazenamento é chamado de armazenamento de certificados e consiste nos seguintes armazenamentos lógicos.

| Armazenamento lógico                                         | Descrição                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Pessoal<br/>                                   | Contém certificados associados a uma chave privada controlada pelo usuário ou computador.<br/>                     |
| Autoridades de Certificação Confiáveis<br/>     | Contém certificados de CAs (autoridades de certificação) implicitamente confiáveis.<br/>                              |
| Confiabilidade Empresarial<br/>                           | Contém listas de confiança de certificado normalmente usadas para confiar em certificados auto-assinados de outras organizações.<br/> |
| Autoridades de Certificação Intermediárias<br/>     | Contém certificados emitidos para ACs subordinadas na hierarquia de certificação.<br/>                             |
| Objeto de Usuário do Active Directory<br/>               | Contém o certificado de objeto de usuário ou certificados publicados no Active Directory.<br/>                         |
| Editores Confiáveis<br/>                         | Contém certificados de CAs confiáveis.<br/>                                                                     |
| Certificados Não Confiáveis<br/>                     | Contém certificados que foram explicitamente identificados como nãotrusados.<br/>                                    |
| Autoridades de Certificação Raiz de Terceiros<br/> | Contém certificados raiz confiáveis de CAs fora da hierarquia de certificado interna.<br/>                     |
| Pessoas de Confiança<br/>                             | Contém certificados emitidos para usuários ou entidades que foram explicitamente confiáveis.<br/>                        |
| Outras pessoas<br/>                               | Contém certificados emitidos para usuários ou entidades que foram implicitamente confiáveis.<br/>                        |
| Solicitações de registro de certificado<br/>            | Contém solicitações de certificado pendentes ou rejeitadas.<br/>                                                          |



 

Você não pode usar a API de Registro de Certificado para especificar ou recuperar propriedades do armazenamento ou copiar certificados para armazenamentos específicos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 




