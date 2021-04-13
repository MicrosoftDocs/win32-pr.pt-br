---
title: Método ISoftKbd CreateSoftKeyboardWindow (Softkbdc. h)
description: O método ISoftKbd CreateSoftKeyboardWindow cria uma janela de teclado suave.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- Estrutura de serviços de texto do método CreateSoftKeyboardWindow
- Método CreateSoftKeyboardWindow de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método CreateSoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499584"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a><span data-ttu-id="51975-106">Método ISoftKbd:: CreateSoftKeyboardWindow</span><span class="sxs-lookup"><span data-stu-id="51975-106">ISoftKbd::CreateSoftKeyboardWindow method</span></span>

<span data-ttu-id="51975-107">O método **ISoftKbd:: CreateSoftKeyboardWindow** cria uma janela de teclado suave.</span><span class="sxs-lookup"><span data-stu-id="51975-107">The **ISoftKbd::CreateSoftKeyboardWindow** method creates a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="51975-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51975-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a><span data-ttu-id="51975-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51975-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51975-110">*hOwner* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51975-110">*hOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51975-111">Identificador da janela para conter o teclado virtual.</span><span class="sxs-lookup"><span data-stu-id="51975-111">Handle of the window to contain the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="51975-112">*\_ Tipo de TitleBar* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="51975-112">*Titlebar\_type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51975-113">Tipo de barra de título da janela de teclado flexível.</span><span class="sxs-lookup"><span data-stu-id="51975-113">Type of title bar for the soft keyboard window.</span></span> <span data-ttu-id="51975-114">Os tipos possíveis são definidos pela enumeração de [**\_ tipo TITLEBAR**](titlebar-type.md) .</span><span class="sxs-lookup"><span data-stu-id="51975-114">Possible types are defined by the [**TITLEBAR\_TYPE**](titlebar-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="51975-115">*XPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51975-115">*xPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51975-116">A posição x do canto superior esquerdo da janela de teclado suave.</span><span class="sxs-lookup"><span data-stu-id="51975-116">The x position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="51975-117">*YPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51975-117">*yPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51975-118">A posição y do canto superior esquerdo da janela de teclado suave.</span><span class="sxs-lookup"><span data-stu-id="51975-118">The y position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="51975-119">*largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51975-119">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51975-120">A largura da janela de teclado flexível.</span><span class="sxs-lookup"><span data-stu-id="51975-120">The width of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="51975-121">*altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51975-121">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51975-122">A altura da janela de teclado suave.</span><span class="sxs-lookup"><span data-stu-id="51975-122">The height of the soft keyboard window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51975-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51975-123">Return value</span></span>

<span data-ttu-id="51975-124">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="51975-124">This method can return one of these values.</span></span>



| <span data-ttu-id="51975-125">Valor</span><span class="sxs-lookup"><span data-stu-id="51975-125">Value</span></span>                                                                                        | <span data-ttu-id="51975-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="51975-126">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="51975-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="51975-127"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="51975-128">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="51975-128">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="51975-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="51975-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="51975-130">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="51975-130">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="51975-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51975-131">Requirements</span></span>



| <span data-ttu-id="51975-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="51975-132">Requirement</span></span> | <span data-ttu-id="51975-133">Valor</span><span class="sxs-lookup"><span data-stu-id="51975-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51975-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51975-134">Minimum supported client</span></span><br/> | <span data-ttu-id="51975-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51975-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="51975-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51975-136">Minimum supported server</span></span><br/> | <span data-ttu-id="51975-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51975-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="51975-138">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="51975-138">Redistributable</span></span><br/>          | <span data-ttu-id="51975-139">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="51975-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="51975-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51975-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="51975-141"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="51975-141"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="51975-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="51975-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="51975-143"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="51975-143"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="51975-144">DLL</span><span class="sxs-lookup"><span data-stu-id="51975-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51975-145"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51975-145"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51975-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="51975-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51975-147">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="51975-147">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="51975-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="51975-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[<span data-ttu-id="51975-149">**ISoftKbd::D estroySoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="51975-149">**ISoftKbd::DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[<span data-ttu-id="51975-150">**ISoftKbd::ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="51975-150">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[<span data-ttu-id="51975-151">**tipo de TITLEBAR \_**</span><span class="sxs-lookup"><span data-stu-id="51975-151">**TITLEBAR\_TYPE**</span></span>](titlebar-type.md)
</dt> </dl>

 

 





