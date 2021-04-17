---
title: Propriedade TargetName ITsSbSession
description: Recupera o nome do destino no qual esta sessão foi criada.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TargetName
- Propriedade TargetName Serviços de Área de Trabalho Remota, interface ITsSbSession
- Serviços de Área de Trabalho Remota de interface ITsSbSession, Propriedade TargetName
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc703a32faedd250115da0b95215e620a8c15e19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761932"
---
# <a name="itssbsessiontargetname-property"></a><span data-ttu-id="12725-106">Propriedade ITsSbSession:: TargetName</span><span class="sxs-lookup"><span data-stu-id="12725-106">ITsSbSession::TargetName property</span></span>

<span data-ttu-id="12725-107">Recupera o nome do destino no qual esta sessão foi criada.</span><span class="sxs-lookup"><span data-stu-id="12725-107">Retrieves the name of the target on which this session was created.</span></span>

<span data-ttu-id="12725-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="12725-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="12725-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12725-109">Syntax</span></span>


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a><span data-ttu-id="12725-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="12725-110">Property value</span></span>

<span data-ttu-id="12725-111">Um ponteiro para uma variável **BSTR** que recebe o nome do destino no qual essa sessão foi criada.</span><span class="sxs-lookup"><span data-stu-id="12725-111">A pointer to a **BSTR** variable that receives the name of the target on which this session was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="12725-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12725-112">Requirements</span></span>



| <span data-ttu-id="12725-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="12725-113">Requirement</span></span> | <span data-ttu-id="12725-114">Valor</span><span class="sxs-lookup"><span data-stu-id="12725-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="12725-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12725-115">Minimum supported client</span></span><br/> | <span data-ttu-id="12725-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="12725-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="12725-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12725-117">Minimum supported server</span></span><br/> | <span data-ttu-id="12725-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12725-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="12725-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="12725-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12725-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="12725-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12725-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="12725-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12725-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="12725-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





