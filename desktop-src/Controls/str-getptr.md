---
title: Função Str_GetPtr
description: Copia uma cadeia de caracteres de um buffer para outro.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Controles do Windows da função Str_GetPtr
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644402"
---
# <a name="str_getptr-function"></a><span data-ttu-id="bb235-104">\_Função GetPtr Str</span><span class="sxs-lookup"><span data-stu-id="bb235-104">Str\_GetPtr function</span></span>

<span data-ttu-id="bb235-105">\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb235-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="bb235-106">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bb235-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="bb235-107">Copia uma cadeia de caracteres de um buffer para outro.</span><span class="sxs-lookup"><span data-stu-id="bb235-107">Copies a string from one buffer to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb235-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb235-108">Syntax</span></span>


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a><span data-ttu-id="bb235-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb235-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb235-110">*pszSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bb235-110">*pszSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb235-111">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bb235-111">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bb235-112">Um ponteiro para uma cadeia de caracteres de origem.</span><span class="sxs-lookup"><span data-stu-id="bb235-112">A pointer to a source string.</span></span>

</dd> <dt>

<span data-ttu-id="bb235-113">*pszDest* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="bb235-113">*pszDest* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb235-114">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bb235-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bb235-115">Um ponteiro para o buffer de destino.</span><span class="sxs-lookup"><span data-stu-id="bb235-115">A pointer to the destination buffer.</span></span> <span data-ttu-id="bb235-116">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bb235-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bb235-117">*cchDest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bb235-117">*cchDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb235-118">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="bb235-118">Type: **int**</span></span>

<span data-ttu-id="bb235-119">O tamanho de *pszDest*, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="bb235-119">The size of *pszDest*, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb235-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb235-120">Return value</span></span>

<span data-ttu-id="bb235-121">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="bb235-121">Type: **int**</span></span>

<span data-ttu-id="bb235-122">Se *pszDest* for **nulo** ou *cchDest* for zero, retornará o tamanho do buffer, em caracteres, necessário para conter uma cópia terminada em nulo da cadeia de caracteres apontada por *pszSource*.</span><span class="sxs-lookup"><span data-stu-id="bb235-122">If *pszDest* is **NULL** or *cchDest* is zero, returns the size of the buffer, in characters, needed to contain a null-terminated copy of the string pointed to by *pszSource*.</span></span>

<span data-ttu-id="bb235-123">Se *pszDest* for não **nulo**, retornará o número de caracteres copiados com êxito, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="bb235-123">If *pszDest* is non-**NULL**, returns the number of characters successfully copied, including the terminating null character.</span></span>

<span data-ttu-id="bb235-124">Se *pszDest* não puder conter a cadeia de caracteres inteira apontada por *pszSource*, os caracteres (*cchDest*-1) serão copiados, a cadeia de caracteres com terminação nula e *cchDest* retornado.</span><span class="sxs-lookup"><span data-stu-id="bb235-124">If *pszDest* cannot hold the entire string pointed to by *pszSource*, then (*cchDest*-1) characters are copied, the string null-terminated, and *cchDest* returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb235-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb235-125">Remarks</span></span>

<span data-ttu-id="bb235-126">**Str \_ GetPtr** está disponível como ANSI (**Str \_ GetPtrA**) e versões Unicode (**Str \_ GetPtrW**).</span><span class="sxs-lookup"><span data-stu-id="bb235-126">**Str\_GetPtr** is available as ANSI (**Str\_GetPtrA**) and Unicode (**Str\_GetPtrW**) versions.</span></span> <span data-ttu-id="bb235-127">Essas funções não são exportadas por nome ou declaradas em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="bb235-127">These functions are not exported by name or declared in a public header file.</span></span> <span data-ttu-id="bb235-128">Para usá-los, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 233 (**Str \_ GetPtrA**) ou 235 (**Str \_ GetPtrW**) de ComCtl32.dll para obter um ponteiro de função.</span><span class="sxs-lookup"><span data-stu-id="bb235-128">To use them, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 233 (**Str\_GetPtrA**) or 235 (**Str\_GetPtrW**) from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb235-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb235-129">Requirements</span></span>



| <span data-ttu-id="bb235-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb235-130">Requirement</span></span> | <span data-ttu-id="bb235-131">Valor</span><span class="sxs-lookup"><span data-stu-id="bb235-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb235-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb235-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bb235-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb235-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bb235-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb235-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bb235-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb235-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb235-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bb235-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb235-137"><dt>ComCtl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb235-137"><dt>ComCtl32.dll</dt></span></span> </dl> |
| <span data-ttu-id="bb235-138">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bb235-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bb235-139">**Str \_ GetPtrW** (Unicode) e **\_ GetPtrA de Str** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bb235-139">**Str\_GetPtrW** (Unicode) and **Str\_GetPtrA** (ANSI)</span></span><br/>                       |



 

