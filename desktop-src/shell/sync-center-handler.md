---
description: Este tópico fornece um exame passo a passo dos requisitos para criar um arquivo DLL que implementa um manipulador a ser usado com a central de sincronização. Essas informações são válidas a partir do Windows Vista.
title: Desenvolvendo um manipulador da central de sincronização do Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 66b40f81-9515-4190-8ced-44f20bb9df86
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 11185aa5976c27b7af95787b081e1eaacd99c8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967962"
---
# <a name="developing-a-windows-sync-center-handler"></a>Desenvolvendo um manipulador da central de sincronização do Windows

Este tópico fornece um exame passo a passo dos requisitos para criar um arquivo DLL que implementa um manipulador a ser usado com a central de sincronização. Essas informações são válidas a partir do Windows Vista.

-   [A experiência de sincronização do Windows antes do vista](#the-windows-synchronization-experience-before-vista)
-   [APIs da central de sincronização](#sync-center-apis)
    -   [Interfaces essenciais](#essential-interfaces)

## <a name="the-windows-synchronization-experience-before-vista"></a>A experiência de sincronização do Windows antes do vista

O Windows XP fornecia um [Gerenciador de sincronização](syncmgr-start-page.md) (mobsync.exe). Muitos dispositivos, como players de MP3, celulares e câmeras, também forneciam suas próprias interfaces de sincronização em vez de usar o Gerenciador de sincronização. Isso resultou em uma experiência de usuário inconsistente e não centralizada.

O novo recurso da central de sincronização fornecido no Windows Vista tem várias vantagens em relação ao Gerenciador de sincronização mais antigo.

-   Melhor descoberta
-   Menos necessidade de ação direta do usuário
-   Não bloqueia outras operações
-   Melhor visualização do progresso da sincronização
-   Mais fácil de entender o modelo de desenvolvimento

## <a name="sync-center-apis"></a>APIs da central de sincronização

A central de sincronização se comunica com manipuladores por meio de várias interfaces de Component Object Model (COM). Nem todas essas interfaces são necessárias para implementar um manipulador de central de sincronização. Este tópico foi dividido em duas seções. A primeira seção explica as interfaces COM essenciais que cada manipulador deve oferecer suporte e a segunda seção examina as interfaces COM opcionais e examina os motivos pelos quais um manipulador ofereceria suporte a elas.

-   [Interfaces essenciais](#essential-interfaces)

### <a name="essential-interfaces"></a>Interfaces essenciais

Todos os manipuladores da central de sincronização devem dar suporte às seguintes interfaces:

-   [**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler)
-   [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo)
-   [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer)
-   [**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems)
-   [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem)
-   [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo)

[**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) e [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) são usados para descrever um único item de sincronização envolvido na sincronização para a central de sincronização. Um item de sincronização geralmente representa um tipo de dados específico (como imagens) ou um local específico de dados.

Os itens de sincronização que representam diferentes locais de dados permitem sincronizações muito específicas. A granularidade do local é até o autor do manipulador, mas deve-se ter cuidado com o design. Se houver poucos itens de sincronização (locais), o usuário será restrito em sua capacidade de sincronizar apenas determinados dados. No outro extremo, muita granularidade pode se tornar não gerenciável.

Se um manipulador oferecer suporte a mais de um tipo de dados ou a vários locais de dados, ele precisará dar suporte a mais de um objeto de item de sincronização. Um exemplo pode ser um PDA (Assistente de dados pessoais) que permite ao usuário sincronizar contatos, itens de calendário e documentos. Esses três tipos de dados precisariam ser representados por três objetos exclusivos que expõem as interfaces [**ISyncMgrSyncItem**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem) e [**ISyncMgrSyncItemInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo) .

A interface [**IEnumSyncMgrSyncItems**](/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems) fornece um mecanismo para enumerar por meio de itens de sincronização de um manipulador. Para recuperar esse enumerador, a central de sincronização chama o método [**ISyncMgrSyncItemContainer:: GetSyncItemEnumerator**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator) exposto pelo manipulador. O [**ISyncMgrSyncItemContainer**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer) também contém dois outros métodos que a central de sincronização pode usar para recuperar informações sobre os itens de sincronização do manipulador:

-   [**GetSyncItem**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem) retorna um item de sincronização específico.
-   [**GetSyncItemCount**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount) retorna o número de itens de sincronização com suporte pelo manipulador.

[**ISyncMgrHandler**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler) e [**ISyncMgrHandlerInfo**](/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo) são usados para descrever as propriedades do manipulador e iniciar a sincronização real. [**ISyncMgrHandler:: Synchronize**](/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandler-synchronize) é onde o código do manipulador executa a sincronização e fornece comentários sobre o progresso e quaisquer problemas que ocorram.

Muitos dos métodos de interface não precisam ser totalmente implementados. A central de sincronização fornece uma determinada quantidade de informações padrão. As interfaces permitem que um manipulador substitua essas informações e forneça informações personalizadas a serem exibidas, se necessário.

 

 



