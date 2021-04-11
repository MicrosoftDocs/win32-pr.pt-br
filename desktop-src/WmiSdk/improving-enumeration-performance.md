---
description: As enumerações tendem a usar uma quantidade significativa de recursos do sistema.
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: Melhorando o desempenho da enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170611"
---
# <a name="improving-enumeration-performance"></a><span data-ttu-id="b6160-103">Melhorando o desempenho da enumeração</span><span class="sxs-lookup"><span data-stu-id="b6160-103">Improving Enumeration Performance</span></span>

<span data-ttu-id="b6160-104">As enumerações tendem a usar uma quantidade significativa de recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="b6160-104">Enumerations tend to use a significant amount of system resources.</span></span> <span data-ttu-id="b6160-105">Portanto, você deve tentar otimizar o processo de enumeração do WMI se planeja executar enumerações em um grupo grande.</span><span class="sxs-lookup"><span data-stu-id="b6160-105">Therefore, you should try to optimize the WMI enumeration process if you plan on performing enumerations on a large group.</span></span> <span data-ttu-id="b6160-106">Os scripts também podem usar uma consulta para evitar a degradação do desempenho nas operações "for each.... Next" com um conjunto grande.</span><span class="sxs-lookup"><span data-stu-id="b6160-106">Scripts can also use a query to avoid performance degradation in "For each….Next" operations with a large set.</span></span> <span data-ttu-id="b6160-107">Para obter mais informações, consulte [consultando o WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b6160-107">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="b6160-108">O procedimento a seguir descreve como melhorar o desempenho de enumeração.</span><span class="sxs-lookup"><span data-stu-id="b6160-108">The following procedure describes how to improve enumeration performance.</span></span>

<span data-ttu-id="b6160-109">**Para melhorar o desempenho de enumeração**</span><span class="sxs-lookup"><span data-stu-id="b6160-109">**To improve enumeration performance**</span></span>

1.  <span data-ttu-id="b6160-110">Defina o parâmetro *lFlags* para permitir o retorno de semisynchronous dos dados com um enumerador que descarta cada item do WMI à medida que ele é entregue.</span><span class="sxs-lookup"><span data-stu-id="b6160-110">Set the *lFlags* parameter to allow semisynchronous return of the data with an enumerator that discards each item from WMI as it is delivered.</span></span> <span data-ttu-id="b6160-111">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b6160-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="b6160-112">O exemplo de código C++ a seguir mostra como usar **o \_ sinalizador WBEM \_ retornar sinalizadores \_ imediatos** e de **\_ \_ \_ somente encaminhamento do sinalizador WBEM** .</span><span class="sxs-lookup"><span data-stu-id="b6160-112">The following C++ code example shows how to use the **WBEM\_FLAG\_RETURN\_IMMEDIATE** and **WBEM\_FLAG\_FORWARD\_ONLY** flags.</span></span>

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    <span data-ttu-id="b6160-113">No VBScript ou Visual Basic, use os sinalizadores de script **WbemFlagReturnImmediately** e **WbemFlagForwardOnly** do [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="b6160-113">In VBScript or Visual Basic, use the scripting flags **WbemFlagReturnImmediately** and **WbemFlagForwardOnly** from [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span> <span data-ttu-id="b6160-114">O valor combinado desses sinalizadores é decimal 48.</span><span class="sxs-lookup"><span data-stu-id="b6160-114">The combined value of these flags is decimal 48.</span></span>

    <span data-ttu-id="b6160-115">Os sinalizadores de script e de parâmetro causam o seguinte comportamento:</span><span class="sxs-lookup"><span data-stu-id="b6160-115">The scripting and parameter flags cause the following behavior:</span></span>

    -   <span data-ttu-id="b6160-116">O **\_ sinalizador WBEM \_ retorna \_** o comportamento de semisynchronous imediato ou **wbemFlagReturnImmediately** sinalizador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="b6160-116">The **WBEM\_FLAG\_RETURN\_IMMEDIATE** or **wbemFlagReturnImmediately** flag requests semisynchronous behavior.</span></span> <span data-ttu-id="b6160-117">A chamada para criar o enumerador retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="b6160-117">The call to create the enumerator returns immediately.</span></span> <span data-ttu-id="b6160-118">Em seguida, você pode começar a atravessar o conjunto de objetos que receber.</span><span class="sxs-lookup"><span data-stu-id="b6160-118">You can then begin to traverse the object set that you receive.</span></span>
    -   <span data-ttu-id="b6160-119">O sinalizador de **\_ \_ \_ somente encaminhamento** do sinalizador WBEM ou sinalizador **wbemFlagForwardOnly** solicita um enumerador que você não pode retroceder.</span><span class="sxs-lookup"><span data-stu-id="b6160-119">The **WBEM\_FLAG\_FORWARD\_ONLY** flag or **wbemFlagForwardOnly** flag requests an enumerator that you cannot rewind.</span></span> <span data-ttu-id="b6160-120">Ou seja, o WMI pode liberar um objeto depois de exibir o objeto.</span><span class="sxs-lookup"><span data-stu-id="b6160-120">That is, WMI can release an object after you view the object.</span></span>

    <span data-ttu-id="b6160-121">Em situações em que a enumeração é grande e o aplicativo é muito rápido, o uso de enumeradores somente de encaminhamento com processamento semisynchronous permite que o WMI mantenha um número muito menor de objetos, aumentando significativamente o tempo de resposta e o desempenho da memória.</span><span class="sxs-lookup"><span data-stu-id="b6160-121">In situations where the enumeration is large and the application is very fast, using forward-only enumerators with semisynchronous processing allows WMI to hold on to far fewer objects, thereby increasing response time and memory performance significantly.</span></span>

    <span data-ttu-id="b6160-122">O exemplo de código VBScript a seguir mostra como fazer uma chamada usando os sinalizadores **wbemFlagReturnImmediately** e **wbemFlagForwardOnly** combinados para obter uma coleção de eventos de um log de eventos.</span><span class="sxs-lookup"><span data-stu-id="b6160-122">The following VBScript code example shows how to make a call using the combined **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** flags to obtain a collection of events from an event log.</span></span>

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  <span data-ttu-id="b6160-123">Sempre que possível, evite usar o [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) em C++ ou [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)e, em vez disso, use **ExecQuery**.</span><span class="sxs-lookup"><span data-stu-id="b6160-123">Whenever possible, avoid using [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) in C++ or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), and instead use **ExecQuery**.</span></span>

    <span data-ttu-id="b6160-124">O método **ExecQuery** consulta o WMI usando tecnologias de banco de dados, enquanto o [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) ou [**SWBEMSERVICES. InstancesOf**](swbemservices-instancesof.md) enumera objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="b6160-124">The **ExecQuery** method queries WMI using database technologies, while [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) enumerates WMI objects.</span></span> <span data-ttu-id="b6160-125">Especificamente, o **ExecQuery** pode solicitar subconjuntos específicos de dados que os métodos de enumeração não podem.</span><span class="sxs-lookup"><span data-stu-id="b6160-125">Specifically, **ExecQuery** can request specific subsets of data that the enumerating methods cannot.</span></span>

    <span data-ttu-id="b6160-126">Como alguns provedores não têm recursos de consulta, o WMI fornece um recurso de "post Filter" que permite ao WMI descartar instâncias que não atendam às especificações de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="b6160-126">Because some providers do not have querying capabilities, WMI provides a "post filter" feature that allows WMI to discard instances that do not fulfill a query's specifications.</span></span> <span data-ttu-id="b6160-127">Se um provedor específico se beneficia desse recurso, ele é o autor do provedor.</span><span class="sxs-lookup"><span data-stu-id="b6160-127">Whether a particular provider takes advantage of this feature is up to the provider author.</span></span>

3.  <span data-ttu-id="b6160-128">Experimente consultas diferentes para determinar o que oferece o melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="b6160-128">Experiment with different queries to determine what gives you the best performance.</span></span>

    <span data-ttu-id="b6160-129">Por exemplo, o WMI raramente processa consultas com cláusulas **Where** no formato Prop1 < "x".</span><span class="sxs-lookup"><span data-stu-id="b6160-129">For example, WMI seldom efficiently processes queries with **WHERE** clauses of the form Prop1 < "x".</span></span> <span data-ttu-id="b6160-130">Por outro lado, o WMI normalmente processa consultas no formato KeyProp1 = "x" com eficiência.</span><span class="sxs-lookup"><span data-stu-id="b6160-130">In contrast, WMI normally processes queries of the form KeyProp1 = "x" efficiently.</span></span>

<span data-ttu-id="b6160-131">Para obter mais informações, consulte [enumerando o WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b6160-131">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

 

 



