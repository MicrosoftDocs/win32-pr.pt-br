---
title: Método ISoftKbd SetKeyboardLabelText (Softkbdc. h)
description: O método ISoftKbd SetKeyboardLabelText define o texto do rótulo do layout de um teclado virtual.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Estrutura de serviços de texto do método SetKeyboardLabelText
- Método SetKeyboardLabelText de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetKeyboardLabelText
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644972"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a><span data-ttu-id="bbfeb-106">Método ISoftKbd:: SetKeyboardLabelText</span><span class="sxs-lookup"><span data-stu-id="bbfeb-106">ISoftKbd::SetKeyboardLabelText method</span></span>

<span data-ttu-id="bbfeb-107">O método **ISoftKbd:: SetKeyboardLabelText** define o texto do rótulo do layout de um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="bbfeb-107">The **ISoftKbd::SetKeyboardLabelText** method sets the label text from the layout for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbfeb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbfeb-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a><span data-ttu-id="bbfeb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbfeb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbfeb-110">*hKl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bbfeb-110">*hKl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbfeb-111">Identificador que é usado para recuperar o layout instalado para o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="bbfeb-111">Handle that is used to retrieve the installed layout for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbfeb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bbfeb-112">Return value</span></span>

<span data-ttu-id="bbfeb-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="bbfeb-113">This method can return one of these values.</span></span>



| <span data-ttu-id="bbfeb-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bbfeb-114">Value</span></span>                                                                                        | <span data-ttu-id="bbfeb-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbfeb-115">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="bbfeb-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bbfeb-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="bbfeb-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="bbfeb-117">The method was successful.</span></span><br/>      |
| <dl> <span data-ttu-id="bbfeb-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bbfeb-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="bbfeb-119">O parâmetro *hKl* é inválido.</span><span class="sxs-lookup"><span data-stu-id="bbfeb-119">The *hKl* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bbfeb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbfeb-120">Requirements</span></span>



| <span data-ttu-id="bbfeb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbfeb-121">Requirement</span></span> | <span data-ttu-id="bbfeb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bbfeb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbfeb-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbfeb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bbfeb-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bbfeb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bbfeb-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbfeb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bbfeb-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bbfeb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bbfeb-127">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="bbfeb-127">Redistributable</span></span><br/>          | <span data-ttu-id="bbfeb-128">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bbfeb-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="bbfeb-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bbfeb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbfeb-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbfeb-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="bbfeb-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="bbfeb-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bbfeb-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bbfeb-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="bbfeb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bbfeb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbfeb-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbfeb-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbfeb-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbfeb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbfeb-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="bbfeb-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="bbfeb-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span><span class="sxs-lookup"><span data-stu-id="bbfeb-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





