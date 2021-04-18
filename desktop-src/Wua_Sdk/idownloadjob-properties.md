---
description: A interface IDownloadJob define as propriedades a seguir.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Propriedades de IDownloadJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810807"
---
# <a name="idownloadjob-properties"></a>Propriedades de IDownloadJob

A interface [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) define as propriedades a seguir.



| Propriedade                                        | Descrição                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | Obtém o objeto de estado específico do chamador que é passado para o método [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .           |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | Obtém a configuração que indica se a chamada para [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) foi processada completamente. |
| [**Atualizações**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | Obtém uma interface que contém uma coleção somente leitura das atualizações que são especificadas em um download.                                                  |



 

 

 



