---
description: Para permitir que seu aplicativo funcione com o Gerenciador de sincronização, você deve implementar um objeto de Component Object Model (COM) para lidar com as notificações de sincronização recebidas do SyncMgr.
title: Usando o Gerenciador de sincronização de um programa
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bf18d493-0fe7-46e7-9686-f7ee75b3039b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9bd5abdc382c82c6c1aafcda3a967337384dc807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506235"
---
# <a name="using-synchronization-manager-from-a-program"></a>Usando o Gerenciador de sincronização de um programa

Para permitir que seu aplicativo funcione com o Gerenciador de sincronização, você deve implementar um objeto de Component Object Model (COM) para lidar com as notificações de sincronização recebidas do SyncMgr. O manipulador de seu aplicativo executa a sincronização para os itens que você manipula. Incluído em seu manipulador, você deve implementar a interface [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) . Além disso, você deve fornecer um objeto de enumerador e [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) para quaisquer itens separados que seu aplicativo possa sincronizar.

SyncMgr implementa [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) e [**ISyncMgrSynchronizeInvoke**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke).

O SyncMgr chama métodos em seu [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) para obter informações sobre os itens que seu aplicativo manipula e informações sobre o manipulador que você fornece para sincronizar esses itens.

Em tempo de execução, o processo de sincronização segue estas etapas.

1.  O SyncMgr notifica seu aplicativo de que é hora de que a sincronização ocorra para um dos itens que seu aplicativo manipula chamando o método [**ISyncMgrSynchronize:: Initialize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize) .
2.  SyncMgr chama [**ISyncMgrSynchronize:: EnumSyncMgrItems**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems) para obter a interface [**ISyncMgrEnumItems**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems) para os itens manipulados pelo seu aplicativo.
3.  SyncMgr chama [**ISyncMgrSynchronize:: SetProgressCallback**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback) para fornecer seu manipulador com o ponteiro de interface para a interface [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) . Seu manipulador usa essa interface para chamar de volta para o SyncMgr durante a sincronização.
4.  Em seguida, SyncMgr chama o método [**ISyncMgrSynchronize::P repareforsync**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync) para dar ao seu manipulador uma oportunidade de exibir qualquer elemento de interface do usuário necessário antes do início da sincronização. Por exemplo, um aplicativo de email pode exibir uma caixa de diálogo de logon do usuário.
5.  Seu manipulador chama [**ISyncMgrSynchronizeCallback:: EnableModeless**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless) antes e depois de exibir qualquer elemento da interface do usuário. Seu manipulador chama [**ISyncMgrSynchronizeCallback::P repareforsynccompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted) quando você terminar.
6.  SyncMgr chama o método [**ISyncMgrSynchronize:: Synchronize**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-synchronize) para iniciar a sincronização.

Durante o processo de sincronização, o SyncMgr continua a chamar métodos na sua interface [**ISyncMgrSynchronize**](/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize) . Ele pode enviar os erros, o progresso e as notificações do manipulador. Ele também pode enumerar por meio dos itens que seu aplicativo manipula ou permite que seu aplicativo mostre as propriedades dos itens.

Seu manipulador chama métodos em [**ISyncMgrSynchronizeCallback**](/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback) para determinar se um item deve ser ignorado, registrar em log erros e postar informações de progresso durante o processo de sincronização.

Para obter mais informações, consulte as páginas de referência relacionadas para as interfaces envolvidas.

Quando a sincronização for concluída, seu manipulador chamará [**ISyncMgrSynchronizeCallback:: SynchronizeCompleted**](/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted).

 

 



