---
description: Indica o status atual de um especialista em execução.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: Estrutura EXPERTSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501357"
---
# <a name="expertstatus-structure"></a><span data-ttu-id="d056c-103">Estrutura EXPERTSTATUS</span><span class="sxs-lookup"><span data-stu-id="d056c-103">EXPERTSTATUS structure</span></span>

<span data-ttu-id="d056c-104">A estrutura **EXPERTSTATUS** indica o status atual de um especialista em execução.</span><span class="sxs-lookup"><span data-stu-id="d056c-104">The **EXPERTSTATUS** structure indicates the current status of a running expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="d056c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d056c-105">Syntax</span></span>


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a><span data-ttu-id="d056c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d056c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d056c-107">**Status**</span><span class="sxs-lookup"><span data-stu-id="d056c-107">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="d056c-108">Valor de status de especialista atual definido pela enumeração [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="d056c-108">Current expert status value defined by the [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="d056c-109">**SubStatus**</span><span class="sxs-lookup"><span data-stu-id="d056c-109">**SubStatus**</span></span>
</dt> <dd>

<span data-ttu-id="d056c-110">Valor de substatus.</span><span class="sxs-lookup"><span data-stu-id="d056c-110">Sub-status value.</span></span>

</dd> <dt>

<span data-ttu-id="d056c-111">**PercentDone**</span><span class="sxs-lookup"><span data-stu-id="d056c-111">**PercentDone**</span></span>
</dt> <dd>

<span data-ttu-id="d056c-112">Porcentagem de conclusão da análise do especialista de dados de rede.</span><span class="sxs-lookup"><span data-stu-id="d056c-112">Percentage completion of the expert analysis of network data.</span></span>

</dd> <dt>

<span data-ttu-id="d056c-113">**Frame**</span><span class="sxs-lookup"><span data-stu-id="d056c-113">**Frame**</span></span>
</dt> <dd>

<span data-ttu-id="d056c-114">Número do quadro.</span><span class="sxs-lookup"><span data-stu-id="d056c-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="d056c-115">**szStatusText**</span><span class="sxs-lookup"><span data-stu-id="d056c-115">**szStatusText**</span></span>
</dt> <dd>

<span data-ttu-id="d056c-116">Texto que descreve o status do especialista.</span><span class="sxs-lookup"><span data-stu-id="d056c-116">Text that describes the expert status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d056c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d056c-117">Requirements</span></span>



| <span data-ttu-id="d056c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d056c-118">Requirement</span></span> | <span data-ttu-id="d056c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d056c-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d056c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d056c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d056c-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d056c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d056c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d056c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d056c-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d056c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d056c-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d056c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d056c-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d056c-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




