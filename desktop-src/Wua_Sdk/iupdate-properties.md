---
description: A interface IUpdate define as propriedades a seguir.
ms.assetid: d87544f1-a107-440f-8ce0-77d9f2d90578
title: Propriedades de IUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93db8e7d8d6786e3f3f827d9eb2e9f97c43aae4781edf0a05fcf6d03e8fb1f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859854"
---
# <a name="iupdate-properties"></a>Propriedades de IUpdate

A [**interface IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) define as propriedades a seguir.



| Propriedade                                                                           | Descrição                                                                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoSelectOnWebSites**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_autoselectonwebsites)                       | Obtém um valor booliana que indica se a atualização é sinalizada para ser selecionada automaticamente pelo Windows Update.                                                                   |
| [**BundledUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_bundledupdates)                                   | Obtém uma interface que contém informações sobre a lista ordenada das atualizações agrupadas para a atualização.                                                                           |
| [**CanRequireSource**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_canrequiresource)                               | Obtém um valor booliana que indica se a mídia de origem da atualização é necessária para instalação ou desinstalação.                                                          |
| [**Categorias**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_categories)                                           | Obtém uma interface que contém uma coleção de categorias às quais a atualização pertence.                                                                                             |
| [**Prazo**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deadline)                                               | Obtém a data pela qual a atualização deve ser instalada.                                                                                                                                |
| [**DeltaCompressedContentAvailable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentavailable) | Obtém um valor booliana que indica se o conteúdo compactado em delta está disponível em um servidor para a atualização.                                                                       |
| [**DeltaCompressedContentPreferred**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentpreferred) | Obtém um valor boolano que indica se o conteúdo compactado delta deve ser preferível durante o download e a instalação ou desinstalação da atualização se o conteúdo compactado por delta estiver disponível. |
| [**DeploymentAction**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deploymentaction)                               | Obtém a ação para a qual a atualização é implantada.                                                                                                                                   |
| [**Descrição**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_description)                                         | Obtém a descrição localizada da atualização.                                                                                                                                       |
| [**DownloadContents**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadcontents)                               | Obtém informações de arquivo sobre o conteúdo de download da atualização.                                                                                                                    |
| [**DownloadPriority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadpriority)                               | Obtém a prioridade de download sugerida da atualização.                                                                                                                                 |
| [**EulaAccepted**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulaaccepted)                                       | Obtém um valor boolano que indica se os Termos de Licença para Software Microsoft associados à atualização são aceitos para o computador.                                 |
| [**EulaText**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulatext)                                               | Obtém o texto localizado completo do Termos de Licença para Software Microsoft que estão associados à atualização.                                                                           |
| [**HandlerID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_handlerid)                                             | Obtém o manipulador de instalação da atualização.                                                                                                                                             |
| [**Identidade**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_identity)                                               | Obtém uma interface que contém o identificador exclusivo da atualização.                                                                                                                |
| [**Imagem**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_image)                                                     | Obtém uma interface que contém informações sobre uma imagem associada à atualização.                                                                                      |
| [**InstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_installationbehavior)                       | Obtém uma interface que contém as opções de instalação da atualização.                                                                                                             |
| [**IsBeta**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isbeta)                                                   | Obtém um valor booliana que indica se a atualização é uma versão beta.                                                                                                           |
| [**IsDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isdownloaded)                                       | Obtém um valor booliana que indica se todo o conteúdo de atualização é armazenado em cache no computador.                                                                                       |
| [**IsHidden**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)                                               | Obtém um valor booliana que indica se uma atualização está oculta por um usuário.                                                                                                          |
| [**IsInstalled**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isinstalled)                                         | Obtém um valor booliana que indica se a atualização é instalada em um computador quando a pesquisa é executada.                                                                     |
| [**IsMandatory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ismandatory)                                         | Obtém um valor booliana que indica se a instalação da atualização é obrigatória.                                                                                            |
| [**IsUninstallable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isuninstallable)                                 | Obtém um valor booliana que indica se um usuário pode desinstalar a atualização de um computador.                                                                                        |
| [**KBArticleIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_kbarticleids)                                       | Obtém uma coleção Base de Dados de Conhecimento Microsoft IDs de artigo que estão associadas à atualização.                                                                                      |
| [**Idiomas**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_languages)                                              | Obtém uma interface que contém os idiomas com suporte pela atualização.                                                                                                     |
| [**LastDeploymentChangeTime**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_lastdeploymentchangetime)               | Obtém a última data de publicação da atualização, em Tempo Universal Coordenado (UTC) e hora, no servidor que implanta a atualização.                                               |
| [**MaxDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_maxdownloadsize)                                 | Obtém o tamanho máximo de download da atualização.                                                                                                                                       |
| [**MinDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_mindownloadsize)                                 | Obtém o tamanho mínimo de download da atualização.                                                                                                                                       |
| [**MoreInfoUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_moreinfourls)                                       | Obtém uma coleção de cadeias de caracteres específicas de linguagem que especificam os hiperlinks para obter mais informações sobre a atualização.                                                                    |
| [**MsrcSeverity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_msrcseverity)                                       | Obtém a Microsoft Security Response Center de gravidade da atualização.                                                                                                          |
| [**RecommendedCPUSpeed**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed)                         | Obtém a velocidade de CPU recomendada usada para instalar a atualização, em megahertz (MHz).                                                                                                      |
| [**RecommendedHardDiskSpace**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace)               | Obtém o espaço livre recomendado que deve estar disponível no disco rígido antes de instalar a atualização. O espaço livre é especificado em megabytes (MB).                             |
| [**RecommendedMemory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedmemory)                             | Obtém o tamanho de memória física recomendado que deve estar disponível em seu computador antes de instalar a atualização. O tamanho da memória física é especificado em megabytes (MB).         |
| [**ReleaseNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_releasenotes)                                       | Obtém as notas de versão localizadas para a atualização.                                                                                                                                    |
| [**SecurityBulletinIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_securitybulletinids)                         | Obtém uma coleção de valores de cadeia de caracteres que contêm as IDs de boletim de segurança associadas à atualização.                                                                      |
| [**SupersededUpdateIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supersededupdateids)                         | Obtém uma coleção de identificadores de atualização. Essa coleção de identificadores especifica as atualizações que são superadas pela atualização.                                                    |
| [**Supporturl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supporturl)                                           | Obtém um hiperlink para as informações de suporte específicas do idioma para a atualização.                                                                                                       |
| [**Título**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)                                                     | Obtém o título localizado da atualização.                                                                                                                                             |
| [**Tipo**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_type)                                                       | Obtém o tipo da atualização.                                                                                                                                                        |
| [**DesinstalarBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationbehavior)                   | Obtém uma interface que contém as opções de desinstalação para a atualização.                                                                                                          |
| [**DesinstalaçãoNotas**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationnotes)                         | Obtém as notas de desinstalação para a atualização.                                                                                                                                       |
| [**DesinstalaçãoEtapas**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationsteps)                         | Obtém uma interface que contém as etapas de desinstalação para a atualização.                                                                                                            |



 

 

 



