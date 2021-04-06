---
title: Método IRDVTaskPluginNotifySink DeleteSchedule
description: Chamado pelo agente de tarefa para excluir uma tarefa agendada.
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DeleteSchedule
- Método DeleteSchedule Serviços de Área de Trabalho Remota, interface IRDVTaskPluginNotifySink
- Serviços de Área de Trabalho Remota de interface IRDVTaskPluginNotifySink, método DeleteSchedule
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f00bcc740f87acb7f051decd5f2fc9b55ffbf642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086385"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a><span data-ttu-id="ce466-106">IRDVTaskPluginNotifySink: método eleteSchedule de:D</span><span class="sxs-lookup"><span data-stu-id="ce466-106">IRDVTaskPluginNotifySink::DeleteSchedule method</span></span>

<span data-ttu-id="ce466-107">Chamado pelo agente de tarefa para excluir uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="ce466-107">Called by the task agent to delete a scheduled task.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce466-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce466-108">Syntax</span></span>


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a><span data-ttu-id="ce466-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce466-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce466-110">*bstrIdentifier* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce466-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce466-111">O identificador da tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="ce466-111">The identifier of the scheduled task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce466-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce466-112">Return value</span></span>

<span data-ttu-id="ce466-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ce466-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce466-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce466-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce466-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce466-115">Requirements</span></span>



| <span data-ttu-id="ce466-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce466-116">Requirement</span></span> | <span data-ttu-id="ce466-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ce466-117">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="ce466-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce466-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ce466-119">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="ce466-119">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="ce466-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce466-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ce466-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ce466-121">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce466-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce466-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce466-123">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="ce466-123">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





