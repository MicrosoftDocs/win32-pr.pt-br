---
title: Método ISoftKbd GetSoftKeyboardColors (Softkbdc. h)
description: O método ISoftKbd GetSoftKeyboardColors recupera a cor do teclado flexível correspondente ao tipo de cor fornecido.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Estrutura de serviços de texto do método GetSoftKeyboardColors
- Método GetSoftKeyboardColors de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método GetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2021
ms.locfileid: "105758128"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a><span data-ttu-id="3ea0c-106">Método ISoftKbd:: GetSoftKeyboardColors</span><span class="sxs-lookup"><span data-stu-id="3ea0c-106">ISoftKbd::GetSoftKeyboardColors method</span></span>

<span data-ttu-id="3ea0c-107">O método **ISoftKbd:: GetSoftKeyboardColors** recupera a cor do teclado flexível correspondente ao tipo de cor fornecido.</span><span class="sxs-lookup"><span data-stu-id="3ea0c-107">The **ISoftKbd::GetSoftKeyboardColors** method retrieves the soft keyboard color corresponding to the supplied color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ea0c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ea0c-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a><span data-ttu-id="3ea0c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ea0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ea0c-110">*ColorType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ea0c-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea0c-111">Um valor que especifica o tipo de cor a ser recuperado para o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="3ea0c-111">A value specifying the color type to retrieve for the soft keyboard.</span></span> <span data-ttu-id="3ea0c-112">Os valores possíveis são definidos para a enumeração [**ColorType**](/windows/win32/api/icm/ne-icm-colortype) .</span><span class="sxs-lookup"><span data-stu-id="3ea0c-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="3ea0c-113">*lpColor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3ea0c-113">*lpColor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ea0c-114">Ponteiro para um buffer no qual esse método recupera um valor de [**COLORREF**](/windows/desktop/gdi/colorref) de 32 bits especificando uma cor RGB.</span><span class="sxs-lookup"><span data-stu-id="3ea0c-114">Pointer to a buffer in which this method retrieves a 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ea0c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ea0c-115">Return value</span></span>

<span data-ttu-id="3ea0c-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="3ea0c-116">This method can return one of these values.</span></span>



| <span data-ttu-id="3ea0c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3ea0c-117">Value</span></span>                                                                                        | <span data-ttu-id="3ea0c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ea0c-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3ea0c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3ea0c-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3ea0c-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3ea0c-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="3ea0c-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3ea0c-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3ea0c-122">Um dos parâmetros é inválido.</span><span class="sxs-lookup"><span data-stu-id="3ea0c-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3ea0c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ea0c-123">Requirements</span></span>



| <span data-ttu-id="3ea0c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ea0c-124">Requirement</span></span> | <span data-ttu-id="3ea0c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3ea0c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ea0c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ea0c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3ea0c-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ea0c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3ea0c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ea0c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3ea0c-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ea0c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3ea0c-130">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="3ea0c-130">Redistributable</span></span><br/>          | <span data-ttu-id="3ea0c-131">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3ea0c-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="3ea0c-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ea0c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ea0c-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ea0c-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="3ea0c-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="3ea0c-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ea0c-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ea0c-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ea0c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3ea0c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ea0c-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ea0c-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ea0c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ea0c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ea0c-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="3ea0c-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="3ea0c-140">**ISoftKbd::SetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="3ea0c-140">**ISoftKbd::SetSoftKeyboardColors**</span></span>](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[<span data-ttu-id="3ea0c-141">**COLORtype**</span><span class="sxs-lookup"><span data-stu-id="3ea0c-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="3ea0c-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="3ea0c-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

