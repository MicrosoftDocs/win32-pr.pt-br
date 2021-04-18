---
description: A interface IDelaydC fornece os métodos usados para se conectar à rede, capturar o tráfego de rede para um arquivo de captura, recuperar estatísticas e desconectar da rede.
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Interface IDelaydC (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: cb87bc9f821e758b83a1bc3dee5d81a4b1b771d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760408"
---
# <a name="idelaydc-interface"></a><span data-ttu-id="77126-103">Interface IDelaydC</span><span class="sxs-lookup"><span data-stu-id="77126-103">IDelaydC interface</span></span>

<span data-ttu-id="77126-104">A interface **IDelaydC** fornece os métodos usados para se conectar à rede, capturar o tráfego de rede para um arquivo de captura, recuperar estatísticas e desconectar da rede.</span><span class="sxs-lookup"><span data-stu-id="77126-104">The **IDelaydC** interface provides the methods used to connect to the network, capture network traffic to a capture file, retrieve statistics, and disconnect from the network.</span></span>

<span data-ttu-id="77126-105">Essa interface captura quadros do fluxo de dados de rede e, em seguida, copia os quadros em um arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="77126-105">This interface captures frames from the network data stream and then copies the frames to a capture file.</span></span> <span data-ttu-id="77126-106">Essa interface é usada pelos aplicativos Monitor de Rede e NPP.</span><span class="sxs-lookup"><span data-stu-id="77126-106">This interface is used by Network Monitor and NPP applications.</span></span> <span data-ttu-id="77126-107">Para receber os dados de rede, a NIC de destino deve dar suporte ao modo promíscuo.</span><span class="sxs-lookup"><span data-stu-id="77126-107">To receive the network data, the targeted NIC must support promiscuous mode.</span></span>

## <a name="members"></a><span data-ttu-id="77126-108">Membros</span><span class="sxs-lookup"><span data-stu-id="77126-108">Members</span></span>

<span data-ttu-id="77126-109">A interface **IDelaydC** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="77126-109">The **IDelaydC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="77126-110">**IDelaydC** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="77126-110">**IDelaydC** also has these types of members:</span></span>

-   [<span data-ttu-id="77126-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="77126-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="77126-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="77126-112">Methods</span></span>

<span data-ttu-id="77126-113">A interface **IDelaydC** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="77126-113">The **IDelaydC** interface has these methods.</span></span>



| <span data-ttu-id="77126-114">Método</span><span class="sxs-lookup"><span data-stu-id="77126-114">Method</span></span>                                                                  | <span data-ttu-id="77126-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="77126-115">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77126-116">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="77126-116">**Configure**</span></span>](idelaydc-configure.md)                                 | <span data-ttu-id="77126-117">Envia informações de configuração usadas para uma captura.</span><span class="sxs-lookup"><span data-stu-id="77126-117">Submits configuration information used for a capture.</span></span><br/>                                                                                        |
| [<span data-ttu-id="77126-118">**Conectar**</span><span class="sxs-lookup"><span data-stu-id="77126-118">**Connect**</span></span>](idelaydc-connect.md)                                     | <span data-ttu-id="77126-119">Conecta o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="77126-119">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="77126-120">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="77126-120">**Disconnect**</span></span>](idelaydc-disconnect.md)                               | <span data-ttu-id="77126-121">Desconecta o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="77126-121">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="77126-122">**Getcontrolstate**</span><span class="sxs-lookup"><span data-stu-id="77126-122">**GetControlState**</span></span>](idelaydc-getcontrolstate.md)                     | <span data-ttu-id="77126-123">Recupera o estado da [*captura*](c.md), que indica se a captura está em execução ou em pausa.</span><span class="sxs-lookup"><span data-stu-id="77126-123">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="77126-124">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="77126-124">**GetConversationStatistics**</span></span>](idelaydc-getconversationstatistics.md) | <span data-ttu-id="77126-125">Recupera informações de [*sessão*](s.md) e de [*estação*](s.md) para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="77126-125">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="77126-126">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="77126-126">**GetTotalStatistics**</span></span>](idelaydc-gettotalstatistics.md)               | <span data-ttu-id="77126-127">Extrai tempo, buffer, Driver e outras estatísticas de rede da captura em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="77126-127">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="77126-128">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="77126-128">**Pause**</span></span>](idelaydc-pause.md)                                         | <span data-ttu-id="77126-129">Interrompe temporariamente a captura atual.</span><span class="sxs-lookup"><span data-stu-id="77126-129">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="77126-130">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="77126-130">**QueryStations**</span></span>](idelaydc-querystations.md)                         | <span data-ttu-id="77126-131">Recupera uma lista de todos os computadores que usam Monitor de Rede para capturar dados em uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="77126-131">Retrieves a list of all computers that use Network Monitor to capture data on a subnet.</span></span><br/>                                                      |
| [<span data-ttu-id="77126-132">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="77126-132">**QueryStatus**</span></span>](idelaydc-querystatus.md)                             | <span data-ttu-id="77126-133">Recupera o status do NPP.</span><span class="sxs-lookup"><span data-stu-id="77126-133">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="77126-134">**Retomar**</span><span class="sxs-lookup"><span data-stu-id="77126-134">**Resume**</span></span>](idelaydc-resume.md)                                       | <span data-ttu-id="77126-135">Retoma uma captura pausada.</span><span class="sxs-lookup"><span data-stu-id="77126-135">Resumes a paused capture.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="77126-136">**Iniciar**</span><span class="sxs-lookup"><span data-stu-id="77126-136">**Start**</span></span>](idelaydc-start.md)                                         | <span data-ttu-id="77126-137">Inicia uma captura e cria o [*arquivo de captura*](c.md).</span><span class="sxs-lookup"><span data-stu-id="77126-137">Starts a capture and creates the [*capture file*](c.md).</span></span><br/>                                                           |
| [<span data-ttu-id="77126-138">**Stop**</span><span class="sxs-lookup"><span data-stu-id="77126-138">**Stop**</span></span>](idelaydc-stop.md)                                           | <span data-ttu-id="77126-139">Interrompe a captura atual e fecha o [*arquivo de captura*](c.md).</span><span class="sxs-lookup"><span data-stu-id="77126-139">Stops the current capture and closes the [*capture file*](c.md).</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="77126-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77126-140">Requirements</span></span>



| <span data-ttu-id="77126-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="77126-141">Requirement</span></span> | <span data-ttu-id="77126-142">Valor</span><span class="sxs-lookup"><span data-stu-id="77126-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77126-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77126-143">Minimum supported client</span></span><br/> | <span data-ttu-id="77126-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="77126-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="77126-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77126-145">Minimum supported server</span></span><br/> | <span data-ttu-id="77126-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="77126-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="77126-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="77126-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="77126-148"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="77126-148"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="77126-149">DLL</span><span class="sxs-lookup"><span data-stu-id="77126-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77126-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77126-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

