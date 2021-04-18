---
title: Método IMsTscAxEvents OnIdleTimeoutNotification
description: Chamado quando não há entrada de mouse ou de teclado pelo usuário durante o período definido pelo método IMsRdpClientAdvancedSettings Put \_ MinutesToIdleTimeout.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnIdleTimeoutNotification
- Método OnIdleTimeoutNotification Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnIdleTimeoutNotification
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e305b0ed22e733053e33451aa35d3b8f8d6c138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781019"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a><span data-ttu-id="69f66-106">Método IMsTscAxEvents:: OnIdleTimeoutNotification</span><span class="sxs-lookup"><span data-stu-id="69f66-106">IMsTscAxEvents::OnIdleTimeoutNotification method</span></span>

<span data-ttu-id="69f66-107">Chamado quando não há entrada de mouse ou de teclado pelo usuário durante o período definido pelo método [**IMsRdpClientAdvancedSettings::p UT \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="69f66-107">Called when there has been no mouse or keyboard input by the user during the period of time set by the [**IMsRdpClientAdvancedSettings::put\_MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f66-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69f66-108">Syntax</span></span>


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a><span data-ttu-id="69f66-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69f66-109">Parameters</span></span>

<span data-ttu-id="69f66-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="69f66-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69f66-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69f66-111">Return value</span></span>

<span data-ttu-id="69f66-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="69f66-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69f66-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="69f66-113">Remarks</span></span>

<span data-ttu-id="69f66-114">Por padrão, o valor da propriedade [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) é definido como zero e o sistema não monitora o tempo limite de ociosidade.</span><span class="sxs-lookup"><span data-stu-id="69f66-114">By default, the value of the [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) property is set to zero and the system does not monitor for idle time-outs.</span></span> <span data-ttu-id="69f66-115">Esse evento ocorrerá somente se a propriedade estiver definida como um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="69f66-115">This event occurs only if the property is set to a nonzero value.</span></span>

<span data-ttu-id="69f66-116">O valor de [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) é redefinido automaticamente cada vez que o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="69f66-116">The value of [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) is automatically reset each time the event occurs.</span></span>

<span data-ttu-id="69f66-117">Os aplicativos podem usar o [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) em situações em que é útil desconectar um usuário; por exemplo, em um quiosque ou em outro cenário de terminal público.</span><span class="sxs-lookup"><span data-stu-id="69f66-117">Applications can use [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in situations where it is useful to disconnect a user; for example, in a kiosk or other public terminal scenario.</span></span>

## <a name="requirements"></a><span data-ttu-id="69f66-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69f66-118">Requirements</span></span>



| <span data-ttu-id="69f66-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="69f66-119">Requirement</span></span> | <span data-ttu-id="69f66-120">Valor</span><span class="sxs-lookup"><span data-stu-id="69f66-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69f66-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69f66-121">Minimum supported client</span></span><br/> | <span data-ttu-id="69f66-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69f66-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="69f66-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69f66-123">Minimum supported server</span></span><br/> | <span data-ttu-id="69f66-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69f66-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="69f66-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="69f66-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="69f66-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69f66-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="69f66-127">DLL</span><span class="sxs-lookup"><span data-stu-id="69f66-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69f66-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69f66-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="69f66-129">IID</span><span class="sxs-lookup"><span data-stu-id="69f66-129">IID</span></span><br/>                      | <span data-ttu-id="69f66-130">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="69f66-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="69f66-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="69f66-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f66-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="69f66-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





