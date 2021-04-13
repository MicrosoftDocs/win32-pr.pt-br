---
title: Método IRDVTaskPlugin Terminate
description: Chamado quando o agente de tarefa está sendo desligado.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Método Terminate Serviços de Área de Trabalho Remota
- Método Terminate Serviços de Área de Trabalho Remota, interface IRDVTaskPlugin
- Serviços de Área de Trabalho Remota de interface IRDVTaskPlugin, método Terminate
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369723"
---
# <a name="irdvtaskpluginterminate-method"></a><span data-ttu-id="1af3f-106">Método IRDVTaskPlugin:: Terminate</span><span class="sxs-lookup"><span data-stu-id="1af3f-106">IRDVTaskPlugin::Terminate method</span></span>

<span data-ttu-id="1af3f-107">Chamado quando o agente de tarefa está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="1af3f-107">Called when the task agent is being shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="1af3f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1af3f-108">Syntax</span></span>


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="1af3f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1af3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1af3f-110">*HR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1af3f-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1af3f-111">Indica se o desligamento é devido a um desligamento normal ou uma falha.</span><span class="sxs-lookup"><span data-stu-id="1af3f-111">Indicates whether the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="1af3f-112">Se o desligamento for normal, isso conterá **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1af3f-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="1af3f-113">Caso contrário, ele contém um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1af3f-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1af3f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1af3f-114">Return value</span></span>

<span data-ttu-id="1af3f-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1af3f-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1af3f-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1af3f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1af3f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1af3f-117">Requirements</span></span>



| <span data-ttu-id="1af3f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1af3f-118">Requirement</span></span> | <span data-ttu-id="1af3f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1af3f-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="1af3f-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1af3f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1af3f-121">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="1af3f-121">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="1af3f-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1af3f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1af3f-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1af3f-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1af3f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1af3f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af3f-125">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="1af3f-125">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





