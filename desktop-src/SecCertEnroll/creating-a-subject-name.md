---
description: Você pode usar a interface IX500DistinguishedName para criar um nome de entidade a partir de uma cadeia de caracteres de nome distinto.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Criando um nome de entidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe512be48c9a727857c4fac4abc6e04a705b7f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501337"
---
# <a name="creating-a-subject-name"></a>Criando um nome de entidade

Você pode usar a interface [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) para criar um nome de entidade a partir de uma cadeia de caracteres de nome distinto. A cadeia de caracteres consiste em nomes distintos relativos (RDNs) concatenados. As seguintes chaves RDN são suportadas pela API de registro de certificado.

| Chave                               | OID                                             | Descrição                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| C<br/>                      | \_nome do \_ país do OID do XCN \_<br/>              | Contém um código de país ou região ISO 3166 de duas letras.<br/>                                  |
| CN<br/>                     | \_ \_ nome comum do OID XCN \_<br/>               | Contém um nome comum.<br/>                                                                 |
| E<br/> Email<br/>     | XCN \_ OID \_ RSA \_ emailAddr<br/>             | Contém um endereço de email.<br/>                                                              |
| DC<br/>                     | componente de domínio do XCN \_ OID \_ \_<br/>          | Contém uma parte de um nome DNS (sistema de nomes de domínio).<br/>                                   |
| G<br/> GivenName<br/> | \_nome do OID XCN \_ fornecido \_<br/>                | Contém a parte do nome de uma pessoa que não é um sobrenome.<br/>                             |
| I<br/>                      | \_iniciais do OID do XCN \_<br/>                   | Contém as iniciais de uma pessoa.<br/>                                                           |
| L<br/>                      | \_nome de \_ localidade do OID XCN \_<br/>             | Contém o nome de localidade que identifica uma cidade, país ou outra região geográfica.<br/> |
| O<br/>                      | \_nome da \_ organização do OID XCN \_<br/>         | Contém o nome de uma organização.<br/>                                                   |
| OU<br/>                     | \_nome da \_ \_ unidade organizacional XCN OID \_<br/> | Contém o nome de uma subdivisão de unidade em uma organização.<br/>                         |
| S<br/> ST<br/>        | \_ \_ \_ \_ nome ou província \_ do XCN OID<br/>  | Contém o nome completo de um Estado ou província.<br/>                                          |
| RUA<br/>                 | \_endereço do OID do XCN \_ \_<br/>            | Contém o endereço físico.<br/>                                                          |
| SN<br/>                     | \_nome do \_ sur do OID do XCN \_<br/>                  | Contém o nome da família de uma pessoa.<br/>                                                   |
| T<br/> TITLE<br/>     | \_título do OID XCN \_<br/>                      | Contém o título de uma pessoa na organização.<br/>                                     |



 

Ao inicializar um objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , você pode identificar o formato do nome distinto especificando um valor do tipo de enumeração [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) . Por exemplo, suponha que o nome distinto da entidade consiste no seguinte RDNs:<dl> CN = administrador  
CN = usuários  
DC = jdomcsc  
DC = nttest  
DC = Microsoft  
DC = com  
</dl>

Se você concatenar esses RDNs na cadeia de caracteres de nome distinto delimitada por vírgulas a seguir, poderá especificar o valor do **\_ \_ \_ \_ \_ sinalizador de vírgula Str de nome de certificado XCN** ao inicializar um objeto [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) .

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificando um nome de entidade](encoding-a-subject-name.md)
</dt> <dt>

[Nomes de Entidades](subject-names.md)
</dt> </dl>

 

 




