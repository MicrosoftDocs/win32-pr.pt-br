---
description: Um certificado X. 509 padrão, contém versão, número de série, identificador de algoritmo, nome do emissor, intervalo de datas válido, nome da entidade, algoritmo e informações de chave pública da entidade e, opcionalmente, ID exclusiva do emissor, ID exclusiva da entidade e extensões.
ms.assetid: 91425185-2a06-4040-b83d-c42ee080d55f
title: Certificados e CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325086ab0dd46ace85745ca292bcab9bcd5324e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760204"
---
# <a name="certificates-and-cryptoapi"></a>Certificados e CryptoAPI

O [*CryptoAPI*](../secgloss/c-gly.md) dá suporte ao uso de certificados X. 509 conforme definido em [IETF RFC 3280](https://www.ietf.org/rfc/rfc3280.txt). Esta documentação pressupõe o uso de um [*certificado digital*](../secgloss/c-gly.md)X. 509 ou comparável.

Um certificado X. 509 padrão contém as informações a seguir.



| Campo                | Descrição                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão              | Número de versão do certificado.                                                                                                                                                                                         |
| Número de Série        | Número de série do certificado.                                                                                                                                                                                          |
| Identificador de algoritmo | Algoritmo de assinatura usado pelo assinante de certificado.                                                                                                                                                                        |
| Nome do emissor          | Nome do emissor do certificado.                                                                                                                                                                                     |
| Não Antes De           | Data antes da qual o certificado não é válido.                                                                                                                                                                            |
| Não Após            | Data após a qual o certificado não é válido.                                                                                                                                                                             |
| Nome do assunto         | Nome da pessoa ou entidade para a qual o certificado está sendo emitido.                                                                                                                                                      |
| Algoritmo            | Algoritmo usado para a chave pública.                                                                                                                                                                                         |
| Chave pública de assunto   | Chave pública real (uma cadeia de caracteres de bits).                                                                                                                                                                                          |
| ID exclusiva do emissor     | Campo opcional. Se estiver presente, a versão deverá ser a versão 2.                                                                                                                                                                     |
| ID exclusiva da entidade    | Campo opcional. Se estiver presente, a versão deverá ser a versão 2.                                                                                                                                                                     |
| Extensões           | Campo opcional. Representa dados adicionais que um emissor pode querer adicionar a um certificado, como endereço de email ou autorização para emitir certificados. Se as extensões estiverem presentes, a versão deverá ser a versão 3.<br/> |



 

 

 
