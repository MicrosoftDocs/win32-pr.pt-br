---
description: A estrutura de FOLLOWENTRY do PF \_ define um protocolo que monitor de rede adiciona ao conjunto de acompanhamento de um analisador.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: Estrutura de PF_FOLLOWENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828961"
---
# <a name="pf_followentry-structure"></a><span data-ttu-id="ee13b-103">Estrutura de FOLLOWENTRY de PF \_</span><span class="sxs-lookup"><span data-stu-id="ee13b-103">PF\_FOLLOWENTRY structure</span></span>

<span data-ttu-id="ee13b-104">A estrutura de **\_ FOLLOWENTRY do PF** define um protocolo que monitor de rede adiciona ao conjunto de acompanhamento de um analisador.</span><span class="sxs-lookup"><span data-stu-id="ee13b-104">The **PF\_FOLLOWENTRY** structure defines a protocol that Network Monitor adds to the follow set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee13b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee13b-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a><span data-ttu-id="ee13b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ee13b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ee13b-107">**szProtocol**</span><span class="sxs-lookup"><span data-stu-id="ee13b-107">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="ee13b-108">O nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="ee13b-108">The name of the protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee13b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee13b-109">Remarks</span></span>

<span data-ttu-id="ee13b-110">A estrutura de [ \_ acompanhamento de PF](pf-followset.md) usa uma matriz de estruturas **\_ FOLLOWENTRY de PF** .</span><span class="sxs-lookup"><span data-stu-id="ee13b-110">The [PF\_FOLLOWSET](pf-followset.md) structure uses an array of **PF\_FOLLOWENTRY** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee13b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee13b-111">Requirements</span></span>



| <span data-ttu-id="ee13b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee13b-112">Requirement</span></span> | <span data-ttu-id="ee13b-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ee13b-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ee13b-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee13b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ee13b-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee13b-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ee13b-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee13b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ee13b-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee13b-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ee13b-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ee13b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee13b-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee13b-119"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee13b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee13b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee13b-121">seguir do PF \_</span><span class="sxs-lookup"><span data-stu-id="ee13b-121">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> </dl>

 

 




