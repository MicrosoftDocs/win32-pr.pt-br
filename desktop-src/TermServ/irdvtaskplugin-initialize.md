---
title: Método de inicialização IRDVTaskPlugin
description: Chamado para inicializar o agente de tarefa.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método Initialize
- Método Initialize Serviços de Área de Trabalho Remota, interface IRDVTaskPlugin
- Serviços de Área de Trabalho Remota de interface IRDVTaskPlugin, método Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369365"
---
# <a name="irdvtaskplugininitialize-method"></a><span data-ttu-id="43a57-106">Método IRDVTaskPlugin:: Initialize</span><span class="sxs-lookup"><span data-stu-id="43a57-106">IRDVTaskPlugin::Initialize method</span></span>

<span data-ttu-id="43a57-107">Chamado para inicializar o agente de tarefa.</span><span class="sxs-lookup"><span data-stu-id="43a57-107">Called to initialize the task agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a57-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43a57-108">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a><span data-ttu-id="43a57-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43a57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a57-110">*pNotifySink* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43a57-110">*pNotifySink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a57-111">Tipo: \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) \** _</span><span class="sxs-lookup"><span data-stu-id="43a57-111">Type: \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\** _</span></span>

<span data-ttu-id="43a57-112">Um ponteiro para uma interface [_ *IRDVTaskPluginNotifySink* \*](irdvtaskpluginnotifysink.md) que o agente de tarefa usa para se comunicar com o agente de gatilho.</span><span class="sxs-lookup"><span data-stu-id="43a57-112">A pointer to an [_ *IRDVTaskPluginNotifySink*\*](irdvtaskpluginnotifysink.md) interface that the task agent uses to communicate with the trigger agent.</span></span> <span data-ttu-id="43a57-113">Você deve liberar essa interface quando ela não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="43a57-113">You must release this interface when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a57-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43a57-114">Return value</span></span>

<span data-ttu-id="43a57-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="43a57-115">Type: **HRESULT**</span></span>

<span data-ttu-id="43a57-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="43a57-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43a57-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43a57-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a57-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43a57-118">Requirements</span></span>



| <span data-ttu-id="43a57-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a57-119">Requirement</span></span> | <span data-ttu-id="43a57-120">Valor</span><span class="sxs-lookup"><span data-stu-id="43a57-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="43a57-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a57-121">Minimum supported client</span></span><br/> | <span data-ttu-id="43a57-122">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="43a57-122">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="43a57-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a57-123">Minimum supported server</span></span><br/> | <span data-ttu-id="43a57-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="43a57-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43a57-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="43a57-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a57-126">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="43a57-126">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





