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
# <a name="pf_followentry-structure"></a><span data-ttu-id="fe67e-103">Estrutura de FOLLOWENTRY de PF \_</span><span class="sxs-lookup"><span data-stu-id="fe67e-103">PF\_FOLLOWENTRY structure</span></span>

<span data-ttu-id="fe67e-104">A estrutura de **\_ FOLLOWENTRY do PF** define um protocolo que monitor de rede adiciona ao conjunto de acompanhamento de um analisador.</span><span class="sxs-lookup"><span data-stu-id="fe67e-104">The **PF\_FOLLOWENTRY** structure defines a protocol that Network Monitor adds to the follow set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe67e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe67e-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a><span data-ttu-id="fe67e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fe67e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe67e-107">**szProtocol**</span><span class="sxs-lookup"><span data-stu-id="fe67e-107">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="fe67e-108">O nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="fe67e-108">The name of the protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe67e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe67e-109">Remarks</span></span>

<span data-ttu-id="fe67e-110">A estrutura de [ \_ acompanhamento de PF](pf-followset.md) usa uma matriz de estruturas **\_ FOLLOWENTRY de PF** .</span><span class="sxs-lookup"><span data-stu-id="fe67e-110">The [PF\_FOLLOWSET](pf-followset.md) structure uses an array of **PF\_FOLLOWENTRY** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe67e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe67e-111">Requirements</span></span>



| <span data-ttu-id="fe67e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe67e-112">Requirement</span></span> | <span data-ttu-id="fe67e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="fe67e-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fe67e-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe67e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fe67e-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fe67e-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fe67e-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe67e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fe67e-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fe67e-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fe67e-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fe67e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe67e-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe67e-119"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe67e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe67e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe67e-121">seguir do PF \_</span><span class="sxs-lookup"><span data-stu-id="fe67e-121">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> </dl>

 

 




