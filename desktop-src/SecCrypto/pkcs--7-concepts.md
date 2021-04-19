---
description: As funções de mensagem do CryptoAPI aderem ao \# padrão de CMS (criptografia de mensagem criptográfica) do PKCS 7. Os desenvolvedores precisam estar familiarizados com essa especificação para usar com mais eficiência as funções de mensagens de nível baixo. Algumas de suas definições são realçadas aqui.
ms.assetid: 99b633fe-9898-4570-ba8b-16ee78d351da
title: '\#Conceitos de sintaxe de mensagens criptográficas PKCS 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ead1c5e75737db80adbca725a30cb730b547be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757065"
---
# <a name="pkcs-7-cryptographic-messaging-syntax-concepts"></a>\#Conceitos de sintaxe de mensagens criptográficas PKCS 7

As funções de mensagem do CryptoAPI aderem ao [padrão de CMS (criptografia de mensagem criptográfica)](https://www.ietf.org/rfc/rfc3369.txt)do [*PKCS \# 7*](../secgloss/p-gly.md) . Os desenvolvedores precisam estar familiarizados com essa especificação para usar com mais eficiência as [*funções de mensagens de nível baixo*](../secgloss/l-gly.md). Algumas de suas definições são realçadas aqui.

O \# padrão PKCS 7 descreve uma sintaxe geral para dados que podem ter [*criptografia*](../secgloss/c-gly.md) aplicada a ele, como [*assinaturas digitais*](../secgloss/d-gly.md) e [*envelopes digitais*](../secgloss/d-gly.md). A sintaxe admite recursão, de modo que, por exemplo, um envelope possa ser aninhado dentro de outro, ou uma parte pode assinar dados digitais que já foram colocados em um envelope. Ele também permite que atributos arbitrários, como o tempo de assinatura, sejam autenticados junto com o conteúdo de uma mensagem. Além disso, ele fornece outros atributos, como [*referendas*](../secgloss/c-gly.md), a serem associados a uma assinatura.

O tipo de dados contido em uma \# mensagem PKCS 7 é chamado de tipo de conteúdo. Há duas classes de tipos de conteúdo: base e aprimorada.

-   Os tipos de conteúdo base contêm apenas dados sem aprimoramentos de criptografia. Atualmente, há apenas um tipo de conteúdo nessa classe, o [*tipo de conteúdo de dados*](../secgloss/d-gly.md).
-   [*Tipos de conteúdo aprimorados*](../secgloss/e-gly.md) contêm dados de algum tipo (possivelmente criptografados) e outros aprimoramentos de criptografia (como hashes ou assinaturas).

O conteúdo na classe avançada emprega encapsulamento, aumentando o [*conteúdo externo*](../secgloss/o-gly.md) dos termos (aquele que contém os aprimoramentos) e o [*conteúdo interno*](../secgloss/i-gly.md) (aquele que está sendo aprimorado). Por exemplo, uma classe avançada pode conter o [*tipo de conteúdo de dados*](../secgloss/d-gly.md) (classe base) que tem uma assinatura incluída nele. Nesse caso, o tipo de conteúdo de dados é o *conteúdo interno* e a combinação do tipo de conteúdo de dados e a assinatura forma o conteúdo externo.

Os tipos de conteúdo definidos no \# padrão PKCS 7 são os seguintes.



| Tipo de conteúdo              | Descrição                                                                                                                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dados                      | Uma cadeia de caracteres de octeto (**byte**).                                                                                                                                                                                                                                                                                           |
| Dados assinados               | Conteúdo de qualquer tipo e [*hashes*](../secgloss/h-gly.md) de mensagem criptografada ([*resumos*](../secgloss/m-gly.md)) do conteúdo para zero ou mais assinantes.                                                                           |
| Dados de envelope            | Conteúdo criptografado de qualquer tipo e chaves de criptografia de conteúdo criptografado para um ou mais destinatários. A combinação de conteúdo criptografado e chave de criptografia de conteúdo criptografado para um destinatário é um [*envelope digital*](../secgloss/d-gly.md) para esse destinatário. |
| Dados assinados e envelopado | Conteúdo criptografado de qualquer tipo, chaves de criptografia de conteúdo criptografado para um ou mais destinatários e resumos de mensagens criptografadas duplicadas para um ou mais assinantes. A criptografia dupla consiste em uma criptografia com a chave privada de um signatário seguida por uma criptografia com a chave de criptografia de conteúdo.                     |
| Dados resumidos             | Conteúdo de qualquer tipo e um [*hash*](../secgloss/h-gly.md) de mensagem (Digest) do conteúdo.                                                                                                                                                                                             |
| Dados criptografados            | Conteúdo criptografado de qualquer tipo. Ao contrário do tipo de [*conteúdo de dados*](../secgloss/d-gly.md)envelopado, o tipo de conteúdo Encrypted-data não tem destinatários nem chaves de criptografia de conteúdo criptografadas. As chaves são consideradas para serem gerenciadas por outros meios.               |



 

> [!Note]  
> Em toda a \# especificação PKCS 7, os termos *Resumo* e [*Resumo*](../secgloss/d-gly.md) referem-se ao valor produzido pela aplicação de um [*algoritmo de hash*](../secgloss/h-gly.md) aos dados. Esta documentação usa os termos [*hash*](../secgloss/h-gly.md) e *hash* para a mesma finalidade. Por exemplo, o tipo de dados usado com as [*funções de mensagem de nível baixo*](../secgloss/l-gly.md) é chamado de hash em vez de Digest. Para os fins desta documentação, os dois conjuntos de termos podem ser usados de maneira intercambiável.

 

 

 
