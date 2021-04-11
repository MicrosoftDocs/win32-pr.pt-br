---
description: Contém informações sobre um evento do sistema do Tablet.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: Estrutura de SYSTEM_EVENT_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172061"
---
# <a name="system_event_data-structure"></a><span data-ttu-id="c426b-103">Estrutura de dados de \_ evento do sistema \_</span><span class="sxs-lookup"><span data-stu-id="c426b-103">SYSTEM\_EVENT\_DATA structure</span></span>

<span data-ttu-id="c426b-104">Contém informações sobre um evento do sistema do Tablet.</span><span class="sxs-lookup"><span data-stu-id="c426b-104">Contains information about a tablet system event.</span></span>

## <a name="syntax"></a><span data-ttu-id="c426b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c426b-105">Syntax</span></span>


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a><span data-ttu-id="c426b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c426b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c426b-107">**bModifier**</span><span class="sxs-lookup"><span data-stu-id="c426b-107">**bModifier**</span></span>
</dt> <dd>

<span data-ttu-id="c426b-108">Valores de bits para os modificadores.</span><span class="sxs-lookup"><span data-stu-id="c426b-108">Bit values for the modifiers.</span></span> <span data-ttu-id="c426b-109">Consulte a seção de comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c426b-109">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="c426b-110">**wKey**</span><span class="sxs-lookup"><span data-stu-id="c426b-110">**wKey**</span></span>
</dt> <dd>

<span data-ttu-id="c426b-111">Código de verificação do caractere de teclado.</span><span class="sxs-lookup"><span data-stu-id="c426b-111">Scan code for the keyboard character.</span></span>

</dd> <dt>

<span data-ttu-id="c426b-112">**xPos**</span><span class="sxs-lookup"><span data-stu-id="c426b-112">**xPos**</span></span>
</dt> <dd>

<span data-ttu-id="c426b-113">Posição X do evento.</span><span class="sxs-lookup"><span data-stu-id="c426b-113">X position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="c426b-114">**yPos**</span><span class="sxs-lookup"><span data-stu-id="c426b-114">**yPos**</span></span>
</dt> <dd>

<span data-ttu-id="c426b-115">Posição Y do evento.</span><span class="sxs-lookup"><span data-stu-id="c426b-115">Y position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="c426b-116">**bCursorMode**</span><span class="sxs-lookup"><span data-stu-id="c426b-116">**bCursorMode**</span></span>
</dt> <dd>

<span data-ttu-id="c426b-117">O tipo de cursor que causou o evento.</span><span class="sxs-lookup"><span data-stu-id="c426b-117">The type of cursor that caused the event.</span></span> <span data-ttu-id="c426b-118">Consulte a seção de comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c426b-118">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="c426b-119">**dwButtonState**</span><span class="sxs-lookup"><span data-stu-id="c426b-119">**dwButtonState**</span></span>
</dt> <dd>

<span data-ttu-id="c426b-120">Estado dos botões no momento do evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="c426b-120">State of the buttons at the time of the system event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c426b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c426b-121">Remarks</span></span>

<span data-ttu-id="c426b-122">Os eventos do sistema a seguir são definidos para uso no membro **bModifier** .</span><span class="sxs-lookup"><span data-stu-id="c426b-122">The following system events are defined for use in the **bModifier** member.</span></span>



| <span data-ttu-id="c426b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c426b-123">Value</span></span>               | <span data-ttu-id="c426b-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="c426b-124">Description</span></span>                  |
|---------------------|------------------------------|
| <span data-ttu-id="c426b-125">\_modificador de se \_ Ctrl</span><span class="sxs-lookup"><span data-stu-id="c426b-125">SE\_MODIFIER\_CTRL</span></span>  | <span data-ttu-id="c426b-126">A tecla Control foi pressionada.</span><span class="sxs-lookup"><span data-stu-id="c426b-126">The Control key was pressed.</span></span> |
| <span data-ttu-id="c426b-127">\_modificador de se \_ ALT</span><span class="sxs-lookup"><span data-stu-id="c426b-127">SE\_MODIFIER\_ALT</span></span>   | <span data-ttu-id="c426b-128">A tecla Alt foi pressionada.</span><span class="sxs-lookup"><span data-stu-id="c426b-128">The Alt key was pressed.</span></span>     |
| <span data-ttu-id="c426b-129">\_alternância de modificador se \_</span><span class="sxs-lookup"><span data-stu-id="c426b-129">SE\_MODIFIER\_SHIFT</span></span> | <span data-ttu-id="c426b-130">A tecla Shift foi pressionada.</span><span class="sxs-lookup"><span data-stu-id="c426b-130">The Shift key was pressed.</span></span>   |



 

<span data-ttu-id="c426b-131">Os eventos do sistema a seguir são definidos para uso no membro **bCursorMode** .</span><span class="sxs-lookup"><span data-stu-id="c426b-131">The following system events are defined for use in the **bCursorMode** member.</span></span>



| <span data-ttu-id="c426b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c426b-132">Value</span></span>              | <span data-ttu-id="c426b-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="c426b-133">Description</span></span>               |
|--------------------|---------------------------|
| <span data-ttu-id="c426b-134">\_cursor normal do se \_</span><span class="sxs-lookup"><span data-stu-id="c426b-134">SE\_NORMAL\_CURSOR</span></span> | <span data-ttu-id="c426b-135">Indica a dica de caneta.</span><span class="sxs-lookup"><span data-stu-id="c426b-135">Indicates the pen tip.</span></span>    |
| <span data-ttu-id="c426b-136">\_cursor de borracha \_ se</span><span class="sxs-lookup"><span data-stu-id="c426b-136">SE\_ERASER\_CURSOR</span></span> | <span data-ttu-id="c426b-137">Indica a borracha da caneta.</span><span class="sxs-lookup"><span data-stu-id="c426b-137">Indicates the pen eraser.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c426b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c426b-138">Requirements</span></span>



| <span data-ttu-id="c426b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c426b-139">Requirement</span></span> | <span data-ttu-id="c426b-140">Valor</span><span class="sxs-lookup"><span data-stu-id="c426b-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c426b-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c426b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c426b-142">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c426b-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c426b-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c426b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c426b-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c426b-144">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="c426b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="c426b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c426b-146">**Método IStylusPlugin:: SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="c426b-146">**IStylusPlugin::SystemEvent Method**</span></span>](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[<span data-ttu-id="c426b-147">**Método ITabletEventSink:: SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="c426b-147">**ITabletEventSink::SystemEvent Method**</span></span>](itableteventsink-systemevent.md)
</dt> </dl>

 

 




