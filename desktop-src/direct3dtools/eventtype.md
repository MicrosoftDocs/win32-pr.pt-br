---
description: Uma enumeração usada para indicar o tipo de um evento.
MS-HAID: vspixengine.EVENTTYPE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração EVENTTYPE
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7A6F396-5BC0-4963-ABFD-ACB7AAE475F5
api_name:
- EVENTTYPE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 60af0090e440cd101211394cff98c9d9a501f4ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370168"
---
# <a name="span-idvspixengineeventtypespaneventtype-enumeration"></a><span data-ttu-id="f1c92-103"><span id="vspixengine.eventtype"></span>Enumeração EVENTTYPE</span><span class="sxs-lookup"><span data-stu-id="f1c92-103"><span id="vspixengine.eventtype"></span>EVENTTYPE enumeration</span></span>

<span data-ttu-id="f1c92-104">Uma enumeração usada para indicar o tipo de um evento.</span><span class="sxs-lookup"><span data-stu-id="f1c92-104">An enum used to indicate the type of an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c92-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1c92-105">Syntax</span></span>

```cpp
C++ 
enum EVENTTYPE {
  ET_NONE = 0, 
  ET_SESSIONSTART, 
  ET_SESSIONEND, 
  ET_PROCESSSTART, 
  ET_PROCESSEND, 
  ET_FRAMEBEGIN, 
  ET_FRAMEEND, 
  ET_USEREVENTBEGIN, 
  ET_USEREVENTEND, 
  ET_USERMARKER, 
  ET_CALL, 
  ET_OBJECTCREATION, 
  ET_OBJECTPOPULATION, 
  ET_CALLSYNC, 
  ET_DRAW, 
  ET_DISPATCH 
};
```

## <a name="constants"></a><span data-ttu-id="f1c92-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f1c92-106">Constants</span></span>

<span data-ttu-id="f1c92-107"><span id="ET_NONE"></span><span id="et_none"></span>**ET \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="f1c92-107"><span id="ET_NONE"></span><span id="et_none"></span>**ET\_NONE**</span></span>  
<span data-ttu-id="f1c92-108">Um valor que corresponde a nenhum evento.</span><span class="sxs-lookup"><span data-stu-id="f1c92-108">A value that corresponds to no event.</span></span>

<span data-ttu-id="f1c92-109"><span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**\_SESSIONSTART et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-109"><span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**ET\_SESSIONSTART**</span></span>  
<span data-ttu-id="f1c92-110">Um valor que corresponde a um evento de início de sessão.</span><span class="sxs-lookup"><span data-stu-id="f1c92-110">A value that corresponds to a session start event.</span></span>

<span data-ttu-id="f1c92-111"><span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**\_SESSIONEND et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-111"><span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**ET\_SESSIONEND**</span></span>  
<span data-ttu-id="f1c92-112">Um valor que corresponde a um evento de término de sessão.</span><span class="sxs-lookup"><span data-stu-id="f1c92-112">A value that corresponds to a session end event.</span></span>

<span data-ttu-id="f1c92-113"><span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**\_PROCESSSTART et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-113"><span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**ET\_PROCESSSTART**</span></span>  
<span data-ttu-id="f1c92-114">Um valor que corresponde a um evento de início de processo.</span><span class="sxs-lookup"><span data-stu-id="f1c92-114">A value that corresponds to a process start event.</span></span>

<span data-ttu-id="f1c92-115"><span id="ET_PROCESSEND"></span><span id="et_processend"></span>**\_PROCESSEND et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-115"><span id="ET_PROCESSEND"></span><span id="et_processend"></span>**ET\_PROCESSEND**</span></span>  
<span data-ttu-id="f1c92-116">Um valor que corresponde a um evento Process end.</span><span class="sxs-lookup"><span data-stu-id="f1c92-116">A value that corresponds to a process end event.</span></span>

<span data-ttu-id="f1c92-117"><span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**\_FRAMEBEGIN et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-117"><span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**ET\_FRAMEBEGIN**</span></span>  
<span data-ttu-id="f1c92-118">Um valor que corresponde a um evento de início de quadro.</span><span class="sxs-lookup"><span data-stu-id="f1c92-118">A value that corresponds to a frame begin event.</span></span>

