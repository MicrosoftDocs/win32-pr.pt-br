---
description: A interface IRTC fornece os métodos usados para conectar o NPP à rede, capturar o tráfego de rede, recuperar estatísticas e desconectar o NPP da rede.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Interface IRTC (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c937d7d9233b1df063a7cf4a12e57e909145b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921365"
---
# <a name="irtc-interface"></a><span data-ttu-id="71beb-103">Interface IRTC</span><span class="sxs-lookup"><span data-stu-id="71beb-103">IRTC interface</span></span>

<span data-ttu-id="71beb-104">A interface **IRTC** fornece os métodos usados para conectar o NPP à rede, capturar o tráfego de rede, recuperar estatísticas e desconectar o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="71beb-104">The **IRTC** interface provides the methods used to connect the NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="71beb-105">**IRTC** Obtém uma interface para pontos de entrada somente locais, que são necessários para envolver a captura em tempo real.</span><span class="sxs-lookup"><span data-stu-id="71beb-105">**IRTC** gets an interface to local-only entry points, which are necessary to engage in real-time capture.</span></span> <span data-ttu-id="71beb-106">Essa interface inclui um método que transmite um retorno de chamada para o NPP.</span><span class="sxs-lookup"><span data-stu-id="71beb-106">This interface includes a method that hands off a callback to the NPP.</span></span>

## <a name="members"></a><span data-ttu-id="71beb-107">Membros</span><span class="sxs-lookup"><span data-stu-id="71beb-107">Members</span></span>

<span data-ttu-id="71beb-108">A interface **IRTC** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="71beb-108">The **IRTC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="71beb-109">**IRTC** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="71beb-109">**IRTC** also has these types of members:</span></span>

-   [<span data-ttu-id="71beb-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="71beb-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="71beb-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="71beb-111">Methods</span></span>

<span data-ttu-id="71beb-112">A interface **IRTC** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="71beb-112">The **IRTC** interface has these methods.</span></span>



| <span data-ttu-id="71beb-113">Método</span><span class="sxs-lookup"><span data-stu-id="71beb-113">Method</span></span>                                                              | <span data-ttu-id="71beb-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="71beb-114">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71beb-115">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="71beb-115">**Configure**</span></span>](irtc-configure.md)                                 | <span data-ttu-id="71beb-116">Define o gatilho, a correspondência de padrões e o tamanho do buffer da captura.</span><span class="sxs-lookup"><span data-stu-id="71beb-116">Sets the trigger, pattern match, and buffer size of the capture.</span></span><br/>                                                                             |
| [<span data-ttu-id="71beb-117">**Connect**</span><span class="sxs-lookup"><span data-stu-id="71beb-117">**Connect**</span></span>](irtc-connect.md)                                     | <span data-ttu-id="71beb-118">Conecta o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="71beb-118">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="71beb-119">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="71beb-119">**Disconnect**</span></span>](irtc-disconnect.md)                               | <span data-ttu-id="71beb-120">Desconecta o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="71beb-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="71beb-121">**Getcontrolstate**</span><span class="sxs-lookup"><span data-stu-id="71beb-121">**GetControlState**</span></span>](irtc-getcontrolstate.md)                     | <span data-ttu-id="71beb-122">Recupera o estado da [*captura*](c.md), que indica se a captura está em execução ou em pausa.</span><span class="sxs-lookup"><span data-stu-id="71beb-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="71beb-123">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="71beb-123">**GetConversationStatistics**</span></span>](irtc-getconversationstatistics.md) | <span data-ttu-id="71beb-124">Recupera informações de [*sessão*](s.md) e de [*estação*](s.md) para a captura atual.</span><span class="sxs-lookup"><span data-stu-id="71beb-124">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="71beb-125">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="71beb-125">**GetTotalStatistics**</span></span>](irtc-gettotalstatistics.md)               | <span data-ttu-id="71beb-126">Extrai tempo, buffer, Driver e outras estatísticas de rede da captura em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="71beb-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="71beb-127">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="71beb-127">**Pause**</span></span>](irtc-pause.md)                                         | <span data-ttu-id="71beb-128">Interrompe temporariamente a captura atual.</span><span class="sxs-lookup"><span data-stu-id="71beb-128">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="71beb-129">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="71beb-129">**QueryStations**</span></span>](irtc-querystations.md)                         | <span data-ttu-id="71beb-130">Recupera uma lista de todos os computadores em uma sub-rede que estão usando Monitor de Rede para capturar dados de rede.</span><span class="sxs-lookup"><span data-stu-id="71beb-130">Retrieves a list of all computers on a subnet that are using Network Monitor to capture network data.</span></span><br/>                                        |
| [<span data-ttu-id="71beb-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="71beb-131">**QueryStatus**</span></span>](irtc-querystatus.md)                             | <span data-ttu-id="71beb-132">Recupera o status do NPP.</span><span class="sxs-lookup"><span data-stu-id="71beb-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="71beb-133">**Retomar**</span><span class="sxs-lookup"><span data-stu-id="71beb-133">**Resume**</span></span>](irtc-resume.md)                                       | <span data-ttu-id="71beb-134">Reinicia uma captura pausada.</span><span class="sxs-lookup"><span data-stu-id="71beb-134">Restarts a paused capture.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="71beb-135">**Iniciar**</span><span class="sxs-lookup"><span data-stu-id="71beb-135">**Start**</span></span>](irtc-start.md)                                         | <span data-ttu-id="71beb-136">Inicia uma captura.</span><span class="sxs-lookup"><span data-stu-id="71beb-136">Starts a capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="71beb-137">**Stop**</span><span class="sxs-lookup"><span data-stu-id="71beb-137">**Stop**</span></span>](irtc-stop.md)                                           | <span data-ttu-id="71beb-138">Interrompe a captura atual.</span><span class="sxs-lookup"><span data-stu-id="71beb-138">Stops the current capture.</span></span><br/>                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="71beb-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71beb-139">Requirements</span></span>



| <span data-ttu-id="71beb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="71beb-140">Requirement</span></span> | <span data-ttu-id="71beb-141">Valor</span><span class="sxs-lookup"><span data-stu-id="71beb-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71beb-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71beb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="71beb-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="71beb-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="71beb-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71beb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="71beb-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="71beb-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="71beb-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="71beb-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="71beb-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="71beb-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="71beb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="71beb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71beb-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71beb-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

