---
description: Substituição de caminho da plataforma
ms.assetid: f430fd9a-f865-4cdb-b0ea-4e6d79913308
title: Substituição de caminho da plataforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63cc1e6ba4b1cb53c26e380eeab95a96091d5159e8356d8f7067529a6b589d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992616"
---
# <a name="platform-path-override"></a>Substituição de caminho da plataforma

A [**função SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) é usada para definir uma substituição de caminho de plataforma para um computador de destino ao trabalhar com arquivos INF de um computador diferente. Assim, ele pode se referir a uma plataforma diferente da que está sendo executado no momento. Para lidar com fontes de mídia, ele pode se referir a plataformas que não têm mais suporte, como Alfa, MIPS e PPC. Ele removerá a substituição do caminho da plataforma se nenhum for especificado.

Depois que uma substituição de caminho de plataforma é definida por uma chamada para [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea), qualquer função de instalação que enfileira operações de cópia de arquivo examinará o componente final do caminho de origem. Se o componente final corresponde ao nome da plataforma do usuário, a função de instalação a substituirá pela cadeia de caracteres de substituição definida por **SetupSetPlatformPathOverride**.

Por exemplo, ao instalar drivers de impressora em um servidor MIPS, talvez você queira instalar drivers para todas as plataformas com suporte. A fila dos arquivos normalmente instalaria os arquivos especificados nas seções dependentes de MIPS do arquivo INF, com caminhos de origem, como mips de \\ \\ \\ \\ origem raiz. Para instalar os arquivos de uma segunda plataforma, você deve chamar [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) com *Substituir* indicando a plataforma de substituição. Se o local  indicado por Override contiver o valor de cadeia de caracteres "alfa", as operações de cópia de arquivo enviadas para a fila com um caminho de origem de mips de origem raiz terão seu caminho de origem alterado para alfa de origem \\ \\ \\ \\ \\ \\ \\ \\ raiz. Você repetiria esse processo para cada plataforma de interesse.

 

 



