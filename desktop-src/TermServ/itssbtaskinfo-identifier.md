---
title: Propriedade do identificador ITsSbTaskInfo
description: Recupera um GUID que é usado como um identificador exclusivo pelo agente de tarefa.
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de Propriedade do identificador
- Serviços de Área de Trabalho Remota de Propriedade do identificador, interface ITsSbTaskInfo
- Serviços de Área de Trabalho Remota de interface ITsSbTaskInfo, Propriedade do identificador
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 241ed2966e9ec92aa420af20ce142bcb724ad222
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645184"
---
# <a name="itssbtaskinfoidentifier-property"></a><span data-ttu-id="042d8-106">Propriedade ITsSbTaskInfo:: Identifier</span><span class="sxs-lookup"><span data-stu-id="042d8-106">ITsSbTaskInfo::Identifier property</span></span>

<span data-ttu-id="042d8-107">Recupera um GUID que é usado como um identificador exclusivo pelo agente de tarefa.</span><span class="sxs-lookup"><span data-stu-id="042d8-107">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

<span data-ttu-id="042d8-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="042d8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="042d8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="042d8-109">Syntax</span></span>


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a><span data-ttu-id="042d8-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="042d8-110">Property value</span></span>

<span data-ttu-id="042d8-111">Um ponteiro para um valor **BSTR** que recebe o GUID.</span><span class="sxs-lookup"><span data-stu-id="042d8-111">A pointer to a **BSTR** value that receives the GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="042d8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="042d8-112">Requirements</span></span>



| <span data-ttu-id="042d8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="042d8-113">Requirement</span></span> | <span data-ttu-id="042d8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="042d8-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="042d8-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="042d8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="042d8-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="042d8-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="042d8-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="042d8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="042d8-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="042d8-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="042d8-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="042d8-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="042d8-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="042d8-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="042d8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="042d8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="042d8-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="042d8-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





