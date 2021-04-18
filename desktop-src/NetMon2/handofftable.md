---
description: A estrutura de ENTREGAtable define os protocolos de uma tabela de entrega.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: Estrutura de ENTREGAtable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756885"
---
# <a name="handofftable-structure"></a><span data-ttu-id="c7051-103">Estrutura de entrega</span><span class="sxs-lookup"><span data-stu-id="c7051-103">HANDOFFTABLE structure</span></span>

<span data-ttu-id="c7051-104">A estrutura de **entregatable** define os protocolos de uma tabela de entrega.</span><span class="sxs-lookup"><span data-stu-id="c7051-104">The **HANDOFFTABLE** structure defines the protocols of a handoff table.</span></span>

<span data-ttu-id="c7051-105">Essa estrutura é preenchida por Monitor de Rede com base nas informações de um arquivo. ini fornecido pelo usuário fornecido ao chamar a função [**Createentregatable**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="c7051-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7051-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7051-106">Syntax</span></span>


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a><span data-ttu-id="c7051-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c7051-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c7051-108">**\_assinatura quente**</span><span class="sxs-lookup"><span data-stu-id="c7051-108">**hot\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="c7051-109">Assinatura que identifica essa tabela como uma tabela de entrega.</span><span class="sxs-lookup"><span data-stu-id="c7051-109">Signature that identifies this table as a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="c7051-110">**\_NumEntries quente**</span><span class="sxs-lookup"><span data-stu-id="c7051-110">**hot\_NumEntries**</span></span>
</dt> <dd>

<span data-ttu-id="c7051-111">Número de entradas que Monitor de Rede adicionadas à tabela entrega.</span><span class="sxs-lookup"><span data-stu-id="c7051-111">Number of entries that Network Monitor added to the handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="c7051-112">**entradas de acesso \_**</span><span class="sxs-lookup"><span data-stu-id="c7051-112">**hot\_Entries**</span></span>
</dt> <dd>

<span data-ttu-id="c7051-113">Tabela de entrega.</span><span class="sxs-lookup"><span data-stu-id="c7051-113">Handoff table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7051-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7051-114">Remarks</span></span>

<span data-ttu-id="c7051-115">Essa estrutura, e suas estruturas HANDOFFENTRY associadas, são preenchidas por Monitor de Rede quando Monitor de Rede cria uma tabela de entrega.</span><span class="sxs-lookup"><span data-stu-id="c7051-115">This structure, and its associated HANDOFFENTRY structures, are filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

<span data-ttu-id="c7051-116">As informações de protocolo usadas ao criar uma tabela de entrega são fornecidas em um arquivo. ini fornecido pelo aplicativo quando [**Createentregatable**](createhandofftable.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="c7051-116">The protocol information that is used when creating a handoff table is provided in an .ini file supplied by the application when [**CreateHandoffTable**](createhandofftable.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7051-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7051-117">Requirements</span></span>



| <span data-ttu-id="c7051-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7051-118">Requirement</span></span> | <span data-ttu-id="c7051-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c7051-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c7051-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7051-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c7051-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7051-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c7051-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7051-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c7051-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7051-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c7051-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c7051-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7051-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7051-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7051-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7051-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7051-127">HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="c7051-127">HANDOFFENTRY</span></span>](handoffentry.md)
</dt> <dt>

[<span data-ttu-id="c7051-128">Createentregatable</span><span class="sxs-lookup"><span data-stu-id="c7051-128">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> </dl>

 

 




