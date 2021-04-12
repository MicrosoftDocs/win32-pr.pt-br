---
title: Método ISoftKbd SetSoftKeyboardPosSize (Softkbdc. h)
description: O método ISoftKbd SetSoftKeyboardPosSize define a posição inicial e o tamanho de um teclado suave.
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- Estrutura de serviços de texto do método SetSoftKeyboardPosSize
- Método SetSoftKeyboardPosSize de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7131d9c46c90917f2ebdf471916f872aedb2e33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455643"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a><span data-ttu-id="ae3d4-106">Método ISoftKbd:: SetSoftKeyboardPosSize</span><span class="sxs-lookup"><span data-stu-id="ae3d4-106">ISoftKbd::SetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="ae3d4-107">O método **ISoftKbd:: SetSoftKeyboardPosSize** define a posição inicial e o tamanho de um teclado suave.</span><span class="sxs-lookup"><span data-stu-id="ae3d4-107">The **ISoftKbd::SetSoftKeyboardPosSize** method sets the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae3d4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae3d4-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardPosSize(
  [in] POINT StartPoint,
  [in] WORD  width,
  [in] WORD  height
);
```



## <a name="parameters"></a><span data-ttu-id="ae3d4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae3d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae3d4-110">*StartPoint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae3d4-110">*StartPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae3d4-111">Uma estrutura de [ponto](/previous-versions//dd162805(v=vs.85)) que indica as coordenadas da posição superior esquerda do teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="ae3d4-111">A [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="ae3d4-112">*largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae3d4-112">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae3d4-113">Largura do teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="ae3d4-113">Width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="ae3d4-114">*altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae3d4-114">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae3d4-115">Altura do teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="ae3d4-115">Height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae3d4-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae3d4-116">Return value</span></span>

<span data-ttu-id="ae3d4-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ae3d4-117">This method can return one of these values.</span></span>



| <span data-ttu-id="ae3d4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ae3d4-118">Value</span></span>                                                                                        | <span data-ttu-id="ae3d4-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae3d4-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ae3d4-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ae3d4-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ae3d4-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ae3d4-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="ae3d4-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ae3d4-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ae3d4-123">Um dos parâmetros é inválido.</span><span class="sxs-lookup"><span data-stu-id="ae3d4-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ae3d4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae3d4-124">Requirements</span></span>



| <span data-ttu-id="ae3d4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae3d4-125">Requirement</span></span> | <span data-ttu-id="ae3d4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ae3d4-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae3d4-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae3d4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ae3d4-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ae3d4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ae3d4-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae3d4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ae3d4-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ae3d4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ae3d4-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="ae3d4-131">Redistributable</span></span><br/>          | <span data-ttu-id="ae3d4-132">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ae3d4-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ae3d4-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae3d4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae3d4-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae3d4-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ae3d4-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="ae3d4-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ae3d4-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae3d4-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="ae3d4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ae3d4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae3d4-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae3d4-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae3d4-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae3d4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae3d4-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="ae3d4-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

