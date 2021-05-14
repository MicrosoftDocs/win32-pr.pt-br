---
description: Pega uma estrutura STRRET retornada por IShellFolder::GetDisplayNameOf, converte-a em uma cadeia de caracteres e coloca o resultado em um buffer.
title: Função StrRetToStrN
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 50295d712e539c94f10a708674cea595a47ae4e0
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841027"
---
# <a name="strrettostrn-function"></a><span data-ttu-id="d1095-103">Função StrRetToStrN</span><span class="sxs-lookup"><span data-stu-id="d1095-103">StrRetToStrN function</span></span>

<span data-ttu-id="d1095-104">Aceita uma [**estrutura STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) retornada por [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), converte-a em uma cadeia de caracteres e coloca o resultado em um buffer.</span><span class="sxs-lookup"><span data-stu-id="d1095-104">Takes an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure returned by [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), converts it to a string, and places the result in a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1095-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1095-105">Syntax</span></span>


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a><span data-ttu-id="d1095-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1095-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1095-107">*pszOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d1095-107">*pszOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1095-108">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="d1095-108">Type: **LPTSTR**</span></span>

<span data-ttu-id="d1095-109">Buffer para manter o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="d1095-109">Buffer to hold the display name.</span></span> <span data-ttu-id="d1095-110">Ele será retornado como uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="d1095-110">It will be returned as a null-terminated string.</span></span> <span data-ttu-id="d1095-111">Se *cchOut* for muito pequeno, o nome será truncado para caber.</span><span class="sxs-lookup"><span data-stu-id="d1095-111">If *cchOut* is too small, the name will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="d1095-112">*cchOut* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="d1095-112">*cchOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1095-113">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="d1095-113">Type: **UINT**</span></span>

<span data-ttu-id="d1095-114">Tamanho de *pszOut*, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="d1095-114">Size of *pszOut*, in characters.</span></span> <span data-ttu-id="d1095-115">Se *cchOut* for muito pequeno, a cadeia de caracteres será truncada para caber.</span><span class="sxs-lookup"><span data-stu-id="d1095-115">If *cchOut* is too small, the string will be truncated to fit.</span></span>

</dd> <dt>

<span data-ttu-id="d1095-116">*pStrRet* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d1095-116">*pStrRet* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1095-117">Tipo: **LPSTRRET**</span><span class="sxs-lookup"><span data-stu-id="d1095-117">Type: **LPSTRRET**</span></span>

<span data-ttu-id="d1095-118">Ponteiro para uma [**estrutura STRRET.**](/windows/desktop/api/Shtypes/ns-shtypes-strret)</span><span class="sxs-lookup"><span data-stu-id="d1095-118">Pointer to an [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) structure.</span></span> <span data-ttu-id="d1095-119">Quando a função retornar, esse ponteiro não será mais válido.</span><span class="sxs-lookup"><span data-stu-id="d1095-119">When the function returns, this pointer will no longer be valid.</span></span>

</dd> <dt>

<span data-ttu-id="d1095-120">*pidl* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="d1095-120">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1095-121">Tipo: **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="d1095-121">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="d1095-122">Ponteiro para a estrutura [**ITEMIDLIST do**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) item.</span><span class="sxs-lookup"><span data-stu-id="d1095-122">Pointer to the item's [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1095-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1095-123">Return value</span></span>

<span data-ttu-id="d1095-124">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="d1095-124">Type: **BOOL**</span></span>

<span data-ttu-id="d1095-125">**Verdadeiro** para êxito, **falso** para falha.</span><span class="sxs-lookup"><span data-stu-id="d1095-125">**TRUE** for success, **FALSE** for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1095-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1095-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d1095-127">A partir da versão Shell32.dll 5,0, chamar essa função é equivalente a chamar [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span><span class="sxs-lookup"><span data-stu-id="d1095-127">As of Shell32.dll version 5.0, calling this function is equivalent to calling [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).</span></span>

 

<span data-ttu-id="d1095-128">**StrRetToStrN** não é exportado pelo nome.</span><span class="sxs-lookup"><span data-stu-id="d1095-128">**StrRetToStrN** is not exported by name.</span></span> <span data-ttu-id="d1095-129">Para usá-lo, você deve usar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 96 de Shell32.dll para obter um ponteiro de função.</span><span class="sxs-lookup"><span data-stu-id="d1095-129">To use it, you must use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 96 from Shell32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="d1095-130">Se o membro **uType** da estrutura apontada por *pStrRet* for definido como **Strret \_ WSTR**, o membro **pOleStr** dessa estrutura será liberado no retorno.</span><span class="sxs-lookup"><span data-stu-id="d1095-130">If the **uType** member of the structure pointed to by *pStrRet* is set to **STRRET\_WSTR**, the **pOleStr** member of that structure will be freed on return.</span></span>

<span data-ttu-id="d1095-131">Observe que essa função é exportada de Shell32.dll em vez de Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="d1095-131">Note that this function is exported from Shell32.dll rather than Shlwapi.dll.</span></span> <span data-ttu-id="d1095-132">Ele também está incluído em shlobj. h em vez de shlwapi. h.</span><span class="sxs-lookup"><span data-stu-id="d1095-132">It is also included in Shlobj.h rather than Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1095-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1095-133">Requirements</span></span>



| <span data-ttu-id="d1095-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1095-134">Requirement</span></span> | <span data-ttu-id="d1095-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d1095-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1095-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1095-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d1095-137">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d1095-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d1095-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1095-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d1095-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1095-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d1095-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d1095-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1095-141"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d1095-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1095-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1095-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1095-143">**StrRetToStr**</span><span class="sxs-lookup"><span data-stu-id="d1095-143">**StrRetToStr**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[<span data-ttu-id="d1095-144">**StrRetToBuf**</span><span class="sxs-lookup"><span data-stu-id="d1095-144">**StrRetToBuf**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
