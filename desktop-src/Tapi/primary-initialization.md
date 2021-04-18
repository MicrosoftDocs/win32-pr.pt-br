---
description: Um aplicativo TAPI deve chamar uma operação de inicialização, que solicita uma série de ações da TAPI e os provedores de serviço que configuram o ambiente de comunicação para o aplicativo.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Inicialização primária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757955"
---
# <a name="primary-initialization"></a>Inicialização primária

Um aplicativo TAPI deve chamar uma operação de inicialização, que solicita uma série de ações da TAPI e os provedores de serviço que configuram o ambiente de comunicação para o aplicativo.

-   A inicialização é síncrona e não retorna até que a operação seja concluída ou tenha falhado.
-   Se o TAPISRV ainda não estiver em execução, a TAPI o iniciará.
-   A TAPI configura uma conexão com o processo TAPISRV.
-   O TAPISVR carrega os provedores de serviço especificados no registro e solicita que eles inicializem os dispositivos para os quais dão suporte.

**TAPI 2. x:** Os aplicativos executam a inicialização chamando [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).

**TAPI 3. x:** Os aplicativos chamam [**ITTAPI:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).

 

 
