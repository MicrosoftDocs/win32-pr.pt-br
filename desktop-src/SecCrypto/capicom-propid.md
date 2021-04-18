---
description: Define os identificadores de propriedade CAPICOM.
ms.assetid: faf10018-3ed8-4de6-9838-c553626f6dd7
title: Enumeração de CAPICOM_PROPID (CAPICOM. h)
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
ms.openlocfilehash: d817262b869ef694c2cf9ff5b1e577840c3168a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750759"
---
# <a name="capicom_propid-enumeration"></a>Enumeração de Propid CAPICOM \_

A **enumeração \_ Propid capicor** define os identificadores de propriedade CAPICOM.

## <a name="members"></a>Membros



| Membro                                                 | DESCRIÇÃO                                                                                                                                                                                                                                                                                | Valor      |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **capico de \_ Propid \_ desconhecido**                           | O tipo da propriedade não é conhecido.<br/>                                                                                                                                                                                                                                          | 0          |
| **\_identificador de \_ Prov de chave Propid \_ de CAPICOM \_**                 | Um identificador para um contêiner de chave em um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).<br/>                                                                                        | 1          |
| **\_informações de \_ Prov de chave Propid \_ de CAPICOM \_**                   | Informações sobre um contêiner de chave em um CSP.<br/>                                                                                                                                                                                                                                 | 2          |
| **\_ \_ Hash SHA1 de CAPICOM Propid \_**                        | Um objeto hash SHA1.<br/>                                                                                                                                                                                                                                                             | 3          |
| **PROP. de \_ hash Propid de CApicom \_ \_**                        | As propriedades de um objeto de hash.<br/>                                                                                                                                                                                                                                                | 3          |
| **\_ \_ Hash MD5 de CAPICOM de Propid \_**                         | Um objeto hash MD5.<br/>                                                                                                                                                                                                                                                             | 4          |
| **\_contexto de \_ chave de Propid de CAPICOM \_**                      | O [*contexto*](../secgloss/c-gly.md)de chave.<br/>                                                                                                                                                                                                | 5          |
| **\_especificação de \_ chave de Propid de CAPICOM \_**                         | As especificações de uma chave.<br/>                                                                                                                                                                                                                                                   | 6          |
| **Capicor \_ Propid \_ IE30 \_ reservado**                    | Informações sobre se o objeto está reservado no Internet Explorer 3,0.<br/>                                                                                                                                                                                                      | 7          |
| **HASH de capicot \_ Propid \_ PUBKEY \_ \_ reservado**            | Informações sobre se o hash da chave pública está reservado.<br/>                                                                                                                                                                                                               | 8          |
| **uso de CAPICOM de \_ utilização de Propid \_ \_**                     | Um EKU ( [*uso avançado de chave*](../secgloss/e-gly.md) ).<br/>                                                                                                                                                              | 9          |
| **uso da CTL de CAPICOM \_ Propid \_ \_**                        | Um uso de CTL ( [*lista de certificados confiáveis*](../secgloss/c-gly.md) ).<br/>                                                                                                                                             | 9          |
| **\_ \_ próximo local de \_ atualização \_ do CAPICOM propid**            | O local da próxima atualização para a CRL ( [*lista de certificados revogados*](../secgloss/c-gly.md) ).<br/>                                                                                               | 10         |
| **\_ \_ nome amigável do CAPICOM de Propid \_**                    | Um nome legível.<br/>                                                                                                                                                                                                                                                          | 11         |
| **arquivo do capico de \_ Propid \_ PVK \_**                         | Um arquivo que contém uma chave privada.<br/>                                                                                                                                                                                                                                             | 12         |
| **Descrição do CAPICOM \_ Propid \_**                       | Uma descrição legível.<br/>                                                                                                                                                                                                                                                   | 13         |
| **Estado de acesso do CAPICOM \_ Propid \_ \_**                     | O estado do acesso.<br/>                                                                                                                                                                                                                                                        | 14         |
| **\_hash de \_ assinatura \_ Propid CAPICOM**                   | Um hash da assinatura.<br/>                                                                                                                                                                                                                                                        | 15         |
| **\_dados de \_ \_ cartão inteligente \_ CAPICOM de propid**                 | Dados do cartão inteligente.<br/>                                                                                                                                                                                                                                                                | 16         |
| **CAPICOM do \_ \_ EFS propid**                               | Um [*sistema de arquivos com criptografia*](../secgloss/e-gly.md) (EFS).<br/>                                                                                                                                                  | 17         |
| **dados do CAPICOM de \_ Fortezza de Propid \_ \_**                    | Dados criados usando os protocolos criptográficos e algoritmos de Propriedade do [*Instituto Nacional de normas e tecnologia*](../secgloss/n-gly.md) (NIST).<br/> | 18         |
| **CAPICOM \_ \_ arquivo morto de propid**                          | Informações sobre se o objeto é arquivado.<br/>                                                                                                                                                                                                                               | 19         |
| **\_identificador de \_ chave de Propid de CAPICOM \_**                   | Um identificador de chave.<br/>                                                                                                                                                                                                                                                               | 20         |
| **\_ \_ registro automático de Propid de CAPICOM \_**                      | Informações de registro automático para um certificado.<br/>                                                                                                                                                                                                                                  | 21         |
| **CAPICOM \_ Propid \_ PUBKEY \_ alg \_ para**                 | Parâmetros para um algoritmo de chave pública.<br/>                                                                                                                                                                                                                                          | 22         |
| **\_pontos de \_ distribuição de certificado cruzado Propid de \_ \_ CAPICOM \_**         | Informações usadas para atualizar certificados cruzados dinâmicos.<br/>                                                                                                                                                                                                                          | 23         |
| **\_ \_ \_ \_ Hash MD5 de chave pública \_ do emissor de Propid \_ de CAPICOM**    | O hash MD5 da chave pública do emissor.<br/>                                                                                                                                                                                                                                        | 24         |
| **\_ \_ \_ \_ Hash MD5 da chave pública \_ \_ do CAPICOM de requerente propid**   | O hash MD5 da chave pública da entidade.<br/>                                                                                                                                                                                                                                       | 25         |
| **registro do CAPICOM de \_ Propid \_**                        | Informações sobre o registro do certificado.<br/>                                                                                                                                                                                                                                 | 26         |
| **\_carimbo de \_ data de Propid de CAPICOM \_**                       | Um carimbo de data/hora.<br/>                                                                                                                                                                                                                                                                   | 27         |
| **\_ \_ \_ \_ Hash MD5 de número de série \_ do \_ emissor propid do CAPICOM** | O hash MD5 do número de série do emissor.<br/>                                                                                                                                                                                                                                     | 28         |
| **\_ \_ \_ Hash MD5 de nome de entidade \_ do \_ CAPICOM**          | O hash MD5 do nome da entidade.<br/>                                                                                                                                                                                                                                             | 29         |
| **\_informações de \_ erro estendido Propid \_ de CAPICOM \_**             | Informações estendidas sobre um erro.<br/>                                                                                                                                                                                                                                            | 30         |
| **\_renovação de Propid de CApicom \_**                           | Informações sobre a renovação de uma [*autoridade de certificação*](../secgloss/c-gly.md).<br/>                                                                                                                     | 64         |
| **\_hash de \_ chave arquivada Propid \_ CAPICOM \_**               | Um hash arquivado de uma chave.<br/>                                                                                                                                                                                                                                                      | 65         |
| **capicor \_ Propid \_ primeiro \_ reservado**                   | Informações sobre a primeira reserva.<br/>                                                                                                                                                                                                                                        | 66         |
| **capicor \_ Propid \_ por último \_ reservado**                    | Informações sobre a reserva mais recente.<br/>                                                                                                                                                                                                                                  | 0x00007FFF |
| **capicore \_ Propid \_ First \_ User**                       | Informações sobre o primeiro usuário.<br/>                                                                                                                                                                                                                                               | 0x00008000 |
| **CAPICOM \_ propid do \_ último \_ usuário**                        | Informações sobre o usuário mais recente.<br/>                                                                                                                                                                                                                                         | 0x0000FFFF |



## <a name="remarks"></a>Comentários

Essa enumeração é usada pelas seguintes propriedades de CAPICOM:

-   [**Estendiproperty. PropID**](extendedproperty-propid.md)
-   [**ExtendedProperties. Remove**](extendedproperties-remove.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
