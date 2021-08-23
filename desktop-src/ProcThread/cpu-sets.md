---
description: Os conjuntos de CPU fornecem APIs para declarar a afinidade de aplicativo de maneira "suave" que é compatível com o gerenciamento de energia do sistema operacional.
ms.assetid: FF8BE790-19D9-473F-B184-C54FB392D61A
title: Conjuntos de CPU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 092559fbf5646a0938696c953f4136f1fe1a9567e56e02a04c6c36510d03d729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143119"
---
# <a name="cpu-sets"></a>Conjuntos de CPU

Os conjuntos de CPU fornecem APIs para declarar a afinidade de aplicativo de maneira "suave" que é compatível com o gerenciamento de energia do sistema operacional. Além disso, a API fornece aos aplicativos a capacidade de reaffinitize todos os threads em segundo plano no processo para um subconjunto de processadores usando o mecanismo **padrão do processo** para evitar a interferência de threads do sistema operacional dentro do processo. algumas versões do Windows dão suporte a políticas de reserva de núcleo, nas quais um subconjunto dos conjuntos de CPU do sistema pode ser dedicado ao uso exclusivo de aplicativos e cargas de trabalho individuais.

A API do conjunto de CPU funciona com IDs de conjunto de CPU, que estão associadas a afinidades de processador virtual. Na maioria dos sistemas, e na maioria das condições, cada ID de conjunto de CPU será mapeada diretamente para um único processador lógico **doméstico** . Um relacionados de thread para um determinado conjunto de CPU normalmente será executado em um dos processadores em sua lista de IDs de conjunto de CPU selecionadas.

Os conjuntos de CPU que são reservados podem ser determinados inspecionando o sinalizador **alocado** nas informações do conjunto de CPU do sistema \_ \_ \_ . O sistema controla o acesso a conjuntos de CPU reservados e a atribuição pode ser consultada usando o sinalizador **AllocatedToTargetProcess** da \_ estrutura de informações do conjunto de CPU do sistema \_ \_ . Se um processo tentar usar uma atribuição de conjunto de CPU que é alocada exclusivamente a outros processos, sua solicitação será ignorada e os threads atribuídos a conjuntos de CPU não permitidos serão agendados em outro lugar. Os conjuntos de CPU podem ser atribuídos em dois níveis. Os conjuntos de CPU padrão do processo são atribuídos a todos os threads em um processo que não têm uma atribuição no nível de thread selecionado. Se um thread ou processo tiver uma máscara de afinidade restritiva definida, a máscara de afinidade será respeitada acima de qualquer atribuição de conjunto de CPU conflitante. Em sistemas de vários grupos, as atribuições de CPU são ignoradas se estiverem em grupos que não correspondem ao grupo na máscara de afinidade do thread. Se um thread for atribuído a vários conjuntos de CPU válidos, ele será executado em um dos processadores correspondentes de acordo com suas prioridades e as prioridades dos threads concorrentes nesses processadores.

**Funções/enumerações/estruturas de conjunto de CPU**

-   Função [**GetProcessDefaultCpuSets**](getprocessdefaultcpusets.md)
-   Função [**GetSystemCpuSetInformation**](getsystemcpusetinformation.md)
-   Função [**GetThreadSelectedCpuSets**](getthreadselectedcpusets.md)
-   Função [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md)
-   Função [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md)
-   [**CPU \_ DEFINIR enumeração de \_ \_ tipo de informação**](cpu-set-information-type.md)
-   [**Sistema \_ Estrutura \_ de \_ informações de conjunto de CPU**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)

 

 



