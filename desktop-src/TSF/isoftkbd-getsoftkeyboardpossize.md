---
title: Método ISoftKbd GetSoftKeyboardPosSize (Softkbdc. h)
description: O método ISoftKbd GetSoftKeyboardPosSize recupera a posição inicial e o tamanho de um teclado suave.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- Estrutura de serviços de texto do método GetSoftKeyboardPosSize
- Método GetSoftKeyboardPosSize de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método GetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295830"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a><span data-ttu-id="0fc1f-106">Método ISoftKbd:: GetSoftKeyboardPosSize</span><span class="sxs-lookup"><span data-stu-id="0fc1f-106">ISoftKbd::GetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="0fc1f-107">O método **ISoftKbd:: GetSoftKeyboardPosSize** recupera a posição inicial e o tamanho de um teclado suave.</span><span class="sxs-lookup"><span data-stu-id="0fc1f-107">The **ISoftKbd::GetSoftKeyboardPosSize** method retrieves the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc1f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fc1f-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a><span data-ttu-id="0fc1f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fc1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fc1f-110">*lpStartPoint* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0fc1f-110">*lpStartPoint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fc1f-111">Ponteiro para um buffer no qual esse método recupera uma estrutura de [ponto](/previous-versions//dd162805(v=vs.85)) que indica as coordenadas da posição superior esquerda do teclado suave.</span><span class="sxs-lookup"><span data-stu-id="0fc1f-111">Pointer to a buffer in which this method retrieves a [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="0fc1f-112">*lpwidth* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0fc1f-112">*lpwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fc1f-113">Ponteiro para um buffer no qual esse método recupera a largura do teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="0fc1f-113">Pointer to a buffer in which this method retrieves the width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="0fc1f-114">*lpheight* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0fc1f-114">*lpheight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fc1f-115">Ponteiro para um buffer no qual esse método recupera a altura do teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="0fc1f-115">Pointer to a buffer in which this method retrieves the height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fc1f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0fc1f-116">Return value</span></span>

<span data-ttu-id="0fc1f-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="0fc1f-117">This method can return one of these values.</span></span>



| <span data-ttu-id="0fc1f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0fc1f-118">Value</span></span>                                                                                        | <span data-ttu-id="0fc1f-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="0fc1f-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0fc1f-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0fc1f-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0fc1f-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0fc1f-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="0fc1f-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0fc1f-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0fc1f-123">Um dos parâmetros é inválido.</span><span class="sxs-lookup"><span data-stu-id="0fc1f-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0fc1f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fc1f-124">Requirements</span></span>



| <span data-ttu-id="0fc1f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fc1f-125">Requirement</span></span> | <span data-ttu-id="0fc1f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0fc1f-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fc1f-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fc1f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0fc1f-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0fc1f-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0fc1f-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fc1f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0fc1f-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0fc1f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0fc1f-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="0fc1f-131">Redistributable</span></span><br/>          | <span data-ttu-id="0fc1f-132">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0fc1f-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="0fc1f-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fc1f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fc1f-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fc1f-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="0fc1f-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="0fc1f-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0fc1f-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0fc1f-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="0fc1f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0fc1f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fc1f-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fc1f-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fc1f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fc1f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc1f-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="0fc1f-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="0fc1f-141">**ISoftKbd::SetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="0fc1f-141">**ISoftKbd::SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

