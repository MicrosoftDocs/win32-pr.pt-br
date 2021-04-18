---
title: Método ISoftKbd CreateSoftKeyboardLayoutFromResource (Softkbdc. h)
description: O método ISoftKbd CreateSoftKeybboardLayoutFromResource cria um layout de teclado flexível a partir do recurso especificado.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- Estrutura de serviços de texto do método CreateSoftKeyboardLayoutFromResource
- Método CreateSoftKeyboardLayoutFromResource de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método CreateSoftKeyboardLayoutFromResource
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810474"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a><span data-ttu-id="cb07b-106">Método ISoftKbd:: CreateSoftKeyboardLayoutFromResource</span><span class="sxs-lookup"><span data-stu-id="cb07b-106">ISoftKbd::CreateSoftKeyboardLayoutFromResource method</span></span>

<span data-ttu-id="cb07b-107">O método **ISoftKbd:: CreateSoftKeybboardLayoutFromResource** cria um layout de teclado flexível a partir do recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="cb07b-107">The **ISoftKbd::CreateSoftKeybboardLayoutFromResource** method creates a soft keyboard layout from the specified resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb07b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb07b-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="cb07b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb07b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb07b-110">*lpszResFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cb07b-110">*lpszResFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb07b-111">Ponteiro para uma cadeia de caracteres terminada em zero que indica o nome do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="cb07b-111">Pointer to a zero-terminated string indicating the name of the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="cb07b-112">*lpszResType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cb07b-112">*lpszResType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb07b-113">Ponteiro para uma cadeia de caracteres terminada em zero que indica o tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="cb07b-113">Pointer to a zero-terminated string indicating the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="cb07b-114">*lpszXMLResString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cb07b-114">*lpszXMLResString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb07b-115">Ponteiro para uma cadeia de caracteres terminada em zero que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="cb07b-115">Pointer to a zero-terminated string identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="cb07b-116">*lpdwLayoutCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cb07b-116">*lpdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb07b-117">Ponteiro para o buffer no qual esse método recupera um cookie de layout de teclado flexível.</span><span class="sxs-lookup"><span data-stu-id="cb07b-117">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb07b-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb07b-118">Return value</span></span>

<span data-ttu-id="cb07b-119">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="cb07b-119">This method can return one of these values.</span></span>



| <span data-ttu-id="cb07b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cb07b-120">Value</span></span>                                                                                        | <span data-ttu-id="cb07b-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb07b-121">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="cb07b-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cb07b-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="cb07b-123">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cb07b-123">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="cb07b-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cb07b-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="cb07b-125">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="cb07b-125">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cb07b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb07b-126">Requirements</span></span>



| <span data-ttu-id="cb07b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb07b-127">Requirement</span></span> | <span data-ttu-id="cb07b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="cb07b-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb07b-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb07b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cb07b-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cb07b-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cb07b-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb07b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cb07b-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cb07b-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cb07b-133">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="cb07b-133">Redistributable</span></span><br/>          | <span data-ttu-id="cb07b-134">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cb07b-134">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="cb07b-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb07b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb07b-136"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb07b-136"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="cb07b-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="cb07b-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb07b-138"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb07b-138"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="cb07b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cb07b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb07b-140"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb07b-140"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb07b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb07b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb07b-142">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="cb07b-142">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="cb07b-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span><span class="sxs-lookup"><span data-stu-id="cb07b-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[<span data-ttu-id="cb07b-144">**ISoftKbd::ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="cb07b-144">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





