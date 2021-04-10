---
description: A interface IESP fornece os métodos que conectam o NPP à rede, capturam o tráfego de rede para um arquivo de captura, recuperam estatísticas e desconectam o NPP da rede.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: Interface IESP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a7400bb9a16e6ece5f5f26fe95a0398a7d45e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090255"
---
# <a name="iesp-interface"></a><span data-ttu-id="0aefc-103">Interface IESP</span><span class="sxs-lookup"><span data-stu-id="0aefc-103">IESP interface</span></span>

<span data-ttu-id="0aefc-104">A interface **IESP** fornece os métodos que conectam o NPP à rede, capturam o tráfego de rede para um arquivo de captura, recuperam estatísticas e desconectam o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="0aefc-104">The **IESP** interface provides the methods that connect the NPP to the network, capture network traffic to a capture file, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="0aefc-105">Essa interface é usada principalmente quando você precisa coletar estatísticas de [*conversa*](c.md) de rede em um formato de arquivo ESP proprietário.</span><span class="sxs-lookup"><span data-stu-id="0aefc-105">This interface is used primarily when you need to collect network [*conversation statistics*](c.md) in a proprietary ESP file format.</span></span>

## <a name="members"></a><span data-ttu-id="0aefc-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0aefc-106">Members</span></span>

<span data-ttu-id="0aefc-107">A interface **IESP** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0aefc-107">The **IESP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0aefc-108">**IESP** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0aefc-108">**IESP** also has these types of members:</span></span>

-   [<span data-ttu-id="0aefc-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0aefc-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0aefc-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="0aefc-110">Methods</span></span>

<span data-ttu-id="0aefc-111">A interface **IESP** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0aefc-111">The **IESP** interface has these methods.</span></span>



| <span data-ttu-id="0aefc-112">Método</span><span class="sxs-lookup"><span data-stu-id="0aefc-112">Method</span></span>                                          | <span data-ttu-id="0aefc-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="0aefc-113">Description</span></span>                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0aefc-114">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="0aefc-114">**Configure**</span></span>](iesp-configure.md)             | <span data-ttu-id="0aefc-115">Envia informações de configuração para uma captura</span><span class="sxs-lookup"><span data-stu-id="0aefc-115">Submits configuration information for a capture</span></span><br/>                                                                         |
| [<span data-ttu-id="0aefc-116">**Connect**</span><span class="sxs-lookup"><span data-stu-id="0aefc-116">**Connect**</span></span>](iesp-connect.md)                 | <span data-ttu-id="0aefc-117">Conecta o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="0aefc-117">Connects the NPP to the network.</span></span><br/>                                                                                        |
| [<span data-ttu-id="0aefc-118">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="0aefc-118">**Disconnect**</span></span>](iesp-disconnect.md)           | <span data-ttu-id="0aefc-119">Desconecta o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="0aefc-119">Disconnects the NPP from the network.</span></span><br/>                                                                                   |
| [<span data-ttu-id="0aefc-120">**Getcontrolstate**</span><span class="sxs-lookup"><span data-stu-id="0aefc-120">**GetControlState**</span></span>](iesp-getcontrolstate.md) | <span data-ttu-id="0aefc-121">Recupera o estado da [*captura*](c.md), que indica se a captura está em execução ou em pausa.</span><span class="sxs-lookup"><span data-stu-id="0aefc-121">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/> |
| [<span data-ttu-id="0aefc-122">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="0aefc-122">**Pause**</span></span>](iesp-pause.md)                     | <span data-ttu-id="0aefc-123">Interrompe temporariamente a captura atual.</span><span class="sxs-lookup"><span data-stu-id="0aefc-123">Temporarily stops the current capture.</span></span><br/>                                                                                  |
| [<span data-ttu-id="0aefc-124">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="0aefc-124">**QueryStations**</span></span>](iesp-querystations.md)     | <span data-ttu-id="0aefc-125">Recupera uma lista de todos os computadores que estão usando Monitor de Rede para capturar dados em uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="0aefc-125">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                           |
| [<span data-ttu-id="0aefc-126">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="0aefc-126">**QueryStatus**</span></span>](iesp-querystatus.md)         | <span data-ttu-id="0aefc-127">Recupera o status do NPP.</span><span class="sxs-lookup"><span data-stu-id="0aefc-127">Retrieves the status of the NPP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="0aefc-128">**Retomar**</span><span class="sxs-lookup"><span data-stu-id="0aefc-128">**Resume**</span></span>](iesp-resume.md)                   | <span data-ttu-id="0aefc-129">Retoma uma captura pausada.</span><span class="sxs-lookup"><span data-stu-id="0aefc-129">Resumes a paused capture.</span></span><br/>                                                                                               |
| [<span data-ttu-id="0aefc-130">**Iniciar**</span><span class="sxs-lookup"><span data-stu-id="0aefc-130">**Start**</span></span>](iesp-start.md)                     | <span data-ttu-id="0aefc-131">Inicia a captura e cria o arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="0aefc-131">Starts the capture and creates the capture file.</span></span><br/>                                                                        |
| [<span data-ttu-id="0aefc-132">**Stop**</span><span class="sxs-lookup"><span data-stu-id="0aefc-132">**Stop**</span></span>](iesp-stop.md)                       | <span data-ttu-id="0aefc-133">Interrompe a captura atual.</span><span class="sxs-lookup"><span data-stu-id="0aefc-133">Stops the current capture.</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="0aefc-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aefc-134">Requirements</span></span>



| <span data-ttu-id="0aefc-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aefc-135">Requirement</span></span> | <span data-ttu-id="0aefc-136">Valor</span><span class="sxs-lookup"><span data-stu-id="0aefc-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aefc-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0aefc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0aefc-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0aefc-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0aefc-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0aefc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0aefc-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0aefc-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0aefc-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0aefc-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aefc-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aefc-142"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0aefc-143">DLL</span><span class="sxs-lookup"><span data-stu-id="0aefc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aefc-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aefc-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

