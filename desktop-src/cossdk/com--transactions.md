---
description: Transações COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Transações COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f800f637a9faec7564d929f3fe7f638ba36d9556db138283c0e6ff3aee87a4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070796"
---
# <a name="com-transactions"></a>Transações COM+

Ao comprar um livro de uma loja online, você usa um cartão de crédito para trocar dinheiro por um livro. Depois de enviar seu pedido, uma série de operações relacionadas (validação de seu cartão de crédito, verificação da disponibilidade de estoque e assim por diante) garante que você receba o livro e que a biblioteca receba seu dinheiro. Se uma única operação na série falhar durante a troca, toda a troca falhará. Você não obterá o livro e a loja de livros não obterá seu dinheiro.

A tecnologia responsável por tornar essa troca online equilibrada e previsível é chamada *de processamento de transações*. Programaticamente, uma *transação é* uma unidade de trabalho na qual ocorre uma série de operações. O COM+ usa transações programáticas para garantir que os recursos não sejam atualizados permanentemente, a menos que todas as operações dentro da transação sejam concluídas com êxito. Ao vincular um conjunto de operações relacionadas em uma transação COM+ que é completamente bem-sucedida ou falha completamente, você pode simplificar muito a recuperação de erros.

Os tópicos a seguir apresentam a teoria geral do processamento de transações, fornecem uma análise mais próxima das transações em COM+e apresentam dicas práticas para escrever componentes transacionais.



| Tópico                                                                   | Descrição                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Conceitos de transações COM+](com--transactions-concepts.md)<br/> | Apresenta termos e conceitos básicos.<br/>                                  |
| [Tarefas de transações COM+](com--transactions-tasks.md)<br/>       | Fornece informações práticas sobre como escrever componentes transacionais.<br/> |



 

 

 




