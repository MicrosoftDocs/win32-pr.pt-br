---
description: A estrutura do gatilho indica uma ação a ser tomada pelo driver em um horário especificado.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Estrutura do gatilho (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758450"
---
# <a name="trigger-structure"></a><span data-ttu-id="eee78-103">Estrutura do gatilho</span><span class="sxs-lookup"><span data-stu-id="eee78-103">TRIGGER structure</span></span>

<span data-ttu-id="eee78-104">A estrutura do **gatilho** indica uma ação a ser tomada pelo driver em um horário especificado.</span><span class="sxs-lookup"><span data-stu-id="eee78-104">The **TRIGGER** structure indicates an action to be taken by the driver at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="eee78-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eee78-105">Syntax</span></span>


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a><span data-ttu-id="eee78-106">Membros</span><span class="sxs-lookup"><span data-stu-id="eee78-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="eee78-107">**TriggerActive**</span><span class="sxs-lookup"><span data-stu-id="eee78-107">**TriggerActive**</span></span>
</dt> <dd>

<span data-ttu-id="eee78-108">Um valor booliano que determina se o gatilho deve ser pago pelo driver.</span><span class="sxs-lookup"><span data-stu-id="eee78-108">A Boolean value that determines if the trigger should be paid attention to by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="eee78-109">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="eee78-109">**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="eee78-110">O código op do gatilho.</span><span class="sxs-lookup"><span data-stu-id="eee78-110">The op code of the trigger.</span></span>

</dd> <dt>

<span data-ttu-id="eee78-111">**TriggerAction**</span><span class="sxs-lookup"><span data-stu-id="eee78-111">**TriggerAction**</span></span>
</dt> <dd>

<span data-ttu-id="eee78-112">Ação que o gatilho deve tomar se for acionado.</span><span class="sxs-lookup"><span data-stu-id="eee78-112">Action that the trigger is to take if it is fired.</span></span>

</dd> <dt>

<span data-ttu-id="eee78-113">**TriggerFlags**</span><span class="sxs-lookup"><span data-stu-id="eee78-113">**TriggerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="eee78-114">Sinalizadores de gatilho.</span><span class="sxs-lookup"><span data-stu-id="eee78-114">Trigger flags.</span></span>

</dd> <dt>

<span data-ttu-id="eee78-115">**TriggerPatternMatch**</span><span class="sxs-lookup"><span data-stu-id="eee78-115">**TriggerPatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="eee78-116">A correspondência do padrão de gatilho.</span><span class="sxs-lookup"><span data-stu-id="eee78-116">The trigger pattern match.</span></span>

</dd> <dt>

<span data-ttu-id="eee78-117">**TriggerBufferSize**</span><span class="sxs-lookup"><span data-stu-id="eee78-117">**TriggerBufferSize**</span></span>
</dt> <dd>

<span data-ttu-id="eee78-118">Tamanho do buffer de gatilho.</span><span class="sxs-lookup"><span data-stu-id="eee78-118">Trigger buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="eee78-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="eee78-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="eee78-120">Reservado.</span><span class="sxs-lookup"><span data-stu-id="eee78-120">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eee78-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eee78-121">Requirements</span></span>



| <span data-ttu-id="eee78-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eee78-122">Requirement</span></span> | <span data-ttu-id="eee78-123">Valor</span><span class="sxs-lookup"><span data-stu-id="eee78-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="eee78-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eee78-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eee78-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eee78-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="eee78-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eee78-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eee78-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eee78-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="eee78-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="eee78-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eee78-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="eee78-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




