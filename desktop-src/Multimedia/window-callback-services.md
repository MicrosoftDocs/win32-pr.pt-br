---
title: Serviços de retorno de chamada de janela
description: Serviços de retorno de chamada de janela
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- áudio de multimídia, serviços de retorno de chamada de janela
- serviços de retorno de chamada de áudio, janela
- mixers de áudio, serviços de retorno de chamada de janela
- mixers, serviços de retorno de chamada de janela
- serviços de retorno de chamada de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48faf2dd94b61f5d4fc47e073fe0f3875bcbb503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454028"
---
# <a name="window-callback-services"></a>Serviços de retorno de chamada de janela

Os serviços de mixer fornecem serviços de retorno de chamada de janela para que seu aplicativo possa processar mensagens de drivers de mixer. Para usar esses serviços, especifique o sinalizador da janela de retorno de chamada \_ no parâmetro *fdwOpen* e um identificador de janela no parâmetro *dwCallback* da função [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) . As mensagens de driver são enviadas para a função de procedimento de janela para a janela identificada pelo identificador em *dwCallback*. As mensagens são específicas para o tipo de dispositivo de áudio.

 

 