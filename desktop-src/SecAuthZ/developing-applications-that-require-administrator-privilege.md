---
description: É possível desenvolver um aplicativo que executa operações que exigem privilégios de administrador, ainda que sejam executadas como um usuário padrão.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Desenvolvendo aplicativos que exigem privilégios de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d22687dad0a8914c5dcaebe8ea85a525529a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751609"
---
# <a name="developing-applications-that-require-administrator-privilege"></a>Desenvolvendo aplicativos que exigem privilégios de administrador

É possível desenvolver um aplicativo que executa operações que exigem privilégios de administrador, ainda que sejam executadas como um usuário padrão.

Há vários modelos para realizar isso.



| Tópico                                                                | Descrição                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modelo de tarefa elevada](elevated-task-model.md)                       | Um aplicativo em execução como um usuário padrão executa operações que exigem privilégios de administrador, iniciando uma tarefa agendada.                                                                     |
| [Modelo de serviço do sistema operacional](operating-system-service-model.md) | Um aplicativo em execução como um usuário padrão se comunica com um serviço em execução como **sistema** usando RPC ( [chamada de procedimento remoto](/windows/desktop/Rpc/rpc-start-page) ).                                              |
| [Modelo de agente do administrador](administrator-broker-model.md)         | O aplicativo é dividido em dois programas. Um dos programas é executado como usuário padrão e o outro é executado com o privilégio de administrador.                                                          |
| [Modelo de objeto COM do administrador](administrator-com-object-model.md) | Um aplicativo em execução como um usuário padrão executa operações que exigem privilégios de administrador criando um objeto de [Component Object Model](/windows/desktop/com/component-object-model--com--portal) elevado. |



 

 

 
