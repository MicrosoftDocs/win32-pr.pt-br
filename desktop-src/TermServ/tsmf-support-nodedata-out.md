---
title: Estrutura de TSMF_SUPPORT_NODEDATA_OUT
description: Usado na estrutura de \_ saída de dados de suporte do TSMF \_ \_ para conter informações sobre formatos de mídia com suporte.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- Estrutura de TSMF_SUPPORT_NODEDATA_OUT Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PTSMF_SUPPORT_NODEDATA_OUT Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824542"
---
# <a name="tsmf_support_nodedata_out-structure"></a><span data-ttu-id="96934-105">TSMF \_ dá suporte à \_ \_ estrutura de saída NODEDATA</span><span class="sxs-lookup"><span data-stu-id="96934-105">TSMF\_SUPPORT\_NODEDATA\_OUT structure</span></span>

<span data-ttu-id="96934-106">Usado na estrutura [**de \_ \_ \_ saída de dados de suporte do TSMF**](tsmf-support-data-out.md) para conter informações sobre formatos de mídia com suporte.</span><span class="sxs-lookup"><span data-stu-id="96934-106">Used inside the [**TSMF\_SUPPORT\_DATA\_OUT**](tsmf-support-data-out.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="96934-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96934-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a><span data-ttu-id="96934-108">Membros</span><span class="sxs-lookup"><span data-stu-id="96934-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="96934-109">**nodeId**</span><span class="sxs-lookup"><span data-stu-id="96934-109">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="96934-110">O nó.</span><span class="sxs-lookup"><span data-stu-id="96934-110">The node.</span></span>

</dd> <dt>

<span data-ttu-id="96934-111">**hrSupportStatus**</span><span class="sxs-lookup"><span data-stu-id="96934-111">**hrSupportStatus**</span></span>
</dt> <dd>

<span data-ttu-id="96934-112">Se o coletor identificado pelo parâmetro *clsidNewSink* tem suporte.</span><span class="sxs-lookup"><span data-stu-id="96934-112">Whether the sink identified by the *clsidNewSink* parameter is supported.</span></span>

<span data-ttu-id="96934-113">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="96934-113">The possible values are.</span></span>

<dt>

<span data-ttu-id="96934-114">0</span><span class="sxs-lookup"><span data-stu-id="96934-114">0</span></span>
</dt> <dd>

<span data-ttu-id="96934-115">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="96934-115">Not supported</span></span>

</dd> <dt>

<span data-ttu-id="96934-116">1</span><span class="sxs-lookup"><span data-stu-id="96934-116">1</span></span>
</dt> <dd>

<span data-ttu-id="96934-117">Com suporte</span><span class="sxs-lookup"><span data-stu-id="96934-117">Supported</span></span>

</dd> </dl>

<span data-ttu-id="96934-118">Outros valores são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="96934-118">Other values are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="96934-119">**clsidNewSink**</span><span class="sxs-lookup"><span data-stu-id="96934-119">**clsidNewSink**</span></span>
</dt> <dd>

<span data-ttu-id="96934-120">O coletor associado ao tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="96934-120">The sink associated with the media type.</span></span>

</dd> <dt>

<span data-ttu-id="96934-121">**supportedMediaTypeIndex**</span><span class="sxs-lookup"><span data-stu-id="96934-121">**supportedMediaTypeIndex**</span></span>
</dt> <dd>

<span data-ttu-id="96934-122">O índice de base zero do tipo de mídia com suporte no coletor.</span><span class="sxs-lookup"><span data-stu-id="96934-122">The zero-based index of the media type supported by the sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96934-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96934-123">Requirements</span></span>



| <span data-ttu-id="96934-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="96934-124">Requirement</span></span> | <span data-ttu-id="96934-125">Valor</span><span class="sxs-lookup"><span data-stu-id="96934-125">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="96934-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96934-126">Minimum supported client</span></span><br/> | <span data-ttu-id="96934-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="96934-127">None supported</span></span><br/>         |
| <span data-ttu-id="96934-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96934-128">Minimum supported server</span></span><br/> | <span data-ttu-id="96934-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="96934-129">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96934-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="96934-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96934-131">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="96934-131">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="96934-132">**\_saída de \_ dados de suporte do TSMF \_**</span><span class="sxs-lookup"><span data-stu-id="96934-132">**TSMF\_SUPPORT\_DATA\_OUT**</span></span>](tsmf-support-data-out.md)
</dt> </dl>

 

 





