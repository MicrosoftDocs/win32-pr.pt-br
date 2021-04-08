---
title: Um modelo de replicação do programador no Active Directory Domain Services
description: Veja a seguir uma descrição do modelo de replicação para Active Directory Domain Services.
ms.assetid: 45baf7ff-9474-4f86-81c8-03336901fec2
ms.tgt_platform: multiple
keywords:
- O modelo do programador de Active Directory AD de replicação
- Um modelo de replicação do programador no Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ada20bc07411528eaea4b7ff8c773c50ae8b6ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004825"
---
# <a name="a-programmers-model-of-replication-in-active-directory-domain-services"></a>Um modelo de replicação do programador no Active Directory Domain Services

Veja a seguir uma descrição do modelo de replicação para Active Directory Domain Services.

Todas as atualizações para o controlador de Domínio do Active Directory (DC) são executadas usando solicitações LDAP que criam, modificam ou excluem um objeto para cada solicitação. Uma única solicitação pode definir ou modificar vários atributos em um objeto.

Uma solicitação de atualização é processada como uma transação atômica em algum DC. Toda a atualização ocorre ou nenhuma delas. Se o solicitante receber uma resposta bem-sucedida a uma solicitação de atualização, essa solicitação inteira terá êxito (confirmada). Isso é chamado de "gravação de origem". Várias solicitações LDAP não podem ser agrupadas em uma única transação maior.

Em uma gravação de origem, um DC computa um "carimbo" para cada valor de atributo novo ou modificado e anexa esse carimbo ao valor, de modo que, quando o valor for replicado, o carimbo também seja replicado. O novo carimbo é exclusivo e, no caso de uma atualização, o novo carimbo é maior do que o carimbo no valor antigo nesse DC.

Ocasionalmente, um DC seleciona o conjunto de objetos que foram alterados desde a última vez em que o DC realizou a replicação. Em seguida, para cada objeto, ele envia uma única mensagem para todos os outros DCs que contêm todos os valores atuais de atributos alterados desde a última vez em que o objeto foi replicado. As mensagens de replicação são confiáveis e são entregues em ordem, mas podem exigir mais tempo para serem entregues.

Quando um DC recebe uma mensagem de replicação de outro DC, ele a processa da seguinte maneira: para cada atributo modificado, se o carimbo no valor na mensagem de replicação for maior do que o carimbo no valor atual, o controlador de domínio aplicará a atualização; caso contrário, o DC descartará a atualização. Cada mensagem de replicação é aplicada como uma transação atômica, assim como uma gravação de origem.

Esse é o modelo de replicação de Active Directory Domain Services. As principais propriedades desse modelo incluem:

-   Uma gravação de origem em um único objeto é atômica.
-   Ao replicar as alterações, todas as alterações feitas por uma gravação de origem são enviadas ou nenhuma delas é.
-   Uma gravação replicada em um único objeto é atômica, mas os conflitos são resolvidos atributo-por-atributo.

O modelo não garante a ordenação de replicação de alterações feitas em objetos diferentes. Não grave aplicativos que supõem que as alterações sejam replicadas na ordem de gravação de origem. O modelo não garante que, se um atributo de um objeto for alterado duas vezes, ambos os valores serão replicados; A replicação envia apenas o valor atual no momento da replicação.

O modelo difere da realidade de várias maneiras que afetam apenas o desempenho. Por exemplo, o servidor de Active Directory envia mensagens de replicação que contêm as alterações a vários objetos, mas processa o conteúdo de uma mensagem de vários objetos como se fosse uma série de mensagens de objeto único. O servidor de Active Directory não executa a replicação ponto a ponto conforme descrito no modelo, mas realiza uma replicação transitiva mais complexa e eficiente que é funcionalmente equivalente ao modelo.

 

 




