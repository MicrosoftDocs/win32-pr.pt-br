---
description: Este tópico aplica-se ao Windows XP Service Pack 2 ou posterior. A estrutura de conexão do KSTOPOLOGY \_ descreve uma conexão de nó em um filtro de streaming de kernel (KS). Um nó pode ser conectado a outro nó dentro do filtro ou a um PIN no filtro.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: Estrutura de KSTOPOLOGY_CONNECTION (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767672"
---
# <a name="kstopology_connection-structure"></a><span data-ttu-id="74311-105">Estrutura de conexão do KSTOPOLOGY \_</span><span class="sxs-lookup"><span data-stu-id="74311-105">KSTOPOLOGY\_CONNECTION structure</span></span>

<span data-ttu-id="74311-106">Este tópico aplica-se ao Windows XP Service Pack 2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="74311-106">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="74311-107">A estrutura de **\_ conexão do KSTOPOLOGY** descreve uma conexão de nó em um filtro de streaming de kernel (KS).</span><span class="sxs-lookup"><span data-stu-id="74311-107">The **KSTOPOLOGY\_CONNECTION** structure describes a node connection within a kernel-streaming (KS) filter.</span></span> <span data-ttu-id="74311-108">Um nó pode ser conectado a outro nó dentro do filtro ou a um PIN no filtro.</span><span class="sxs-lookup"><span data-stu-id="74311-108">A node can be connected to another node within the filter, or to a pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="74311-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74311-109">Syntax</span></span>


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a><span data-ttu-id="74311-110">Membros</span><span class="sxs-lookup"><span data-stu-id="74311-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="74311-111">**FromNode**</span><span class="sxs-lookup"><span data-stu-id="74311-111">**FromNode**</span></span>
</dt> <dd>

<span data-ttu-id="74311-112">Índice do nó upstream na conexão.</span><span class="sxs-lookup"><span data-stu-id="74311-112">Index of the upstream node in the connection.</span></span> <span data-ttu-id="74311-113">Se a conexão upstream for um PIN, em vez de um nó, o valor será KSFILTER \_ nó.</span><span class="sxs-lookup"><span data-stu-id="74311-113">If the upstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="74311-114">**FromNodePin**</span><span class="sxs-lookup"><span data-stu-id="74311-114">**FromNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="74311-115">Se o valor do campo **FromNode** for KSFILTER \_ nó, esse campo especificará o índice do pino upstream.</span><span class="sxs-lookup"><span data-stu-id="74311-115">If the value of the **FromNode** field is KSFILTER\_NODE, this field specifies the index of the upstream pin.</span></span> <span data-ttu-id="74311-116">Caso contrário, esse campo será ignorado.</span><span class="sxs-lookup"><span data-stu-id="74311-116">Otherwise, this field is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="74311-117">**ToNode**</span><span class="sxs-lookup"><span data-stu-id="74311-117">**ToNode**</span></span>
</dt> <dd>

<span data-ttu-id="74311-118">Índice do nó downstream na conexão.</span><span class="sxs-lookup"><span data-stu-id="74311-118">Index of the downstream node in the connection.</span></span> <span data-ttu-id="74311-119">Se a conexão downstream for um PIN, em vez de um nó, o valor será KSFILTER \_ nó.</span><span class="sxs-lookup"><span data-stu-id="74311-119">If the downstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="74311-120">**ToNodePin**</span><span class="sxs-lookup"><span data-stu-id="74311-120">**ToNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="74311-121">Se o valor do campo **tonode** for KSFILTER \_ node, esse campo especificará o índice do PIN do downstream.</span><span class="sxs-lookup"><span data-stu-id="74311-121">If the value of the **ToNode** field is KSFILTER\_NODE, this field specifies the index of the downstream pin.</span></span> <span data-ttu-id="74311-122">Caso contrário, esse campo será ignorado.</span><span class="sxs-lookup"><span data-stu-id="74311-122">Otherwise, this field is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74311-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74311-123">Requirements</span></span>



| <span data-ttu-id="74311-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="74311-124">Requirement</span></span> | <span data-ttu-id="74311-125">Valor</span><span class="sxs-lookup"><span data-stu-id="74311-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="74311-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74311-126">Header</span></span><br/> | <dl> <span data-ttu-id="74311-127"><dt>KS. h</dt></span><span class="sxs-lookup"><span data-stu-id="74311-127"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74311-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="74311-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74311-129">Estruturas do DirectShow</span><span class="sxs-lookup"><span data-stu-id="74311-129">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="74311-130">**IKsTopologyInfo:: get \_ ConnectionInfo**</span><span class="sxs-lookup"><span data-stu-id="74311-130">**IKsTopologyInfo::get\_ConnectionInfo**</span></span>](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




