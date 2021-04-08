---
title: Propriedade de contexto ITsSbTaskInfo
description: Recupera os bytes de contexto associados à tarefa.
ms.assetid: ce55ce2a-957f-4b50-b632-42079277102b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de contexto
- Propriedade de contexto Serviços de Área de Trabalho Remota, interface ITsSbTaskInfo
- Serviços de Área de Trabalho Remota de interface ITsSbTaskInfo, propriedade de contexto
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Context
- ITsSbTaskInfo.get_Context
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2adc4715f23b2c23ac6dfbdcdd8a489b2b0f5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086357"
---
# <a name="itssbtaskinfocontext-property"></a><span data-ttu-id="a515a-106">Propriedade ITsSbTaskInfo:: Context</span><span class="sxs-lookup"><span data-stu-id="a515a-106">ITsSbTaskInfo::Context property</span></span>

<span data-ttu-id="a515a-107">Recupera os bytes de contexto associados à tarefa.</span><span class="sxs-lookup"><span data-stu-id="a515a-107">Retrieves the context bytes associated with the task.</span></span>

<span data-ttu-id="a515a-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a515a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a515a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a515a-109">Syntax</span></span>


```C++
HRESULT get_Context(
  [out, retval] SAFEARRAY(BYTE) *pContext
);
```



## <a name="property-value"></a><span data-ttu-id="a515a-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a515a-110">Property value</span></span>

<span data-ttu-id="a515a-111">O contexto da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a515a-111">The context of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="a515a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a515a-112">Requirements</span></span>



| <span data-ttu-id="a515a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a515a-113">Requirement</span></span> | <span data-ttu-id="a515a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a515a-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a515a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a515a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a515a-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a515a-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="a515a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a515a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a515a-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a515a-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="a515a-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="a515a-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a515a-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a515a-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a515a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a515a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a515a-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="a515a-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





