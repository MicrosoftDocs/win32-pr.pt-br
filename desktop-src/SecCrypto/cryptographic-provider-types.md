---
description: O campo de criptografia é grande e crescente.
ms.assetid: ec50d6f1-999d-4ce9-85b4-816afb17550e
title: Tipos de provedor criptográfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e976909cec25b5194187d61d2e753eeb830c09f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647003"
---
# <a name="cryptographic-provider-types"></a>Tipos de provedor criptográfico

O campo de [*criptografia*](../secgloss/c-gly.md) é grande e crescente. Há muitos protocolos e formatos de dados padrão diferentes. Eles geralmente são organizados em grupos ou famílias, cada um deles tem seu próprio conjunto de formatos de dados e maneira de fazer as coisas. Mesmo que duas famílias usem o mesmo algoritmo (por exemplo, a [](../secgloss/r-gly.md) [*codificação do bloco*](../secgloss/b-gly.md)RC2), elas geralmente usarão esquemas de [*preenchimento*](../secgloss/p-gly.md) diferentes, diferentes [*comprimentos de chave*](../secgloss/k-gly.md)e modos padrão diferentes. O CryptoAPI foi projetado para que um tipo de provedor CSP represente uma família específica.

Quando um aplicativo se conecta a um CSP de um tipo específico, cada uma das funções de CryptoAPI, por padrão, funciona de uma maneira prescrita pela família que corresponde a esse tipo de CSP. A escolha do tipo de provedor do aplicativo especifica os seguintes itens:



| Item                                                                                                                                | Descrição                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Algoritmo de troca de chaves*](../secgloss/k-gly.md)                | Cada tipo de provedor especifica apenas um algoritmo de troca de chave. Cada CSP de um tipo específico deve implementar esse algoritmo. Os aplicativos especificam o algoritmo de troca de chaves a ser usado selecionando um CSP do tipo de provedor apropriado.                                                        |
| [*Algoritmo de assinatura digital*](../secgloss/d-gly.md) | Cada tipo de provedor especifica um e apenas um algoritmo de assinatura digital. Cada CSP de um tipo específico deve implementar esse algoritmo. Aplicativos especifique o algoritmo de assinatura digital a ser usado selecionando um CSP do tipo de provedor apropriado.                                              |
| Formatos de BLOB de chave                                                                                                                    | O tipo de fornecimento determina o formato do [*blob de chave*](../secgloss/k-gly.md) usado para exportar chaves do [*CSP*](../secgloss/c-gly.md) e importar chaves para um CSP. |
| Formato de assinatura digital                                                                                                            | O tipo de provedor determina o formato de assinatura digital. Isso garante que uma assinatura produzida por um CSP de um determinado tipo de provedor possa ser verificada por qualquer CSP do mesmo tipo de provedor.                                                                                                              |
| Esquema de derivação de chave de sessão                                                                                                       | O tipo de provedor determina o método usado para derivar uma [*chave de sessão*](../secgloss/s-gly.md) de um [*hash*](../secgloss/h-gly.md).                                                                                   |
| [*Comprimento da chave*](../secgloss/k-gly.md)                                                    | Alguns tipos de provedor especificam o comprimento de [*pares de chaves pública/privada*](../secgloss/p-gly.md) e as chaves de sessão.                                                                                                               |
| Modos padrão                                                                                                                       | O tipo de provedor geralmente especifica os modos padrão para várias opções, como o [*modo de codificação*](../secgloss/c-gly.md) de criptografia de bloco ou o método de [*preenchimento*](../secgloss/p-gly.md) de criptografia de bloco.          |



 

Alguns aplicativos avançados podem se conectar a mais de um CSP de cada vez, mas a maioria dos aplicativos geralmente usa apenas um único CSP.

Atualmente, há um número de tipos de provedor predefinidos. As próximas seções fornecem informações sobre os seguintes tipos de provedor:

-   [PROV \_ RSA \_ completo](prov-rsa-full.md)
-   [PROV \_ RSA \_ AES](prov-rsa-aes.md)
-   [PROV \_ RSA \_ SIG](prov-rsa-sig.md)
-   [PROV \_ RSA \_ Schannel](prov-rsa-schannel.md)
-   [PROV \_ DSS](prov-dss.md)
-   [o PROV \_ DSS \_ DH](prov-dss-dh.md)
-   [PROV \_ DH \_ Schannel](prov-dh-schannel.md)
-   [PROV \_ Fortezza](prov-fortezza.md)
-   [PROV \_ MS \_ Exchange](prov-ms-exchange.md)
-   [PROV \_ SSL](prov-ssl.md)

Embora alguns tipos de CSP possam ser parcialmente compatíveis com outras pessoas, dois ou mais aplicativos que precisam [*trocar chaves*](../secgloss/e-gly.md) e mensagens criptografadas devem usar CSPs do mesmo tipo.

Um gravador CSP personalizado pode definir um novo tipo de provedor. No entanto, o gravador CSP é, então, responsável por distribuir o novo tipo de provedor para os autores de aplicativos que o utilizam. Para obter informações sobre como escrever CSPs personalizados, consulte [provedores de serviços de criptografia](cryptographic-service-providers.md).

 

 
