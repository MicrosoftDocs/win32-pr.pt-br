---
description: Retorna um valor que representa os recursos do hardware do Tablet.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: 'Método ITablet:: GetHardwareCaps'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829691"
---
# <a name="itabletgethardwarecaps-method"></a><span data-ttu-id="8357c-103">Método ITablet:: GetHardwareCaps</span><span class="sxs-lookup"><span data-stu-id="8357c-103">ITablet::GetHardwareCaps method</span></span>

<span data-ttu-id="8357c-104">Retorna um valor que representa os recursos do hardware do Tablet.</span><span class="sxs-lookup"><span data-stu-id="8357c-104">Returns a value that represents the capabilities of the tablet hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="8357c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8357c-105">Syntax</span></span>


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a><span data-ttu-id="8357c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8357c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8357c-107">*pdwCaps* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8357c-107">*pdwCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8357c-108">Sinalizadores de bits que representam os recursos do hardware do Tablet.</span><span class="sxs-lookup"><span data-stu-id="8357c-108">Bit flags that represent the capabilities of the tablet hardware.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8357c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8357c-109">Return value</span></span>

<span data-ttu-id="8357c-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8357c-110">This method can return one of these values.</span></span>



| <span data-ttu-id="8357c-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8357c-111">Return code</span></span>                                                                            | <span data-ttu-id="8357c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8357c-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="8357c-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8357c-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="8357c-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="8357c-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="8357c-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="8357c-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="8357c-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8357c-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8357c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8357c-117">Remarks</span></span>

<span data-ttu-id="8357c-118">O parâmetro *pdwCaps* é um conjunto de sinalizadores de bits que descrevem os recursos de hardware do Tablet.</span><span class="sxs-lookup"><span data-stu-id="8357c-118">The *pdwCaps* parameter is a set of bit flags that describe tablet hardware capabilities.</span></span> <span data-ttu-id="8357c-119">A tabela a seguir descreve esses sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="8357c-119">The following table describes these flags.</span></span>



| <span data-ttu-id="8357c-120">Nome do sinalizador</span><span class="sxs-lookup"><span data-stu-id="8357c-120">Flag Name</span></span>                         | <span data-ttu-id="8357c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8357c-121">Value</span></span>                 | <span data-ttu-id="8357c-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="8357c-122">Description</span></span>                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8357c-123">THWC \_ integrado</span><span class="sxs-lookup"><span data-stu-id="8357c-123">THWC\_INTEGRATED</span></span><br/>       | <span data-ttu-id="8357c-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8357c-124">0x00000001</span></span><br/> | <span data-ttu-id="8357c-125">Indica que a exibição e o digitalizador compartilham a mesma superfície.</span><span class="sxs-lookup"><span data-stu-id="8357c-125">Indicates that the display and digitizer share the same surface.</span></span><br/>                                                    |
| <span data-ttu-id="8357c-126">o \_ CSR THWC \_ deve \_ tocar</span><span class="sxs-lookup"><span data-stu-id="8357c-126">THWC\_CSR\_MUST\_TOUCH</span></span><br/> | <span data-ttu-id="8357c-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8357c-127">0x00000002</span></span><br/> | <span data-ttu-id="8357c-128">Indica que o cursor deve estar no contato físico com o dispositivo para a posição do relatório.</span><span class="sxs-lookup"><span data-stu-id="8357c-128">Indicates that the cursor must be in physical contact with the device to report position.</span></span><br/>                           |
| <span data-ttu-id="8357c-129">\_proximidade THWC \_</span><span class="sxs-lookup"><span data-stu-id="8357c-129">THWC\_HARD\_PROXIMITY</span></span><br/>  | <span data-ttu-id="8357c-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="8357c-130">0x00000004</span></span><br/> | <span data-ttu-id="8357c-131">Indica que o dispositivo pode gerar eventos quando o cursor está entrando e saindo do intervalo de detecção física.</span><span class="sxs-lookup"><span data-stu-id="8357c-131">Indicates that the device can generate events when the cursor is entering and leaving the physical detection range.</span></span><br/> |
| <span data-ttu-id="8357c-132">THWC \_ PHYSID \_ SACs</span><span class="sxs-lookup"><span data-stu-id="8357c-132">THWC\_PHYSID\_CSRS</span></span><br/>     | <span data-ttu-id="8357c-133">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8357c-133">0x00000008</span></span><br/> | <span data-ttu-id="8357c-134">Indica que o dispositivo pode identificar exclusivamente o cursor ativo no hardware.</span><span class="sxs-lookup"><span data-stu-id="8357c-134">Indicates that the device can uniquely identify the active cursor in hardware.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="8357c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8357c-135">Requirements</span></span>



| <span data-ttu-id="8357c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8357c-136">Requirement</span></span> | <span data-ttu-id="8357c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="8357c-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8357c-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8357c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8357c-139">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8357c-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8357c-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8357c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8357c-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8357c-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8357c-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8357c-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="8357c-143"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8357c-143"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8357c-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="8357c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8357c-145">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="8357c-145">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




