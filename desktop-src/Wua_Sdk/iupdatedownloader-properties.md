---
description: A interface IUpdateDownloader define as propriedades a seguir.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Propriedades de IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647295"
---
# <a name="iupdatedownloader-properties"></a>Propriedades de IUpdateDownloader

A interface [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) define as propriedades a seguir.



| Propriedade                                                             | Descrição                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | Obtém e define o aplicativo cliente atual.                                                                                                                              |
| [**Isforced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | Obtém e define um valor booliano que indica se o WUA (agente de Windows Update) força o download de atualizações que já estão instaladas ou que não podem ser instaladas. |
| [**Priority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | Obtém e define o nível de prioridade do download.                                                                                                                          |
| [**Atualizações**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | Obtém e define uma interface que contém uma coleção somente leitura das atualizações que são especificadas para download.                                                            |



 

 

 



