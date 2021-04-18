---
description: Ocorre quando o cursor se move sobre o digitalizador digitalizador.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'Método ITabletEventSink:: CursorMove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788136"
---
# <a name="itableteventsinkcursormove-method"></a><span data-ttu-id="034f4-103">Método ITabletEventSink:: CursorMove</span><span class="sxs-lookup"><span data-stu-id="034f4-103">ITabletEventSink::CursorMove method</span></span>

<span data-ttu-id="034f4-104">Ocorre quando o cursor se move sobre o digitalizador digitalizador.</span><span class="sxs-lookup"><span data-stu-id="034f4-104">Occurs when the cursor moves over the tablet digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="034f4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="034f4-105">Syntax</span></span>


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a><span data-ttu-id="034f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="034f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="034f4-107">*tcid*</span><span class="sxs-lookup"><span data-stu-id="034f4-107">*tcid*</span></span> 
</dt> <dd>

<span data-ttu-id="034f4-108">Dentifier exclusivo do digitalizador do Tablet.</span><span class="sxs-lookup"><span data-stu-id="034f4-108">Unique dentifier of the tablet digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="034f4-109">*CID*</span><span class="sxs-lookup"><span data-stu-id="034f4-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="034f4-110">Identificador exclusivo da caneta digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="034f4-110">Unique identifier of the tablet stylus.</span></span>

</dd> <dt>

<span data-ttu-id="034f4-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="034f4-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="034f4-112">A janela sobre a qual o cursor foi movido.</span><span class="sxs-lookup"><span data-stu-id="034f4-112">The window over which the cursor moved.</span></span>

</dd> <dt>

<span data-ttu-id="034f4-113">*xPos*</span><span class="sxs-lookup"><span data-stu-id="034f4-113">*xPos*</span></span> 
</dt> <dd>

<span data-ttu-id="034f4-114">A posição X da caneta.</span><span class="sxs-lookup"><span data-stu-id="034f4-114">The X position of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="034f4-115">*yPos*</span><span class="sxs-lookup"><span data-stu-id="034f4-115">*yPos*</span></span> 
</dt> <dd>

<span data-ttu-id="034f4-116">A posição Y da caneta.</span><span class="sxs-lookup"><span data-stu-id="034f4-116">The Y position of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="034f4-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="034f4-117">Return value</span></span>

<span data-ttu-id="034f4-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="034f4-118">This method can return one of these values.</span></span>



| <span data-ttu-id="034f4-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="034f4-119">Return code</span></span>                                                                            | <span data-ttu-id="034f4-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="034f4-120">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="034f4-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-121"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="034f4-122">Êxito.</span><span class="sxs-lookup"><span data-stu-id="034f4-122">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="034f4-123"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-123"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="034f4-124">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="034f4-124">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="034f4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="034f4-125">Requirements</span></span>



| <span data-ttu-id="034f4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="034f4-126">Requirement</span></span> | <span data-ttu-id="034f4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="034f4-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="034f4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="034f4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="034f4-129">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="034f4-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="034f4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="034f4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="034f4-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="034f4-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="034f4-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="034f4-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="034f4-133"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-133"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="034f4-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="034f4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="034f4-135">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="034f4-135">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




