---
title: Método ISoftKbd EnumSoftKeyboard (Softkbdc. h)
description: O método ISoftKbd EnumSoftKeyboard enumera os teclados suaves possíveis que dão suporte ao idioma especificado.
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- Estrutura de serviços de texto do método EnumSoftKeyboard
- Método EnumSoftKeyboard de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método EnumSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455574"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a><span data-ttu-id="e1977-106">Método ISoftKbd:: EnumSoftKeyboard</span><span class="sxs-lookup"><span data-stu-id="e1977-106">ISoftKbd::EnumSoftKeyboard method</span></span>

<span data-ttu-id="e1977-107">O método **ISoftKbd:: EnumSoftKeyboard** enumera os teclados Soft possíveis que dão suporte ao idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="e1977-107">The **ISoftKbd::EnumSoftKeyboard** method enumerates the possible soft keyboards that support the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1977-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1977-108">Syntax</span></span>


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a><span data-ttu-id="e1977-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1977-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1977-110">*LangID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e1977-110">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1977-111">Identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="e1977-111">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e1977-112">*lpdwKeyboard* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e1977-112">*lpdwKeyboard* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1977-113">Ponteiro para um buffer no qual esse método recupera identificadores dos teclados Soft disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e1977-113">Pointer to a buffer in which this method retrieves identifiers of the available soft keyboards.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1977-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1977-114">Return value</span></span>

<span data-ttu-id="e1977-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e1977-115">This method can return one of these values.</span></span>



| <span data-ttu-id="e1977-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e1977-116">Value</span></span>                                                                                        | <span data-ttu-id="e1977-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1977-117">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="e1977-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e1977-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e1977-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e1977-119">The method was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="e1977-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e1977-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e1977-121">O parâmetro *LangID* é inválido.</span><span class="sxs-lookup"><span data-stu-id="e1977-121">The *langid* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e1977-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1977-122">Requirements</span></span>



| <span data-ttu-id="e1977-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1977-123">Requirement</span></span> | <span data-ttu-id="e1977-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e1977-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1977-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1977-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e1977-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1977-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e1977-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1977-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e1977-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1977-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e1977-129">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e1977-129">Redistributable</span></span><br/>          | <span data-ttu-id="e1977-130">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e1977-130">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="e1977-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1977-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1977-132"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1977-132"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="e1977-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="e1977-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1977-134"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1977-134"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="e1977-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e1977-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1977-136"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1977-136"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1977-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1977-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1977-138">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="e1977-138">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





