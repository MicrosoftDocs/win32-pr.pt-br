---
description: 'Uma transação é um grupo de operações que tem as seguintes propriedades: Atomic, consistente, isolado e durável (ACID).'
ms.assetid: b3da52a3-1c52-4577-a997-7e72ebc03fa8
title: O que é uma transação?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c459462d3aee3d7eef556ce0951ede537e8109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828112"
---
# <a name="what-is-a-transaction"></a>O que é uma transação?

Uma transação é um grupo de operações que tem as seguintes propriedades: Atomic, consistente, isolado e durável (ACID). O suporte de transações permite que novos tipos de aplicativos sejam desenvolvidos, simplificando o processo de desenvolvimento e tornando o aplicativo mais robusto. O restante deste tópico fornece cenários que demonstram a necessidade dessas propriedades, depois uma tabela que define cada propriedade.

Em um grupo *atômico* de operações, cada operação no grupo deve ser bem-sucedida ou os efeitos de todos eles devem ser desfeitos (também conhecido como *reversão*). Por exemplo, uma transferência bancária deve ser um conjunto atômico de duas operações: um débito de uma conta e um crédito para outra conta. O débito e o crédito devem ser implementados como um grupo atômico. Se essas duas operações não tiverem sucesso, a transferência será injustamente em favor do banco ou do titular da conta.

O requisito de *consistência* significa que os dados são consistentes após a transação (supondo que começamos com um sistema consistente antes da transação). Para o exemplo de transferência bancária, a consistência pode ser definida como se o saldo combinado da conta das duas contas fosse uma constante. Para implementar a consistência no exemplo de transferência bancária, as operações de débito e crédito simplesmente precisam ser para o mesmo valor de dinheiro.

Outro exemplo de uma transação é uma atualização para um site. Um site de comércio eletrônico requer que uma nova página de navegação de categoria de produto seja exibida exatamente ao mesmo tempo que as páginas de detalhes do produto que descrevem os novos produtos. Nesse caso, há a necessidade de atualizar e adicionar várias entradas de diretório sob o controle de uma transação. Não só é necessário que as atualizações sejam atômicas, mas também é necessário que um cliente que esteja comprando atualmente não deva ver as atualizações em andamento. Este é um exemplo da propriedade de *isolamento* das transações.

A propriedade da *durabilidade* exige que, após a conclusão de uma atualização, seus efeitos persistem mesmo se o sistema parar de responder. No exemplo anterior, a durabilidade pode ser fornecida simplesmente garantindo a recuperação de dados adequada para que todas as novas entradas do sistema de arquivos que representam a adição de um novo produto ao site apareçam depois que um sistema para de responder. Isso requer um sistema com mecanismos de backup, recuperação e alta disponibilidade de dados.

A garantia da atomicidade de uma transação, bem como das outras propriedades, está presente na face de qualquer número de falhas, incluindo falhas que ocorrem durante a fase de recuperação de uma falha anterior. Eventualmente, o sistema alcançará um dos dois Estados: todas as operações foram aplicadas ou nenhuma das operações foi aplicada.

As propriedades de uma transação são resumidas na tabela a seguir.



| Termo                                                                                                         | Descrição                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atômica<br/>                 | Todas as operações na transação têm sucesso ou nenhuma das operações persistem.<br/>                             |
| <span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Coerente<br/> | Se os dados forem consistentes antes do início da transação, eles serão consistentes após a conclusão da transação.<br/> |
| <span id="Isolated_"></span><span id="isolated_"></span><span id="ISOLATED_"></span>Isolados <br/>     | Os efeitos de uma transação em andamento ficam ocultos de todas as outras transações.<br/>                               |
| <span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Permanente<br/>             | Quando uma transação é concluída, seus resultados são persistentes e sobreviver a uma falha do sistema.<br/>                               |



 

Essas propriedades garantem que o software possa lidar com erros inesperados, pois ele pode simplesmente anular uma transação quando uma situação inesperada impedir uma conclusão bem-sucedida. A infraestrutura de transação garante que todos os efeitos da transação abortada sejam revertidos, retornando os dados para um estado consistente. Portanto, um sistema transacional permite uma recuperação normal de falhas do sistema.

Para garantir as propriedades ACID, um sistema que dá suporte a transações deve ter um recurso de log robusto que pode ser usado para confirmar ou reverter transações, conforme necessário. Para obter mais informações, consulte [sistema de arquivos de log comum](/previous-versions/windows/desktop/clfs/common-log-file-system-portal).

 

