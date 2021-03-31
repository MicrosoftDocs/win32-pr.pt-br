---
title: Enumeração de CB_RESOURCE_TYPE (Cbclient. h)
description: Especifica o tipo de recurso ao qual a conexão de entrada está se conectando.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração de CB_RESOURCE_TYPE
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644420"
---
# <a name="cb_resource_type-enumeration"></a><span data-ttu-id="b1a95-104">Enumeração de tipo de \_ recurso CB \_</span><span class="sxs-lookup"><span data-stu-id="b1a95-104">CB\_RESOURCE\_TYPE enumeration</span></span>

<span data-ttu-id="b1a95-105">Especifica o tipo de recurso ao qual a conexão de entrada está se conectando.</span><span class="sxs-lookup"><span data-stu-id="b1a95-105">Specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="b1a95-106">Essa enumeração é usada com a estrutura de [**\_ \_ informações de conexão CB**](cb-connection-info.md) .</span><span class="sxs-lookup"><span data-stu-id="b1a95-106">This enumeration is used with the [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a95-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1a95-107">Syntax</span></span>


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="b1a95-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="b1a95-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b1a95-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**\_recurso CB \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="b1a95-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB\_RESOURCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="b1a95-110">O tipo de recurso não está definido.</span><span class="sxs-lookup"><span data-stu-id="b1a95-110">The resource type is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="b1a95-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**\_sessão de recurso CB \_**</span><span class="sxs-lookup"><span data-stu-id="b1a95-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB\_RESOURCE\_SESSION**</span></span>
</dt> <dd>

<span data-ttu-id="b1a95-112">O recurso é uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="b1a95-112">The resource is a remote session.</span></span>

</dd> <dt>

<span data-ttu-id="b1a95-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_VM de recurso CB \_**</span><span class="sxs-lookup"><span data-stu-id="b1a95-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**CB\_RESOURCE\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="b1a95-114">O recurso é uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b1a95-114">The resource is a virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1a95-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1a95-115">Requirements</span></span>



| <span data-ttu-id="b1a95-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1a95-116">Requirement</span></span> | <span data-ttu-id="b1a95-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a95-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a95-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1a95-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a95-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b1a95-119">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="b1a95-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1a95-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a95-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1a95-121">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="b1a95-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1a95-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1a95-123"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1a95-123"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1a95-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b1a95-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a95-125">**\_informações de conexão CB \_**</span><span class="sxs-lookup"><span data-stu-id="b1a95-125">**CB\_CONNECTION\_INFO**</span></span>](cb-connection-info.md)
</dt> </dl>

 

 





