---
description: Os tipos de contador não computacional não têm uma fórmula associada. O valor bruto é diretamente significativo.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Tipos de contadores não computacionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170385"
---
# <a name="noncomputational-counter-types"></a><span data-ttu-id="bb10c-104">Tipos de contadores não computacionais</span><span class="sxs-lookup"><span data-stu-id="bb10c-104">Noncomputational Counter Types</span></span>

<span data-ttu-id="bb10c-105">Os tipos de contador não computacional não têm uma fórmula associada.</span><span class="sxs-lookup"><span data-stu-id="bb10c-105">Noncomputational counter types do not have an associated formula.</span></span> <span data-ttu-id="bb10c-106">O valor bruto é diretamente significativo.</span><span class="sxs-lookup"><span data-stu-id="bb10c-106">The raw value is directly meaningful.</span></span>

<span data-ttu-id="bb10c-107">A propriedade **FilesToBeIndexed** na classe [**Win32 \_ PerfRawData \_ ContentIndex \_ IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) é um exemplo do tipo de contador **contador de desempenho \_ \_ RAWCOUNT** .</span><span class="sxs-lookup"><span data-stu-id="bb10c-107">The **FilesToBeIndexed** property in the [**Win32\_PerfRawData\_ContentIndex\_IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class is an example of the **PERF\_COUNTER\_RAWCOUNT** counter type.</span></span> <span data-ttu-id="bb10c-108">Ele contém uma contagem de arquivos que não foram indexados.</span><span class="sxs-lookup"><span data-stu-id="bb10c-108">It contains a count of files that have not been indexed.</span></span>

<span data-ttu-id="bb10c-109">Os tipos de contador são designados pela constante definida em WINPERF. h localizada no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bb10c-109">Counter types are designated by the constant defined in Winperf.h located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bb10c-110">A tabela a seguir lista os tipos de contadores não computacionais que são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="bb10c-110">The following table lists the noncomputational counter types that are provided.</span></span>



| <span data-ttu-id="bb10c-111">CounterType</span><span class="sxs-lookup"><span data-stu-id="bb10c-111">CounterType</span></span>                                                                                                 | <span data-ttu-id="bb10c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb10c-112">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb10c-113">[Desempenho \_ \_Texto do contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 2816</span><span class="sxs-lookup"><span data-stu-id="bb10c-113">[PERF\_COUNTER\_TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816</span></span><br/>                | <span data-ttu-id="bb10c-114">Esse tipo de contador mostra uma cadeia de caracteres de texto de comprimento variável em Unicode.</span><span class="sxs-lookup"><span data-stu-id="bb10c-114">This counter type shows a variable-length text string in Unicode.</span></span> <span data-ttu-id="bb10c-115">Ele não exibe valores calculados.</span><span class="sxs-lookup"><span data-stu-id="bb10c-115">It does not display calculated values.</span></span>               |
| <span data-ttu-id="bb10c-116">[Desempenho \_ COUNTER \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 65536</span><span class="sxs-lookup"><span data-stu-id="bb10c-116">[PERF\_COUNTER\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536</span></span><br/>           | <span data-ttu-id="bb10c-117">Valor de contador bruto que não requer cálculos e representa um exemplo que é o último valor observado apenas.</span><span class="sxs-lookup"><span data-stu-id="bb10c-117">Raw counter value that does not require calculations, and represents one sample which is the last observed value only.</span></span> |
| <span data-ttu-id="bb10c-118">[Desempenho \_ CONTADOR \_ grande \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 65792</span><span class="sxs-lookup"><span data-stu-id="bb10c-118">[PERF\_COUNTER\_LARGE\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792</span></span><br/>    | <span data-ttu-id="bb10c-119">O mesmo que o **contador de desempenho \_ \_ RAWCOUNT**, mas uma representação de 64 bits para valores maiores.</span><span class="sxs-lookup"><span data-stu-id="bb10c-119">Same as **PERF\_COUNTER\_RAWCOUNT**, but a 64-bit representation for larger values.</span></span>                                    |
| <span data-ttu-id="bb10c-120">[Desempenho \_ CONTADOR \_ RAWCOUNT \_ hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span><span class="sxs-lookup"><span data-stu-id="bb10c-120">[PERF\_COUNTER\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span></span><br/>                  | <span data-ttu-id="bb10c-121">Valor observado mais recentemente no formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="bb10c-121">Most recently observed value in hexadecimal format.</span></span> <span data-ttu-id="bb10c-122">Ele não exibe uma média.</span><span class="sxs-lookup"><span data-stu-id="bb10c-122">It does not display an average.</span></span>                                    |
| <span data-ttu-id="bb10c-123">[Desempenho \_ CONTADOR \_ grande \_ RAWCOUNT Decimal \_ hexadecimal](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))256</span><span class="sxs-lookup"><span data-stu-id="bb10c-123">[PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256</span></span><br/> | <span data-ttu-id="bb10c-124">O mesmo que o **contador de desempenho \_ \_ RAWCOUNT \_ hex**, mas uma representação de 64 bits em hexadecimal para uso com valores grandes.</span><span class="sxs-lookup"><span data-stu-id="bb10c-124">Same as **PERF\_COUNTER\_RAWCOUNT\_HEX**, but a 64-bit representation in hexadecimal for use with large values.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bb10c-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb10c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb10c-126">Tipos de contador de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="bb10c-126">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

