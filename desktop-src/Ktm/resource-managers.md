---
description: Gerenciadores de recursos
ms.assetid: c717b731-cf0b-45cb-bbff-695410fcf6ce
title: Gerenciadores de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d32d697d58705760002065d005f5927717055f235358c12fd0629de86e14b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870016"
---
# <a name="resource-managers"></a>Gerenciadores de recursos

Um Gerenciador de recursos usa o log do Gerenciador de transações para acompanhar o estado da transação. A ação do Gerenciador de recursos ao processar uma transação é a seguinte:

-   O cliente passa explicitamente uma transação para o RM.
-   O RM se inscreve na transação usando [**Createalistaing**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment).
-   Em seguida, o usuário pode continuar executando qualquer operação.
-   Quando o usuário chama CommitTransaction, o KTM envia uma notificação de preparação de \_ transação para o RM. Neste ponto, o RM libera para o disco as alterações que seriam necessárias para confirmar a transação, mas poderia falhar. Se essas operações forem realizadas com sucesso, o RM sinalizará que ela foi concluída com a operação de preparação chamando [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete). Se essas operações falharem, o RM responderá chamando [**RollBackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).
-   O Gerenciador de recursos recebe uma notificação de preparação.
-   O Gerenciador de recursos libera todos os dados associados à transação para seu arquivo de log de serviços de log comum.
-   O Gerenciador de recursos chama a função [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) e aguarda para receber o resultado da transação do KTM.
-   Dependendo do resultado da transação, o Gerenciador de recursos recebe um evento de notificação de confirmação ou reversão. Se o Gerenciador de recursos receber uma notificação de confirmação, ele tornará as alterações permanentes e informará o KTM chamando a função [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) . Se o Gerenciador de recursos receber uma notificação de reversão, ele descartará todas as alterações e reverterá para o estado que existia antes de qualquer uma das alterações transacionadas e informará o KTM chamando [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete).

## <a name="resource-manager-functions"></a>Funções do Gerenciador de recursos

As funções a seguir são usadas com gerenciadores de recursos.



| Função                                                                           | Descrição                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Cria um novo objeto do Gerenciador de recursos (RM) e associa o RM a um Gerenciador de transações (TM).                                                                               |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Solicita e recebe uma notificação para um Gerenciador de recursos (RM). Essa função é usada pelo registro do RM para receber notificações quando um estado de transação é alterado.            |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Solicita e recebe notificação assíncrona para um Gerenciador de recursos (RM). Essa função é usada pelo registro do RM para receber notificações quando um estado de transação é alterado. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Abre um Gerenciador de recursos (RM) existente.                                                                                                                                         |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indica que o RM (Gerenciador de recursos) concluiu todo o processamento necessário para garantir que uma operação de confirmação ou anulação terá sucesso para a transação especificada.        |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Sinaliza que este gerenciador de recursos concluiu seu trabalho de preprepare, para que outros gerenciadores de recursos agora possam iniciar suas operações de preparação.                                    |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Associa a porta de conclusão de e/s especificada ao Gerenciador de recursos especificado (RM). Esta porta recebe todas as notificações para o RM.                                          |



 

 

 



