---
title: Método ISoftKbd SetKeyboardLabelTextCombination (Softkbdc. h)
description: O método ISoftKbd SetKeyboardLabelTextCombination define uma combinação de rótulo e texto usado para descrever um teclado suave.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Estrutura de serviços de texto do método SetKeyboardLabelTextCombination
- Método SetKeyboardLabelTextCombination de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetKeyboardLabelTextCombination
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810473"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a><span data-ttu-id="c1c85-106">Método ISoftKbd:: SetKeyboardLabelTextCombination</span><span class="sxs-lookup"><span data-stu-id="c1c85-106">ISoftKbd::SetKeyboardLabelTextCombination method</span></span>

<span data-ttu-id="c1c85-107">O método **ISoftKbd:: SetKeyboardLabelTextCombination** define uma combinação de rótulo e texto usado para descrever um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="c1c85-107">The **ISoftKbd::SetKeyboardLabelTextCombination** method sets a combination of label and text used to describe a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c85-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1c85-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a><span data-ttu-id="c1c85-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1c85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c85-110">*nModifierCombination* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1c85-110">*nModifierCombination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c85-111">Combinação de rótulo e texto usado para descrever o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="c1c85-111">Combination of label and text used to describe the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c85-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1c85-112">Return value</span></span>

<span data-ttu-id="c1c85-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="c1c85-113">This method can return one of these values.</span></span>



| <span data-ttu-id="c1c85-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c1c85-114">Value</span></span>                                                                                        | <span data-ttu-id="c1c85-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1c85-115">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="c1c85-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c85-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c1c85-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c1c85-117">The method was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="c1c85-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c1c85-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c1c85-119">O parâmetro *nModifierCombination* é inválido.</span><span class="sxs-lookup"><span data-stu-id="c1c85-119">The *nModifierCombination* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c1c85-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1c85-120">Requirements</span></span>



| <span data-ttu-id="c1c85-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1c85-121">Requirement</span></span> | <span data-ttu-id="c1c85-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c1c85-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c85-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1c85-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c85-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c1c85-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c1c85-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1c85-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c85-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c1c85-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c1c85-127">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c1c85-127">Redistributable</span></span><br/>          | <span data-ttu-id="c1c85-128">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c1c85-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="c1c85-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1c85-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1c85-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1c85-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="c1c85-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="c1c85-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c1c85-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c1c85-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="c1c85-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c1c85-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1c85-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1c85-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c85-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1c85-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c85-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="c1c85-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="c1c85-137">**ISoftKbd::SetKeyboardLabelText**</span><span class="sxs-lookup"><span data-stu-id="c1c85-137">**ISoftKbd::SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





