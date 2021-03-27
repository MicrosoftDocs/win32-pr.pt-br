---
description: O Synchronization Manager inclui componentes de interface do usuário, como as caixas de diálogo com guias no serviço SyncMgr, diálogos de erro e caixas de diálogo de progresso.
title: Arquitetura do Gerenciador de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f178b407c1f7d568c9de2ce7c81d937e7d1cdef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663491"
---
# <a name="synchronization-manager-architecture"></a>Arquitetura do Gerenciador de sincronização

O Synchronization Manager inclui componentes de interface do usuário, como as caixas de diálogo com guias no serviço SyncMgr, diálogos de erro e caixas de diálogo de progresso. Com os componentes da interface do usuário, o usuário final pode agendar aplicativos para sincronização e configurar a sincronização automática para ocorrer em conjunto com os eventos do sistema especificados. Por exemplo, o SyncMgr pode ser invocado no logon do usuário ou no desligamento do sistema. O usuário também pode invocar uma sincronização manual.

O usuário seleciona um aplicativo e especifica os itens dentro do aplicativo a ser sincronizado e define um evento de gatilho. Por exemplo, em um aplicativo de email, a caixa de entrada, caixa de saída ou alguma outra pasta contendo mensagens pode ser um item separado para o aplicativo.

O SyncMgr também inclui uma interface de programação para que os aplicativos possam se registrar para usar recursos de sincronização, podem processar erros e receber informações de progresso e notificações durante o processo de sincronização.

 

 



