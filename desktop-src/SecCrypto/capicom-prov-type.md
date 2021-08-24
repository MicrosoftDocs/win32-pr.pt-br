---
description: Especifica o tipo de CSP (provedor de serviços criptográficos).
ms.assetid: faf2390d-bf78-4943-91f3-1db9939fedfb
title: CAPICOM_PROV_TYPE enumeração (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROV_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bf85d2eb01ffd4290c5200e09c842f280cd5418dc5203bba068ecb5bcd65c355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879016"
---
# <a name="capicom_prov_type-enumeration"></a>Enumeração CAPICOM \_ PROV \_ TYPE

A **enumeração CAPICOM \_ PROV \_ TYPE** especifica o tipo de CSP [*(provedor*](../secgloss/c-gly.md) de serviços de criptografia).

## <a name="members"></a>Membros



| Membro                             | DESCRIÇÃO                                                                                                                                                                                                                                                                                                                                                                        | Valor |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ PROV \_ RSA \_ FULL**       | O [*CSP RSA*](../secgloss/r-gly.md) completo. Esse tipo de provedor dá suporte a [*assinaturas digitais*](../secgloss/d-gly.md) e criptografia de [*dados*](../secgloss/e-gly.md).<br/>                                                            | 1     |
| **CAPICOM \_ PROV \_ RSA \_ SIG**        | O subconjunto do CSP RSA que dá suporte apenas a funções e algoritmos necessários para hashes e assinaturas digitais.<br/>                                                                                                                                                                                                                                        | 2     |
| **CAPICOM \_ PROV \_ DSS**             | O CSP DSS [*(Digital Signature Standard).*](../secgloss/d-gly.md) Esse tipo de provedor dá suporte apenas a hashes e assinaturas digitais. O DSS usa o DSA [*(Algoritmo de*](../secgloss/d-gly.md) Assinatura Digital).<br/> | 3     |
| **CAPICOM \_ PROV \_ FORTEZZA**        | O CSP que contém os protocolos criptográficos e algoritmos pertencentes ao NIST (National [*Institute of Standards and Technology).*](../secgloss/n-gly.md)<br/>                                                                                      | 4     |
| **CAPICOM \_ PROV \_ MS \_ EXCHANGE**    | O CSP que foi projetado para as necessidades criptográficas de Exchange e outros aplicativos compatíveis com o Microsoft Mail.<br/>                                                                                                                                                                                                                                       | 5     |
| **CAPICOM \_ PROV \_ SSL**             | O CSP que dá suporte ao [*protocolo protocolo SSL*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                              | 6     |
| **CAPICOM \_ PROV \_ RSA \_ SCHANNEL**   | O CSP que dá suporte a [*protocolos RSA*](../secgloss/r-gly.md) [*e Schannel.*](../secgloss/s-gly.md)<br/>                                                                                                                                                                                        | 12    |
| **CAPICOM \_ PROV \_ DSS \_ DH**         | O CSP que dá suporte a protocolos DSS e [*Diffie-Hellman.*](../secgloss/d-gly.md)<br/>                                                                                                                                                                                                          | 13    |
| **EC \_ \_ \_ ECDSA \_ SIG DO CAPICOM PROV**  | O CSP que dá suporte às funções e algoritmos ECDSA (Algoritmo de Assinatura Digital de Curva Elíptica) necessários para assinaturas digitais.<br/>                                                                                                                                                                                                                                  | 14    |
| **CAPICOM \_ PROV \_ EC \_ ECNRA \_ SIG**  | O CSP que dá suporte às funções e algoritmos ECNRA (ECNRA) de Curva Nyberg-Rueppel Elíptica necessárias para assinaturas digitais.<br/>                                                                                                                                                                                                                                        | 15    |
| **EC \_ \_ \_ ECDSA CAPICOM PROV \_ COMPLETO** | O CSP que dá suporte ao ECDSA completo.<br/>                                                                                                                                                                                                                                                                                                                                   | 16    |
| **CAPICOM \_ PROV \_ EC \_ ECNRA \_ FULL** | O CSP que dá suporte ao ECNRA completo.<br/>                                                                                                                                                                                                                                                                                                                                   | 17    |
| **CAPICOM \_ PROV \_ DH \_ SCHANNEL**    | O CSP que dá suporte a [*protocolos Diffie-Hellman*](../secgloss/d-gly.md) e [*Schannel.*](../secgloss/s-gly.md)<br/>                                                                                                                                   | 18    |
| **CAPICOM \_ PROV \_ SPYRUS \_ LYNKS**   | O CSP que dá suporte ao dispositivo cartão SPYRUS LYNKS.<br/>                                                                                                                                                                                                                                                                                                                     | 20    |
| **CAPICOM \_ PROV \_ RNG**             | O CSP que lida com a geração de número aleatório.<br/>                                                                                                                                                                                                                                                                                                                          | 21    |
| **CAPICOM \_ PROV \_ INTEL \_ SEC**      | O CSP que fornece segurança intel.<br/>                                                                                                                                                                                                                                                                                                                                   | 22    |
| **CAPICOM \_ PROV \_ REPLACE \_ OWF**    | O CSP que dá suporte à substituição da maneira como os formatos avissivos são gerados a partir de senhas.<br/>                                                                                                                                                                                                                                                                  | 23    |
| **CAPICOM \_ PROV \_ RSA \_ AES**        | O CSP que dá suporte a assinaturas digitais e criptografia de dados usando o algoritmo criptografia AES [*(AES).*](../secgloss/a-gly.md)<br/>                                                                                                                                                                                       | 24    |



## <a name="remarks"></a>Comentários

A **enumeração CAPICOM \_ PROV \_ TYPE** é usada pelos seguintes métodos e propriedades:

-   [**Propriedade PrivateKey.ProviderType.**](privatekey-providertype.md)
-   [**Método PrivateKey.Open.**](privatekey-open.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