<span data-ttu-id="f1c92-119"><span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**\_FRAMEEND et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-119"><span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**ET\_FRAMEEND**</span></span>  
<span data-ttu-id="f1c92-120">Um valor que corresponde a um evento de final de quadro.</span><span class="sxs-lookup"><span data-stu-id="f1c92-120">A value that corresponds to a frame end event.</span></span> <span data-ttu-id="f1c92-121">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f1c92-121">Not used.</span></span>

<span data-ttu-id="f1c92-122"><span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**\_USEREVENTBEGIN et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-122"><span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**ET\_USEREVENTBEGIN**</span></span>  
<span data-ttu-id="f1c92-123">Um valor que corresponde a um evento de início de evento do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1c92-123">A value that corresponds to a user-event begin event.</span></span>

<span data-ttu-id="f1c92-124"><span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**\_USEREVENTEND et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-124"><span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**ET\_USEREVENTEND**</span></span>  
<span data-ttu-id="f1c92-125">Um valor que corresponde a um evento de término de evento do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1c92-125">A value that corresponds to a user-event end event.</span></span> <span data-ttu-id="f1c92-126">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f1c92-126">Not used.</span></span>

<span data-ttu-id="f1c92-127"><span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**\_DEFAULTmarker et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-127"><span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**ET\_USERMARKER**</span></span>  
<span data-ttu-id="f1c92-128">Um valor que corresponde a um evento de marcador do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1c92-128">A value that corresponds to a user-marker event.</span></span>

<span data-ttu-id="f1c92-129"><span id="ET_CALL"></span><span id="et_call"></span>**\_chamada et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-129"><span id="ET_CALL"></span><span id="et_call"></span>**ET\_CALL**</span></span>  
<span data-ttu-id="f1c92-130">Um valor que corresponde a um evento de chamada.</span><span class="sxs-lookup"><span data-stu-id="f1c92-130">A value that corresponds to a call event.</span></span>

<span data-ttu-id="f1c92-131"><span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**objectcreation ET \_**</span><span class="sxs-lookup"><span data-stu-id="f1c92-131"><span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**ET\_OBJECTCREATION**</span></span>  
<span data-ttu-id="f1c92-132">Um valor que corresponde a um evento de criação de objeto.</span><span class="sxs-lookup"><span data-stu-id="f1c92-132">A value that corresponds to an object creation event.</span></span>

<span data-ttu-id="f1c92-133"><span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET \_ Population**</span><span class="sxs-lookup"><span data-stu-id="f1c92-133"><span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET\_OBJECTPOPULATION**</span></span>  
<span data-ttu-id="f1c92-134">Um valor que corresponde a um evento de população de objeto.</span><span class="sxs-lookup"><span data-stu-id="f1c92-134">A value that corresponds to an object population event.</span></span>

<span data-ttu-id="f1c92-135"><span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**\_CALLSYNC et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-135"><span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**ET\_CALLSYNC**</span></span>  

<span data-ttu-id="f1c92-136"><span id="ET_DRAW"></span><span id="et_draw"></span>**\_desenho et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-136"><span id="ET_DRAW"></span><span id="et_draw"></span>**ET\_DRAW**</span></span>  
<span data-ttu-id="f1c92-137">Um valor que corresponde a um evento de chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="f1c92-137">A value that corresponds to a draw call event.</span></span>

<span data-ttu-id="f1c92-138"><span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**\_expedição et**</span><span class="sxs-lookup"><span data-stu-id="f1c92-138"><span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**ET\_DISPATCH**</span></span>  
<span data-ttu-id="f1c92-139">Um valor que corresponde a um evento de expedição.</span><span class="sxs-lookup"><span data-stu-id="f1c92-139">A value that corresponds to a dispatch event.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1c92-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1c92-140">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f1c92-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1c92-141">Header</span></span></p></td><td><span data-ttu-id="f1c92-142">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f1c92-142">Vspixengine.h</span></span></td></tr></tbody></table>
