---
description: O Synchronization Manager inclui componentes de interface do usuário, como as caixas de diálogo com guias no serviço SyncMgr, caixas de diálogo de erro e diálogos de progresso.
title: Arquitetura do Synchronization Manager
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 584329a06ee9df80558d9961b734b62a57d5ebccd83f200690812fa99132b06d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451862"
---
# <a name="synchronization-manager-architecture"></a>Arquitetura do Synchronization Manager

O Synchronization Manager inclui componentes de interface do usuário, como as caixas de diálogo com guias no serviço SyncMgr, caixas de diálogo de erro e diálogos de progresso. Com os componentes de interface do usuário, o usuário final pode agendar aplicativos para sincronização e configurar a sincronização automática para ocorrer em conjunto com eventos do sistema especificados. Por exemplo, o SyncMgr pode ser invocado no logon do usuário ou no desligamento do sistema. O usuário também pode invocar uma sincronização manual.

O usuário seleciona um aplicativo e especifica os itens dentro do aplicativo a serem sincronizados e define um evento de gatilho. Por exemplo, em um aplicativo de email, a Caixa de Entrada, a Caixa de Saída ou alguma outra pasta que contém mensagens pode ser um item separado para o aplicativo.

O SyncMgr também inclui uma interface de programação para que os aplicativos possam se registrar para usar recursos de sincronização, processar erros e receber informações de progresso e notificações durante o processo de sincronização.

 

 



