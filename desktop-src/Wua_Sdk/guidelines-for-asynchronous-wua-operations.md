---
description: Este tópico identifica as diretrizes a serem seguidas quando você executar operações do WUA (agente de Windows Update assíncrono).
ms.assetid: 1fb16904-732d-4341-8267-ab8896fc0f7c
title: Diretrizes para operações assíncronas do WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a4b2198a235d9a03e3730e5d6dce2cd54c0e1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793893"
---
# <a name="guidelines-for-asynchronous-wua-operations"></a>Diretrizes para operações assíncronas do WUA

Este tópico identifica as diretrizes a serem seguidas quando você executar operações do WUA (agente de Windows Update assíncrono).

-   As operações assíncronas do WUA não garantem nenhuma velocidade de conclusão específica. O tempo de conclusão para uma operação assíncrona do WUA pode variar muito dependendo do hardware do computador, da versão do sistema operacional e da configuração de rede. Assim como acontece com outras APIs do Windows que têm dependências de rede e que não contêm um parâmetro de tempo limite ou uma duração de tempo limite documentada, recomendamos que você considere a implementação de seus próprios mecanismos de tempo limite se precisar de tempos de resposta garantidos. Por exemplo, você pode criar um thread de trabalho que chama um método WUA assíncrono e que define um evento ou outro objeto de sincronização quando a operação assíncrona do WUA é concluída; o thread principal pode usar a função [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) ou [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) , que permite que você especifique um valor de tempo limite.
-   Ao terminar uma pesquisa, download, instalação ou desinstalação de atualizações, você pode usar [**IUpdateSearcher:: endsearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch), [**IUpdateDowloader:: enddownload**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader), [**IUpdateInstaller:: noinstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall) e [**IUpdateInstaller:: enduninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall) de qualquer thread.
-   Ao iniciar uma pesquisa, download, instalação ou desinstalação de atualizações usando [**IUpdateSearcher:: BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader:: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller:: BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)e [**IUpdateInstaller:: BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall), certifique-se de manter a permissões de acesso suficiente ao liberar referências a objetos da API do WUA.
    -   Verifique se todos os objetos de retorno de chamada usados na operação assíncrona não são referenciados antes de destruí-los. Aguarde até que a contagem de referência de um objeto de retorno de chamada retorne ao valor inicial antes de destruí-lo.
    -   A referência ao objeto de trabalho que é retornado do método **begin** correspondente deve ser controlada por um objeto diferente dos objetos de retorno de chamada. Use um objeto que seja diferente dos objetos de retorno de chamada para evitar referências circulares.
    -   Se você tentar controlar a referência ao objeto de trabalho usando um objeto de retorno de chamada, deverá chamar o método [**IDownloadJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)ou [**ISearchJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) fora da função de retorno de chamada para desconectar o objeto de trabalho do objeto de retorno de chamada. Você deve fazer isso antes de liberar a referência ao objeto de trabalho que é retornado pelo método **begin** .
-   Verifique se as operações assíncronas do WUA foram concluídas. O Windows Script Host pode encerrar um script quando todos os comandos fora de qualquer função forem concluídos, mesmo que a API do WUA ainda tenha referências ao objeto de retorno de chamada.
    -   Use um dos métodos de **limpeza** ou faça com que a função de retorno de chamada defina uma variável global compartilhada após a conclusão.
    -   Nunca chame [**IDownloadJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)ou [**ISearchJob:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) em um objeto de trabalho em sua função de retorno de chamada.
    -   Para garantir a sequência de limpeza correta em um script em execução no Windows Internet Explorer, chame o método de **limpeza** em todos os objetos de trabalho ao processar Window. onBeforeUnload.
-   Não use os tipos de dados definidos pelo usuário (UDT) para operações assíncronas do WUA. O tipo não é suportado por [**IUpdateSearcher:: BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader:: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller:: BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)ou [**IUpdateInstaller:: BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall).

 

 
