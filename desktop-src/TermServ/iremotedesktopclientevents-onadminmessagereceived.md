---
title: Método IRemoteDesktopClientEvents OnAdminMessageReceived
description: Chamado quando o controle de cliente recebe uma mensagem administrativa.
ms.assetid: CD580207-CEC1-493B-989E-7C1D4FA71228
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnAdminMessageReceived
- Método OnAdminMessageReceived Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientEvents
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientEvents, método OnAdminMessageReceived
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAdminMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201dd3111dbac0b6395654ef8dfad21318419de3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369775"
---
# <a name="iremotedesktopclienteventsonadminmessagereceived-method"></a><span data-ttu-id="a055f-106">Método IRemoteDesktopClientEvents:: OnAdminMessageReceived</span><span class="sxs-lookup"><span data-stu-id="a055f-106">IRemoteDesktopClientEvents::OnAdminMessageReceived method</span></span>

<span data-ttu-id="a055f-107">Chamado quando o controle de cliente recebe uma mensagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="a055f-107">Called when the client control receives an administrative message.</span></span>

## <a name="syntax"></a><span data-ttu-id="a055f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a055f-108">Syntax</span></span>


```C++
void OnAdminMessageReceived(
  [in] BSTR adminMessage
);
```



## <a name="parameters"></a><span data-ttu-id="a055f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a055f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a055f-110">*adminMessage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a055f-110">*adminMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a055f-111">A mensagem.</span><span class="sxs-lookup"><span data-stu-id="a055f-111">The message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a055f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a055f-112">Return value</span></span>

<span data-ttu-id="a055f-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a055f-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a055f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a055f-114">Requirements</span></span>



| <span data-ttu-id="a055f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a055f-115">Requirement</span></span> | <span data-ttu-id="a055f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a055f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a055f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a055f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a055f-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a055f-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="a055f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a055f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a055f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a055f-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="a055f-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a055f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a055f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a055f-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="a055f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a055f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a055f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a055f-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="a055f-125">IID</span><span class="sxs-lookup"><span data-stu-id="a055f-125">IID</span></span><br/>                      | <span data-ttu-id="a055f-126">DIID \_ IRemoteDesktopClientEvents é definido como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="a055f-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a055f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a055f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a055f-128">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="a055f-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





