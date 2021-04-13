---
title: Método onconnecting do IMsTscAxEvents
description: Chamado quando o controle de cliente começa a se conectar a um servidor em resposta a uma chamada para IMsTscAx Connect.
ms.assetid: c5e367a8-126a-48bb-bc94-1063f77e8239
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método onconnecting
- Método onconnecting Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método onconnecting
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2004fde83b79aff7b7c5082562de94f943eacb25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369224"
---
# <a name="imstscaxeventsonconnecting-method"></a><span data-ttu-id="ad99b-106">Método IMsTscAxEvents:: onconnecting</span><span class="sxs-lookup"><span data-stu-id="ad99b-106">IMsTscAxEvents::OnConnecting method</span></span>

<span data-ttu-id="ad99b-107">Chamado quando o controle de cliente começa a se conectar a um servidor em resposta a uma chamada para [**IMsTscAx:: Connect**](imstscax-connect.md).</span><span class="sxs-lookup"><span data-stu-id="ad99b-107">Called when the client control begins connecting to a server in response to a call to [**IMsTscAx::Connect**](imstscax-connect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad99b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad99b-108">Syntax</span></span>


```C++
void OnConnecting();
```



## <a name="parameters"></a><span data-ttu-id="ad99b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad99b-109">Parameters</span></span>

<span data-ttu-id="ad99b-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ad99b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad99b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad99b-111">Return value</span></span>

<span data-ttu-id="ad99b-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ad99b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad99b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad99b-113">Remarks</span></span>

<span data-ttu-id="ad99b-114">Implemente esse método em seu coletor de eventos para receber uma notificação de que o controle começou a se conectar.</span><span class="sxs-lookup"><span data-stu-id="ad99b-114">Implement this method in your event sink to receive notification that the control has begun connecting.</span></span>

## <a name="examples"></a><span data-ttu-id="ad99b-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ad99b-115">Examples</span></span>

<span data-ttu-id="ad99b-116">O exemplo a seguir mostra como tratar esse evento com Visual Basic código de script.</span><span class="sxs-lookup"><span data-stu-id="ad99b-116">The following example shows how to handle this event with Visual Basic Scripting code.</span></span> <span data-ttu-id="ad99b-117">A suposição neste exemplo é que seu objeto de controle é denominado "MsRdpClient".</span><span class="sxs-lookup"><span data-stu-id="ad99b-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="ad99b-118">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ad99b-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnConnecting()
    Msgbox("Connecting")
End sub
```



## <a name="requirements"></a><span data-ttu-id="ad99b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad99b-119">Requirements</span></span>



| <span data-ttu-id="ad99b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad99b-120">Requirement</span></span> | <span data-ttu-id="ad99b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ad99b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad99b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad99b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ad99b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad99b-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ad99b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad99b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ad99b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad99b-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ad99b-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ad99b-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="ad99b-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad99b-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ad99b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ad99b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad99b-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad99b-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ad99b-130">IID</span><span class="sxs-lookup"><span data-stu-id="ad99b-130">IID</span></span><br/>                      | <span data-ttu-id="ad99b-131">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="ad99b-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ad99b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad99b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad99b-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="ad99b-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





