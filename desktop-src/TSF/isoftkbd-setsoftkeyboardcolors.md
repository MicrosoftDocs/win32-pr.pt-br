---
title: Método ISoftKbd SetSoftKeyboardColors (Softkbdc. h)
description: O método ISoftKbd SetSoftKeyboardColors define a cor do teclado flexível para o tipo de cor especificado.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Estrutura de serviços de texto do método SetSoftKeyboardColors
- Método SetSoftKeyboardColors de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38357331db2440c35ca7557d08c97729fde9c9f0
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2021
ms.locfileid: "105811020"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a><span data-ttu-id="d9350-106">Método ISoftKbd:: SetSoftKeyboardColors</span><span class="sxs-lookup"><span data-stu-id="d9350-106">ISoftKbd::SetSoftKeyboardColors method</span></span>

<span data-ttu-id="d9350-107">O método **ISoftKbd:: SetSoftKeyboardColors** define a cor do teclado flexível para o tipo de cor especificado.</span><span class="sxs-lookup"><span data-stu-id="d9350-107">The **ISoftKbd::SetSoftKeyboardColors** method sets the soft keyboard color for the specified color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9350-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9350-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a><span data-ttu-id="d9350-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9350-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9350-110">*ColorType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d9350-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9350-111">Um valor que especifica o tipo de cor para o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="d9350-111">A value specifying the color type for the soft keyboard.</span></span> <span data-ttu-id="d9350-112">Os valores possíveis são definidos para a enumeração [**ColorType**](/windows/win32/api/icm/ne-icm-colortype) .</span><span class="sxs-lookup"><span data-stu-id="d9350-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="d9350-113">*Cor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d9350-113">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9350-114">Um valor de [**COLORREF**](/windows/desktop/gdi/colorref) de 32 bits especificando uma cor RGB.</span><span class="sxs-lookup"><span data-stu-id="d9350-114">A 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9350-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9350-115">Return value</span></span>

<span data-ttu-id="d9350-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="d9350-116">This method can return one of these values.</span></span>



| <span data-ttu-id="d9350-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d9350-117">Value</span></span>                                                                                        | <span data-ttu-id="d9350-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9350-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d9350-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d9350-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d9350-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d9350-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="d9350-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d9350-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d9350-122">Um dos parâmetros é inválido.</span><span class="sxs-lookup"><span data-stu-id="d9350-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d9350-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9350-123">Requirements</span></span>



| <span data-ttu-id="d9350-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9350-124">Requirement</span></span> | <span data-ttu-id="d9350-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d9350-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9350-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9350-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d9350-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d9350-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d9350-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9350-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d9350-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d9350-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d9350-130">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d9350-130">Redistributable</span></span><br/>          | <span data-ttu-id="d9350-131">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d9350-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="d9350-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9350-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9350-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9350-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="d9350-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="d9350-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d9350-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d9350-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="d9350-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d9350-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9350-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9350-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9350-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9350-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9350-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="d9350-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="d9350-140">**ISoftKbd::GetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="d9350-140">**ISoftKbd::GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[<span data-ttu-id="d9350-141">**COLORtype**</span><span class="sxs-lookup"><span data-stu-id="d9350-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="d9350-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="d9350-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

