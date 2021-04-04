---
title: Função DrawTextWrap
description: Desenha texto formatado no retângulo especificado. Ele formata o texto de acordo com o método especificado (expandindo guias, justificando caracteres, quebrando linhas e assim por diante). Essa função encapsula uma chamada para DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- Controles do Windows da função DrawTextWrap
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918040"
---
# <a name="drawtextwrap-function"></a><span data-ttu-id="45c8d-106">Função DrawTextWrap</span><span class="sxs-lookup"><span data-stu-id="45c8d-106">DrawTextWrap function</span></span>

<span data-ttu-id="45c8d-107">\[O **DrawTextWrap** está disponível por meio do Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="45c8d-107">\[**DrawTextWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="45c8d-108">Ele pode ser alterado ou indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="45c8d-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="45c8d-109">É recomendável usar o [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) diretamente em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="45c8d-109">It is recommended to use [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) directly instead.\]</span></span>

<span data-ttu-id="45c8d-110">Desenha texto formatado no retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="45c8d-110">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="45c8d-111">Ele formata o texto de acordo com o método especificado (expandindo guias, justificando caracteres, quebrando linhas e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="45c8d-111">It formats the text according to the specified method (expanding tabs, justifying characters, breaking lines, and so on).</span></span> <span data-ttu-id="45c8d-112">Essa função encapsula uma chamada para [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="45c8d-112">This function wraps a call to [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="syntax"></a><span data-ttu-id="45c8d-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45c8d-113">Syntax</span></span>


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="45c8d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45c8d-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c8d-115">*HDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45c8d-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45c8d-116">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="45c8d-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="45c8d-117">Um identificador para o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45c8d-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="45c8d-118">*LPSTR* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="45c8d-118">*lpString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="45c8d-119">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="45c8d-119">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="45c8d-120">Um ponteiro para um buffer que contém o texto a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="45c8d-120">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="45c8d-121">Se o parâmetro *nCount* for-1, a cadeia de caracteres deverá ser terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="45c8d-121">If the *nCount* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="45c8d-122">Se *uFormat* incluir \_ o DT modifystring, a função poderá adicionar até quatro caracteres adicionais a essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="45c8d-122">If *uFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="45c8d-123">O buffer que contém a cadeia de caracteres deve ser grande o suficiente para acomodar esses caracteres extras.</span><span class="sxs-lookup"><span data-stu-id="45c8d-123">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="45c8d-124">*nCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45c8d-124">*nCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45c8d-125">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="45c8d-125">Type: **int**</span></span>

<span data-ttu-id="45c8d-126">O comprimento da cadeia de caracteres apontada por *lpString*.</span><span class="sxs-lookup"><span data-stu-id="45c8d-126">The length of the string pointed to by *lpString*.</span></span> <span data-ttu-id="45c8d-127">Se *nCount* for-1, o parâmetro *LPSTR* será considerado como um ponteiro para uma cadeia de caracteres terminada em nulo e o [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) calculará automaticamente a contagem de caracteres.</span><span class="sxs-lookup"><span data-stu-id="45c8d-127">If *nCount* is -1, then the *lpString* parameter is assumed to be a pointer to a null-terminated string and [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="45c8d-128">*lpRect* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="45c8d-128">*lpRect* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="45c8d-129">Tipo: **lpRect**</span><span class="sxs-lookup"><span data-stu-id="45c8d-129">Type: **LPRECT**</span></span>

<span data-ttu-id="45c8d-130">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém o retângulo, em coordenadas lógicas, em que o texto deve ser formatado.</span><span class="sxs-lookup"><span data-stu-id="45c8d-130">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="45c8d-131">*uFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45c8d-131">*uFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45c8d-132">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="45c8d-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="45c8d-133">As opções de formatação.</span><span class="sxs-lookup"><span data-stu-id="45c8d-133">The formatting options.</span></span> <span data-ttu-id="45c8d-134">Consulte a documentação do [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) para obter uma lista completa de opções.</span><span class="sxs-lookup"><span data-stu-id="45c8d-134">See the documentation for [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="45c8d-135">*lpDTParams* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45c8d-135">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45c8d-136">Tipo: **LPDRAWTEXTPARAMS**</span><span class="sxs-lookup"><span data-stu-id="45c8d-136">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="45c8d-137">Um ponteiro para uma estrutura [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) que especifica opções de formatação adicionais.</span><span class="sxs-lookup"><span data-stu-id="45c8d-137">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="45c8d-138">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="45c8d-138">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45c8d-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45c8d-139">Return value</span></span>

<span data-ttu-id="45c8d-140">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="45c8d-140">Type: **int**</span></span>

<span data-ttu-id="45c8d-141">Se a função for realizada com sucesso, o valor de retorno será a altura do texto em unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="45c8d-141">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="45c8d-142">Se a **\_ parte inferior** de **dt \_ VCENTER** ou DT for especificada, o valor de retorno será o deslocamento do membro **superior** de *lprc* para a parte inferior do texto desenhado se a função falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="45c8d-142">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text If the function fails, the return value is zero.</span></span>

<span data-ttu-id="45c8d-143">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="45c8d-143">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="45c8d-144">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="45c8d-144">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="45c8d-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="45c8d-145">Remarks</span></span>

<span data-ttu-id="45c8d-146">**DrawTextWrap** não é exportado pelo nome ou declarado em um cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="45c8d-146">**DrawTextWrap** is not exported by name or declared in a public header.</span></span> <span data-ttu-id="45c8d-147">Para usá-lo, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 415 de ComCtl32.dll para obter um ponteiro de função.</span><span class="sxs-lookup"><span data-stu-id="45c8d-147">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 415 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="45c8d-148">Para comentários adicionais, consulte [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="45c8d-148">For additional remarks, please see [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).</span></span>

## <a name="requirements"></a><span data-ttu-id="45c8d-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45c8d-149">Requirements</span></span>



| <span data-ttu-id="45c8d-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="45c8d-150">Requirement</span></span> | <span data-ttu-id="45c8d-151">Valor</span><span class="sxs-lookup"><span data-stu-id="45c8d-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45c8d-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45c8d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="45c8d-153">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45c8d-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="45c8d-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45c8d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="45c8d-155">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="45c8d-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="45c8d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="45c8d-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45c8d-157"><dt>Comctl32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="45c8d-157"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

