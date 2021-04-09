---
description: Cunhado por pioneiros no processamento de transações, o acrônimo ACID significa Atomic, consistente, isolado e durável.
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: Propriedades ACID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089138"
---
# <a name="acid-properties"></a>Propriedades ACID

Cunhado por pioneiros no processamento de transações, o acrônimo ACID significa Atomic, consistente, isolado e durável. Para garantir um comportamento previsível, todas as transações devem possuir essas propriedades básicas, reforçando a função de transações críticas como proposições de todas as-ou-nenhuma.

A lista a seguir contém uma definição e uma descrição de cada propriedade ACID:

<dl> <dt>

<span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atômica
</dt> <dd>

Uma transação deve ser executada exatamente uma vez e deve ser atômica – qualquer trabalho é feito ou nenhum deles é. As operações em uma transação geralmente compartilham uma intenção comum e são interdependentes. Ao executar apenas um subconjunto dessas operações, o sistema pode comprometer a intenção geral da transação. A atomicidade elimina a chance de processar apenas um subconjunto de operações.

</dd> <dt>

<span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Coerente
</dt> <dd>

Uma transação deve preservar a consistência dos dados, transformando um estado consistente de dados em outro estado consistente de dados. Grande parte da responsabilidade de manter a consistência cai ao desenvolvedor do aplicativo.

</dd> <dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolados
</dt> <dd>

Uma transação deve ser uma unidade de isolamento, o que significa que as transações simultâneas devem se comportar como se cada uma fosse a única transação em execução no sistema. Como um alto grau de isolamento pode limitar o número de transações simultâneas, alguns aplicativos reduzem o nível de isolamento no Exchange para melhorar a taxa de transferência. Consulte [Configurando níveis de isolamento da transação](configuring-transaction-isolation-levels.md) para obter mais informações.

</dd> <dt>

<span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Permanente
</dt> <dd>

Uma transação deve ser recuperável e, portanto, deve ter durabilidade. Se uma transação for confirmada, o sistema garante que suas atualizações possam persistir mesmo se o computador falhar imediatamente após a confirmação. O log especializado permite que o procedimento de reinicialização do sistema conclua as operações não concluídas exigidas pela transação, tornando a transação durável.

</dd> </dl>

 

 



