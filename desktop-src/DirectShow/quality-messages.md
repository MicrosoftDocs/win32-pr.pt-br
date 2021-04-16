---
description: Mensagens de qualidade
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Mensagens de qualidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b290833be7550e255590a5bcda449ce19743c0b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500369"
---
# <a name="quality-messages"></a><span data-ttu-id="8e408-103">Mensagens de qualidade</span><span class="sxs-lookup"><span data-stu-id="8e408-103">Quality Messages</span></span>

<span data-ttu-id="8e408-104">As mensagens de qualidade são definidas com a estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) .</span><span class="sxs-lookup"><span data-stu-id="8e408-104">Quality messages are defined with the [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure.</span></span> <span data-ttu-id="8e408-105">Essa estrutura contém os seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="8e408-105">This structure contains the following members:</span></span>

-   <span data-ttu-id="8e408-106">**Tipo:** Definido pela enumeração [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) ; Famine, indicando que o filtro está recebendo poucos dados ou inundações, indicando que o filtro está recebendo muitos dados.</span><span class="sxs-lookup"><span data-stu-id="8e408-106">**Type:** Defined by the [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) enumeration; either Famine, indicating that the filter is receiving too little data, or Flood, indicating that the filter is receiving too much data.</span></span>
-   <span data-ttu-id="8e408-107">**Proporção:** O ajuste solicitado na taxa de dados, de uma linha de base de 1000.</span><span class="sxs-lookup"><span data-stu-id="8e408-107">**Proportion:** The requested adjustment in the data rate, from a baseline of 1000.</span></span> <span data-ttu-id="8e408-108">Por exemplo, 750 indica 75% e 1500 indica 150%.</span><span class="sxs-lookup"><span data-stu-id="8e408-108">For example, 750 indicates 75% and 1500 indicates 150%.</span></span>
-   <span data-ttu-id="8e408-109">**Tarde:** Tempo de referência que indica o atraso do exemplo mais recente.</span><span class="sxs-lookup"><span data-stu-id="8e408-109">**Late:** Reference time indicating how late the most recent sample arrived.</span></span> <span data-ttu-id="8e408-110">O valor será negativo se o exemplo chegou cedo.</span><span class="sxs-lookup"><span data-stu-id="8e408-110">The value is negative if the sample arrived early.</span></span>
-   <span data-ttu-id="8e408-111">**Carimbo de data/hora:** O carimbo de data/hora no exemplo mais recente.</span><span class="sxs-lookup"><span data-stu-id="8e408-111">**TimeStamp:** The time stamp on the most recent sample.</span></span>

<span data-ttu-id="8e408-112">Por exemplo, suponha que um exemplo com um carimbo de data/hora de 240 milissegundos (MS) atinja o renderizador em 280 MS, fluxo de tempo.</span><span class="sxs-lookup"><span data-stu-id="8e408-112">For example, suppose that a sample with a time stamp of 240 milliseconds (ms) reaches the renderer at 280 ms, stream time.</span></span> <span data-ttu-id="8e408-113">O processador cria uma mensagem de qualidade do tipo Famine.</span><span class="sxs-lookup"><span data-stu-id="8e408-113">The renderer creates a quality message of type Famine.</span></span> <span data-ttu-id="8e408-114">O exemplo chegou 40 MS atrasado, portanto, o membro **atrasado** é 400000.</span><span class="sxs-lookup"><span data-stu-id="8e408-114">The sample arrived 40 ms late, so the **Late** member is 400000.</span></span> <span data-ttu-id="8e408-115">(Todos os tempos de referência estão em unidades de 100 nanossegundos.) O membro do **carimbo de data/hora** é 2,4 milhões.</span><span class="sxs-lookup"><span data-stu-id="8e408-115">(All reference times are in 100-nanosecond units.) The **TimeStamp** member is 2400000.</span></span>

<span data-ttu-id="8e408-116">Para o membro de **proporção** , o renderizador pode usar uma média em execução para calcular o valor.</span><span class="sxs-lookup"><span data-stu-id="8e408-116">For the **Proportion** member, the renderer might use a running average to calculate the value.</span></span> <span data-ttu-id="8e408-117">Talvez as amostras cheguem ao tempo, e este exemplo é uma anomalia.</span><span class="sxs-lookup"><span data-stu-id="8e408-117">Perhaps samples have been arriving on time, and this sample is an anomaly.</span></span> <span data-ttu-id="8e408-118">Nesse caso, o renderizador pode solicitar apenas uma pequena correção.</span><span class="sxs-lookup"><span data-stu-id="8e408-118">In that case the renderer might request only a small correction.</span></span> <span data-ttu-id="8e408-119">Por outro lado, se os exemplos forem consistentemente atrasados, o renderizador poderá solicitar uma correção maior.</span><span class="sxs-lookup"><span data-stu-id="8e408-119">On the other hand, if samples are consistently late, the renderer might request a larger correction.</span></span>

<span data-ttu-id="8e408-120">O controle de qualidade é manipulado por meio da interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) .</span><span class="sxs-lookup"><span data-stu-id="8e408-120">Quality control is handled through the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface.</span></span> <span data-ttu-id="8e408-121">Ele contém dois métodos.</span><span class="sxs-lookup"><span data-stu-id="8e408-121">It contains two methods.</span></span>

-   <span data-ttu-id="8e408-122">[**Notificar**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): envia uma mensagem de qualidade.</span><span class="sxs-lookup"><span data-stu-id="8e408-122">[**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): Sends a quality message.</span></span>
-   <span data-ttu-id="8e408-123">[**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): especifica um Gerenciador de qualidade personalizado.</span><span class="sxs-lookup"><span data-stu-id="8e408-123">[**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): Specifies a custom quality manager.</span></span>

<span data-ttu-id="8e408-124">Um objeto que implementa o **IQualityControl** recebe mensagens de qualidade por meio de seu método **Notify** .</span><span class="sxs-lookup"><span data-stu-id="8e408-124">An object that implements **IQualityControl** receives quality messages through its **Notify** method.</span></span> <span data-ttu-id="8e408-125">Ele pode tratar a mensagem ou passar a mensagem para outro objeto.</span><span class="sxs-lookup"><span data-stu-id="8e408-125">It can either handle the message or pass the message to another object.</span></span> <span data-ttu-id="8e408-126">Se o aplicativo chamar o método **SetSink** do objeto, o objeto deverá delegar o controle de qualidade para o Gerenciador de qualidade especificado.</span><span class="sxs-lookup"><span data-stu-id="8e408-126">If the application calls the object's **SetSink** method, the object should delegate quality control to the specified quality manager.</span></span>

 

 



