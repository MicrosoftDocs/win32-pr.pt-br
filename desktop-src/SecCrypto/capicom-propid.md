---
description: Define os identificadores de propriedade CAPICOM.
ms.assetid: faf10018-3ed8-4de6-9838-c553626f6dd7
title: CAPICOM_PROPID enumeração (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROPID
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 6d99c823d5396d2b8ece4484fa8888dff19b7898fb7d3b6ebedc5841b85c7e80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772262"
---
# <a name="capicom_propid-enumeration"></a>Enumeração CAPICOM \_ PROPID

A **enumeração CAPICOM \_ PROPID** define os identificadores de propriedade CAPICOM.

## <a name="members"></a>Membros



| Membro                                                 | DESCRIÇÃO                                                                                                                                                                                                                                                                                | Valor      |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ PROPID \_ UNKNOWN**                           | O tipo da propriedade não é conhecido.<br/>                                                                                                                                                                                                                                          | 0          |
| **CAPICOM \_ PROPID \_ KEY \_ PROV \_ HANDLE**                 | Um handle para um contêiner de chave dentro de um CSP [*(provedor de serviços de*](../secgloss/c-gly.md) criptografia).<br/>                                                                                        | 1          |
| **CAPICOM \_ PROPID \_ KEY \_ PROV \_ INFO**                   | Informações sobre um contêiner de chave em um CSP.<br/>                                                                                                                                                                                                                                 | 2          |
| **CAPICOM \_ PROPID \_ SHA1 \_ HASH**                        | Um objeto de hash SHA1.<br/>                                                                                                                                                                                                                                                             | 3          |
| **CAPICOM \_ PROPID \_ HASH \_ PROP**                        | As propriedades de um objeto hash.<br/>                                                                                                                                                                                                                                                | 3          |
| **CAPICOM \_ PROPID \_ MD5 \_ HASH**                         | Um objeto de hash MD5.<br/>                                                                                                                                                                                                                                                             | 4          |
| **CONTEXTO DE CHAVE \_ CAPICOM \_ \_ PROPID**                      | O contexto [*de chave*](../secgloss/c-gly.md).<br/>                                                                                                                                                                                                | 5          |
| **CAPICOM \_ PROPID \_ KEY \_ SPEC**                         | As especificações de uma chave.<br/>                                                                                                                                                                                                                                                   | 6          |
| **CAPICOM \_ PROPID \_ IE30 \_ RESERVED**                    | Informações sobre se o objeto está reservado no Internet Explorer 3.0.<br/>                                                                                                                                                                                                      | 7          |
| **CAPICOM \_ PROPID \_ PUBKEY \_ HASH \_ RESERVED**            | Informações sobre se o hash da chave pública está reservado.<br/>                                                                                                                                                                                                               | 8          |
| **CAPICOM \_ PROPID \_ ENHKEY \_ USAGE**                     | Um [*EKU (uso de chave) aprimorado.*](../secgloss/e-gly.md)<br/>                                                                                                                                                              | 9          |
| **CAPICOM \_ PROPID \_ CTL \_ USAGE**                        | Um [*uso de*](../secgloss/c-gly.md) CTL (lista de confiança de certificado).<br/>                                                                                                                                             | 9          |
| **CAPICOM \_ PROPID \_ NEXT \_ UPDATE \_ LOCATION**            | O local da próxima atualização para a CRL (lista [*de certificados revogados).*](../secgloss/c-gly.md)<br/>                                                                                               | 10         |
| **CAPICOM \_ PROPID \_ FRIENDLY \_ NAME**                    | Um nome acessível por humanos.<br/>                                                                                                                                                                                                                                                          | 11         |
| **ARQUIVO PVK CAPICOM \_ \_ \_ PROPID**                         | Um arquivo que contém uma chave privada.<br/>                                                                                                                                                                                                                                             | 12         |
| **CAPICOM \_ PROPID \_ DESCRIPTION**                       | Uma descrição acessível por humanos.<br/>                                                                                                                                                                                                                                                   | 13         |
| **ESTADO DE ACESSO \_ PROPID \_ DO CAPICOM \_**                     | O estado do acesso.<br/>                                                                                                                                                                                                                                                        | 14         |
| **CAPICOM \_ PROPID \_ SIGNATURE \_ HASH**                   | Um hash da assinatura.<br/>                                                                                                                                                                                                                                                        | 15         |
| **DADOS DE CARTÃO INTELIGENTE \_ CAPICOM \_ \_ \_ PROPID**                 | Dados de cartão inteligente.<br/>                                                                                                                                                                                                                                                                | 16         |
| **CAPICOM \_ PROPID \_ EFS**                               | Um [*Encrypting File System*](../secgloss/e-gly.md) (EFS).<br/>                                                                                                                                                  | 17         |
| **CAPICOM \_ PROPID \_ FORTEZZA \_ DATA**                    | Dados criados usando protocolos criptográficos e algoritmos pertencentes ao NIST (National [*Institute of Standards and Technology).*](../secgloss/n-gly.md)<br/> | 18         |
| **CAPICOM \_ PROPID \_ ARQUIVADO**                          | Informações sobre se o objeto está arquivado.<br/>                                                                                                                                                                                                                               | 19         |
| **IDENTIFICADOR DE \_ CHAVE CAPICOM PROPID \_ \_**                   | Um identificador de chave.<br/>                                                                                                                                                                                                                                                               | 20         |
| **REGISTRO AUTOMÁTICO DO CAPICOM \_ \_ \_ PROPID**                      | Informações de registro automático para um certificado.<br/>                                                                                                                                                                                                                                  | 21         |
| **CAPICOM \_ PROPID \_ PUBKEY \_ ALG \_ PARA**                 | Parâmetros para um algoritmo de chave pública.<br/>                                                                                                                                                                                                                                          | 22         |
| **CAPICOM \_ PROPID \_ CROSS \_ CERT \_ DIST \_ POINTS**         | Informações usadas para atualizar certificados cruzados dinâmicos.<br/>                                                                                                                                                                                                                          | 23         |
| **CAPICOM \_ PROPID \_ ISSUER \_ PUBLIC \_ KEY \_ MD5 \_ HASH**    | O hash MD5 da chave pública do emissor.<br/>                                                                                                                                                                                                                                        | 24         |
| **CAPICOM \_ PROPID \_ SUBJECT \_ PUBLIC \_ KEY \_ MD5 \_ HASH**   | O hash MD5 da chave pública do assunto.<br/>                                                                                                                                                                                                                                       | 25         |
| **REGISTRO DO CAPICOM \_ \_ PROPID**                        | Informações sobre o registro do certificado.<br/>                                                                                                                                                                                                                                 | 26         |
| **CAPICOM \_ PROPID \_ DATE \_ STAMP**                       | Um carimbo de data.<br/>                                                                                                                                                                                                                                                                   | 27         |
| **CAPICOM \_ PROPID \_ ISSUER \_ SERIAL \_ NUMBER \_ MD5 \_ HASH** | O hash MD5 do número de série do emissor.<br/>                                                                                                                                                                                                                                     | 28         |
| **CAPICOM \_ PROPID \_ SUBJECT \_ NAME \_ MD5 \_ HASH**          | O hash MD5 do nome do assunto.<br/>                                                                                                                                                                                                                                             | 29         |
| **INFORMAÇÕES DE ERRO ESTENDIDAS DO CAPICOM \_ \_ \_ \_ PROPID**             | Informações estendidas sobre um erro.<br/>                                                                                                                                                                                                                                            | 30         |
| **RENOVAÇÃO DO CAPICOM \_ \_ PROPID**                           | Informações sobre a renovação de uma autoridade [*de certificação*](../secgloss/c-gly.md).<br/>                                                                                                                     | 64         |
| **CAPICOM \_ PROPID \_ ARCHIVED \_ KEY \_ HASH**               | Um hash arquivado de uma chave.<br/>                                                                                                                                                                                                                                                      | 65         |
| **CAPICOM \_ PROPID \_ FIRST \_ RESERVED**                   | Informações sobre a primeira reserva.<br/>                                                                                                                                                                                                                                        | 66         |
| **CAPICOM \_ PROPID \_ ÚLTIMO \_ RESERVADO**                    | Informações sobre a reserva mais recente.<br/>                                                                                                                                                                                                                                  | 0x00007FFF |
| **CAPICOM \_ PROPID \_ FIRST \_ USER**                       | Informações sobre o primeiro usuário.<br/>                                                                                                                                                                                                                                               | 0x00008000 |
| **ÚLTIMO USUÁRIO DO CAPICOM \_ \_ \_ PROPID**                        | Informações sobre o usuário mais recente.<br/>                                                                                                                                                                                                                                         | 0x0000FFFF |



## <a name="remarks"></a>Comentários

Essa enumeração é usada pelas seguintes propriedades CAPICOM:

-   [**ExtendedProperty.PropID**](extendedproperty-propid.md)
-   [**ExtendedProperties.Remove**](extendedproperties-remove.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
