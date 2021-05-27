---
title: Mensagem de CDM_GETFILEPATH (Commdlg. h)
description: Recupera o caminho e o nome de arquivo do arquivo selecionado em uma caixa de diálogo abrir no estilo do Explorer ou salvar como.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- Caixas de diálogo de CDM_GETFILEPATH mensagem
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d531999757d46e127b73584adf1b563e64ea25b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548661"
---
# <a name="cdm_getfilepath-message"></a><span data-ttu-id="017d4-104">\_Mensagem GETFILEPATH CDM</span><span class="sxs-lookup"><span data-stu-id="017d4-104">CDM\_GETFILEPATH message</span></span>

<span data-ttu-id="017d4-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="017d4-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="017d4-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="017d4-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="017d4-107">Recupera o caminho e o nome de arquivo do arquivo selecionado em uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** .</span><span class="sxs-lookup"><span data-stu-id="017d4-107">Retrieves the path and file name of the selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="017d4-108">A caixa de diálogo deve ter sido criada com o sinalizador **OFN \_ Explorer** ; caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="017d4-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a><span data-ttu-id="017d4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="017d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="017d4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="017d4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="017d4-111">O tamanho, em caracteres, do buffer de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="017d4-111">The size, in characters, of the *lParam* buffer.</span></span> <span data-ttu-id="017d4-112">Para a versão ANSI, este é o número de bytes; para a versão Unicode, este é o número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="017d4-112">For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="017d4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="017d4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="017d4-114">Um ponteiro para o buffer que recebe o nome do arquivo e o caminho.</span><span class="sxs-lookup"><span data-stu-id="017d4-114">A pointer to the buffer that receives the file name and path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="017d4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="017d4-115">Return value</span></span>

<span data-ttu-id="017d4-116">Se a mensagem tiver sucesso, o valor de retorno será o tamanho, em caracteres, do nome do arquivo e da cadeia de caracteres do caminho, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="017d4-116">If the message succeeds, the return value is the size, in characters, of the file name and path string, including the terminating NULL character.</span></span> <span data-ttu-id="017d4-117">Esse é o número de bytes ou caracteres copiados para o buffer ou o tamanho de buffer necessário se o buffer for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="017d4-117">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="017d4-118">Se ocorrer um erro, o valor de retorno será menor que zero.</span><span class="sxs-lookup"><span data-stu-id="017d4-118">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="017d4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="017d4-119">Remarks</span></span>

<span data-ttu-id="017d4-120">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="017d4-120">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="017d4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="017d4-121">Requirements</span></span>



| <span data-ttu-id="017d4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="017d4-122">Requirement</span></span> | <span data-ttu-id="017d4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="017d4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="017d4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="017d4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="017d4-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="017d4-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="017d4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="017d4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="017d4-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="017d4-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="017d4-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="017d4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="017d4-129"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="017d4-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="017d4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="017d4-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="017d4-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="017d4-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="017d4-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="017d4-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="017d4-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="017d4-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="017d4-134">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="017d4-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="017d4-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="017d4-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="017d4-136">Biblioteca de caixas de diálogo comuns</span><span class="sxs-lookup"><span data-stu-id="017d4-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

