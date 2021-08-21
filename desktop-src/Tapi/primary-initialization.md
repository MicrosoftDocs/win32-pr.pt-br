---
description: Um aplicativo TAPI deve chamar uma operação de inicialização, que solicita uma série de ações da TAPI e dos provedores de serviços que configuram o ambiente de comunicação para o aplicativo.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Inicialização primária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae187692f1eb64546398a273bc823ab93f622b6a0472848c31f9d94b9ecd7e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060584"
---
# <a name="primary-initialization"></a>Inicialização primária

Um aplicativo TAPI deve chamar uma operação de inicialização, que solicita uma série de ações da TAPI e dos provedores de serviços que configuram o ambiente de comunicação para o aplicativo.

-   A inicialização é síncrona e não retorna até que a operação seja concluída ou tenha falhado.
-   Se TAPISRV ainda não estiver em execução, o TAPI o iniciará.
-   A TAPI configura uma conexão com o processo TAPISRV.
-   O TAPISVR carrega os provedores de serviço especificados no Registro e solicita que eles inicializem os dispositivos com suporte.

**TAPI 2.x:** Os aplicativos executam a inicialização [**chamando lineInitializeEx.**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)

**TAPI 3.x:** Os aplicativos [**chamam ITTAPI::Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).

 

 
