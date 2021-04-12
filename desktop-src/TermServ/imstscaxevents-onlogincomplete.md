---
title: Método IMsTscAxEvents OnLoginComplete
description: Chamado quando o controle de cliente tiver feito logon com êxito em um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), seguindo a exibição da caixa de diálogo de logon do Windows.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnLoginComplete
- Método OnLoginComplete Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnLoginComplete
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d6b63f74ed99c8af939bafdc8a55a41e33b404
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499467"
---
# <a name="imstscaxeventsonlogincomplete-method"></a><span data-ttu-id="6d47f-106">Método IMsTscAxEvents:: OnLoginComplete</span><span class="sxs-lookup"><span data-stu-id="6d47f-106">IMsTscAxEvents::OnLoginComplete method</span></span>

<span data-ttu-id="6d47f-107">Chamado quando o controle de cliente tiver feito logon com êxito em um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), seguindo a exibição da caixa de diálogo de logon do Windows.</span><span class="sxs-lookup"><span data-stu-id="6d47f-107">Called when the client control has successfully logged on to a Remote Desktop Session Host (RD Session Host) server, following the display of the Windows Logon dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d47f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d47f-108">Syntax</span></span>


```C++
void OnLoginComplete();
```



## <a name="parameters"></a><span data-ttu-id="6d47f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d47f-109">Parameters</span></span>

<span data-ttu-id="6d47f-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6d47f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d47f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d47f-111">Return value</span></span>

<span data-ttu-id="6d47f-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6d47f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d47f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d47f-113">Remarks</span></span>

<span data-ttu-id="6d47f-114">Implemente esse método em seu coletor de eventos para receber uma notificação de que o controle concluiu o logon.</span><span class="sxs-lookup"><span data-stu-id="6d47f-114">Implement this method in your event sink to receive notification that the control has completed logon.</span></span>

## <a name="examples"></a><span data-ttu-id="6d47f-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d47f-115">Examples</span></span>

<span data-ttu-id="6d47f-116">O exemplo a seguir mostra como lidar com esse evento usando Visual Basic código de script.</span><span class="sxs-lookup"><span data-stu-id="6d47f-116">The following example shows how to handle this event by using Visual Basic Scripting code.</span></span> <span data-ttu-id="6d47f-117">A suposição neste exemplo é que seu objeto de controle é denominado "MsRdpClient".</span><span class="sxs-lookup"><span data-stu-id="6d47f-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="6d47f-118">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6d47f-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
End sub
```



## <a name="requirements"></a><span data-ttu-id="6d47f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d47f-119">Requirements</span></span>



| <span data-ttu-id="6d47f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d47f-120">Requirement</span></span> | <span data-ttu-id="6d47f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6d47f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d47f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d47f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6d47f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d47f-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6d47f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d47f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6d47f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d47f-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6d47f-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6d47f-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d47f-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d47f-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6d47f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6d47f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d47f-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d47f-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6d47f-130">IID</span><span class="sxs-lookup"><span data-stu-id="6d47f-130">IID</span></span><br/>                      | <span data-ttu-id="6d47f-131">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="6d47f-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="6d47f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d47f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d47f-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="6d47f-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





