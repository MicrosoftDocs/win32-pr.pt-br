---
description: Substituição de caminho de plataforma
ms.assetid: f430fd9a-f865-4cdb-b0ea-4e6d79913308
title: Substituição de caminho de plataforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9a6ae6795b444c44db91d90ecd93efd19ea9dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755785"
---
# <a name="platform-path-override"></a>Substituição de caminho de plataforma

A função [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) é usada para definir uma substituição de caminho de plataforma para um computador de destino ao trabalhar com arquivos INF de um computador diferente. Como tal, ele pode se referir a uma plataforma diferente daquela em que está sendo executada. Para lidar com fontes de mídia, ele pode se referir a plataformas que não têm mais suporte, como alfa, MIPS e PPC. Ele removerá a substituição do caminho da plataforma se nenhum for especificado.

Depois que uma substituição de caminho de plataforma é definida por uma chamada para [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea), qualquer função de instalação que enfileira as operações de cópia de arquivo examinará o componente final do caminho de origem. Se o componente final corresponder ao nome da plataforma do usuário, a função de instalação o substituirá pela cadeia de caracteres de substituição definida por **SetupSetPlatformPathOverride**.

Por exemplo, ao instalar drivers de impressora em um servidor MIPS, talvez você queira instalar drivers para todas as plataformas com suporte. Enfileirar os arquivos normalmente instalaria os arquivos especificados nas seções dependentes de MIPS do arquivo INF, com caminhos de origem, como \\ \\ \\ MIPS de origem raiz \\ . Para instalar os arquivos de uma segunda plataforma, você deve chamar [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) com *override* indicando a plataforma de substituição. Se o local indicado pela *substituição* contiver o valor de cadeia de caracteres "Alpha", as operações de cópia de arquivo enviadas para a fila com um caminho de origem de \\ \\ \\ MIPS de origem raiz \\ teriam seu caminho de origem alterado para a \\ \\ \\ origem raiz \\ alfa. Você repetiria esse processo para cada plataforma de interesse.

 

 



