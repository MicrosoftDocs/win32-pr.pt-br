---
title: Método ISoftKbd ShowSoftKeyboard (Softkbdc. h)
description: O método ISoftKbd ShowSoftKeyboard exibe um teclado virtual.
ms.assetid: 7e24bef1-accb-40f6-a549-fb676abf9971
keywords:
- Estrutura de serviços de texto do método ShowSoftKeyboard
- Método ShowSoftKeyboard de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método ShowSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.ShowSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b319e7782a19571cf827175566e1af056c34cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008822"
---
# <a name="isoftkbdshowsoftkeyboard-method"></a><span data-ttu-id="b9bfc-106">Método ISoftKbd:: ShowSoftKeyboard</span><span class="sxs-lookup"><span data-stu-id="b9bfc-106">ISoftKbd::ShowSoftKeyboard method</span></span>

<span data-ttu-id="b9bfc-107">O método **ISoftKbd:: ShowSoftKeyboard** exibe um teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="b9bfc-107">The **ISoftKbd::ShowSoftKeyboard** method displays a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9bfc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9bfc-108">Syntax</span></span>


```C++
HRESULT ShowSoftKeyboard(
  [in] INT iShow
);
```



## <a name="parameters"></a><span data-ttu-id="b9bfc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9bfc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9bfc-110">*iShow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9bfc-110">*iShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9bfc-111">Inteiro que indica o tipo de teclado virtual a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b9bfc-111">Integer indicating the type of soft keyboard to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9bfc-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9bfc-112">Return value</span></span>

<span data-ttu-id="b9bfc-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b9bfc-113">This method can return one of these values.</span></span>



| <span data-ttu-id="b9bfc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b9bfc-114">Value</span></span>                                                                                | <span data-ttu-id="b9bfc-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9bfc-115">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="b9bfc-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b9bfc-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b9bfc-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b9bfc-117">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b9bfc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9bfc-118">Requirements</span></span>



| <span data-ttu-id="b9bfc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9bfc-119">Requirement</span></span> | <span data-ttu-id="b9bfc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b9bfc-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9bfc-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9bfc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b9bfc-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b9bfc-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b9bfc-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9bfc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b9bfc-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b9bfc-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b9bfc-125">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b9bfc-125">Redistributable</span></span><br/>          | <span data-ttu-id="b9bfc-126">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b9bfc-126">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="b9bfc-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9bfc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9bfc-128"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9bfc-128"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="b9bfc-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="b9bfc-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9bfc-130"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9bfc-130"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="b9bfc-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b9bfc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9bfc-132"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9bfc-132"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9bfc-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9bfc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9bfc-134">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="b9bfc-134">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





