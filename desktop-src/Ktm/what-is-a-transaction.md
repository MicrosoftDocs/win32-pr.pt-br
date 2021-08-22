---
description: 'Uma transação é um grupo de operações que têm as seguintes propriedades: ACID (atômico, consistente, isolado e durável).'
ms.assetid: b3da52a3-1c52-4577-a997-7e72ebc03fa8
title: O que é uma transação?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f04a21eaec081a42e1cd4bcd60cb7cf48d609075eec772ed18fd41494c47d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289713"
---
# <a name="what-is-a-transaction"></a>O que é uma transação?

Uma transação é um grupo de operações que têm as seguintes propriedades: ACID (atômico, consistente, isolado e durável). O suporte a transações permite que novos tipos de aplicativos sejam desenvolvidos, simplificando o processo de desenvolvimento e tornando o aplicativo mais robusto. O restante deste tópico fornece cenários que demonstram a necessidade dessas propriedades e, em seguida, uma tabela que define cada propriedade.

Em um *grupo atômico* de operações, todas as operações no grupo devem ser bem-sucedidas ou os efeitos de todas elas devem ser desfeitas (também conhecidas como *reverter*). Por exemplo, uma transferência bancária deve ser um conjunto atômico de duas operações: um débito de uma conta e um crédito para outra conta. O débito e o crédito devem ser implementados como um grupo atômico. Se essas duas operações não são bem-sucedidas, a transferência é incorretamente a favor do banco ou do titular da conta.

O requisito de *consistência significa* que os dados são consistentes após a transação (supondo que começamos com um sistema consistente antes da transação). Para o exemplo de transferência bancária, a consistência pode ser definida como tendo o saldo de conta combinado das duas contas como uma constante. Para implementar a consistência no exemplo de transferência bancária, as operações de débito e crédito simplesmente precisam ser para a mesma quantidade de dinheiro.

Outro exemplo de uma transação é uma atualização para um site. Um site de comércio eletrônico exige que uma nova página de navegação da categoria de produto apareça exatamente ao mesmo tempo que as páginas de detalhes do produto que descrevem os novos produtos. Nesse caso, há a necessidade de atualizar e adicionar várias entradas de diretório sob o controle de uma transação. Não apenas é necessário que as atualizações sejam atômicas, mas também é necessário que um cliente que está fazendo compras no momento não veja as atualizações em andamento. Este é um exemplo da propriedade *de isolamento* de transações.

A propriedade de *durabilidade requer que,* após a atualização ser concluída, seus efeitos persistam mesmo que o sistema pare de responder. No exemplo anterior, a durabilidade pode ser fornecida simplesmente garantindo a recuperação de dados adequada para que todas as novas entradas do sistema de arquivos que representam a adição de um novo produto ao site apareçam depois que um sistema parar de responder. Isso requer um sistema com backup de dados, recuperação e mecanismos de alta disponibilidade.

A garantia da atomicidade de uma transação, bem como das outras propriedades, está presente diante de qualquer número de falhas, incluindo falhas que ocorrem durante a fase de recuperação de uma falha anterior. Eventualmente, o sistema atingirá um dos dois estados: todas as operações foram aplicadas ou nenhuma das operações foi aplicada.

As propriedades de uma transação são resumidas na tabela a seguir.



| Termo                                                                                                         | Descrição                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atômica<br/>                 | Todas as operações na transação são bem-sucedidas ou nenhuma das operações persiste.<br/>                             |
| <span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Consistente<br/> | Se os dados são consistentes antes do início da transação, eles serão consistentes depois que a transação for final.<br/> |
| <span id="Isolated_"></span><span id="isolated_"></span><span id="ISOLATED_"></span>Isolado <br/>     | Os efeitos de uma transação que está em andamento são ocultos de todas as outras transações.<br/>                               |
| <span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durável<br/>             | Quando uma transação é final, seus resultados são persistentes e sobreviverão a uma falha do sistema.<br/>                               |



 

Essas propriedades garantem que o software possa lidar com erros inesperados, pois ele pode simplesmente anular uma transação quando uma situação inesperada impede uma conclusão bem-sucedida. A infraestrutura de transação garante que todos os efeitos da transação anulada sejam re roll back, retornando os dados para um estado consistente. Portanto, um sistema transacional permite uma recuperação normalmente de falhas do sistema.

Para garantir as propriedades ACID, um sistema que dá suporte a transações deve ter uma funcionalidade de registro em log robusta que pode ser usada para fazer commit ou reverter transações conforme necessário. Para obter mais informações, [consulte Sistema de Arquivos de Log Comum](/previous-versions/windows/desktop/clfs/common-log-file-system-portal).

 

