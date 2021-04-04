---
title: Função ExtTextOutWrap
description: Desenha o texto usando a fonte, a cor do plano de fundo e a cor do texto selecionados no momento. Opcionalmente, você pode fornecer dimensões a serem usadas para recorte, opacidade ou ambos. Essa função encapsula uma chamada para ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- Controles do Windows da função ExtTextOutWrap
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085212"
---
# <a name="exttextoutwrap-function"></a><span data-ttu-id="d8bb6-106">Função ExtTextOutWrap</span><span class="sxs-lookup"><span data-stu-id="d8bb6-106">ExtTextOutWrap function</span></span>

<span data-ttu-id="d8bb6-107">\[O **ExtTextOutWrap** está disponível por meio do Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="d8bb6-107">\[**ExtTextOutWrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="d8bb6-108">Ele pode ser alterado ou indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-108">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d8bb6-109">Em vez disso, é recomendável usar o [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="d8bb6-109">It is recommended to use [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) directly instead.\]</span></span>

<span data-ttu-id="d8bb6-110">Desenha o texto usando a fonte, a cor do plano de fundo e a cor do texto selecionados no momento.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-110">Draws text using the currently selected font, background color, and text color.</span></span> <span data-ttu-id="d8bb6-111">Opcionalmente, você pode fornecer dimensões a serem usadas para recorte, opacidade ou ambos.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-111">You can optionally provide dimensions to be used for clipping, opacity, or both.</span></span> <span data-ttu-id="d8bb6-112">Essa função encapsula uma chamada para [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span><span class="sxs-lookup"><span data-stu-id="d8bb6-112">This function wraps a call to [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8bb6-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8bb6-113">Syntax</span></span>


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a><span data-ttu-id="d8bb6-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8bb6-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8bb6-115">*HDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8bb6-115">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bb6-116">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8bb6-116">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8bb6-117">Um identificador para o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-117">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="d8bb6-118">*X* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d8bb6-118">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bb6-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="d8bb6-119">Type: **int**</span></span>

<span data-ttu-id="d8bb6-120">A coordenada x, em coordenadas lógicas, do ponto de referência usado para posicionar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-120">The x-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="d8bb6-121">*Y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d8bb6-121">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bb6-122">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="d8bb6-122">Type: **int**</span></span>

<span data-ttu-id="d8bb6-123">A coordenada y, em coordenadas lógicas, do ponto de referência usado para posicionar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-123">The y-coordinate, in logical coordinates, of the reference point used to position the string.</span></span>

</dd> <dt>

<span data-ttu-id="d8bb6-124">*uOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8bb6-124">*uOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bb6-125">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8bb6-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8bb6-126">Valores que especificam como usar o retângulo definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-126">Values that specify how to use the application-defined rectangle.</span></span> <span data-ttu-id="d8bb6-127">Consulte [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) para obter uma lista completa de opções.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-127">See [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) for a complete list of options.</span></span>

</dd> <dt>

<span data-ttu-id="d8bb6-128">*lprc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8bb6-128">*lprc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bb6-129">Tipo: \**const [**Rect**](/previous-versions//dd162897(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="d8bb6-129">Type: \**const [**RECT**](/previous-versions//dd162897(v=vs.85))\** _</span></span>

<span data-ttu-id="d8bb6-130">Um ponteiro para uma estrutura opcional [_ *Rect* \*](/previous-versions//dd162897(v=vs.85)) que especifica as dimensões, em coordenadas lógicas, de um retângulo usado para recorte, opacidade ou ambos.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-130">A pointer to an optional [_ *RECT*\*](/previous-versions//dd162897(v=vs.85)) structure that specifies the dimensions, in logical coordinates, of a rectangle that is used for clipping, opacity, or both.</span></span>

</dd> <dt>

<span data-ttu-id="d8bb6-131">*LPSTR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8bb6-131">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bb6-132">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8bb6-132">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8bb6-133">Um ponteiro para um buffer que contém o texto a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-133">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="d8bb6-134">A cadeia de caracteres não precisa terminar com zero, pois *cbCount* especifica o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-134">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="d8bb6-135">*cbCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8bb6-135">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bb6-136">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8bb6-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8bb6-137">O comprimento da cadeia de caracteres, em bytes, apontado por *LPSTR*.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-137">The length of the string, in bytes, pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="d8bb6-138">*lpDx* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8bb6-138">*lpDx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bb6-139">Tipo: \**const [**int**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="d8bb6-139">Type: \**const [**INT**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="d8bb6-140">Um ponteiro para uma matriz opcional de valores que indicam a distância entre as origens das células de caracteres adjacentes.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-140">A pointer to an optional array of values that indicate the distance between origins of adjacent character cells.</span></span> <span data-ttu-id="d8bb6-141">Por exemplo, _lpDx \[ unidades lógicas \* x separam \] as origens da célula de caractere x e da célula de caractere (x + 1).</span><span class="sxs-lookup"><span data-stu-id="d8bb6-141">For example, _lpDx\*\[x\] logical units separate the origins of character cell x and character cell (x + 1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8bb6-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8bb6-142">Return value</span></span>

<span data-ttu-id="d8bb6-143">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d8bb6-143">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d8bb6-144">Retorna um valor diferente de zero se a cadeia de caracteres é desenhada com êxito.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-144">Returns a nonzero value if the string is drawn successfully.</span></span> <span data-ttu-id="d8bb6-145">No entanto, se a versão ANSI de [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) for chamada com o \_ índice de glifo Eto \_ , a função retornará **true** mesmo que a função não faça nada.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-145">However, if the ANSI version of [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) is called with ETO\_GLYPH\_INDEX, the function returns **TRUE** even though the function does nothing.</span></span>

<span data-ttu-id="d8bb6-146">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-146">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="d8bb6-147">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="d8bb6-147">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8bb6-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8bb6-148">Remarks</span></span>

<span data-ttu-id="d8bb6-149">**ExtTextOutWrap** não é exportado pelo nome ou declarado em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-149">**ExtTextOutWrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="d8bb6-150">Para usá-lo, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 417 de ComCtl32.dll para obter um ponteiro de função.</span><span class="sxs-lookup"><span data-stu-id="d8bb6-150">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 417 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="d8bb6-151">Para comentários adicionais, consulte [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span><span class="sxs-lookup"><span data-stu-id="d8bb6-151">For additional remarks, please see [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8bb6-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8bb6-152">Requirements</span></span>



| <span data-ttu-id="d8bb6-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8bb6-153">Requirement</span></span> | <span data-ttu-id="d8bb6-154">Valor</span><span class="sxs-lookup"><span data-stu-id="d8bb6-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8bb6-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8bb6-155">Minimum supported client</span></span><br/> | <span data-ttu-id="d8bb6-156">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8bb6-156">Windows Vista \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="d8bb6-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8bb6-157">Minimum supported server</span></span><br/> | <span data-ttu-id="d8bb6-158">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8bb6-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d8bb6-159">DLL</span><span class="sxs-lookup"><span data-stu-id="d8bb6-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8bb6-160"><dt>Comctl32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d8bb6-160"><dt>Comctl32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

