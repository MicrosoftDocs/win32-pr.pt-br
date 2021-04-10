---
description: Fornece acesso aos eventos da caneta provenientes de digitalizadores de caneta ou de toque.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Referência do RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170461"
---
# <a name="realtimestylus-reference"></a><span data-ttu-id="feb04-103">Referência do RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="feb04-103">RealTimeStylus Reference</span></span>

<span data-ttu-id="feb04-104">Fornece acesso aos eventos da caneta provenientes de digitalizadores de caneta ou de toque.</span><span class="sxs-lookup"><span data-stu-id="feb04-104">Provides access to the stylus events coming from pen or touch digitizers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="feb04-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="feb04-105">In This Section</span></span>

-   [<span data-ttu-id="feb04-106">Interfaces e classes do RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="feb04-106">RealTimeStylus Classes and Interfaces</span></span>](realtimestylus-classes-and-interfaces.md)
-   [<span data-ttu-id="feb04-107">Enumerações do RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="feb04-107">RealTimeStylus Enumerations</span></span>](realtimestylus-enumerations.md)
-   [<span data-ttu-id="feb04-108">Estruturas RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="feb04-108">RealTimeStylus Structures</span></span>](realtimestylus-structures.md)

## <a name="remarks"></a><span data-ttu-id="feb04-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="feb04-109">Remarks</span></span>

<span data-ttu-id="feb04-110">Esse objeto implementa a interface com do [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .</span><span class="sxs-lookup"><span data-stu-id="feb04-110">This object implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) COM interface.</span></span>

