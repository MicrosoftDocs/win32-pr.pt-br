---
title: Estrutura de TSMF_SUPPORT_DATA_IN
description: Contém informações sobre formatos de mídia. | Estrutura de TSMF_SUPPORT_DATA_IN
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- Estrutura de TSMF_SUPPORT_DATA_IN Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PTSMF_SUPPORT_DATA_IN Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2072363978cb0e70d64a09d855ed2861341e9cf0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105761930"
---
# <a name="tsmf_support_data_in-structure"></a><span data-ttu-id="b5a9c-106">\_ \_ Dados de suporte \_ do TSMF na estrutura</span><span class="sxs-lookup"><span data-stu-id="b5a9c-106">TSMF\_SUPPORT\_DATA\_IN structure</span></span>

<span data-ttu-id="b5a9c-107">Contém informações sobre formatos de mídia.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-107">Contains information about media formats.</span></span> <span data-ttu-id="b5a9c-108">Essa estrutura é usada pelo método [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) durante consultas **de \_ \_ \_ \_ suporte ao formato MF de consulta WRDS** .</span><span class="sxs-lookup"><span data-stu-id="b5a9c-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a9c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5a9c-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a><span data-ttu-id="b5a9c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b5a9c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5a9c-111">**guidMfSession**</span><span class="sxs-lookup"><span data-stu-id="b5a9c-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="b5a9c-112">A sessão.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-112">The session.</span></span>

</dd> <dt>

<span data-ttu-id="b5a9c-113">**numEntries**</span><span class="sxs-lookup"><span data-stu-id="b5a9c-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="b5a9c-114">O número de estruturas nos dados de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="b5a9c-115">**...**</span><span class="sxs-lookup"><span data-stu-id="b5a9c-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="b5a9c-116">Um número variável de estruturas que contém dados de formato de mídia.</span><span class="sxs-lookup"><span data-stu-id="b5a9c-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5a9c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a9c-117">Requirements</span></span>



| <span data-ttu-id="b5a9c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5a9c-118">Requirement</span></span> | <span data-ttu-id="b5a9c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b5a9c-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="b5a9c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5a9c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a9c-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b5a9c-121">None supported</span></span><br/>         |
| <span data-ttu-id="b5a9c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5a9c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a9c-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b5a9c-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5a9c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5a9c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a9c-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="b5a9c-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="b5a9c-126">**TSMF \_ suportam \_ NODEDATA \_**</span><span class="sxs-lookup"><span data-stu-id="b5a9c-126">**TSMF\_SUPPORT\_NODEDATA\_IN**</span></span>](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





