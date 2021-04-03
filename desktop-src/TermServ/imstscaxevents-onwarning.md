---
title: Método OnWarning do IMsTscAxEvents
description: Chamado quando o controle de cliente encontra uma condição de erro que não é fatal.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnWarning
- Método OnWarning Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnWarning
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadc7013f34c93406f93841896a9041bbb1b7cfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644795"
---
# <a name="imstscaxeventsonwarning-method"></a><span data-ttu-id="9e04c-106">Método IMsTscAxEvents:: OnWarning</span><span class="sxs-lookup"><span data-stu-id="9e04c-106">IMsTscAxEvents::OnWarning method</span></span>

<span data-ttu-id="9e04c-107">Chamado quando o controle de cliente encontra uma condição de erro que não é fatal.</span><span class="sxs-lookup"><span data-stu-id="9e04c-107">Called when the client control encounters an error condition that is not fatal.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e04c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e04c-108">Syntax</span></span>


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a><span data-ttu-id="9e04c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e04c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e04c-110">*WarningCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e04c-110">*warningCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e04c-111">O código de erro.</span><span class="sxs-lookup"><span data-stu-id="9e04c-111">The error code.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="9e04c-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9e04c-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9e04c-113">O cache de bitmap está corrompido.</span><span class="sxs-lookup"><span data-stu-id="9e04c-113">Bitmap cache is corrupt.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e04c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e04c-114">Return value</span></span>

<span data-ttu-id="9e04c-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9e04c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e04c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e04c-116">Remarks</span></span>

<span data-ttu-id="9e04c-117">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9e04c-117">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e04c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e04c-118">Requirements</span></span>



| <span data-ttu-id="9e04c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e04c-119">Requirement</span></span> | <span data-ttu-id="9e04c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9e04c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e04c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e04c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9e04c-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e04c-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9e04c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e04c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9e04c-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e04c-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9e04c-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9e04c-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e04c-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e04c-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e04c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9e04c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e04c-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e04c-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e04c-129">IID</span><span class="sxs-lookup"><span data-stu-id="9e04c-129">IID</span></span><br/>                      | <span data-ttu-id="9e04c-130">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="9e04c-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="9e04c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e04c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e04c-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="9e04c-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





