---
title: Método IRDVTaskPluginNotifySink OnTaskStateChange
description: Usado para notificar o agente de disparo de que o estado de uma tarefa foi alterado.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnTaskStateChange
- Método OnTaskStateChange Serviços de Área de Trabalho Remota, interface IRDVTaskPluginNotifySink
- Serviços de Área de Trabalho Remota de interface IRDVTaskPluginNotifySink, método OnTaskStateChange
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811908"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a><span data-ttu-id="31fe9-106">Método IRDVTaskPluginNotifySink:: OnTaskStateChange</span><span class="sxs-lookup"><span data-stu-id="31fe9-106">IRDVTaskPluginNotifySink::OnTaskStateChange method</span></span>

<span data-ttu-id="31fe9-107">Usado para notificar o agente de disparo de que o estado de uma tarefa foi alterado.</span><span class="sxs-lookup"><span data-stu-id="31fe9-107">Used to notify the trigger agent that the state of a task has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="31fe9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31fe9-108">Syntax</span></span>


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a><span data-ttu-id="31fe9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31fe9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31fe9-110">*bstrIdentifier* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31fe9-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31fe9-111">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="31fe9-111">Type: **BSTR**</span></span>

<span data-ttu-id="31fe9-112">O identificador da tarefa.</span><span class="sxs-lookup"><span data-stu-id="31fe9-112">The identifier of the task.</span></span> <span data-ttu-id="31fe9-113">Este é o identificador passado para o método [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="31fe9-113">This is the identifier passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="31fe9-114">*status* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="31fe9-114">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31fe9-115">Tipo: **[ **RDV \_ \_ status da tarefa**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span><span class="sxs-lookup"><span data-stu-id="31fe9-115">Type: **[**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span></span>

<span data-ttu-id="31fe9-116">Um valor da enumeração [**de \_ \_ status da tarefa RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que especifica o novo estado da tarefa.</span><span class="sxs-lookup"><span data-stu-id="31fe9-116">A value of the [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration that specifies the new state of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31fe9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31fe9-117">Return value</span></span>

<span data-ttu-id="31fe9-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="31fe9-118">Type: **HRESULT**</span></span>

<span data-ttu-id="31fe9-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="31fe9-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="31fe9-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31fe9-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="31fe9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31fe9-121">Requirements</span></span>



| <span data-ttu-id="31fe9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="31fe9-122">Requirement</span></span> | <span data-ttu-id="31fe9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="31fe9-123">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="31fe9-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31fe9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="31fe9-125">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="31fe9-125">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="31fe9-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31fe9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="31fe9-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31fe9-127">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31fe9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="31fe9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31fe9-129">**\_status da tarefa RDV \_**</span><span class="sxs-lookup"><span data-stu-id="31fe9-129">**RDV\_TASK\_STATUS**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[<span data-ttu-id="31fe9-130">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="31fe9-130">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





