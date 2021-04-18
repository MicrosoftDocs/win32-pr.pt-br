---
description: Lista os provedores de serviços de criptografia disponíveis na Microsoft.
ms.assetid: 1461914e-5506-4f24-97da-3d2148aafd1c
title: Provedores de serviços de criptografia da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 294d00660cbfa89c6113e6e9fcf2600b2f745e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811053"
---
# <a name="microsoft-cryptographic-service-providers"></a>Provedores de serviços de criptografia da Microsoft

Os [*provedores de serviços de criptografia*](../secgloss/c-gly.md) (CSP) a seguir estão disponíveis atualmente na Microsoft.



| Provedor                                                                                                                                 | Descrição                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Provedor criptográfico base da Microsoft](microsoft-base-cryptographic-provider.md)                                                       | Um amplo conjunto de funcionalidades básicas de criptografia que podem ser exportadas para outros países ou regiões.                                                                                                                                                     |
| [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md)                                                   | Uma extensão do provedor Microsoft Base Cryptographic disponível com o Windows XP e versões posteriores.                                                                                                                                                           |
| [Provedor criptográfico aprimorado da Microsoft](microsoft-enhanced-cryptographic-provider.md)                                               | Provedor criptográfico base da Microsoft com chaves mais longas e algoritmos adicionais.                                                                                                                                                                |
| [Provedor criptográfico do Microsoft AES](microsoft-aes-cryptographic-provider.md)                                                         | Provedor criptográfico aprimorado da Microsoft com suporte para algoritmos de criptografia AES.                                                                                                                                                                    |
| [Provedor criptográfico do Microsoft DSS](microsoft-dss-cryptographic-provider.md)                                                         | Fornece a funcionalidade de hash, assinatura de dados e verificação de assinatura usando os algoritmos [*Sha*](../secgloss/s-gly.md)(algoritmo de hash seguro) e DSS (padrão de assinatura digital). |
| [Microsoft Base DSS e Diffie-Hellman provedor criptográfico](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)         | Um superconjunto do provedor de criptografia DSS que também dá suporte a Diffie-Hellman troca de chaves, hash, assinatura de dados e verificação de assinatura usando os algoritmos de SHA (algoritmo de hash seguro) e DSS (padrão de assinatura digital).                    |
| [Microsoft Enhanced DSS e Diffie-Hellman provedor criptográfico](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md) | Dá suporte à troca de chaves Diffie-Hellman (um derivativo DES de 40 bits), hash de SHA, assinatura de dados DSS e verificação de assinatura DSS.                                                                                                                           |
| [Provedor criptográfico do Microsoft DSS e Diffie-Hellman/Schannel](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md) | Dá suporte a hash, assinatura de dados com DSS, gerando chaves de Diffie-Hellman (D-H), trocando chaves de D-H e exportando uma chave D-H. Esse CSP dá suporte à derivação de chave para os protocolos SSL3 e TLS1.                                                           |
| [Provedor criptográfico RSA/Schannel da Microsoft](microsoft-rsa-schannel-cryptographic-provider.md)                                       | Dá suporte a hash, assinatura de dados e verificação de assinatura. O identificador de algoritmo CALG \_ SSL3 \_ SHAMD5 é usado para autenticação de cliente SSL 3,0 e TLS 1,0. Esse CSP dá suporte à derivação de chave para os protocolos SSL2, PCT1, SSL3 e TLS1.             |
| [Provedor criptográfico da assinatura do Microsoft RSA](microsoft-rsa-signature-cryptographic-provider.md)                                     | Fornece assinatura de dados e verificação de assinatura.                                                                                                                                                                                                        |



 

 

 
