---
description: Ocorre quando um evento do sistema está disponível.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'Método ITabletEventSink:: SystemEvent'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751575"
---
# <a name="itableteventsinksystemevent-method"></a><span data-ttu-id="eadc6-103">Método ITabletEventSink:: SystemEvent</span><span class="sxs-lookup"><span data-stu-id="eadc6-103">ITabletEventSink::SystemEvent method</span></span>

<span data-ttu-id="eadc6-104">Ocorre quando um evento do sistema está disponível.</span><span class="sxs-lookup"><span data-stu-id="eadc6-104">Occurs when a system event is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="eadc6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eadc6-105">Syntax</span></span>


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a><span data-ttu-id="eadc6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eadc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eadc6-107">*TCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eadc6-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eadc6-108">O identificador do Tablet.</span><span class="sxs-lookup"><span data-stu-id="eadc6-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="eadc6-109">*CID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="eadc6-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eadc6-110">O identificador da caneta.</span><span class="sxs-lookup"><span data-stu-id="eadc6-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="eadc6-111">*evento* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="eadc6-111">*event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eadc6-112">O código do evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="eadc6-112">The system event code.</span></span>

</dd> <dt>

<span data-ttu-id="eadc6-113">*EVENTDATA* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eadc6-113">*eventdata* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eadc6-114">Os dados de evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="eadc6-114">The system event data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eadc6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eadc6-115">Return value</span></span>

<span data-ttu-id="eadc6-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="eadc6-116">This method can return one of these values.</span></span>



| <span data-ttu-id="eadc6-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="eadc6-117">Return code</span></span>                                                                            | <span data-ttu-id="eadc6-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="eadc6-118">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="eadc6-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eadc6-119"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="eadc6-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="eadc6-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="eadc6-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="eadc6-121"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="eadc6-122">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="eadc6-122">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eadc6-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="eadc6-123">Remarks</span></span>

<span data-ttu-id="eadc6-124">A lista a seguir contém os valores válidos para o parâmetro de evento.</span><span class="sxs-lookup"><span data-stu-id="eadc6-124">The following list contains the valid values for the event parameter.</span></span>

-   <span data-ttu-id="eadc6-125">\_toque em</span><span class="sxs-lookup"><span data-stu-id="eadc6-125">SE\_TAP</span></span>
-   <span data-ttu-id="eadc6-126">\_toque duplo \_ se</span><span class="sxs-lookup"><span data-stu-id="eadc6-126">SE\_DBL\_TAP</span></span>
-   <span data-ttu-id="eadc6-127">toque com o \_ botão direito \_</span><span class="sxs-lookup"><span data-stu-id="eadc6-127">SE\_RIGHT\_TAP</span></span>
-   <span data-ttu-id="eadc6-128">\_arrastar para</span><span class="sxs-lookup"><span data-stu-id="eadc6-128">SE\_DRAG</span></span>
-   <span data-ttu-id="eadc6-129">arrastar para a \_ direita \_</span><span class="sxs-lookup"><span data-stu-id="eadc6-129">SE\_RIGHT\_DRAG</span></span>
-   <span data-ttu-id="eadc6-130">\_ \_ Inserir</span><span class="sxs-lookup"><span data-stu-id="eadc6-130">SE\_HOLD\_ENTER</span></span>
-   <span data-ttu-id="eadc6-131">\_deixar de manter \_</span><span class="sxs-lookup"><span data-stu-id="eadc6-131">SE\_HOLD\_LEAVE</span></span>
-   <span data-ttu-id="eadc6-132">\_inserir em foco \_ Enter</span><span class="sxs-lookup"><span data-stu-id="eadc6-132">SE\_HOVER\_ENTER</span></span>
-   <span data-ttu-id="eadc6-133">\_sair do foco de se \_</span><span class="sxs-lookup"><span data-stu-id="eadc6-133">SE\_HOVER\_LEAVE</span></span>
-   <span data-ttu-id="eadc6-134">\_clique no meio \_</span><span class="sxs-lookup"><span data-stu-id="eadc6-134">SE\_MIDDLE\_CLICK</span></span>
-   <span data-ttu-id="eadc6-135">\_chave se</span><span class="sxs-lookup"><span data-stu-id="eadc6-135">SE\_KEY</span></span>
-   <span data-ttu-id="eadc6-136">\_chave do modificador se \_</span><span class="sxs-lookup"><span data-stu-id="eadc6-136">SE\_MODIFIER\_KEY</span></span>
-   <span data-ttu-id="eadc6-137">\_modo de gesto de se \_</span><span class="sxs-lookup"><span data-stu-id="eadc6-137">SE\_GESTURE\_MODE</span></span>
-   <span data-ttu-id="eadc6-138">\_cursor se</span><span class="sxs-lookup"><span data-stu-id="eadc6-138">SE\_CURSOR</span></span>

## <a name="requirements"></a><span data-ttu-id="eadc6-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eadc6-139">Requirements</span></span>



| <span data-ttu-id="eadc6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="eadc6-140">Requirement</span></span> | <span data-ttu-id="eadc6-141">Valor</span><span class="sxs-lookup"><span data-stu-id="eadc6-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eadc6-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eadc6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="eadc6-143">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="eadc6-143">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="eadc6-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eadc6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="eadc6-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="eadc6-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eadc6-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eadc6-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="eadc6-147"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eadc6-147"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eadc6-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="eadc6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eadc6-149">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="eadc6-149">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




