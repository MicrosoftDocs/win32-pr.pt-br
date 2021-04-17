---
description: Representa informações sobre destinos de chamada para a proteção de fluxo de controle (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: Estrutura de CFG_CALL_TARGET_INFO (Ntmmapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775552"
---
# <a name="cfg_call_target_info-structure"></a><span data-ttu-id="a6a6e-103">CFG \_ chamar \_ estrutura de informações de destino \_</span><span class="sxs-lookup"><span data-stu-id="a6a6e-103">CFG\_CALL\_TARGET\_INFO structure</span></span>

<span data-ttu-id="a6a6e-104">Representa informações sobre destinos de chamada para a proteção de fluxo de controle (CFG).</span><span class="sxs-lookup"><span data-stu-id="a6a6e-104">Represents information about call targets for Control Flow Guard (CFG).</span></span>

## <a name="syntax"></a><span data-ttu-id="a6a6e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6a6e-105">Syntax</span></span>


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="a6a6e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a6a6e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a6a6e-107">**Deslocamento**</span><span class="sxs-lookup"><span data-stu-id="a6a6e-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="a6a6e-108">Deslocamento relativo a um endereço virtual (inicial) fornecido.</span><span class="sxs-lookup"><span data-stu-id="a6a6e-108">Offset relative to a provided (start) virtual address.</span></span> <span data-ttu-id="a6a6e-109">Esse deslocamento deve ser alinhado em 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="a6a6e-109">This offset should be 16 byte aligned.</span></span>

</dd> <dt>

<span data-ttu-id="a6a6e-110">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="a6a6e-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a6a6e-111">Sinalizadores que descrevem a operação a ser executada no endereço.</span><span class="sxs-lookup"><span data-stu-id="a6a6e-111">Flags describing the operation to be performed on the address.</span></span> <span data-ttu-id="a6a6e-112">Se o destino da chamada de cfg for definido como **\_ \_ \_ válido** , o endereço será marcado como válido para cfg.</span><span class="sxs-lookup"><span data-stu-id="a6a6e-112">If **CFG\_CALL\_TARGET\_VALID** is set, then the address will be marked valid for CFG.</span></span> <span data-ttu-id="a6a6e-113">Caso contrário, ele será marcado como um destino de chamada inválido.</span><span class="sxs-lookup"><span data-stu-id="a6a6e-113">Otherwise, it will be marked an invalid call target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6a6e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6a6e-114">Requirements</span></span>



| <span data-ttu-id="a6a6e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6a6e-115">Requirement</span></span> | <span data-ttu-id="a6a6e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a6a6e-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a6e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6a6e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a6a6e-118">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a6a6e-118">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a6a6e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6a6e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a6a6e-120">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="a6a6e-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a6a6e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6a6e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6a6e-122"><dt>Ntmmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6a6e-122"><dt>Ntmmapi.h</dt></span></span> </dl> |



 

 




