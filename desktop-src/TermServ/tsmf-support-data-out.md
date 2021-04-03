---
title: Estrutura de TSMF_SUPPORT_DATA_OUT
description: Contém informações sobre formatos de mídia. | Estrutura de TSMF_SUPPORT_DATA_OUT
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- Estrutura de TSMF_SUPPORT_DATA_OUT Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PTSMF_SUPPORT_DATA_OUT Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930314"
---
# <a name="tsmf_support_data_out-structure"></a><span data-ttu-id="8be51-106">\_Estrutura de \_ saída de dados de suporte do TSMF \_</span><span class="sxs-lookup"><span data-stu-id="8be51-106">TSMF\_SUPPORT\_DATA\_OUT structure</span></span>

<span data-ttu-id="8be51-107">Contém informações sobre formatos de mídia.</span><span class="sxs-lookup"><span data-stu-id="8be51-107">Contains information about media formats.</span></span> <span data-ttu-id="8be51-108">Essa estrutura é usada pelo método [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) durante consultas **de \_ \_ \_ \_ suporte ao formato MF de consulta WRDS** .</span><span class="sxs-lookup"><span data-stu-id="8be51-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be51-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8be51-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a><span data-ttu-id="8be51-110">Membros</span><span class="sxs-lookup"><span data-stu-id="8be51-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="8be51-111">**guidMfSession**</span><span class="sxs-lookup"><span data-stu-id="8be51-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="8be51-112">Isso deve corresponder à propriedade **guidMfSession** nos dados de [**suporte de TSMF correspondentes \_ \_ \_ na**](tsmf-support-data-in.md) estrutura.</span><span class="sxs-lookup"><span data-stu-id="8be51-112">This must match the **guidMfSession** property in the corresponding [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8be51-113">**numEntries**</span><span class="sxs-lookup"><span data-stu-id="8be51-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="8be51-114">O número de estruturas nos dados de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="8be51-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="8be51-115">**...**</span><span class="sxs-lookup"><span data-stu-id="8be51-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="8be51-116">Um número variável de estruturas que contém dados de formato de mídia.</span><span class="sxs-lookup"><span data-stu-id="8be51-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8be51-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8be51-117">Requirements</span></span>



| <span data-ttu-id="8be51-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8be51-118">Requirement</span></span> | <span data-ttu-id="8be51-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8be51-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="8be51-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8be51-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8be51-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8be51-121">None supported</span></span><br/>         |
| <span data-ttu-id="8be51-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8be51-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8be51-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8be51-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8be51-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8be51-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be51-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="8be51-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="8be51-126">**TSMF \_ suporte \_ NODEDATA \_**</span><span class="sxs-lookup"><span data-stu-id="8be51-126">**TSMF\_SUPPORT\_NODEDATA\_OUT**</span></span>](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





