---
description: A interface IDownloadJob define os métodos a seguir.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Métodos IDownloadJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a153120f2d558dcc905d4e8b4de8a0993d842eaec895b7fd881ed2b8504f8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756806"
---
# <a name="idownloadjob-methods"></a>Métodos IDownloadJob

A interface [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) define os métodos a seguir.



| Método                                            | Descrição                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Limpeza**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | Aguarda a conclusão de uma operação assíncrona e libera todos os retornos de chamada.                                        |
| [**GetProgress**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | Retorna uma [**interface IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) que descreve o progresso atual de um download. |
| [**RequestAbort**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | Faz uma solicitação para encerrar um download assíncrono.                                                                       |



 

 

 



