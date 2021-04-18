---
title: Propriedade de domínio ITsSbSession
description: Recupera o nome de domínio do usuário.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface ITsSbSession
- Serviços de Área de Trabalho Remota de interface ITsSbSession, propriedade de domínio
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4501413888d17a70610160117df3ad03fde73b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105767722"
---
# <a name="itssbsessiondomain-property"></a><span data-ttu-id="17b9a-106">ITsSbSession: Propriedade omain de:D</span><span class="sxs-lookup"><span data-stu-id="17b9a-106">ITsSbSession::Domain property</span></span>

<span data-ttu-id="17b9a-107">Recupera o nome de domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="17b9a-107">Retrieves the domain name of the user.</span></span>

<span data-ttu-id="17b9a-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="17b9a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b9a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17b9a-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a><span data-ttu-id="17b9a-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="17b9a-110">Property value</span></span>

<span data-ttu-id="17b9a-111">Um ponteiro para uma variável **BSTR** que recebe o nome de domínio do usuário.</span><span class="sxs-lookup"><span data-stu-id="17b9a-111">A pointer to a **BSTR** variable that receives the domain name of the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b9a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17b9a-112">Requirements</span></span>



| <span data-ttu-id="17b9a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b9a-113">Requirement</span></span> | <span data-ttu-id="17b9a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="17b9a-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17b9a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17b9a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="17b9a-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="17b9a-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="17b9a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17b9a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="17b9a-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17b9a-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="17b9a-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="17b9a-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17b9a-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17b9a-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b9a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="17b9a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b9a-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="17b9a-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





