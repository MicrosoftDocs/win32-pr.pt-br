---
title: Método ISoftKbd SelectSoftKeyboard (Softkbdc. h)
description: O método ISoftKbd SelectSoftKeyboard seleciona o teclado virtual especificado.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Estrutura de serviços de texto do método SelectSoftKeyboard
- Método SelectSoftKeyboard de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SelectSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499620"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a><span data-ttu-id="6fdec-106">Método ISoftKbd:: SelectSoftKeyboard</span><span class="sxs-lookup"><span data-stu-id="6fdec-106">ISoftKbd::SelectSoftKeyboard method</span></span>

<span data-ttu-id="6fdec-107">O método **ISoftKbd:: SelectSoftKeyboard** seleciona o teclado virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="6fdec-107">The **ISoftKbd::SelectSoftKeyboard** method selects the specified soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdec-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fdec-108">Syntax</span></span>


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a><span data-ttu-id="6fdec-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fdec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fdec-110">*dwKeyboardId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fdec-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fdec-111">Identificador do teclado virtual a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="6fdec-111">Identifier of the soft keyboard to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fdec-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fdec-112">Return value</span></span>

<span data-ttu-id="6fdec-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="6fdec-113">This method can return one of these values.</span></span>



| <span data-ttu-id="6fdec-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6fdec-114">Value</span></span>                                                                                        | <span data-ttu-id="6fdec-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fdec-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="6fdec-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6fdec-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6fdec-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6fdec-117">The method was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="6fdec-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6fdec-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6fdec-119">O parâmetro *dwKeyboardId* é inválido.</span><span class="sxs-lookup"><span data-stu-id="6fdec-119">The *dwKeyboardId* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6fdec-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fdec-120">Requirements</span></span>



| <span data-ttu-id="6fdec-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fdec-121">Requirement</span></span> | <span data-ttu-id="6fdec-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6fdec-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fdec-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fdec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6fdec-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fdec-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6fdec-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fdec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6fdec-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fdec-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6fdec-127">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6fdec-127">Redistributable</span></span><br/>          | <span data-ttu-id="6fdec-128">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6fdec-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="6fdec-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fdec-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fdec-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fdec-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="6fdec-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="6fdec-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6fdec-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6fdec-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="6fdec-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6fdec-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fdec-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fdec-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fdec-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fdec-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fdec-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="6fdec-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





