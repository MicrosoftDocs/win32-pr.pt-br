---
description: A interface IDownloadJob define os métodos a seguir.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Métodos IDownloadJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f68acd6d7fef37c4ce9309c559a1de1b4d516dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501872"
---
# <a name="idownloadjob-methods"></a>Métodos IDownloadJob

A interface [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) define os métodos a seguir.



| Método                                            | Descrição                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Eliminação**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | Aguarda a conclusão de uma operação assíncrona e libera todos os retornos de chamada.                                        |
| [**GetProgress**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | Retorna uma interface [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) que descreve o progresso atual de um download. |
| [**RequestAbort**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | Faz uma solicitação para finalizar um download assíncrono.                                                                       |



 

 

 



