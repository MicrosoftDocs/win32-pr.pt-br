---
title: Método ISoftKbd CreateSoftKeyboardLayoutFromXMLFile (Softkbdc. h)
description: O método ISoftKbd CreateSoftKeyboardLayoutFromXMLFile cria um layout de teclado flexível a partir do arquivo XML especificado.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- Estrutura de serviços de texto do método CreateSoftKeyboardLayoutFromXMLFile
- Método CreateSoftKeyboardLayoutFromXMLFile de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método CreateSoftKeyboardLayoutFromXMLFile
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811021"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a><span data-ttu-id="b5ff8-106">Método ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile</span><span class="sxs-lookup"><span data-stu-id="b5ff8-106">ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile method</span></span>

<span data-ttu-id="b5ff8-107">O método **ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile** cria um layout de teclado flexível a partir do arquivo XML especificado.</span><span class="sxs-lookup"><span data-stu-id="b5ff8-107">The **ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile** method creates a soft keyboard layout from the specified XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ff8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5ff8-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="b5ff8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5ff8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ff8-110">*lpszKeyboardDesFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5ff8-110">*lpszKeyboardDesFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ff8-111">Ponteiro para uma cadeia de caracteres terminada em zero que indica o nome do arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="b5ff8-111">Pointer to a zero-terminated string indicating the name of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="b5ff8-112">*szFileStrLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5ff8-112">*szFileStrLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ff8-113">Cadeia de caracteres terminada em zero indicando o comprimento do arquivo XML.</span><span class="sxs-lookup"><span data-stu-id="b5ff8-113">Zero-terminated string indicating the length of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="b5ff8-114">*pdwLayoutCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b5ff8-114">*pdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ff8-115">Ponteiro para o buffer no qual esse método recupera um cookie de layout de teclado flexível.</span><span class="sxs-lookup"><span data-stu-id="b5ff8-115">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ff8-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5ff8-116">Return value</span></span>

<span data-ttu-id="b5ff8-117">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b5ff8-117">This method can return one of these values.</span></span>



| <span data-ttu-id="b5ff8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b5ff8-118">Value</span></span>                                                                                        | <span data-ttu-id="b5ff8-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5ff8-119">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="b5ff8-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b5ff8-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b5ff8-121">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b5ff8-121">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="b5ff8-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b5ff8-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b5ff8-123">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="b5ff8-123">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b5ff8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5ff8-124">Requirements</span></span>



| <span data-ttu-id="b5ff8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5ff8-125">Requirement</span></span> | <span data-ttu-id="b5ff8-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b5ff8-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ff8-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5ff8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ff8-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b5ff8-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b5ff8-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5ff8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ff8-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b5ff8-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b5ff8-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="b5ff8-131">Redistributable</span></span><br/>          | <span data-ttu-id="b5ff8-132">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b5ff8-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="b5ff8-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5ff8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5ff8-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5ff8-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="b5ff8-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="b5ff8-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5ff8-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5ff8-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="b5ff8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b5ff8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5ff8-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5ff8-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5ff8-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5ff8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ff8-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="b5ff8-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="b5ff8-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="b5ff8-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





