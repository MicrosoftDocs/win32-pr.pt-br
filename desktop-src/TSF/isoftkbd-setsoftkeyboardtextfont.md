---
title: Método ISoftKbd SetSoftKeyboardTextFont (Softkbdc. h)
description: O método ISoftKbd SetSoftKeyboardTextFont define a fonte de texto usada por um teclado suave.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Estrutura de serviços de texto do método SetSoftKeyboardTextFont
- Método SetSoftKeyboardTextFont de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813076"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a><span data-ttu-id="e5811-106">Método ISoftKbd:: SetSoftKeyboardTextFont</span><span class="sxs-lookup"><span data-stu-id="e5811-106">ISoftKbd::SetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="e5811-107">O método **ISoftKbd:: SetSoftKeyboardTextFont** define a fonte de texto usada por um teclado suave.</span><span class="sxs-lookup"><span data-stu-id="e5811-107">The **ISoftKbd::SetSoftKeyboardTextFont** method sets the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5811-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5811-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="e5811-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5811-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5811-110">*pLogFont* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5811-110">*pLogFont* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5811-111">Ponteiro para uma estrutura [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que define a fonte do texto para o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="e5811-111">Pointer to a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5811-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5811-112">Return value</span></span>

<span data-ttu-id="e5811-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e5811-113">This method can return one of these values.</span></span>



| <span data-ttu-id="e5811-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e5811-114">Value</span></span>                                                                                        | <span data-ttu-id="e5811-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5811-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e5811-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e5811-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e5811-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e5811-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="e5811-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e5811-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e5811-119">O parâmetro *pLogFont* é inválido.</span><span class="sxs-lookup"><span data-stu-id="e5811-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e5811-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5811-120">Requirements</span></span>



| <span data-ttu-id="e5811-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5811-121">Requirement</span></span> | <span data-ttu-id="e5811-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e5811-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5811-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5811-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e5811-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5811-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e5811-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5811-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e5811-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5811-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e5811-127">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e5811-127">Redistributable</span></span><br/>          | <span data-ttu-id="e5811-128">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e5811-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="e5811-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5811-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5811-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5811-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="e5811-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="e5811-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5811-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5811-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="e5811-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e5811-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5811-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5811-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5811-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5811-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5811-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="e5811-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="e5811-137">**ISoftKbd::GetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="e5811-137">**ISoftKbd::GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

