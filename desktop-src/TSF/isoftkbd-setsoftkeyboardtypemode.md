---
title: Método ISoftKbd SetSoftKeyboardTypeMode (Softkbdc. h)
description: O método ISoftKbd SetSoftKeyboardTypeMode define o modo de tipo para um teclado virtual.
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- Estrutura de serviços de texto do método SetSoftKeyboardTypeMode
- Método SetSoftKeyboardTypeMode de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55c01465debc42926888e2cb12a3a5b9d884498b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455644"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a><span data-ttu-id="73747-106">Método ISoftKbd:: SetSoftKeyboardTypeMode</span><span class="sxs-lookup"><span data-stu-id="73747-106">ISoftKbd::SetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="73747-107">O método **ISoftKbd:: SetSoftKeyboardTypeMode** define o modo de tipo para um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="73747-107">The **ISoftKbd::SetSoftKeyboardTypeMode** method sets the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="73747-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73747-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="73747-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73747-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73747-110">*Tipo de* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73747-110">*TypeMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73747-111">O modo de tipo.</span><span class="sxs-lookup"><span data-stu-id="73747-111">The type mode.</span></span> <span data-ttu-id="73747-112">Os valores possíveis são definidos para a enumeração [**typemode**](typemode.md) .</span><span class="sxs-lookup"><span data-stu-id="73747-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73747-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73747-113">Return value</span></span>

<span data-ttu-id="73747-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="73747-114">This method can return one of these values.</span></span>



| <span data-ttu-id="73747-115">Valor</span><span class="sxs-lookup"><span data-stu-id="73747-115">Value</span></span>                                                                                        | <span data-ttu-id="73747-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="73747-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="73747-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="73747-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="73747-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="73747-118">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="73747-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="73747-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="73747-120">O parâmetro *typemode* é inválido.</span><span class="sxs-lookup"><span data-stu-id="73747-120">The *TypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="73747-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73747-121">Requirements</span></span>



| <span data-ttu-id="73747-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="73747-122">Requirement</span></span> | <span data-ttu-id="73747-123">Valor</span><span class="sxs-lookup"><span data-stu-id="73747-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73747-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73747-124">Minimum supported client</span></span><br/> | <span data-ttu-id="73747-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="73747-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="73747-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73747-126">Minimum supported server</span></span><br/> | <span data-ttu-id="73747-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="73747-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="73747-128">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="73747-128">Redistributable</span></span><br/>          | <span data-ttu-id="73747-129">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="73747-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="73747-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73747-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="73747-131"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="73747-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="73747-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="73747-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="73747-133"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="73747-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="73747-134">DLL</span><span class="sxs-lookup"><span data-stu-id="73747-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73747-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73747-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73747-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="73747-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73747-137">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="73747-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="73747-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="73747-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="73747-139">**TIPO de**</span><span class="sxs-lookup"><span data-stu-id="73747-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





