---
title: Método onterminado IRDVTaskPluginNotifySink (Sbtsv. h)
description: Chamado pelo agente de tarefa para solicitar que o agente de tarefa seja desligado.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Método onterminado Serviços de Área de Trabalho Remota
- Método onterminado Serviços de Área de Trabalho Remota, interface IRDVTaskPluginNotifySink
- Serviços de Área de Trabalho Remota de interface IRDVTaskPluginNotifySink, método onterminado
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499760"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a><span data-ttu-id="09fb0-106">Método IRDVTaskPluginNotifySink:: onterminable</span><span class="sxs-lookup"><span data-stu-id="09fb0-106">IRDVTaskPluginNotifySink::OnTerminated method</span></span>

<span data-ttu-id="09fb0-107">Chamado pelo agente de tarefa para solicitar que o agente de tarefa seja desligado.</span><span class="sxs-lookup"><span data-stu-id="09fb0-107">Called by the task agent to request that the task agent be shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="09fb0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09fb0-108">Syntax</span></span>


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="09fb0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09fb0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09fb0-110">*HR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09fb0-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fb0-111">Indica se o desligamento é devido a um desligamento normal ou uma falha.</span><span class="sxs-lookup"><span data-stu-id="09fb0-111">Indicates if the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="09fb0-112">Se o desligamento for normal, isso conterá **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="09fb0-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="09fb0-113">Caso contrário, ele contém um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09fb0-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09fb0-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09fb0-114">Return value</span></span>

<span data-ttu-id="09fb0-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="09fb0-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="09fb0-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09fb0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="09fb0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09fb0-117">Requirements</span></span>



| <span data-ttu-id="09fb0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="09fb0-118">Requirement</span></span> | <span data-ttu-id="09fb0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="09fb0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09fb0-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09fb0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="09fb0-121">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="09fb0-121">Windows 7 Enterprise</span></span><br/>                                                    |
| <span data-ttu-id="09fb0-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09fb0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="09fb0-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09fb0-123">Windows Server 2008 R2</span></span><br/>                                                  |
| <span data-ttu-id="09fb0-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09fb0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="09fb0-125"><dt>Sbtsv. h</dt></span><span class="sxs-lookup"><span data-stu-id="09fb0-125"><dt>Sbtsv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09fb0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="09fb0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09fb0-127">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="09fb0-127">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





