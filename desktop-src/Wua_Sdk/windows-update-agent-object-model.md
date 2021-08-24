---
description: Os programadores que usam o WUA (agente de atualização do Windows) começam adicionando uma referência ao Wuapi.dll ao projeto atual (em Visual C++, Microsoft Visual Basic ou C) ou referenciando \# Wuapi.h e Wuguid.lib em um projeto C ou C++.
ms.assetid: ec9cbb0b-b5d4-41f2-8a25-143130d08a3b
title: Windows Atualizar modelo de objeto do agente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b60f9306dfae5910418ddc07353a421e0325c0953fb1f47994ad007ded5ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855437"
---
# <a name="windows-update-agent-object-model"></a>Windows Atualizar modelo de objeto do agente

Os programadores que usam o WUA (agente de atualização do Windows) começam adicionando uma referência ao Wuapi.dll ao projeto atual (em Visual C++, Microsoft Visual Basic ou C) ou referenciando \# Wuapi.h e Wuguid.lib em um projeto C ou C++. A primeira etapa no uso da API WUA é criar uma instância de uma das interfaces criando um objeto da coclasse apropriada.

A ilustração a seguir descreve o modelo de objeto WUA. Para obter mais informações, consulte a seção "[Objetos WUA e tarefas associadas](#wua-objects-and-associated-tasks)". Para ver uma lista completa de todas as interfaces WUA, consulte [Interfaces](interfaces.md).

![modelo de objeto do agente do Windows Update](images/wua-object-model.png)

## <a name="wua-objects-and-associated-tasks"></a>Objetos WUA e tarefas associadas

A tabela a seguir lista os objetos WUA e as tarefas típicas associadas aos objetos WUA.



| Objeto                                                                | Descrição                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)                         | Comece, pause ou retome Atualizações Automáticas.                                                                                                                                                                                                  |
| [**AutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)         | Recuperar ou definir o dia e a hora para instalar atualizações. Especifique como os usuários são notificados sobre um Atualizações Automáticas evento.                                                                                                                          |
| [**Categoria**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)                                         | Recupere informações sobre a categoria da atualização, incluindo o nome, a ID, a descrição, o proprietário e o produto pretendido. Recupere uma coleção de atualizações que pertencem a essa categoria. Recupere uma coleção das categorias pai ou filho. |
| [**Categorycollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)                     | Acesse uma coleção de objetos Category.                                                                                                                                                                                                    |
| [**DownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadresult)                             | Recuperar informações sobre o resultado de um download.                                                                                                                                                                                        |
| [**InstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)                     | Recuperar informações sobre o resultado de uma instalação ou desinstalação. Determine se uma reinicialização do sistema é necessária para concluir a instalação ou desinstalação.                                                                  |
| [**Searchresult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)                                 | Recuperar informações sobre o resultado de uma pesquisa de categorias ou atualizações. Recupere uma coleção de categorias encontrada no computador de destino pela pesquisa. Recupere uma coleção de atualizações encontradas pela pesquisa.                     |
| [**Systeminformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)                       | Recupere informações sobre os requisitos de reinicialização do sistema e hardware do OEM no computador de destino.                                                                                                                                        |
| [**Atualizar**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)                                             | Recupere a maioria das informações sobre a atualização, incluindo atualizações agrupadas, requisitos de origem, identidade, descrição, opções de desinstalação, prioridade de download, tamanho e prazo.                                                                |
| [**UpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)                         | Acesse uma coleção de objetos Update.                                                                                                                                                                                                      |
| [**UpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)                         | Inicie um download assíncrono ou síncrono dos arquivos associados às atualizações.                                                                                                                                            |
| [**UpdateDownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadresult)                 | Recupere informações sobre o resultado do download para uma atualização.                                                                                                                                                                       |
| [**Updateexception**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)                           | Recupere a descrição e o contexto de uma exceção que é lançada quando ocorre um erro de atualização.                                                                                                                                            |
| [**UpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)       | Acesse uma coleção de objetos UpdateException.                                                                                                                                                                                             |
| [**UpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)                     | Recupere informações sobre uma atualização que foi instalada ou desinstalada, incluindo o aplicativo processado, a data e a descrição.                                                                                                    |
| [**UpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) | Acesse uma coleção de objetos UpdateHistoryEntry.                                                                                                                                                                                          |
| [**UpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)         | Recupere informações sobre o resultado da instalação ou da desinstalação de uma atualização.                                                                                                                                                  |
| [**UpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)                           | Inicie uma instalação assíncrona ou síncrona ou desinstalação de uma atualização. Inicie uma sequência de diálogo interativa para orientar o usuário pelas etapas para instalar atualizações.                                                              |
| [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)                             | Pesquisa atualizações no servidor por critérios como o tipo de atualização, a ID ou a categoria.                                                                                                                                            |
| [**UpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)                               | Inicie uma sessão para pesquisar, baixar, instalar ou desinstalar as atualizações de um aplicativo.                                                                                                                                                  |
| [**Webproxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)                                         | Recuperar e definir configurações de proxy HTTP.                                                                                                                                                                                                       |



 

 

 



