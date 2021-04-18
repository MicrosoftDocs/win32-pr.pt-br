---
title: Estrutura de TSMF_SUPPORT_NODEDATA_IN
description: Usado dentro dos dados de suporte do TSMF \_ \_ \_ na estrutura para conter informações sobre formatos de mídia com suporte.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- Estrutura de TSMF_SUPPORT_NODEDATA_IN Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PTSMF_SUPPORT_NODEDATA_IN Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796294"
---
# <a name="tsmf_support_nodedata_in-structure"></a><span data-ttu-id="a800b-105">TSMF \_ dá suporte a \_ NODEDATA \_ na estrutura</span><span class="sxs-lookup"><span data-stu-id="a800b-105">TSMF\_SUPPORT\_NODEDATA\_IN structure</span></span>

<span data-ttu-id="a800b-106">Usado dentro dos [**dados de suporte do TSMF \_ \_ \_ na**](tsmf-support-data-in.md) estrutura para conter informações sobre formatos de mídia com suporte.</span><span class="sxs-lookup"><span data-stu-id="a800b-106">Used inside the [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="a800b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a800b-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a><span data-ttu-id="a800b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a800b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a800b-109">**byteCount**</span><span class="sxs-lookup"><span data-stu-id="a800b-109">**byteCount**</span></span>
</dt> <dd>

<span data-ttu-id="a800b-110">O tamanho da estrutura em bytes.</span><span class="sxs-lookup"><span data-stu-id="a800b-110">The size of the structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a800b-111">**nodeId**</span><span class="sxs-lookup"><span data-stu-id="a800b-111">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="a800b-112">O nó.</span><span class="sxs-lookup"><span data-stu-id="a800b-112">The node.</span></span>

</dd> <dt>

<span data-ttu-id="a800b-113">**numMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="a800b-113">**numMediaTypes**</span></span>
</dt> <dd>

<span data-ttu-id="a800b-114">O número de estruturas de formato de mídia.</span><span class="sxs-lookup"><span data-stu-id="a800b-114">The number of media format structures.</span></span>

</dd> <dt>

<span data-ttu-id="a800b-115">**...**</span><span class="sxs-lookup"><span data-stu-id="a800b-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="a800b-116">Um número variável de estruturas que definem formatos de mídia de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="a800b-116">A variable number of structures defining audio or video media formats.</span></span> <span data-ttu-id="a800b-117">O **formatType** é o **formato \_ WaveFormatEx** para áudio ou **formato \_ MFVideoFormat** para vídeo.</span><span class="sxs-lookup"><span data-stu-id="a800b-117">The **FormatType** is either **FORMAT\_WaveFormatEx** for audio or **FORMAT\_MFVideoFormat** for video.</span></span>

<span data-ttu-id="a800b-118">Para obter detalhes dessa estrutura, consulte [ \_ estrutura do \_ \_ tipo de mídia TS am](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span><span class="sxs-lookup"><span data-stu-id="a800b-118">For details of this structure, see [TS\_AM\_MEDIA\_TYPE Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a800b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a800b-119">Requirements</span></span>



| <span data-ttu-id="a800b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a800b-120">Requirement</span></span> | <span data-ttu-id="a800b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a800b-121">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="a800b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a800b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a800b-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a800b-123">None supported</span></span><br/>         |
| <span data-ttu-id="a800b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a800b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a800b-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a800b-125">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a800b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a800b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a800b-127">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="a800b-127">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="a800b-128">**\_ \_ dados de suporte \_ do TSMF em**</span><span class="sxs-lookup"><span data-stu-id="a800b-128">**TSMF\_SUPPORT\_DATA\_IN**</span></span>](tsmf-support-data-in.md)
</dt> </dl>

 

