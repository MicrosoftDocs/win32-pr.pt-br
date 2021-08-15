---
description: A interface IUpdateDownloader define as propriedades a seguir.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Propriedades de IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf66fbdad678ef6a78d0fa049ecb59c34be2ca9d08c873e24e82c35c9d1eb1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738285"
---
# <a name="iupdatedownloader-properties"></a>Propriedades de IUpdateDownloader

A interface [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) define as propriedades a seguir.



| Propriedade                                                             | Descrição                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | Obtém e define o aplicativo cliente atual.                                                                                                                              |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | Obtém e define um valor booliana que indica se o WUA (Agente de Atualização do Windows) força o download de atualizações que já estão instaladas ou que não podem ser instaladas. |
| [**Priority**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | Obtém e define o nível de prioridade do download.                                                                                                                          |
| [**Atualizações**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | Obtém e define uma interface que contém uma coleção somente leitura das atualizações especificadas para download.                                                            |



 

 

 



