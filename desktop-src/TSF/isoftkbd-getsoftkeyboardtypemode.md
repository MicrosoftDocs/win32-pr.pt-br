---
title: Método ISoftKbd GetSoftKeyboardTypeMode (Softkbdc. h)
description: O método ISoftKbd GetSoftKeyboardTypeMode recupera o modo de tipo para um teclado virtual.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- Estrutura de serviços de texto do método GetSoftKeyboardTypeMode
- Método GetSoftKeyboardTypeMode de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método GetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369199"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a><span data-ttu-id="b1a93-106">Método ISoftKbd:: GetSoftKeyboardTypeMode</span><span class="sxs-lookup"><span data-stu-id="b1a93-106">ISoftKbd::GetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="b1a93-107">O método **ISoftKbd:: GetSoftKeyboardTypeMode** recupera o modo de tipo para um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="b1a93-107">The **ISoftKbd::GetSoftKeyboardTypeMode** method retrieves the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a93-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1a93-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="b1a93-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1a93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1a93-110">*lpTypeMode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b1a93-110">*lpTypeMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a93-111">Ponteiro para um buffer no qual esse método recupera o modo de tipo.</span><span class="sxs-lookup"><span data-stu-id="b1a93-111">Pointer to a buffer in which this method retrieves the type mode.</span></span> <span data-ttu-id="b1a93-112">Os valores possíveis são definidos para a enumeração [**typemode**](typemode.md) .</span><span class="sxs-lookup"><span data-stu-id="b1a93-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1a93-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1a93-113">Return value</span></span>

<span data-ttu-id="b1a93-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b1a93-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b1a93-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a93-115">Value</span></span>                                                                                        | <span data-ttu-id="b1a93-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1a93-116">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="b1a93-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b1a93-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b1a93-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b1a93-118">The method was successful.</span></span><br/>             |
| <dl> <span data-ttu-id="b1a93-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b1a93-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b1a93-120">O parâmetro *lpTypeMode* é inválido.</span><span class="sxs-lookup"><span data-stu-id="b1a93-120">The *lpTypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b1a93-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1a93-121">Requirements</span></span>



| <span data-ttu-id="b1a93-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1a93-122">Requirement</span></span> | <span data-ttu-id="b1a93-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a93-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a93-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1a93-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a93-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b1a93-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b1a93-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1a93-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a93-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b1a93-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b1a93-128">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b1a93-128">Redistributable</span></span><br/>          | <span data-ttu-id="b1a93-129">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b1a93-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="b1a93-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1a93-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1a93-131"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1a93-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="b1a93-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="b1a93-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1a93-133"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1a93-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="b1a93-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b1a93-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1a93-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1a93-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1a93-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1a93-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a93-137">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="b1a93-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="b1a93-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="b1a93-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="b1a93-139">**TIPO de**</span><span class="sxs-lookup"><span data-stu-id="b1a93-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





