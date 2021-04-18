---
description: A interface IUpdate define as propriedades a seguir.
ms.assetid: d87544f1-a107-440f-8ce0-77d9f2d90578
title: Propriedades de IUpdate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df3f67f95936ea54dd09131e605da9e439caa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501869"
---
# <a name="iupdate-properties"></a>Propriedades de IUpdate

A interface [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) define as propriedades a seguir.



| Propriedade                                                                           | Descrição                                                                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutoSelectOnWebSites**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_autoselectonwebsites)                       | Obtém um valor booliano que indica se a atualização está sinalizada para ser selecionada automaticamente pelo Windows Update.                                                                   |
| [**BundledUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_bundledupdates)                                   | Obtém uma interface que contém informações sobre a lista ordenada das atualizações agrupadas para a atualização.                                                                           |
| [**Canrequirename**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_canrequiresource)                               | Obtém um valor booliano que indica se a mídia de origem da atualização é necessária para instalação ou desinstalação.                                                          |
| [**Categorias**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_categories)                                           | Obtém uma interface que contém uma coleção de categorias à qual a atualização pertence.                                                                                             |
| [**Prazo**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deadline)                                               | Obtém a data até a qual a atualização deve ser instalada.                                                                                                                                |
| [**DeltaCompressedContentAvailable**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentavailable) | Obtém um valor booliano que indica se o conteúdo compactado Delta está disponível em um servidor para a atualização.                                                                       |
| [**DeltaCompressedContentPreferred**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deltacompressedcontentpreferred) | Obtém um valor booliano que indica se o conteúdo compactado por Delta deve ser preferido durante o download e a instalação ou desinstalação da atualização se o conteúdo compactado por Delta estiver disponível. |
| [**Deploymentaction**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_deploymentaction)                               | Obtém a ação para a qual a atualização está implantada.                                                                                                                                   |
| [**Descrição**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_description)                                         | Obtém a descrição localizada da atualização.                                                                                                                                       |
| [**DownloadContents**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadcontents)                               | Obtém informações de arquivo sobre o conteúdo de download da atualização.                                                                                                                    |
| [**DownloadPriority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_downloadpriority)                               | Obtém a prioridade de download sugerida da atualização.                                                                                                                                 |
| [**EulaAccepted**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulaaccepted)                                       | Obtém um valor booliano que indica se os termos de licença para software Microsoft associados à atualização são aceitos para o computador.                                 |
| [**EulaText**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_eulatext)                                               | Obtém o texto localizado completo dos termos de licença para software Microsoft associados à atualização.                                                                           |
| [**Handlerid**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_handlerid)                                             | Obtém o manipulador de instalação da atualização.                                                                                                                                             |
| [**Identidade**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_identity)                                               | Obtém uma interface que contém o identificador exclusivo da atualização.                                                                                                                |
| [**Imagem**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_image)                                                     | Obtém uma interface que contém informações sobre uma imagem associada à atualização.                                                                                      |
| [**InstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_installationbehavior)                       | Obtém uma interface que contém as opções de instalação da atualização.                                                                                                             |
| [**Isbeta**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isbeta)                                                   | Obtém um valor booliano que indica se a atualização é uma versão beta.                                                                                                           |
| [**Isdownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isdownloaded)                                       | Obtém um valor booliano que indica se todo o conteúdo de atualização é armazenado em cache no computador.                                                                                       |
| [**IsHidden**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)                                               | Obtém um valor booliano que indica se uma atualização está oculta por um usuário.                                                                                                          |
| [**IsInstalled**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isinstalled)                                         | Obtém um valor booliano que indica se a atualização está instalada em um computador quando a pesquisa é executada.                                                                     |
| [**Isobrigatório**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ismandatory)                                         | Obtém um valor booliano que indica se a instalação da atualização é obrigatória.                                                                                            |
| [**Isuninstallble**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_isuninstallable)                                 | Obtém um valor booliano que indica se um usuário pode desinstalar a atualização de um computador.                                                                                        |
| [**KBArticleIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_kbarticleids)                                       | Obtém uma coleção de IDs de artigos da base de dados de conhecimento Microsoft que estão associados à atualização.                                                                                      |
| [**Idiomas**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_languages)                                              | Obtém uma interface que contém os idiomas com suporte da atualização.                                                                                                     |
| [**LastDeploymentChangeTime**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_lastdeploymentchangetime)               | Obtém a data da última publicação da atualização, em data e hora do UTC (tempo Universal Coordenado), no servidor que implanta a atualização.                                               |
| [**MaxDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_maxdownloadsize)                                 | Obtém o tamanho máximo de download da atualização.                                                                                                                                       |
| [**MinDownloadSize**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_mindownloadsize)                                 | Obtém o tamanho mínimo de download da atualização.                                                                                                                                       |
| [**MoreInfoUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_moreinfourls)                                       | Obtém uma coleção de cadeias de caracteres específicas do idioma que especificam os hiperlinks para obter mais informações sobre a atualização.                                                                    |
| [**MsrcSeverity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_msrcseverity)                                       | Obtém a classificação de gravidade do Microsoft Security Response Center da atualização.                                                                                                          |
| [**RecommendedCPUSpeed**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed)                         | Obtém a velocidade de CPU recomendada usada para instalar a atualização, em megahertz (MHz).                                                                                                      |
| [**RecommendedHardDiskSpace**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace)               | Obtém o espaço livre recomendado que deve estar disponível no disco rígido antes de instalar a atualização. O espaço livre é especificado em megabytes (MB).                             |
| [**RecommendedMemory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_recommendedmemory)                             | Obtém o tamanho da memória física recomendada que deve estar disponível em seu computador antes de instalar a atualização. O tamanho da memória física é especificado em megabytes (MB).         |
| [**ReleaseNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_releasenotes)                                       | Obtém as notas de versão localizadas para a atualização.                                                                                                                                    |
| [**SecurityBulletinIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_securitybulletinids)                         | Obtém uma coleção de valores de cadeia de caracteres que contêm as IDs de boletim de segurança que estão associadas à atualização.                                                                      |
| [**SupersededUpdateIDs**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supersededupdateids)                         | Obtém uma coleção de identificadores de atualização. Essa coleção de identificadores especifica as atualizações que são substituídas pela atualização.                                                    |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_supporturl)                                           | Obtém um hiperlink para as informações de suporte específicas a um idioma para a atualização.                                                                                                       |
| [**Título**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)                                                     | Obtém o título localizado da atualização.                                                                                                                                             |
| [**Escreva**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_type)                                                       | Obtém o tipo da atualização.                                                                                                                                                        |
| [**UninstallationBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationbehavior)                   | Obtém uma interface que contém as opções de desinstalação para a atualização.                                                                                                          |
| [**UninstallationNotes**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationnotes)                         | Obtém as notas de desinstalação da atualização.                                                                                                                                       |
| [**UninstallationSteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_uninstallationsteps)                         | Obtém uma interface que contém as etapas de desinstalação para a atualização.                                                                                                            |



 

 

 



