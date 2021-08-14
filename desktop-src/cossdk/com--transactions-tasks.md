---
description: Tarefas de transações COM+
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Tarefas de transações COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102b0ec6ae54430be5499c67b5041ee26035eb077e27b1b860377cd728e3e42d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307586"
---
# <a name="com-transactions-tasks"></a>Tarefas de transações COM+

Embora o processamento automático de transações no COM+ permita que você gaste um tempo de desenvolvimento mais produtivo na criação e configuração de objetos que você deseja participar de transações automáticas, há algumas tarefas de programação que você pode executar para personalizar o comportamento da transação para os requisitos do aplicativo.

Os tópicos a seguir discutem opções de programação específicas relacionadas ao processamento de transações.



| Tópico                                                                                             | Descrição                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Configurando o atributo de transação](setting-the-transaction-attribute.md)<br/>             | Descreve como definir valores de atributo de transação para seus objetos de transação.<br/>         |
| [Configurar o nível de isolamento da transação](setting-the-transaction-isolation-level.md)<br/> | Descreve como definir os níveis de isolamento da transação para seus objetos de transação.<br/>     |
| [Definindo o tempo limite da transação](setting-the-transaction-time-out.md)<br/>               | Descreve como definir intervalos de tempo limite para suas transações.<br/>                          |
| [Definindo os sinalizadores consistentes e concluídos](setting-the-consistent-and-done-flags.md)<br/>     | Mostra como usar os sinalizadores consistentes e concluídos para controlar o resultado de uma transação.<br/> |
| [Criando objetos BYOT](creating-byot-objects.md)<br/>                                     | Descreve como criar objetos para que você possa trazer sua própria transação (BYOT).<br/>           |



 

> [!Note]  
> Como regra geral, qualquer componente que atualize o estado persistente deve dar suporte a transações. Os componentes que combinam as operações de dois ou mais objetos em uma única tarefa devem usar transações para simplificar a recuperação de erros. Além disso, para liberar recursos, como conexões de banco de dados, as transações em COM+ devem ser tão curtas quanto você pode fazer.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de transações COM+](com--transactions-concepts.md)
</dt> </dl>

 

 




