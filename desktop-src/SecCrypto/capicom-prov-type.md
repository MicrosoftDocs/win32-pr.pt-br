---
description: Especifica o tipo de CSP (provedor de serviços de criptografia).
ms.assetid: faf2390d-bf78-4943-91f3-1db9939fedfb
title: Enumeração de CAPICOM_PROV_TYPE (CAPICOM. h)
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
ms.openlocfilehash: d9c701b453656a68573fe391775c5b27fdd2461a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749679"
---
# <a name="capicom_prov_type-enumeration"></a>Enumeração de tipo CAPICOM \_ Prov \_

A enumeração do **\_ \_ tipo CAPICOM Prov** especifica o tipo de CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).

## <a name="members"></a>Membros



| Membro                             | DESCRIÇÃO                                                                                                                                                                                                                                                                                                                                                                        | Valor |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM de \_ \_ RSA Prov \_ Full**       | O [*RSA*](../secgloss/r-gly.md) CSP completo. Esse tipo de provedor dá suporte a [*assinaturas digitais*](../secgloss/d-gly.md) e [*criptografia*](../secgloss/e-gly.md)de dados.<br/>                                                            | 1     |
| **CAPICOM \_ Prov \_ RSA \_ SIG**        | O subconjunto do CSP RSA que dá suporte apenas a essas funções e algoritmos necessários para hashes e assinaturas digitais.<br/>                                                                                                                                                                                                                                        | 2     |
| **capicore \_ Prov \_ DSS**             | O CSP DSS ( [*padrão de assinatura digital*](../secgloss/d-gly.md) ). Esse tipo de provedor dá suporte apenas a hashes e assinaturas digitais. O DSS usa o DSA ( [*algoritmo de assinatura digital*](../secgloss/d-gly.md) ).<br/> | 3     |
| **capicor \_ Prov \_ Fortezza**        | O CSP que contém os protocolos criptográficos e os algoritmos de Propriedade do [*Instituto Nacional de normas e tecnologia*](../secgloss/n-gly.md) (NIST).<br/>                                                                                      | 4     |
| **CAPICOM do \_ \_ Microsoft Prov MS \_ Exchange**    | O CSP que foi projetado para as necessidades criptográficas do Exchange e de outros aplicativos que são compatíveis com o Microsoft mail.<br/>                                                                                                                                                                                                                                       | 5     |
| **capicore \_ Prov \_ SSL**             | O CSP que dá suporte ao protocolo [*protocolo SSL*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                              | 6     |
| **capicore \_ Prov \_ RSA \_ Schannel**   | O CSP que dá suporte aos protocolos [*RSA*](../secgloss/r-gly.md) e [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                        | 12    |
| **CAPICOM de \_ \_ DH Prov DSS \_**         | O CSP que dá suporte aos protocolos DSS e [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                                                                          | 13    |
| **capicore \_ Prov \_ EC \_ ECDSA \_ SIG**  | O CSP que dá suporte às funções de ECDSA (algoritmo de assinatura digital de curva elíptica) e algoritmos necessários para assinaturas digitais.<br/>                                                                                                                                                                                                                                  | 14    |
| **capicore \_ Prov \_ EC \_ ECNRA \_ SIG**  | O CSP que dá suporte à curva elíptica Nyberg-Rueppel funções analógicas (ECNRA) e algoritmos necessários para assinaturas digitais.<br/>                                                                                                                                                                                                                                        | 15    |
| **CAPICOM de ECDSA do EC para o \_ \_ \_ \_ completo** | O CSP que dá suporte ao ECDSA completo.<br/>                                                                                                                                                                                                                                                                                                                                   | 16    |
| **capicore \_ Prov \_ EC \_ ECNRA \_ Full** | O CSP que dá suporte ao ECNRA completo.<br/>                                                                                                                                                                                                                                                                                                                                   | 17    |
| **capicore \_ Prov \_ DH \_ Schannel**    | O CSP que dá suporte aos protocolos [*Diffie-Hellman*](../secgloss/d-gly.md) e [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                   | 18    |
| **CAPICOM \_ Prov \_ SPYRUS \_ Lynks**   | O CSP que dá suporte ao dispositivo de cartão SPYRUS LYNKS.<br/>                                                                                                                                                                                                                                                                                                                     | 20    |
| **CAPICOM \_ Prov \_ RNG**             | O CSP que lida com a geração de números aleatórios.<br/>                                                                                                                                                                                                                                                                                                                          | 21    |
| **CAPICOM de \_ Prov \_ Intel \_ SEC**      | O CSP que fornece segurança Intel.<br/>                                                                                                                                                                                                                                                                                                                                   | 22    |
| **CAPICOM \_ Prov \_ substituir \_ OWF**    | O CSP que dá suporte à substituição da maneira em que os formatos unidirecionais são gerados a partir de senhas.<br/>                                                                                                                                                                                                                                                                  | 23    |
| **CAPICOM do \_ \_ \_ AES RSA**        | O CSP que dá suporte a assinaturas digitais e criptografia de dados usando o algoritmo criptografia AES ([*AES*](../secgloss/a-gly.md)).<br/>                                                                                                                                                                                       | 24    |



## <a name="remarks"></a>Comentários

A enumeração do **\_ \_ tipo CAPICOM Prov** é usada pelos seguintes métodos e propriedades:

-   Propriedade [**PrivateKey. ProviderType**](privatekey-providertype.md) .
-   Método [**PrivateKey. Open**](privatekey-open.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
