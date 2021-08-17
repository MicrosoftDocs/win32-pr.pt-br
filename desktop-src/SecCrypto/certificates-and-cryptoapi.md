---
description: Um certificado padrão X.509 contém informações de versão, número de série, identificador de algoritmo, nome do emissor, intervalo de datas válido, nome da assunto, algoritmo e informações de chave pública de assunto e, opcionalmente, ID exclusiva do emissor, ID exclusiva da assunto e extensões.
ms.assetid: 91425185-2a06-4040-b83d-c42ee080d55f
title: Certificados e CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8af32073cc3f42bbee07d1702fd1e6044c424ac236cf05ed8374c33757c1408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770737"
---
# <a name="certificates-and-cryptoapi"></a>Certificados e CryptoAPI

[*O CryptoAPI dá*](../secgloss/c-gly.md) suporte ao uso de certificados X.509 conforme definido no [IETF RFC 3280.](https://www.ietf.org/rfc/rfc3280.txt) Esta documentação pressupo o uso de um certificado digital X.509 ou [*comparável.*](../secgloss/c-gly.md)

Um certificado padrão X.509 contém as informações a seguir.



| Campo                | Descrição                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão              | Número de versão do certificado.                                                                                                                                                                                         |
| Número de Série        | Número de série do certificado.                                                                                                                                                                                          |
| Identificador de algoritmo | Algoritmo de assinatura usado pelo signante do certificado.                                                                                                                                                                        |
| Nome do emissor          | Nome do emissor do certificado.                                                                                                                                                                                     |
| Não Antes De           | Data anterior à qual o certificado não é válido.                                                                                                                                                                            |
| Não Após            | Data após a qual o certificado não é válido.                                                                                                                                                                             |
| Nome do assunto         | Nome da pessoa ou entidade para a qual o certificado está sendo emitido.                                                                                                                                                      |
| Algoritmo            | Algoritmo usado para a chave pública.                                                                                                                                                                                         |
| Chave pública do assunto   | Chave pública real (uma cadeia de caracteres de bits).                                                                                                                                                                                          |
| ID Exclusiva do Emissor     | Campo opcional. Se estiver presente, a versão deverá ser a versão 2.                                                                                                                                                                     |
| ID exclusiva da assunto    | Campo opcional. Se estiver presente, a versão deverá ser a versão 2.                                                                                                                                                                     |
| Extensões           | Campo opcional. Representa dados adicionais que um emissor pode querer adicionar a um certificado, como endereço de email ou autorização para emitir certificados. Se as extensões estão presentes, a versão deve ser a versão 3.<br/> |



 

 

 
