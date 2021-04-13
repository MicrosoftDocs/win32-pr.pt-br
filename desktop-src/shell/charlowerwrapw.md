---
description: Converte uma cadeia de caracteres Unicode ou um único caractere em minúsculas.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: Função CharLowerWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501438"
---
# <a name="charlowerwrapw-function"></a><span data-ttu-id="c943a-103">Função CharLowerWrapW</span><span class="sxs-lookup"><span data-stu-id="c943a-103">CharLowerWrapW function</span></span>

<span data-ttu-id="c943a-104">\[O **CharLowerWrapW** está disponível para uso no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c943a-104">\[**CharLowerWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="c943a-105">Ele pode não estar disponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c943a-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="c943a-106">Você deve usar [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) em seu lugar.\]</span><span class="sxs-lookup"><span data-stu-id="c943a-106">You should use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in its place.\]</span></span>

<span data-ttu-id="c943a-107">Converte uma cadeia de caracteres Unicode ou um único caractere em minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c943a-107">Converts a Unicode character string or a single character to lowercase.</span></span> <span data-ttu-id="c943a-108">Se o operando for uma cadeia de caracteres, a função converterá os caracteres em vigor.</span><span class="sxs-lookup"><span data-stu-id="c943a-108">If the operand is a character string, the function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="c943a-109">**CharLowerWrapW** é um wrapper para a função **CharLowerW** .</span><span class="sxs-lookup"><span data-stu-id="c943a-109">**CharLowerWrapW** is a wrapper for the **CharLowerW** function.</span></span> <span data-ttu-id="c943a-110">Consulte a página [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) para ver mais observações de uso.</span><span class="sxs-lookup"><span data-stu-id="c943a-110">See the [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c943a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c943a-111">Syntax</span></span>


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a><span data-ttu-id="c943a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c943a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c943a-113">*PCH* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c943a-113">*pch* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c943a-114">Tipo: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c943a-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="c943a-115">Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo ou um único caractere.</span><span class="sxs-lookup"><span data-stu-id="c943a-115">A pointer to a null-terminated Unicode string or a single character.</span></span> <span data-ttu-id="c943a-116">Se a palavra de ordem superior desse parâmetro for zero, a palavra de ordem inferior deverá conter apenas um único caractere a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="c943a-116">If the high-order word of this parameter is zero, the low-order word must contain only a single character to be converted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c943a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c943a-117">Return value</span></span>

<span data-ttu-id="c943a-118">Tipo: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="c943a-118">Type: **LPWSTR**</span></span>

<span data-ttu-id="c943a-119">Se *PCH* for uma cadeia de caracteres, a função retornará um ponteiro para a cadeia de caracteres convertida.</span><span class="sxs-lookup"><span data-stu-id="c943a-119">If *pch* is a character string, the function returns a pointer to the converted string.</span></span> <span data-ttu-id="c943a-120">Como a cadeia de caracteres é convertida em vigor, o valor de retorno é igual a *PCH*.</span><span class="sxs-lookup"><span data-stu-id="c943a-120">Since the string is converted in place, the return value is equal to *pch*.</span></span>

<span data-ttu-id="c943a-121">Se *PCH* for um único caractere, o valor de retorno será um valor de 32 bits cuja palavra de ordem superior é zero e a palavra de ordem inferior conterá o caractere convertido.</span><span class="sxs-lookup"><span data-stu-id="c943a-121">If *pch* is a single character, the return value is a 32-bit value whose high-order word is zero, and low-order word contains the converted character.</span></span>

<span data-ttu-id="c943a-122">Não há nenhuma indicação de êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="c943a-122">There is no indication of success or failure.</span></span> <span data-ttu-id="c943a-123">A falha é rara.</span><span class="sxs-lookup"><span data-stu-id="c943a-123">Failure is rare.</span></span> <span data-ttu-id="c943a-124">Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="c943a-124">There is no extended error information for this function; do not call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="c943a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c943a-125">Remarks</span></span>

<span data-ttu-id="c943a-126">O método preferencial é usar [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) em conjunto com a camada Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="c943a-126">The preferred method is to use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="c943a-127">**CharLowerWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 38.</span><span class="sxs-lookup"><span data-stu-id="c943a-127">**CharLowerWrapW** must be called directly from Shlwapi.dll, using ordinal 38.</span></span>

## <a name="requirements"></a><span data-ttu-id="c943a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c943a-128">Requirements</span></span>



| <span data-ttu-id="c943a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c943a-129">Requirement</span></span> | <span data-ttu-id="c943a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="c943a-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c943a-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c943a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c943a-132">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c943a-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c943a-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c943a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c943a-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c943a-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c943a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c943a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c943a-136"><dt>Shlwapi.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c943a-136"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c943a-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c943a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c943a-138">**CharLower**</span><span class="sxs-lookup"><span data-stu-id="c943a-138">**CharLower**</span></span>](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
