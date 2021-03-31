---
title: Função GetTextExtentPoint32Wrap
description: Computa a largura e a altura da cadeia de caracteres especificada de texto. Essa função encapsula uma chamada para GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- Controles do Windows da função GetTextExtentPoint32Wrap
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644302"
---
# <a name="gettextextentpoint32wrap-function"></a><span data-ttu-id="303a7-105">Função GetTextExtentPoint32Wrap</span><span class="sxs-lookup"><span data-stu-id="303a7-105">GetTextExtentPoint32Wrap function</span></span>

<span data-ttu-id="303a7-106">\[O **GetTextExtentPoint32Wrap** está disponível por meio do Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="303a7-106">\[**GetTextExtentPoint32Wrap** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="303a7-107">Ele pode ser alterado ou indisponível nas versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="303a7-107">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="303a7-108">Em vez disso, é recomendável usar o [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="303a7-108">It is recommended to use [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) directly instead.\]</span></span>

<span data-ttu-id="303a7-109">Computa a largura e a altura da cadeia de caracteres especificada de texto.</span><span class="sxs-lookup"><span data-stu-id="303a7-109">Computes the width and height of the specified string of text.</span></span> <span data-ttu-id="303a7-110">Essa função encapsula uma chamada para [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="303a7-110">This function wraps a call to [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="syntax"></a><span data-ttu-id="303a7-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="303a7-111">Syntax</span></span>


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a><span data-ttu-id="303a7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="303a7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="303a7-113">*HDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="303a7-113">*hdc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="303a7-114">Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="303a7-114">Type: **[**HDC**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="303a7-115">Um identificador para o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="303a7-115">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="303a7-116">*LPSTR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="303a7-116">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="303a7-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="303a7-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="303a7-118">Um ponteiro para um buffer que contém o texto a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="303a7-118">A pointer to a buffer that contains the text to be drawn.</span></span> <span data-ttu-id="303a7-119">A cadeia de caracteres não precisa terminar com zero, pois *cbCount* especifica o comprimento da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="303a7-119">The string does not need to be zero-terminated, since *cbCount* specifies the length of the string.</span></span>

</dd> <dt>

<span data-ttu-id="303a7-120">*cbCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="303a7-120">*cbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="303a7-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="303a7-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="303a7-122">O comprimento, em bytes, da cadeia de caracteres apontada por *lpString*.</span><span class="sxs-lookup"><span data-stu-id="303a7-122">The length, in bytes, of the string pointed to by *lpString*.</span></span>

</dd> <dt>

<span data-ttu-id="303a7-123">*lpSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="303a7-123">*lpSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="303a7-124">Tipo: **LPSIZE**</span><span class="sxs-lookup"><span data-stu-id="303a7-124">Type: **LPSIZE**</span></span>

<span data-ttu-id="303a7-125">Quando esse método retorna, contém um ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) que contém as dimensões da cadeia de caracteres, em unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="303a7-125">When this method returns, contains a pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure containing the dimensions of the string, in logical units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="303a7-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="303a7-126">Return value</span></span>

<span data-ttu-id="303a7-127">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="303a7-127">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="303a7-128">Retorna um valor diferente de zero se for bem-sucedido; caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="303a7-128">Returns a nonzero value if successful; otherwise, 0.</span></span>

<span data-ttu-id="303a7-129">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="303a7-129">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="303a7-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="303a7-130">Remarks</span></span>

<span data-ttu-id="303a7-131">**GetTextExtentPoint32Wrap** não é exportado pelo nome ou declarado em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="303a7-131">**GetTextExtentPoint32Wrap** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="303a7-132">Para usá-lo, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 420 de ComCtl32.dll para obter um ponteiro de função.</span><span class="sxs-lookup"><span data-stu-id="303a7-132">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 420 from ComCtl32.dll to obtain a function pointer.</span></span>

<span data-ttu-id="303a7-133">Para comentários adicionais, consulte [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span><span class="sxs-lookup"><span data-stu-id="303a7-133">For additional remarks, please see [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).</span></span>

## <a name="requirements"></a><span data-ttu-id="303a7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="303a7-134">Requirements</span></span>



| <span data-ttu-id="303a7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="303a7-135">Requirement</span></span> | <span data-ttu-id="303a7-136">Valor</span><span class="sxs-lookup"><span data-stu-id="303a7-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="303a7-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="303a7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="303a7-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="303a7-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="303a7-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="303a7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="303a7-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="303a7-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="303a7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="303a7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="303a7-142"><dt>Comctl32.dll (versão 5,81 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="303a7-142"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

