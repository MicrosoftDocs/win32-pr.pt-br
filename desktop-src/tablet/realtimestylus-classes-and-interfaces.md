---
description: Esta seção contém informações sobre as interfaces e classes usadas na caneta em tempo real.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: Interfaces e classes do RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828896"
---
# <a name="realtimestylus-classes-and-interfaces"></a><span data-ttu-id="2adb1-103">Interfaces e classes do RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="2adb1-103">RealTimeStylus Classes and Interfaces</span></span>

<span data-ttu-id="2adb1-104">Esta seção contém informações sobre as interfaces e classes usadas na caneta em tempo real.</span><span class="sxs-lookup"><span data-stu-id="2adb1-104">This section contains information about the interfaces and classes used in the real time stylus.</span></span>

> [!Note]  
> <span data-ttu-id="2adb1-105">As classes e interfaces de caneta em tempo real não são compatíveis com a automação.</span><span class="sxs-lookup"><span data-stu-id="2adb1-105">The real time stylus classes and interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="2adb1-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2adb1-106">In This Section</span></span>



| <span data-ttu-id="2adb1-107">Classe</span><span class="sxs-lookup"><span data-stu-id="2adb1-107">Class</span></span>                                                      | <span data-ttu-id="2adb1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2adb1-108">Description</span></span>                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2adb1-109">**Classe RealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="2adb1-109">**RealTimeStylus Class**</span></span>](realtimestylus-class.md)       | <span data-ttu-id="2adb1-110">Implementa a interface [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .</span><span class="sxs-lookup"><span data-stu-id="2adb1-110">Implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) interface.</span></span><br/>                 |
| <span data-ttu-id="2adb1-111">[**Classe DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2adb1-111">[**DynamicRenderer Class**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span></span>     | <span data-ttu-id="2adb1-112">Implementa a interface de [**interface IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) .</span><span class="sxs-lookup"><span data-stu-id="2adb1-112">Implements the [**IDynamicRenderer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) interface.</span></span><br/>     |
| [<span data-ttu-id="2adb1-113">**Classe GestureRecognizer**</span><span class="sxs-lookup"><span data-stu-id="2adb1-113">**GestureRecognizer Class**</span></span>](gesturerecognizer-class.md) | <span data-ttu-id="2adb1-114">Implementa a interface de [**interface IGestureRecognizer**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) .</span><span class="sxs-lookup"><span data-stu-id="2adb1-114">Implements the [**IGestureRecognizer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) interface.</span></span><br/> |
| [<span data-ttu-id="2adb1-115">**Classe StrokeBuilder**</span><span class="sxs-lookup"><span data-stu-id="2adb1-115">**StrokeBuilder Class**</span></span>](strokebuilder-class.md)         | <span data-ttu-id="2adb1-116">Implementa a interface de [**interface IStrokeBuilder**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) .</span><span class="sxs-lookup"><span data-stu-id="2adb1-116">Implements the [**IStrokeBuilder Interface**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) interface.</span></span><br/>         |



 

## <a name="interfaces"></a><span data-ttu-id="2adb1-117">Interfaces</span><span class="sxs-lookup"><span data-stu-id="2adb1-117">Interfaces</span></span>



| <span data-ttu-id="2adb1-118">Interface</span><span class="sxs-lookup"><span data-stu-id="2adb1-118">Interface</span></span>                                                                          | <span data-ttu-id="2adb1-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="2adb1-119">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2adb1-120">**Interface IDynamicRenderer**</span><span class="sxs-lookup"><span data-stu-id="2adb1-120">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | <span data-ttu-id="2adb1-121">Expõe métodos que permitem controlar a exibição de dados da caneta em tempo real à medida que os dados estão sendo manipulados pelo objeto da [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="2adb1-121">Exposes methods enabling you to control the display of stylus data in real time as the data is being handled by the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/> |
| [<span data-ttu-id="2adb1-122">**Interface IGestureRecognizer**</span><span class="sxs-lookup"><span data-stu-id="2adb1-122">**IGestureRecognizer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | <span data-ttu-id="2adb1-123">Expõe métodos que permitem reagir a eventos reconhecendo gestos da caneta e permitindo que você adicione dados à fila de entrada.</span><span class="sxs-lookup"><span data-stu-id="2adb1-123">Exposes methods enabling you to react to events by recognizing stylus gestures and enabling you to add data to the input queue.</span></span><br/>                                                  |
| [<span data-ttu-id="2adb1-124">**IRealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="2adb1-124">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | <span data-ttu-id="2adb1-125">Manipula os dados de pacote da caneta de um digitalizador em tempo real.</span><span class="sxs-lookup"><span data-stu-id="2adb1-125">Handles the stylus packet data from a digitizer in real time.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="2adb1-126">**IRealTimeStylus2**</span><span class="sxs-lookup"><span data-stu-id="2adb1-126">**IRealTimeStylus2**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | <span data-ttu-id="2adb1-127">Estende a interface IRealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="2adb1-127">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="2adb1-128">**IRealTimeStylus3**</span><span class="sxs-lookup"><span data-stu-id="2adb1-128">**IRealTimeStylus3**</span></span>](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | <span data-ttu-id="2adb1-129">Estende a interface IRealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="2adb1-129">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="2adb1-130">**Interface IRealTimeStylusSynchronization**</span><span class="sxs-lookup"><span data-stu-id="2adb1-130">**IRealTimeStylusSynchronization Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | <span data-ttu-id="2adb1-131">Sincroniza o acesso ao objeto da [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="2adb1-131">Synchronizes access to the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/>                                                                                          |
| [<span data-ttu-id="2adb1-132">**Interface IStrokeBuilder**</span><span class="sxs-lookup"><span data-stu-id="2adb1-132">**IStrokeBuilder Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | <span data-ttu-id="2adb1-133">Expõe métodos que permitem criar traços programaticamente.</span><span class="sxs-lookup"><span data-stu-id="2adb1-133">Exposes methods that enable you to programmatically create strokes.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="2adb1-134">**Interface IStylusPlugin**</span><span class="sxs-lookup"><span data-stu-id="2adb1-134">**IStylusPlugin Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | <span data-ttu-id="2adb1-135">Expõe métodos que permitem que você receba notificações de eventos e execute o processamento personalizado com base nesses eventos.</span><span class="sxs-lookup"><span data-stu-id="2adb1-135">Exposes methods enabling you to receive notifications of events and to perform custom processing based on those events.</span></span><br/>                                                          |
| [<span data-ttu-id="2adb1-136">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="2adb1-136">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | <span data-ttu-id="2adb1-137">Representa um plug-in assíncrono que pode ser adicionado à coleção de plug-ins assíncrono da [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="2adb1-137">Represents an asynchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) asynchronous plug-in collection.</span></span><br/>                                |
| [<span data-ttu-id="2adb1-138">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="2adb1-138">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | <span data-ttu-id="2adb1-139">Representa um plug-in síncrono que pode ser adicionado à coleção de plug-ins síncrona da [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="2adb1-139">Represents a synchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) synchronous plug-in collection.</span></span><br/>                                   |



 

## <a name="return-values"></a><span data-ttu-id="2adb1-140">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="2adb1-140">Return Values</span></span>

<span data-ttu-id="2adb1-141">Os métodos na biblioteca COM retornam valores de **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2adb1-141">Methods in the COM Library return values of **HRESULT**.</span></span> <span data-ttu-id="2adb1-142">Salvo indicação em contrário, os significados dos valores **HRESULT** são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2adb1-142">Unless otherwise noted, the meanings of the **HRESULT** values are described in the following table.</span></span>



| <span data-ttu-id="2adb1-143">Valor HRESULT</span><span class="sxs-lookup"><span data-stu-id="2adb1-143">HRESULT value</span></span>                                   | <span data-ttu-id="2adb1-144">Description</span><span class="sxs-lookup"><span data-stu-id="2adb1-144">Description</span></span>                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2adb1-145">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="2adb1-145">S\_OK</span></span><br/>                                | <span data-ttu-id="2adb1-146">Êxito.</span><span class="sxs-lookup"><span data-stu-id="2adb1-146">Success.</span></span><br/>                                                                      |
| <span data-ttu-id="2adb1-147">\_ponteiro E</span><span class="sxs-lookup"><span data-stu-id="2adb1-147">E\_POINTER</span></span><br/>                           | <span data-ttu-id="2adb1-148">Pelo menos um ponteiro (para um parâmetro de entrada ou de saída) é inválido.</span><span class="sxs-lookup"><span data-stu-id="2adb1-148">At least one pointer (for either an input or an output parameter) is invalid.</span></span><br/> |
| <span data-ttu-id="2adb1-149">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2adb1-149">E\_INVALIDARG</span></span><br/>                        | <span data-ttu-id="2adb1-150">O membro tentou passar um argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="2adb1-150">Member attempted to pass in an invalid argument.</span></span><br/>                              |
| <span data-ttu-id="2adb1-151">\_exceção de tinta E \_</span><span class="sxs-lookup"><span data-stu-id="2adb1-151">E\_INK\_EXCEPTION</span></span><br/>                    | <span data-ttu-id="2adb1-152">Exceção ocorreu.</span><span class="sxs-lookup"><span data-stu-id="2adb1-152">Exception occurred.</span></span><br/>                                                           |
| <span data-ttu-id="2adb1-153">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="2adb1-153">E\_OUTOFMEMORY</span></span><br/>                       | <span data-ttu-id="2adb1-154">O sistema não pode alocar memória para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="2adb1-154">System cannot allocate memory to complete the operation.</span></span><br/>                      |
| <span data-ttu-id="2adb1-155">E \_ falha</span><span class="sxs-lookup"><span data-stu-id="2adb1-155">E\_FAIL</span></span><br/>                              | <span data-ttu-id="2adb1-156">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="2adb1-156">Unspecified failure occurred.</span></span><br/>                                                 |
| <span data-ttu-id="2adb1-157">E \_ INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="2adb1-157">E\_INVALIDOPERATION</span></span><br/>                  | <span data-ttu-id="2adb1-158">O membro tentou usar uma operação inválida.</span><span class="sxs-lookup"><span data-stu-id="2adb1-158">Member attempted to use an invalid operation.</span></span><br/>                                 |
| <span data-ttu-id="2adb1-159">modo do TPC \_ E \_ inválido \_</span><span class="sxs-lookup"><span data-stu-id="2adb1-159">TPC\_E\_INVALID\_MODE</span></span><br/>                | <span data-ttu-id="2adb1-160">O membro tentou usar um modo inválido.</span><span class="sxs-lookup"><span data-stu-id="2adb1-160">Member attempted to use an invalid mode.</span></span><br/>                                      |
| <span data-ttu-id="2adb1-161">configuração de TPC \_ E \_ inválido \_</span><span class="sxs-lookup"><span data-stu-id="2adb1-161">TPC\_E\_INVALID\_CONFIGURATION</span></span><br/>       | <span data-ttu-id="2adb1-162">O membro tentou usar uma configuração inválida.</span><span class="sxs-lookup"><span data-stu-id="2adb1-162">Member attempted to use an invalid configuration.</span></span><br/>                             |
| <span data-ttu-id="2adb1-163">\_Descrição do pacote TPC E \_ inválido \_ \_</span><span class="sxs-lookup"><span data-stu-id="2adb1-163">TPC\_E\_INVALID\_PACKET\_DESCRIPTION</span></span><br/> | <span data-ttu-id="2adb1-164">O membro tentou usar uma descrição de pacote inválida.</span><span class="sxs-lookup"><span data-stu-id="2adb1-164">Member attempted to use an invalid packet description.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="2adb1-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2adb1-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2adb1-166">Referência do RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="2adb1-166">RealTimeStylus Reference</span></span>](realtimestylus-reference.md)
</dt> </dl>

 

 
