---
title: Função DrawTextExPrivWrap
description: Desenha texto formatado no retângulo especificado. Essa função encapsula uma chamada para DrawTextEx.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- Controles do Windows da função DrawTextExPrivWrap
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919170"
---
# <a name="drawtextexprivwrap-function"></a><span data-ttu-id="cbb34-105">Função DrawTextExPrivWrap</span><span class="sxs-lookup"><span data-stu-id="cbb34-105">DrawTextExPrivWrap function</span></span>

<span data-ttu-id="cbb34-106">\[O **DrawTextExPrivWrap** está disponível por meio do Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="cbb34-106">\[**DrawTextExPrivWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="cbb34-107">Ele pode ser alterado ou indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="cbb34-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="cbb34-108">Em vez disso, é recomendável usar o [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="cbb34-108">It is recommended to use [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) directly instead.\]</span></span>

<span data-ttu-id="cbb34-109">Desenha texto formatado no retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="cbb34-109">Draws formatted text in the specified rectangle.</span></span> <span data-ttu-id="cbb34-110">Essa função encapsula uma chamada para [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span><span class="sxs-lookup"><span data-stu-id="cbb34-110">This function wraps a call to [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="cbb34-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbb34-111">Syntax</span></span>


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a><span data-ttu-id="cbb34-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbb34-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbb34-113">*HDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cbb34-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb34-114">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cbb34-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cbb34-115">Um identificador para o contexto do dispositivo no qual desenhar.</span><span class="sxs-lookup"><span data-stu-id="cbb34-115">A handle to the device context in which to draw.</span></span>

</dd> <dt>

<span data-ttu-id="cbb34-116">*lpchText* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="cbb34-116">*lpchText* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb34-117">Tipo: **[ **LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cbb34-117">Type: **[**LPTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cbb34-118">Um ponteiro para um buffer que contém o texto a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="cbb34-118">A pointer to a buffer that contains the text to draw.</span></span> <span data-ttu-id="cbb34-119">Se o parâmetro *cchText* for-1, a cadeia de caracteres deverá ser terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="cbb34-119">If the *cchText* parameter is -1, the string must be null-terminated.</span></span>

<span data-ttu-id="cbb34-120">Se *dwDTFormat* incluir \_ o DT modifystring, a função poderá adicionar até quatro caracteres adicionais a essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cbb34-120">If *dwDTFormat* includes DT\_MODIFYSTRING, the function might add up to four additional characters to this string.</span></span> <span data-ttu-id="cbb34-121">O buffer que contém a cadeia de caracteres deve ser grande o suficiente para acomodar esses caracteres extras.</span><span class="sxs-lookup"><span data-stu-id="cbb34-121">The buffer that contains the string should be large enough to accommodate these extra characters.</span></span>

</dd> <dt>

<span data-ttu-id="cbb34-122">*cchText* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cbb34-122">*cchText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb34-123">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="cbb34-123">Type: **int**</span></span>

<span data-ttu-id="cbb34-124">O comprimento da cadeia de caracteres apontada por *lpchText*.</span><span class="sxs-lookup"><span data-stu-id="cbb34-124">The length of the string pointed to by *lpchText*.</span></span> <span data-ttu-id="cbb34-125">Se *cchText* for-1, o parâmetro *lpchText* será considerado um ponteiro para uma cadeia de caracteres terminada em nulo e [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) calculará automaticamente a contagem de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cbb34-125">If *cchText* is -1, then the *lpchText* parameter is assumed to be a pointer to a null-terminated string and [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="cbb34-126">*lprc* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="cbb34-126">*lprc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb34-127">Tipo: **lpRect**</span><span class="sxs-lookup"><span data-stu-id="cbb34-127">Type: **LPRECT**</span></span>

<span data-ttu-id="cbb34-128">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém o retângulo, em coordenadas lógicas, em que o texto deve ser formatado.</span><span class="sxs-lookup"><span data-stu-id="cbb34-128">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span>

</dd> <dt>

<span data-ttu-id="cbb34-129">*dwDTFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cbb34-129">*dwDTFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb34-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cbb34-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cbb34-131">As opções de formatação.</span><span class="sxs-lookup"><span data-stu-id="cbb34-131">The formatting options.</span></span> <span data-ttu-id="cbb34-132">Consulte a documentação do [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) para obter uma lista completa de opções.</span><span class="sxs-lookup"><span data-stu-id="cbb34-132">See the documentation for [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="cbb34-133">*lpDTParams* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cbb34-133">*lpDTParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb34-134">Tipo: **LPDRAWTEXTPARAMS**</span><span class="sxs-lookup"><span data-stu-id="cbb34-134">Type: **LPDRAWTEXTPARAMS**</span></span>

<span data-ttu-id="cbb34-135">Um ponteiro para uma estrutura [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) que especifica opções de formatação adicionais.</span><span class="sxs-lookup"><span data-stu-id="cbb34-135">A pointer to a [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) structure that specifies additional formatting options.</span></span> <span data-ttu-id="cbb34-136">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cbb34-136">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbb34-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbb34-137">Return value</span></span>

<span data-ttu-id="cbb34-138">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="cbb34-138">Type: **int**</span></span>

<span data-ttu-id="cbb34-139">Se a função for realizada com sucesso, o valor de retorno será a altura do texto em unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="cbb34-139">If the function succeeds, the return value is the text height in logical units.</span></span> <span data-ttu-id="cbb34-140">Se a **\_ parte inferior** de **dt \_ VCENTER** ou DT for especificada, o valor de retorno será o deslocamento do membro **superior** de *lprc* para a parte inferior do texto desenhado.</span><span class="sxs-lookup"><span data-stu-id="cbb34-140">If **DT\_VCENTER** or **DT\_BOTTOM** is specified, the return value is the offset from the **top** member of *lprc* to the bottom of the drawn text.</span></span>

<span data-ttu-id="cbb34-141">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="cbb34-141">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="cbb34-142">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="cbb34-142">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="cbb34-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbb34-143">Remarks</span></span>

<span data-ttu-id="cbb34-144">**DrawTextExPrivWrap** não é exportado pelo nome ou declarado em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="cbb34-144">**DrawTextExPrivWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="cbb34-145">Para usá-lo, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 416 de ComCtl32.dll para obter um ponteiro de função.</span><span class="sxs-lookup"><span data-stu-id="cbb34-145">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 416 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="cbb34-146">Para comentários adicionais, consulte [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span><span class="sxs-lookup"><span data-stu-id="cbb34-146">For additional remarks, please see [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbb34-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbb34-147">Requirements</span></span>



| <span data-ttu-id="cbb34-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbb34-148">Requirement</span></span> | <span data-ttu-id="cbb34-149">Valor</span><span class="sxs-lookup"><span data-stu-id="cbb34-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb34-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbb34-150">Minimum supported client</span></span><br/> | <span data-ttu-id="cbb34-151">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbb34-151">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="cbb34-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbb34-152">Minimum supported server</span></span><br/> | <span data-ttu-id="cbb34-153">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cbb34-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cbb34-154">DLL</span><span class="sxs-lookup"><span data-stu-id="cbb34-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbb34-155"><dt>Comctl32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="cbb34-155"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

