---
title: Propriedade pluginname do IRDVTaskPlugin (Tspubplugincom. h)
description: Contém o nome de exibição do agente de tarefa.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- Propriedade pluginname Serviços de Área de Trabalho Remota
- Propriedade pluginname Serviços de Área de Trabalho Remota, interface IRDVTaskPlugin
- Serviços de Área de Trabalho Remota de interface IRDVTaskPlugin, Propriedade pluginname
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644793"
---
# <a name="irdvtaskpluginpluginname-property"></a><span data-ttu-id="7645f-106">IRDVTaskPlugin: Propriedade luginName de:P</span><span class="sxs-lookup"><span data-stu-id="7645f-106">IRDVTaskPlugin::PluginName property</span></span>

<span data-ttu-id="7645f-107">Contém o nome de exibição do agente de tarefa.</span><span class="sxs-lookup"><span data-stu-id="7645f-107">Contains the display name of the task agent.</span></span> <span data-ttu-id="7645f-108">Esse nome é usado apenas para fins de log.</span><span class="sxs-lookup"><span data-stu-id="7645f-108">This name is used for logging purposes only.</span></span>

<span data-ttu-id="7645f-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7645f-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7645f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7645f-110">Syntax</span></span>


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="7645f-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7645f-111">Property value</span></span>

<span data-ttu-id="7645f-112">O nome de exibição do agente de tarefa.</span><span class="sxs-lookup"><span data-stu-id="7645f-112">The display name of the task agent.</span></span>

## <a name="requirements"></a><span data-ttu-id="7645f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7645f-113">Requirements</span></span>



| <span data-ttu-id="7645f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7645f-114">Requirement</span></span> | <span data-ttu-id="7645f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7645f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7645f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7645f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7645f-117">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="7645f-117">Windows 7 Enterprise</span></span><br/>                                                             |
| <span data-ttu-id="7645f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7645f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7645f-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7645f-119">Windows Server 2008 R2</span></span><br/>                                                           |
| <span data-ttu-id="7645f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7645f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7645f-121"><dt>Tspubplugincom. h</dt></span><span class="sxs-lookup"><span data-stu-id="7645f-121"><dt>Tspubplugincom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7645f-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7645f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7645f-123">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="7645f-123">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





