---
description: Transações COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Transações COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370457"
---
# <a name="com-transactions"></a>Transações COM+

Ao comprar um livro de uma livraria online, você usa um cartão de crédito para comercializar dinheiro para um livro. Depois de enviar seu pedido, uma série de operações relacionadas (validação do seu cartão de crédito, verificação da disponibilidade do inventário e assim por diante) garante que você obtenha o livro e que a livraridade receba seu dinheiro. Se uma única operação na série falhar durante a troca, todo o Exchange falhará. Você não obtém o livro, e a livraria não recebe seu dinheiro.

A tecnologia responsável por tornar essa troca online balanceada e previsível é chamada de *processamento de transações*. Programaticamente, uma *transação* é uma unidade de trabalho na qual ocorrem uma série de operações. O COM+ usa transações programáticas para garantir que os recursos não sejam permanentemente atualizados, a menos que todas as operações na transação sejam concluídas com êxito. Ao associar um conjunto de operações relacionadas em uma transação COM+ que seja completamente bem-sucedida ou completamente malsucedida, você pode simplificar muito a recuperação de erros.

Os tópicos a seguir apresentam teoria geral de processamento de transações, fornecem uma análise mais detalhada das transações no COM+ e apresentam dicas práticas para escrever componentes transacionais.



| Tópico                                                                   | Descrição                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Conceitos de transações COM+](com--transactions-concepts.md)<br/> | Apresenta os termos e conceitos básicos.<br/>                                  |
| [Tarefas de transações COM+](com--transactions-tasks.md)<br/>       | Fornece informações práticas sobre como escrever componentes transacionais.<br/> |



 

 

 




