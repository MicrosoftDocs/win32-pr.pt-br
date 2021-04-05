---
description: A interface IDownloadProgress define as propriedades a seguir.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Propriedades de IDownloadProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920969"
---
# <a name="idownloadprogress-properties"></a>Propriedades de IDownloadProgress

A interface [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) define as propriedades a seguir.



| Propriedade                                                                               | Descrição                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CurrentUpdateBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | Obtém uma cadeia de caracteres que especifica a quantidade de dados que foi transferida para o arquivo de conteúdo ou arquivos da atualização que está sendo baixada, em bytes.  |
| [**CurrentUpdateBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | Obtém uma cadeia de caracteres que estima a quantidade de dados que deve ser transferida para o arquivo de conteúdo ou os arquivos da atualização que está sendo baixada, em bytes. |
| [**CurrentUpdateDownloadPhase**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | Obtém um valor de enumeração [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) que especifica a fase do download que está em andamento no momento.          |
| [**CurrentUpdateIndex**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | Obtém um valor de índice baseado em zero que especifica a atualização que está sendo baixada no momento quando várias atualizações foram selecionadas.             |
| [**CurrentUpdatePercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | Obtém uma estimativa do percentual da atualização atual que foi baixada.                                                               |
| [**PercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | Obtém uma estimativa do percentual de todas as atualizações que foram baixadas.                                                                 |
| [**TotalBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | Obtém uma cadeia de caracteres que especifica a quantidade total de dados baixados, em bytes.                                                        |
| [**TotalBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | Obtém uma cadeia de caracteres que representa a estimativa da quantidade total de dados que serão baixados, em bytes.                                        |



 

 

 



