---
description: Os programadores que usam o WUA (Windows Update Agent) começam adicionando uma referência a Wuapi.dll ao seu projeto atual (em Visual C++, Microsoft Visual Basic ou C \# ) ou referenciando WUAPI. h e Wuguid. lib em um projeto C ou C++.
ms.assetid: ec9cbb0b-b5d4-41f2-8a25-143130d08a3b
title: Modelo de objeto do agente Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5060a76c850ea9ad97e9132f661d4b64f4f4fd03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556579"
---
# <a name="windows-update-agent-object-model"></a>Modelo de objeto do agente Windows Update

Os programadores que usam o WUA (Windows Update Agent) começam adicionando uma referência a Wuapi.dll ao seu projeto atual (em Visual C++, Microsoft Visual Basic ou C \# ) ou referenciando WUAPI. h e Wuguid. lib em um projeto C ou C++. A primeira etapa ao usar a API do WUA é criar uma instância de uma das interfaces criando um objeto da coclasse apropriada.

A ilustração a seguir descreve o modelo de objeto do WUA. Para obter mais informações, consulte a seção "[objetos do WUA e tarefas associadas](#wua-objects-and-associated-tasks)". Para obter uma lista completa de todas as interfaces do WUA, consulte [interfaces](interfaces.md).

![modelo de objeto do Windows Update Agent](images/wua-object-model.png)

## <a name="wua-objects-and-associated-tasks"></a>Objetos do WUA e tarefas associadas

A tabela a seguir lista os objetos do WUA e as tarefas típicas que estão associadas aos objetos WUA.



| Objeto                                                                | Descrição                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)                         | Iniciar, pausar ou retomar Atualizações Automáticas.                                                                                                                                                                                                  |
| [**AutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)         | Recupere ou defina o dia e a hora para instalar atualizações. Especifique como os usuários são notificados de um evento de Atualizações Automáticas.                                                                                                                          |
| [**Categoria**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)                                         | Recupere informações sobre a categoria da atualização, incluindo o nome, a ID, a descrição, o proprietário e o produto pretendido. Recuperar uma coleção de atualizações que pertencem a esta categoria. Recupere uma coleção de categorias pai ou filho. |
| [**Categoriacollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)                     | Acessar uma coleção de objetos Category.                                                                                                                                                                                                    |
| [**DownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadresult)                             | Recuperar informações sobre o resultado de um download.                                                                                                                                                                                        |
| [**InstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)                     | Recuperar informações sobre o resultado de uma instalação ou desinstalação. Determine se uma reinicialização do sistema é necessária para concluir a instalação ou desinstalação.                                                                  |
| [**SearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)                                 | Recuperar informações sobre o resultado de uma pesquisa de categorias ou atualizações. Recupere uma coleção de categorias encontradas no computador de destino pela pesquisa. Recuperar uma coleção de atualizações encontradas pela pesquisa.                     |
| [**SystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)                       | Recupere informações sobre o hardware OEM e requisitos de reinicialização do sistema no computador de destino.                                                                                                                                        |
| [**Cumulativo**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)                                             | Recupere a maioria das informações sobre a atualização, incluindo atualizações agrupadas, requisitos de origem, identidade, descrição, opções de desinstalação, prioridade de download, tamanho e prazo.                                                                |
| [**Updatecollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)                         | Acessar uma coleção de objetos de atualização.                                                                                                                                                                                                      |
| [**UpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)                         | Inicie um download assíncrono ou síncrono dos arquivos associados às atualizações.                                                                                                                                            |
| [**UpdateDownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadresult)                 | Recuperar informações sobre o resultado do download para uma atualização.                                                                                                                                                                       |
| [**UpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)                           | Recupere a descrição e o contexto de uma exceção que é lançada quando ocorre um erro de atualização.                                                                                                                                            |
| [**UpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)       | Acessar uma coleção de objetos UpdateException.                                                                                                                                                                                             |
| [**UpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)                     | Recuperar informações sobre uma atualização que foi instalada ou desinstalada, incluindo o aplicativo processado, a data e a descrição.                                                                                                    |
| [**UpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) | Acessar uma coleção de objetos UpdateHistoryEntry.                                                                                                                                                                                          |
| [**UpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)         | Recuperar informações sobre o resultado da instalação ou desinstalação de uma atualização.                                                                                                                                                  |
| [**UpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)                           | Iniciar uma instalação assíncrona ou síncrona ou desinstalação de uma atualização. Inicie uma sequência de diálogo interativa para orientar o usuário nas etapas para instalar as atualizações.                                                              |
| [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)                             | Pesquisa atualizações no servidor por critérios como o tipo de atualização, a ID ou a categoria.                                                                                                                                            |
| [**UpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)                               | Inicie uma sessão para pesquisar, baixar, instalar ou desinstalar as atualizações de um aplicativo.                                                                                                                                                  |
| [**Atualizar**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)                                         | Recuperar e definir as configurações de proxy HTTP.                                                                                                                                                                                                       |



 

 

 



