---
description: A interface IStats fornece os métodos que você usa para conectar um NPP à rede, capturar o tráfego de rede, recuperar estatísticas e desconectar o NPP da rede. Essa interface gera estatísticas sem quadros.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: Interface IStats (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758176"
---
# <a name="istats-interface"></a><span data-ttu-id="15b2f-104">Interface IStats</span><span class="sxs-lookup"><span data-stu-id="15b2f-104">IStats interface</span></span>

<span data-ttu-id="15b2f-105">A interface **IStats** fornece os métodos que você usa para conectar um NPP à rede, capturar o tráfego de rede, recuperar estatísticas e desconectar o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="15b2f-105">The **IStats** interface provides the methods you use to connect an NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="15b2f-106">Essa interface gera estatísticas sem quadros.</span><span class="sxs-lookup"><span data-stu-id="15b2f-106">This interface generates statistics without frames.</span></span>

## <a name="members"></a><span data-ttu-id="15b2f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="15b2f-107">Members</span></span>

<span data-ttu-id="15b2f-108">A interface **IStats** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="15b2f-108">The **IStats** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="15b2f-109">**IStats** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="15b2f-109">**IStats** also has these types of members:</span></span>

-   [<span data-ttu-id="15b2f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="15b2f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="15b2f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="15b2f-111">Methods</span></span>

<span data-ttu-id="15b2f-112">A interface **IStats** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="15b2f-112">The **IStats** interface has these methods.</span></span>



| <span data-ttu-id="15b2f-113">Método</span><span class="sxs-lookup"><span data-stu-id="15b2f-113">Method</span></span>                                                                | <span data-ttu-id="15b2f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="15b2f-114">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15b2f-115">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="15b2f-115">**Configure**</span></span>](istats-configure.md)                                 | <span data-ttu-id="15b2f-116">Configura o gatilho, a correspondência de padrões e o tamanho do buffer do arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="15b2f-116">Configures the trigger, pattern match, and buffer size of the capture file.</span></span><br/>                                                                    |
| [<span data-ttu-id="15b2f-117">**Conectar**</span><span class="sxs-lookup"><span data-stu-id="15b2f-117">**Connect**</span></span>](istats-connect.md)                                     | <span data-ttu-id="15b2f-118">Conecta o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="15b2f-118">Connects the NPP to the network.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="15b2f-119">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="15b2f-119">**Disconnect**</span></span>](istats-disconnect.md)                               | <span data-ttu-id="15b2f-120">Desconecta o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="15b2f-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="15b2f-121">**Getcontrolstate**</span><span class="sxs-lookup"><span data-stu-id="15b2f-121">**GetControlState**</span></span>](istats-getcontrolstate.md)                     | <span data-ttu-id="15b2f-122">Recupera o estado da [*captura*](c.md), que indica se a captura está em execução ou em pausa.</span><span class="sxs-lookup"><span data-stu-id="15b2f-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                        |
| [<span data-ttu-id="15b2f-123">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="15b2f-123">**GetConversationStatistics**</span></span>](istats-getconversationstatistics.md) | <span data-ttu-id="15b2f-124">Recupera [*as informações*](s.md) de [*sessão*](s.md) e de estação sobre a captura atual.</span><span class="sxs-lookup"><span data-stu-id="15b2f-124">Retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span><br/> |
| [<span data-ttu-id="15b2f-125">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="15b2f-125">**GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)               | <span data-ttu-id="15b2f-126">Extrai tempo, buffer, Driver e outras estatísticas de rede da captura em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="15b2f-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                                |
| [<span data-ttu-id="15b2f-127">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="15b2f-127">**Pause**</span></span>](istats-pause.md)                                         | <span data-ttu-id="15b2f-128">Interrompe temporariamente a captura atual.</span><span class="sxs-lookup"><span data-stu-id="15b2f-128">Temporarily stops the current capture.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="15b2f-129">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="15b2f-129">**QueryStations**</span></span>](istats-querystations.md)                         | <span data-ttu-id="15b2f-130">Recupera uma lista de todos os computadores que estão usando Monitor de Rede para capturar dados em uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="15b2f-130">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                                                  |
| [<span data-ttu-id="15b2f-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="15b2f-131">**QueryStatus**</span></span>](istats-querystatus.md)                             | <span data-ttu-id="15b2f-132">Recupera o status do NPP.</span><span class="sxs-lookup"><span data-stu-id="15b2f-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="15b2f-133">**Retomar**</span><span class="sxs-lookup"><span data-stu-id="15b2f-133">**Resume**</span></span>](istats-resume.md)                                       | <span data-ttu-id="15b2f-134">Reinicia uma captura pausada.</span><span class="sxs-lookup"><span data-stu-id="15b2f-134">Restarts a paused capture.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="15b2f-135">**Iniciar**</span><span class="sxs-lookup"><span data-stu-id="15b2f-135">**Start**</span></span>](istats-start.md)                                         | <span data-ttu-id="15b2f-136">Inicia a captura.</span><span class="sxs-lookup"><span data-stu-id="15b2f-136">Starts the capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="15b2f-137">**Stop**</span><span class="sxs-lookup"><span data-stu-id="15b2f-137">**Stop**</span></span>](istats-stop.md)                                           | <span data-ttu-id="15b2f-138">Interrompe a captura atual.</span><span class="sxs-lookup"><span data-stu-id="15b2f-138">Stops the current capture.</span></span><br/>                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="15b2f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15b2f-139">Requirements</span></span>



| <span data-ttu-id="15b2f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="15b2f-140">Requirement</span></span> | <span data-ttu-id="15b2f-141">Valor</span><span class="sxs-lookup"><span data-stu-id="15b2f-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15b2f-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15b2f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="15b2f-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15b2f-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="15b2f-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15b2f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="15b2f-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15b2f-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="15b2f-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="15b2f-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="15b2f-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="15b2f-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="15b2f-148">DLL</span><span class="sxs-lookup"><span data-stu-id="15b2f-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15b2f-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15b2f-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

