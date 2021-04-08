---
description: O oferece suporte a assinaturas digitais e criptografia de dados. Ele é considerado um CSP (provedor de serviços de criptografia) de uso geral.
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011450"
---
# <a name="prov_rsa_aes"></a>PROV \_ RSA \_ AES

O \_ tipo de provedor de AES RSA Prov \_ oferece suporte a [assinaturas digitais](digital-signatures.md) e criptografia de dados. Ele é considerado um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) de uso geral. O [*algoritmo de chave pública*](../secgloss/p-gly.md) RSA é usado para todas as operações de [*chave pública*](../secgloss/p-gly.md) .

## <a name="algorithms-supported"></a>Algoritmos com suporte

Para obter descrições de cada um desses algoritmos, consulte o Glossário.



| Finalidade      | Algoritmos compatíveis                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Troca de chaves | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Assinatura    | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Criptografia   | [*RC2*](../secgloss/r-gly.md)<br/> [*RC4*](../secgloss/r-gly.md)<br/> [*Criptografia AES*](../secgloss/a-gly.md) (AES) <br/>                                                       |
| Hash      | [*MD2*](../secgloss/m-gly.md)<br/> [*MD4*](../secgloss/m-gly.md)<br/> [*MD5*](../secgloss/m-gly.md)<br/> [*SHA-1*](../secgloss/s-gly.md)<br/> SHA-2 (SHA-256, SHA-384 e SHA-512)<br/> |



 

## <a name="related-documentation"></a>Documentação relacionada

Esse tipo de provedor é definido pela Microsoft e pela RSA Data Security. Ele é descrito nos seguintes documentos:

-   *Guia do programador do provedor de serviços de criptografia da Microsoft*, Microsoft, 1996.
-   Laboratórios RSA, padrões de criptografia de chave pública, segurança de dados RSA, novembro de 1993.

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países ou regiões.

 

 

 
