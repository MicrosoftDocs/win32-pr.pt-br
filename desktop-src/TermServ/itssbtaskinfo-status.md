---
title: Propriedade de status ITsSbTaskInfo
description: Recupera um \_ \_ valor de enumeração de status da tarefa RDV que representa o estado da tarefa.
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de status
- Propriedade de status Serviços de Área de Trabalho Remota, interface ITsSbTaskInfo
- Serviços de Área de Trabalho Remota de interface ITsSbTaskInfo, Propriedade status
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3206013c32ee6cf3323f19c9e95e89c8d6756eb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644602"
---
# <a name="itssbtaskinfostatus-property"></a><span data-ttu-id="f4969-106">Propriedade ITsSbTaskInfo:: status</span><span class="sxs-lookup"><span data-stu-id="f4969-106">ITsSbTaskInfo::Status property</span></span>

<span data-ttu-id="f4969-107">Recupera um valor de enumeração de [**\_ \_ status da tarefa RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa o estado da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f4969-107">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

<span data-ttu-id="f4969-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f4969-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4969-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4969-109">Syntax</span></span>


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a><span data-ttu-id="f4969-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f4969-110">Property value</span></span>

<span data-ttu-id="f4969-111">Um valor de enumeração de [**\_ \_ status da tarefa RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa o estado da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f4969-111">An [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4969-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4969-112">Requirements</span></span>



| <span data-ttu-id="f4969-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4969-113">Requirement</span></span> | <span data-ttu-id="f4969-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f4969-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f4969-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4969-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f4969-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f4969-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="f4969-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4969-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f4969-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4969-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="f4969-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="f4969-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f4969-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4969-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4969-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4969-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4969-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="f4969-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





