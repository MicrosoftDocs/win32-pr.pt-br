---
description: Descreve os conceitos básicos de e/s.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: Conceitos de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761731"
---
# <a name="io-concepts"></a>Conceitos de e/s

Os seguintes conceitos de e/s são descritos nesta seção.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                               | Descrição                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Buffer de arquivo](file-buffering.md)<br/>                                     | Descreve as considerações sobre O controle de aplicativo do buffer de arquivo, também conhecido como e/s (entrada/saída) de arquivo sem buffer.<br/>                                    |
| [Cache de arquivo](file-caching.md)<br/>                                         | O Windows armazena em cache os dados de arquivo que são lidos de discos e gravados em discos.<br/>                                                                                   |
| [E/s síncrona e síncrona](synchronous-and-asynchronous-i-o.md)<br/> | Há dois tipos de sincronização de e/s (entrada/saída): e/s síncrona e e/SS assíncrona. E/s assíncrona também é conhecida como e/s sobreposta.<br/> |
| [Cancelando operações de e/s pendentes](canceling-pending-i-o-operations.md)<br/> | Permitir que os usuários cancelem solicitações de e/s lentas ou bloqueadas pode melhorar a usabilidade e a robustez do seu aplicativo.<br/>                             |
| [E/s alertável](alertable-i-o.md)<br/>                                       | E/s de alerta é o método pelo qual os threads de aplicativo processam solicitações de e/s assíncronas somente quando estão em um estado de alerta.<br/>                     |
| [Portas de conclusão de e/s](i-o-completion-ports.md)<br/>                         | As portas de conclusão de e/s fornecem um modelo de Threading eficiente para processar várias solicitações de e/s assíncronas em um sistema multiprocessador.<br/>                  |



 

 

 




