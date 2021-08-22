---
description: Este tópico identifica as diretrizes a seguir ao executar operações assíncronas Windows WUA (Update Agent).
ms.assetid: 1fb16904-732d-4341-8267-ab8896fc0f7c
title: Diretrizes para operações assíncronas do WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24801c7639e75f34f1517ee626ff7acb7c1d13f85a6ebf57e7d824f7f0d3191d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049484"
---
# <a name="guidelines-for-asynchronous-wua-operations"></a>Diretrizes para operações assíncronas do WUA

Este tópico identifica as diretrizes a seguir ao executar operações assíncronas Windows WUA (Update Agent).

-   As operações assíncronas do WUA não garantem nenhuma velocidade de conclusão específica. O tempo de conclusão de uma operação ASSíncrona WUA pode variar muito dependendo do hardware do computador, da versão do sistema operacional e da configuração de rede. Assim como acontece com outras APIs do Windows que têm dependências de rede e que não contêm um parâmetro de tempo-out ou uma duração de tempo-out documentada, recomendamos que você considere a implementação de seus próprios mecanismos de tempo-máximo se precisar de tempos de resposta garantidos. Por exemplo, você pode criar um thread de trabalho que chama um método WUA assíncrono e que define um evento ou outro objeto de sincronização quando a operação WUA assíncrona é concluída; O thread principal pode usar a [**função WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) ou [**WaitForMultipleObjects,**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) que permite especificar um valor de tempo-out.
-   Ao encerrar uma pesquisa, download, instalação ou desinstalação de atualizações, você pode usar [**IUpdateSearcher::EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch), [**IUpdateDowloader::EndDownload**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader), [**IUpdateInstaller::EndInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall) e [**IUpdateInstaller::EndUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall) de qualquer thread.
-   Ao iniciar uma pesquisa, download, instalação ou desinstalação de atualizações usando [**IUpdateSearcher::BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader::BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller::BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)e [**IUpdateInstaller::BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall), certifique-se de manter as permissões de acesso suficientes ao liberar referências a objetos da API WUA.
    -   Certifique-se de que todos os objetos de retorno de chamada usados na operação assíncrona não sejam identificados antes de você os destruir. Aguarde até que a contagem de referência de um objeto de retorno de chamada retorne ao valor inicial antes de destruir.
    -   A referência ao objeto de trabalho retornado do método **Begin** correspondente deve ser controlada por um objeto que difere dos objetos de retorno de chamada. Use um objeto que difere dos objetos de retorno de chamada para evitar referências circulares.
    -   Se você tentar controlar a referência ao objeto de trabalho usando um objeto de retorno de chamada, deverá chamar o método [**IDownloadJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)ou [**ISearchJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) fora da função de retorno de chamada para desconectar o objeto de trabalho do objeto de retorno de chamada. Você deve fazer isso antes de liberar a referência ao objeto de trabalho retornado pelo **método Begin.**
-   Certifique-se de que as operações assíncronas do WUA estão concluídas. Windows O Host de Script pode encerrar um script quando todos os comandos fora de qualquer função são concluídos, mesmo que a API WUA ainda tenha referências ao objeto de retorno de chamada.
    -   Use um dos métodos **CleanUp** ou fazer com que a função de retorno de chamada desempaque uma variável global compartilhada após a conclusão.
    -   Nunca chame [**IDownloadJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob::CleanUp**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)ou [**ISearchJob::CleanUp em**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) um objeto de trabalho em sua função de retorno de chamada.
    -   Para garantir a sequência de limpeza correta em um script em execução no Windows Internet Explorer, chame o método **CleanUp** em todos os objetos de trabalho ao processar window.onbeforeunload.
-   Não use UDT (tipos de dados definidos pelo usuário) para operações WUA assíncronas. O tipo não é suportado por [**IUpdateSearcher::BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader::BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller::BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)ou [**IUpdateInstaller::BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall).

 

 
