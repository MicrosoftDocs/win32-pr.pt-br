---
description: 'O gerenciador de memória cria os seguintes pools de memória que o sistema usa para alocar memória: pool não pa por página e pool.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Pools de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a49597cf90324395c50a4e44aac03815426f0c1de8ea2c7ca7aa85b5cdac95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808993"
---
# <a name="memory-pools"></a>Pools de memória

O gerenciador de memória cria os seguintes pools de memória que o sistema usa para alocar memória: pool não pa por página e pool. Ambos os pools de memória estão localizados na região do espaço de endereço reservado para o sistema e mapeados para o espaço de endereço virtual de cada processo. O pool não papagado consiste em endereços de memória virtual que têm a garantia de residir na memória física, desde que os objetos de kernel correspondentes sejam alocados. O pool de páginas consiste em memória virtual que pode ser pageada dentro e fora do sistema. Para melhorar o desempenho, os sistemas com um único processador têm três pools de páginas e sistemas multiprocessadores têm cinco pools de páginas.

Os alças para [objetos kernel](../sysinfo/kernel-objects.md) são armazenados no pool de páginas, portanto, o número de alças que você pode criar é baseado na memória disponível.

O sistema registra os limites e os valores atuais para seu pool não pa por página e o uso do arquivo de página. Para obter mais informações, consulte [Informações de desempenho de memória](memory-performance-information.md).

 

 
