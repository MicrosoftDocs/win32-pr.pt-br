---
description: Os tipos de contadores do algoritmo de timer de precisão obtêm leituras mais precisas do que os temporizadores do sistema.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Tipos de contadores de algoritmo de timer de precisão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663245"
---
# <a name="precision-timer-algorithm-counter-types"></a><span data-ttu-id="524b5-103">Tipos de contadores de algoritmo de timer de precisão</span><span class="sxs-lookup"><span data-stu-id="524b5-103">Precision Timer Algorithm Counter Types</span></span>

<span data-ttu-id="524b5-104">Os tipos de contadores do algoritmo de timer de precisão obtêm leituras mais precisas do que os temporizadores do sistema.</span><span class="sxs-lookup"><span data-stu-id="524b5-104">The precision timer algorithm counter types obtain more accurate readings than system timers.</span></span> <span data-ttu-id="524b5-105">O serviço que fornece os dados também fornece um carimbo de data/hora, que elimina os erros que podem ocorrer devido ao tempo pequeno e variável que decorre entre a captura do carimbo de data/hora do sistema e a coleta dos dados da DLL de desempenho.</span><span class="sxs-lookup"><span data-stu-id="524b5-105">The service that provides the data also provides a timestamp, which eliminates the errors that can occur because of the small and variable time that elapses between capture of the system timestamp and collection of the data from the performance DLL.</span></span> <span data-ttu-id="524b5-106">Esse carimbo de data/hora base para temporizadores de precisão é uma \_ propriedade de carimbo de data/hora de precisão de desempenho \_ , que deve seguir imediatamente a \_ \_ Propriedade temporizador</span><span class="sxs-lookup"><span data-stu-id="524b5-106">This base timestamp for precision timers is a PERF\_PRECISION\_TIMESTAMP property, which must immediately follow the PERF\_PRECISION\_TIMER property.</span></span>



| <span data-ttu-id="524b5-107">Constante de tipo</span><span class="sxs-lookup"><span data-stu-id="524b5-107">CounterType Constant</span></span>                                                                                         | <span data-ttu-id="524b5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="524b5-108">Description</span></span>                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="524b5-109">[Desempenho \_ \_ \_ Temporizador do sistema de precisão](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 541525248</span><span class="sxs-lookup"><span data-stu-id="524b5-109">[PERF\_PRECISION\_SYSTEM\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248</span></span><br/> | <span data-ttu-id="524b5-110">Semelhante ao timer do contador de desempenho \_ \_ , exceto que ele usa uma base de tempo definida do contador em vez do carimbo de data/hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="524b5-110">Similar to PERF\_COUNTER\_TIMER except that it uses a counter defined time base instead of the system timestamp.</span></span>             |
| <span data-ttu-id="524b5-111">[Desempenho \_ PRECISÃO de \_ 100 NS do \_ temporizador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 542573824</span><span class="sxs-lookup"><span data-stu-id="524b5-111">[PERF\_PRECISION\_100NS\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 542573824</span></span><br/>  | <span data-ttu-id="524b5-112">Semelhante ao \_ \_ temporizador perf 100NSEC, exceto pelo fato de que ele usa uma base de tempo definida do contador de 100 NS em vez do carimbo de data/hora de 100</span><span class="sxs-lookup"><span data-stu-id="524b5-112">Similar to PERF\_100NSEC\_TIMER except that it uses a 100ns counter defined time base instead of the system 100ns timestamp.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="524b5-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="524b5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="524b5-114">Tipos de contador de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="524b5-114">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

