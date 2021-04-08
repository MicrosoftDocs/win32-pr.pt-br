---
description: A \_ enumeração de tipo KEYSVC define se uma chave se aplica a um computador ou a um serviço.
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: Enumeração de KEYSVC_TYPE (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 71d6724f7bae78a3c1ac4da83289c151b7ec1a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922885"
---
# <a name="keysvc_type-enumeration"></a><span data-ttu-id="c4137-103">\_Enumeração de tipo KEYSVC</span><span class="sxs-lookup"><span data-stu-id="c4137-103">KEYSVC\_TYPE enumeration</span></span>

<span data-ttu-id="c4137-104">A enumeração de **\_ tipo KEYSVC** define se uma chave se aplica a um computador ou a um serviço.</span><span class="sxs-lookup"><span data-stu-id="c4137-104">The **KEYSVC\_TYPE** enumeration defines whether a key applies to a computer or a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4137-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4137-105">Syntax</span></span>


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c4137-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c4137-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c4137-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span><span class="sxs-lookup"><span data-stu-id="c4137-107"><span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**</span></span>
</dt> <dd>

<span data-ttu-id="c4137-108">A chave é para um computador.</span><span class="sxs-lookup"><span data-stu-id="c4137-108">The key is for a computer.</span></span>

</dd> <dt>

<span data-ttu-id="c4137-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span><span class="sxs-lookup"><span data-stu-id="c4137-109"><span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**</span></span>
</dt> <dd>

<span data-ttu-id="c4137-110">A chave é para um serviço.</span><span class="sxs-lookup"><span data-stu-id="c4137-110">The key is for a service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4137-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4137-111">Requirements</span></span>



| <span data-ttu-id="c4137-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4137-112">Requirement</span></span> | <span data-ttu-id="c4137-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c4137-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4137-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4137-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c4137-115">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c4137-115">None supported</span></span><br/>                                                             |
| <span data-ttu-id="c4137-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4137-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c4137-117">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c4137-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4137-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4137-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4137-119"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4137-119"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4137-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4137-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4137-121">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="c4137-121">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 




