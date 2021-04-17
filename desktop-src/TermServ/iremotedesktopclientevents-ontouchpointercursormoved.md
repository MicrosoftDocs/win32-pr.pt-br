---
title: Método IRemoteDesktopClientEvents OnTouchPointerCursorMoved
description: Chamado quando o cursor do ponteiro de toque foi movido e a propriedade EventsEnabled está definida como true.
ms.assetid: 55A6AC99-0723-4215-9428-D2DAAC77A74A
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnTouchPointerCursorMoved
- Método OnTouchPointerCursorMoved Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents, método OnTouchPointerCursorMoved
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnTouchPointerCursorMoved
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae347e19942bf0c82112e5cec6a3fb4fe131349f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755157"
---
# <a name="iremotedesktopclienteventsontouchpointercursormoved-method"></a><span data-ttu-id="6138d-106">Método IRemoteDesktopClientEvents:: OnTouchPointerCursorMoved</span><span class="sxs-lookup"><span data-stu-id="6138d-106">IRemoteDesktopClientEvents::OnTouchPointerCursorMoved method</span></span>

<span data-ttu-id="6138d-107">Chamado quando o cursor do ponteiro de toque foi movido e a propriedade [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) está definida como true.</span><span class="sxs-lookup"><span data-stu-id="6138d-107">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span>

## <a name="syntax"></a><span data-ttu-id="6138d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6138d-108">Syntax</span></span>


```C++
void OnTouchPointerCursorMoved(
  [in] long x,
  [in] long y
);
```



## <a name="parameters"></a><span data-ttu-id="6138d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6138d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6138d-110">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="6138d-110">*x* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6138d-111">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="6138d-111">*y* \[in\]</span></span>
<span data-ttu-id="6138d-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6138d-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="6138d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6138d-113">Return value</span></span>

<span data-ttu-id="6138d-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6138d-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6138d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6138d-115">Requirements</span></span>



| <span data-ttu-id="6138d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6138d-116">Requirement</span></span> | <span data-ttu-id="6138d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6138d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6138d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6138d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6138d-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6138d-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="6138d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6138d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6138d-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6138d-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="6138d-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6138d-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="6138d-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6138d-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="6138d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6138d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6138d-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6138d-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="6138d-126">IID</span><span class="sxs-lookup"><span data-stu-id="6138d-126">IID</span></span><br/>                      | <span data-ttu-id="6138d-127">DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="6138d-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6138d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6138d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6138d-129">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="6138d-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

