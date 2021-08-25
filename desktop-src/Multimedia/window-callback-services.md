---
title: Serviços de retorno de chamada de janela
description: Serviços de retorno de chamada de janela
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- áudio multimídia, serviços de retorno de chamada de janela
- áudio, serviços de retorno de chamada de janela
- mixers de áudio, serviços de retorno de chamada de janela
- mixers, serviços de retorno de chamada de janela
- serviços de retorno de chamada de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0248928d339dc6c1737ee9dc47f72bac0fb42fe76774e6062177c29064b44257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781406"
---
# <a name="window-callback-services"></a>Serviços de retorno de chamada de janela

Os serviços de mixer fornecem serviços de retorno de chamada de janela para que seu aplicativo possa processar mensagens de drivers de mixer. Para usar esses serviços, especifique o sinalizador CALLBACK WINDOW no parâmetro fdwOpen e um alça de janela no parâmetro \_ *dwCallback* da [**função mixerOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)  As mensagens do driver são enviadas para a função de procedimento de janela para a janela identificada pelo identificador *em dwCallback*. As mensagens são específicas para o tipo de dispositivo de áudio.

 

 