---
description: Conceitos de componentes em fila do COM+
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: Conceitos de componentes em fila do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762995"
---
# <a name="com-queued-components-concepts"></a>Conceitos de componentes em fila do COM+

Com base nos serviços de [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) , o serviço de componentes em fila do com+ fornece uma maneira fácil de invocar e executar componentes de forma assíncrona. O processamento pode ocorrer sem considerar a disponibilidade ou a acessibilidade do remetente ou do receptor.

Em termos de COM, uma *fila* é uma área de armazenamento que salva as mensagens para recuperação posterior. O enfileiramento fornece um mecanismo de comunicação sem conexão. Ou seja, o remetente e o destinatário não estão conectados diretamente e se comunicam somente por meio de filas. O enfileiramento fornece uma maneira de manter as informações até que o receptor esteja pronto para obtê-la. O remetente e o destinatário estão se comunicando indiretamente para que cada um possa operar de forma independente, não afetado pelo outro.

No passado, um conhecimento profundo do marshaling era necessário para enfileirar, enviar e receber mensagens assíncronas. Agora, usando chamadas de método que são facilmente compreendidas e usadas por desenvolvedores de componentes, o serviço de componentes em fila COM+ realiza marshaling de dados automaticamente na forma de uma mensagem de enfileiramento de mensagens. E como o serviço de componentes em fila oferece suporte interno para transações, um estado inconsistente não poderá comprometer os dados se ocorrer uma falha de servidor.

Os tópicos a seguir nesta seção contêm informações básicas sobre como criar e gravar componentes enfileirados.



| Tópico                                                                           | Descrição                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Benefícios do processamento em fila](benefits-of-queued-processing.md)<br/>   | Descreve os benefícios da programação com os componentes em fila do COM+.<br/>                                         |
| [Arquitetura de componentes na fila](queued-components-architecture.md)<br/> | Descreve a arquitetura do serviço de componentes em fila do COM+.<br/>                                          |
| [Enfileiramento de mensagens transacionais](transactional-message-queuing.md)<br/>   | Descreve como as transações são manipuladas pelo serviço de componentes em fila do COM+.<br/>                              |
| [Segurança de componentes na fila](queued-components-security.md)<br/>         | Descreve as opções de política para autenticação de mensagens do cliente e suas implicações.<br/>                 |
| [Desenvolvendo componentes em fila](developing-queued-components.md)<br/>     | Descreve considerações de programação ao escrever componentes queuable.<br/>                                     |
| [Erros de componentes na fila](queued-components-errors.md)<br/>             | Descreve os tipos mais comuns de erros que você pode encontrar ao usar o serviço de componentes na fila do COM+.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas de componentes em fila COM+](com--queued-components-tasks.md)
</dt> </dl>

 

 




