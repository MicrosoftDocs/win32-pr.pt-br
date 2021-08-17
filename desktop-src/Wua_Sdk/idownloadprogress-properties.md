---
description: A interface IDownloadProgress define as propriedades a seguir.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Propriedades de IDownloadProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeed70acfb6b350c463b731d44cfe0d48cc1fd8a5190c247fcda316c4707126f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130568"
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



 

 

 



