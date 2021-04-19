---
description: 'O Gerenciador de memória cria os seguintes pools de memória que o sistema usa para alocar memória: pool não paginável e pool paginável.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Pools de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60987b43347e55d8ee2d01672dbb8173ffc8dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810158"
---
# <a name="memory-pools"></a>Pools de memória

O Gerenciador de memória cria os seguintes pools de memória que o sistema usa para alocar memória: pool não paginável e pool paginável. Ambos os pools de memória estão localizados na região do espaço de endereço reservado para o sistema e mapeados para o espaço de endereço virtual de cada processo. O pool não paginável consiste em endereços de memória virtual que têm garantia de residir na memória física, contanto que os objetos kernel correspondentes sejam alocados. O pool paginável consiste em memória virtual que pode ser paginada dentro e fora do sistema. Para melhorar o desempenho, os sistemas com um único processador têm três pools paginável, e sistemas multiprocessadores têm cinco pools paginados.

Os identificadores de [objetos kernel](../sysinfo/kernel-objects.md) são armazenados no pool paginável, de modo que o número de identificadores que você pode criar é baseado na memória disponível.

O sistema registra os limites e os valores atuais para seu pool não paginável, pool paginável e uso do arquivo de paginação. Para obter mais informações, consulte [informações de desempenho da memória](memory-performance-information.md).

 

 