<span data-ttu-id="feb04-111">Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.</span><span class="sxs-lookup"><span data-stu-id="feb04-111">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="feb04-112">Você pode controlar totalmente, dinamicamente renderizar, modificar e até mesmo excluir dados do fluxo de pacotes dentro dos plug-ins síncronos e assíncronos do objeto de [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="feb04-112">You can fully control, dynamically render, modify, and even delete data from the packet stream within the synchronous and asynchronous plug-ins of the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span>

<span data-ttu-id="feb04-113">A caneta em tempo real fornece uma maneira de criar um objeto **InkCollecting** que é de thread único e residente no thread de interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="feb04-113">The real time stylus provides a way to create an **InkCollecting** object that is single-threaded and resident in the application UI thread.</span></span> <span data-ttu-id="feb04-114">Esse objeto **InkCollecting** acessa os dados da caneta em tempo real da fila.</span><span class="sxs-lookup"><span data-stu-id="feb04-114">This **InkCollecting** object accesses the real time stylus data from the queue.</span></span> <span data-ttu-id="feb04-115">Um objeto **InkCollecting** em conjunto com a caneta em tempo real permite a edição de seleção em tempo real e a edição em tempo real dos dados de tinta coletados.</span><span class="sxs-lookup"><span data-stu-id="feb04-115">An **InkCollecting** object in conjunction with real time stylus enables real-time selection editing and real-time editing of the collected ink data.</span></span> <span data-ttu-id="feb04-116">Para obter mais informações, consulte [acessando e manipulando a entrada da caneta](accessing-and-manipulating-stylus-input.md).</span><span class="sxs-lookup"><span data-stu-id="feb04-116">For more information, please see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span>

<span data-ttu-id="feb04-117">Use o objeto da [**classe RealTimeStylus**](realtimestylus-class.md) para interagir diretamente com o fluxo de dados da caneta do Tablet ou para bloquear a escrita em tempo real.</span><span class="sxs-lookup"><span data-stu-id="feb04-117">Use the [**RealTimeStylus Class**](realtimestylus-class.md) object to interact directly with the tablet stylus data stream or to block real-time inking.</span></span> <span data-ttu-id="feb04-118">Use o controle de controle de [**classe InkCollector**](inkcollector-class.md) , objeto de [**classe InkOverlay**](inkoverlay-class.md) , controle de controle [InkPicture](inkpicture-control-reference.md) ou [InkEdit](inkedit-control-reference.md) quando o comportamento padrão desses objetos fornecer o comportamento de que você precisa.</span><span class="sxs-lookup"><span data-stu-id="feb04-118">Use the [**InkCollector Class**](inkcollector-class.md) object, [**InkOverlay Class**](inkoverlay-class.md) object, [InkPicture Control](inkpicture-control-reference.md) control, or [InkEdit Control](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

<span data-ttu-id="feb04-119">Os eventos de caneta em tempo real estão em um identificador de janela específico dentro de um retângulo de entrada de janela específico.</span><span class="sxs-lookup"><span data-stu-id="feb04-119">The real time stylus events are on a specific window handle within a specific window input rectangle.</span></span> <span data-ttu-id="feb04-120">O RealTimeStylusService pode enviar dados de caneta para vários objetos de [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="feb04-120">The RealTimeStylusService can send stylus data to multiple [**RealTimeStylus Class**](realtimestylus-class.md) objects.</span></span> <span data-ttu-id="feb04-121">Cada objeto da **classe RealTimeStylus** recebe dados da caneta para uma seção específica de uma janela com base na [**Propriedade IRealTimeStylus:: WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) definida para esse objeto de **classe do RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="feb04-121">Each **RealTimeStylus Class** object receives stylus data for a specific section of a window based on the defined [**IRealTimeStylus::WindowInputRectangle Property**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) for that **RealTimeStylus Class** object.</span></span> <span data-ttu-id="feb04-122">O objeto da **classe RealTimeStylus** Obtém os dados da caneta e, em seguida, processa isso por meio de uma lista de plug-ins síncronos e assíncronos.</span><span class="sxs-lookup"><span data-stu-id="feb04-122">The **RealTimeStylus Class** object gets the stylus data and then processes this through a list of synchronous and asynchronous plug-ins.</span></span>

<span data-ttu-id="feb04-123">A diferença entre os plug-ins síncronos e os plug-ins assíncronos está no thread em que eles são executados e na sequência de chamada.</span><span class="sxs-lookup"><span data-stu-id="feb04-123">The difference between the synchronous plug-ins and the asynchronous plug-ins lies in the thread in which they execute and the calling sequence.</span></span> <span data-ttu-id="feb04-124">Plug-ins síncronos são chamados pelo thread no qual o objeto de [**classe RealTimeStylus**](realtimestylus-class.md) é executado.</span><span class="sxs-lookup"><span data-stu-id="feb04-124">Synchronous plug-ins are called by the thread in which the [**RealTimeStylus Class**](realtimestylus-class.md) object executes.</span></span> <span data-ttu-id="feb04-125">Toda vez que o objeto de **classe RealTimeStylus** é instanciado, um thread de execução é instanciado.</span><span class="sxs-lookup"><span data-stu-id="feb04-125">Every time **RealTimeStylus Class** object is instantiated, an execution thread is instantiated.</span></span> <span data-ttu-id="feb04-126">Plug-ins síncronos são executados neste novo thread instanciado para a instância do objeto de **classe RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="feb04-126">Synchronous plug-ins are executed on this new thread instantiated for the instance of the **RealTimeStylus Class** object.</span></span> <span data-ttu-id="feb04-127">Plug-ins assíncronos são chamados por meio da interface do usuário ou do thread do aplicativo após o fluxo do pacote ter sido processado pelos plug-ins síncronos e armazenados na fila de saída.</span><span class="sxs-lookup"><span data-stu-id="feb04-127">Asynchronous plug-ins are called through the UI or application thread after the packet stream has been processed by the synchronous plug-ins and stored in the output queue.</span></span>

## <a name="related-topics"></a><span data-ttu-id="feb04-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="feb04-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feb04-129">**Interface IDynamicRenderer**</span><span class="sxs-lookup"><span data-stu-id="feb04-129">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[<span data-ttu-id="feb04-130">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="feb04-130">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[<span data-ttu-id="feb04-131">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="feb04-131">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[<span data-ttu-id="feb04-132">**IRealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="feb04-132">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
