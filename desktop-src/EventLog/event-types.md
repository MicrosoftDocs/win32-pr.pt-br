---
description: Há cinco tipos de eventos que podem ser registrados em log. Todos eles têm dados comuns bem definidos e podem, opcionalmente, incluir dados específicos de eventos.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Tipos de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e94ae69445f660e54c630734b93297acad593c127f32b9d3abfa94f9cd2fc06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069556"
---
# <a name="event-types"></a>Tipos de eventos

Há cinco tipos de eventos que podem ser registrados em log. Todos eles têm dados comuns bem definidos e podem, opcionalmente, incluir dados específicos de eventos.

O aplicativo indica o tipo de evento quando relata um evento. Cada evento deve ser de um único tipo. O Visualizador de Eventos exibe um ícone diferente para cada tipo na exibição de lista do log de eventos.

A tabela a seguir descreve os cinco tipos de evento usados no log de eventos.



| Tipo de evento        | Descrição                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Erro**         | Um evento que indica um problema significativo, como perda de dados ou perda de funcionalidade. Por exemplo, se um serviço não for carregado durante a inicialização, um evento de erro será registrado.                                                                                                                           |
| **Aviso**       | Um evento que não é necessariamente significativo, mas pode indicar um possível problema futuro. Por exemplo, quando há pouco espaço em disco, um evento de aviso é registrado. Se um aplicativo puder se recuperar de um evento sem perda de funcionalidade ou dados, ele geralmente poderá classificar o evento como um evento de aviso.     |
| **Informações**   | Um evento que descreve a operação bem-sucedida de um aplicativo, driver ou serviço. Por exemplo, quando um driver de rede é carregado com êxito, pode ser apropriado registrar um evento de informações. Observe que geralmente é inapropriado que um aplicativo de área de trabalho registre um evento sempre que ele for iniciado. |
| **Auditoria Bem-sucedida** | Um evento que registra uma tentativa de acesso de segurança auditada que é bem-sucedida. Por exemplo, a tentativa bem-sucedida do usuário de fazer logon no sistema é registrada como um evento de auditoria com êxito.                                                                                                                        |
| **Auditoria com Falha** | Um evento que registra uma tentativa de acesso de segurança auditada que falha. Por exemplo, se um usuário tentar acessar uma unidade de rede e falhar, a tentativa será registrada como um evento de auditoria de falha.                                                                                                                   |



 

As atividades selecionadas de usuários podem ser rastreadas por auditoria de eventos de segurança e, em seguida, colocando entradas no log de segurança de um computador.

 

 



