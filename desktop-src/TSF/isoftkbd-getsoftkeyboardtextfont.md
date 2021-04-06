---
title: Método ISoftKbd GetSoftKeyboardTextFont (Softkbdc. h)
description: O método ISoftKbd GetSoftKeyboardTextFont recupera a fonte de texto usada por um teclado virtual.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Estrutura de serviços de texto do método GetSoftKeyboardTextFont
- Método GetSoftKeyboardTextFont de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método GetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086079"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a><span data-ttu-id="d7f0d-106">Método ISoftKbd:: GetSoftKeyboardTextFont</span><span class="sxs-lookup"><span data-stu-id="d7f0d-106">ISoftKbd::GetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="d7f0d-107">O método **ISoftKbd:: GetSoftKeyboardTextFont** recupera a fonte de texto usada por um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-107">The **ISoftKbd::GetSoftKeyboardTextFont** method retrieves the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f0d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7f0d-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="d7f0d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7f0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f0d-110">*pLogFont* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d7f0d-110">*pLogFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f0d-111">Ponteiro para um buffer no qual esse método recupera uma estrutura [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que define a fonte do texto para o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-111">Pointer to a buffer in which this method retrieves a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f0d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7f0d-112">Return value</span></span>

<span data-ttu-id="d7f0d-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-113">This method can return one of these values.</span></span>



| <span data-ttu-id="d7f0d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d7f0d-114">Value</span></span>                                                                                        | <span data-ttu-id="d7f0d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7f0d-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="d7f0d-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f0d-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d7f0d-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="d7f0d-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f0d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d7f0d-119">O parâmetro *pLogFont* é inválido.</span><span class="sxs-lookup"><span data-stu-id="d7f0d-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d7f0d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7f0d-120">Requirements</span></span>



| <span data-ttu-id="d7f0d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f0d-121">Requirement</span></span> | <span data-ttu-id="d7f0d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d7f0d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f0d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7f0d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f0d-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7f0d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7f0d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7f0d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f0d-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7f0d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d7f0d-127">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d7f0d-127">Redistributable</span></span><br/>          | <span data-ttu-id="d7f0d-128">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d7f0d-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="d7f0d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7f0d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f0d-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f0d-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="d7f0d-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="d7f0d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7f0d-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7f0d-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="d7f0d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d7f0d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7f0d-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7f0d-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f0d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7f0d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f0d-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="d7f0d-137">**ISoftKbd::SetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="d7f0d-137">**ISoftKbd::SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

