---
description: A interface IDownloadJob define as propriedades a seguir.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Propriedades de IDownloadJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cdd4f95a14df215017f9fd628497d15c6c7410e4a82cbfb53c076b2112899b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049332"
---
# <a name="idownloadjob-properties"></a>Propriedades de IDownloadJob

A interface [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) define as propriedades a seguir.



| Propriedade                                        | Descrição                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Asyncstate**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | Obtém o objeto de estado específico do chamador que é passado para o [**método IUpdateDownloader.BeginDownload.**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload)           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | Obtém a configuração que indica se a chamada para [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) foi processada completamente. |
| [**Atualizações**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | Obtém uma interface que contém uma coleção somente leitura das atualizações especificadas em um download.                                                  |



 

 

 



