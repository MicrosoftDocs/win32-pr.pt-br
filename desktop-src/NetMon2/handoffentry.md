---
description: A estrutura HANDOFFENTRY define uma entrada de protocolo específica em uma estrutura de entrega.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: Estrutura HANDOFFENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501347"
---
# <a name="handoffentry-structure"></a><span data-ttu-id="394c4-103">Estrutura HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="394c4-103">HANDOFFENTRY structure</span></span>

<span data-ttu-id="394c4-104">A estrutura **HANDOFFENTRY** define uma entrada de protocolo específica em uma estrutura de **entrega** .</span><span class="sxs-lookup"><span data-stu-id="394c4-104">The **HANDOFFENTRY** structure defines a specific protocol entry in a **HANDOFFTABLE** structure.</span></span>

<span data-ttu-id="394c4-105">Essa estrutura é preenchida por Monitor de Rede com base nas informações de um arquivo. ini fornecido pelo usuário fornecido ao chamar a função [**Createentregatable**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="394c4-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span> <span data-ttu-id="394c4-106">Essa estrutura nunca deve ser modificada explicitamente por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="394c4-106">This structure should never be explicitly modified by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="394c4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="394c4-107">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="394c4-108">Membros</span><span class="sxs-lookup"><span data-stu-id="394c4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="394c4-109">**\_SIG como**</span><span class="sxs-lookup"><span data-stu-id="394c4-109">**hoe\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="394c4-110">Assinatura que identifica essa entrada como uma entrada de tabela de entrega.</span><span class="sxs-lookup"><span data-stu-id="394c4-110">Signature that identifies this entry as a handoff table entry.</span></span>

</dd> <dt>

<span data-ttu-id="394c4-111">**como \_ ProtIdentNumber**</span><span class="sxs-lookup"><span data-stu-id="394c4-111">**hoe\_ProtIdentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="394c4-112">Número de protocolo fornecido pelo arquivo. ini fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="394c4-112">Protocol number provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="394c4-113">**como \_ ProtocolHandle**</span><span class="sxs-lookup"><span data-stu-id="394c4-113">**hoe\_ProtocolHandle**</span></span>
</dt> <dd>

<span data-ttu-id="394c4-114">Identificador de protocolo criado usando o nome do protocolo fornecido pelo arquivo. ini fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="394c4-114">Handle of protocol created using the protocol name provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="394c4-115">**como \_ ProtocolData**</span><span class="sxs-lookup"><span data-stu-id="394c4-115">**hoe\_ProtocolData**</span></span>
</dt> <dd>

<span data-ttu-id="394c4-116">Dados de instância de protocolo fornecidos pelo arquivo. ini fornecido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="394c4-116">Protocol instance data provided by user supplied .ini file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="394c4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="394c4-117">Remarks</span></span>

<span data-ttu-id="394c4-118">Essa estrutura é preenchida por Monitor de Rede quando Monitor de Rede cria uma tabela de entrega.</span><span class="sxs-lookup"><span data-stu-id="394c4-118">This structure is filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

## <a name="requirements"></a><span data-ttu-id="394c4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="394c4-119">Requirements</span></span>



| <span data-ttu-id="394c4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="394c4-120">Requirement</span></span> | <span data-ttu-id="394c4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="394c4-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="394c4-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="394c4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="394c4-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="394c4-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="394c4-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="394c4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="394c4-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="394c4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="394c4-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="394c4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="394c4-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="394c4-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="394c4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="394c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="394c4-129">ENTREGA</span><span class="sxs-lookup"><span data-stu-id="394c4-129">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




