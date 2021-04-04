---
title: Propriedade do rótulo ITsSbTaskInfo
description: Recupera o rótulo que descreve a finalidade da tarefa.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de Propriedade do rótulo
- Propriedade do rótulo Serviços de Área de Trabalho Remota, interface ITsSbTaskInfo
- Serviços de Área de Trabalho Remota de interface ITsSbTaskInfo, Propriedade Label
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f85aaea366cf002d4ec1bacce8f29a6aa67fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645151"
---
# <a name="itssbtaskinfolabel-property"></a><span data-ttu-id="0baf4-106">Propriedade ITsSbTaskInfo:: Label</span><span class="sxs-lookup"><span data-stu-id="0baf4-106">ITsSbTaskInfo::Label property</span></span>

<span data-ttu-id="0baf4-107">Recupera o rótulo que descreve a finalidade da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0baf4-107">Retrieves the label that describes the purpose of the task.</span></span>

<span data-ttu-id="0baf4-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="0baf4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0baf4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0baf4-109">Syntax</span></span>


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a><span data-ttu-id="0baf4-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0baf4-110">Property value</span></span>

<span data-ttu-id="0baf4-111">Um ponteiro para um valor **BSTR** que contém o rótulo.</span><span class="sxs-lookup"><span data-stu-id="0baf4-111">A pointer to a **BSTR** value that contains the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="0baf4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0baf4-112">Requirements</span></span>



| <span data-ttu-id="0baf4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0baf4-113">Requirement</span></span> | <span data-ttu-id="0baf4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0baf4-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0baf4-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0baf4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0baf4-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0baf4-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="0baf4-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0baf4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0baf4-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0baf4-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="0baf4-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="0baf4-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0baf4-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0baf4-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0baf4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0baf4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0baf4-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="0baf4-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





