---
description: O campo de criptografia é grande e crescente.
ms.assetid: ec50d6f1-999d-4ce9-85b4-816afb17550e
title: Tipos de provedor criptográfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aaeee585ff9c11e2a20a201f541f3cd147aef6e9b50c37d60156e75a1b9fd94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876203"
---
# <a name="cryptographic-provider-types"></a>Tipos de provedor criptográfico

O campo de [*criptografia é*](../secgloss/c-gly.md) grande e crescente. Há muitos formatos e protocolos de dados padrão diferentes. Eles geralmente são organizados em grupos ou famílias, cada um dos quais tem seu próprio conjunto de formatos de dados e maneira de fazer as coisas. Mesmo que duas famílias usem o mesmo algoritmo (por exemplo, [](../secgloss/p-gly.md) a codificação de bloco [*RC2),*](../secgloss/r-gly.md) [](../secgloss/b-gly.md)elas geralmente usarão esquemas de preenchimento diferentes, [*comprimentos*](../secgloss/k-gly.md)de chave diferentes e modos padrão diferentes. CryptoAPI foi projetado para que um tipo de provedor CSP represente uma família específica.

Quando um aplicativo se conecta a um CSP de um tipo específico, cada uma das funções CryptoAPI operará, por padrão, de uma maneira prescrita pela família que corresponde a esse tipo de CSP. A escolha de um aplicativo do tipo de provedor especifica os seguintes itens:



| Item                                                                                                                                | Descrição                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Algoritmo de troca de chaves*](../secgloss/k-gly.md)                | Cada tipo de provedor especifica um e apenas um algoritmo de troca de chaves. Cada CSP de um tipo específico deve implementar esse algoritmo. Os aplicativos especificam o algoritmo de troca de chaves a ser usado selecionando um CSP do tipo de provedor apropriado.                                                        |
| [*Algoritmo de assinatura digital*](../secgloss/d-gly.md) | Cada tipo de provedor especifica um e apenas um algoritmo de assinatura digital. Cada CSP de um tipo específico deve implementar esse algoritmo. Os aplicativos especificam o algoritmo de assinatura digital a ser usado selecionando um CSP do tipo de provedor apropriado.                                              |
| Formatos de BLOB de chave                                                                                                                    | O tipo de fornecer determina o formato da [*chave BLOB*](../secgloss/k-gly.md) usada para exportar chaves do [*CSP*](../secgloss/c-gly.md) e importar chaves para um CSP. |
| Formato de assinatura digital                                                                                                            | O tipo de provedor determina o formato de assinatura digital. Isso garante que uma assinatura produzida por um CSP de um determinado tipo de provedor possa ser verificada por qualquer CSP do mesmo tipo de provedor.                                                                                                              |
| Esquema de derivação de chave de sessão                                                                                                       | O tipo de provedor determina o método usado para derivar uma chave [*de sessão*](../secgloss/s-gly.md) de um [*hash*](../secgloss/h-gly.md).                                                                                   |
| [*Comprimento da chave*](../secgloss/k-gly.md)                                                    | Alguns tipos de provedor especificam o comprimento dos [*pares de chaves pública/privada e*](../secgloss/p-gly.md) as chaves de sessão.                                                                                                               |
| Modos padrão                                                                                                                       | O tipo de provedor geralmente especifica modos padrão para várias opções, como o modo de criptografia de criptografia de bloco [*ou*](../secgloss/c-gly.md) o método de preenchimento de [*criptografia de*](../secgloss/p-gly.md) bloco.          |



 

Alguns aplicativos avançados podem se conectar a mais de um CSP por vez, mas a maioria dos aplicativos geralmente usa apenas um único CSP.

Atualmente, há vários tipos de provedor predefinidos. As próximas seções fornecem informações sobre os seguintes tipos de provedor:

-   [PROV \_ RSA \_ FULL](prov-rsa-full.md)
-   [PROV \_ RSA \_ AES](prov-rsa-aes.md)
-   [PROV \_ RSA \_ SIG](prov-rsa-sig.md)
-   [PROV \_ RSA \_ SCHANNEL](prov-rsa-schannel.md)
-   [PROV \_ DSS](prov-dss.md)
-   [DH \_ do PROV DSS \_](prov-dss-dh.md)
-   [PROV \_ DH \_ SCHANNEL](prov-dh-schannel.md)
-   [PROV \_ FORTEZZA](prov-fortezza.md)
-   [PROV \_ MS \_ EXCHANGE](prov-ms-exchange.md)
-   [PROV \_ SSL](prov-ssl.md)

Embora alguns tipos CSP possam ser parcialmente compatíveis com [](../secgloss/e-gly.md) outros, dois ou mais aplicativos que precisam trocar chaves e mensagens criptografadas devem usar CSPs do mesmo tipo.

Um CSP writer personalizado pode definir um novo tipo de provedor. No entanto, o autor do CSP é responsável por distribuir o novo tipo de provedor para os autores de qualquer aplicativo que o use. Para obter informações sobre como escrever CSPs personalizados, consulte [Cryptographic Service Providers](cryptographic-service-providers.md).

 

 
