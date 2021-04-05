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
ms.openlocfilehash: f7b7cc278d1d5a2305b3d2a311ce9c82886f9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918925"
---
# <a name="cdm_getfilepath-message"></a><span data-ttu-id="598ae-104">\_Mensagem GETFILEPATH CDM</span><span class="sxs-lookup"><span data-stu-id="598ae-104">CDM\_GETFILEPATH message</span></span>

<span data-ttu-id="598ae-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="598ae-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="598ae-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="598ae-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="598ae-107">Recupera o caminho e o nome de arquivo do arquivo selecionado em uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** .</span><span class="sxs-lookup"><span data-stu-id="598ae-107">Retrieves the path and file name of the selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="598ae-108">A caixa de diálogo deve ter sido criada com o sinalizador **OFN \_ Explorer** ; caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="598ae-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a><span data-ttu-id="598ae-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="598ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="598ae-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="598ae-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="598ae-111">O tamanho, em caracteres, do buffer de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="598ae-111">The size, in characters, of the *lParam* buffer.</span></span> <span data-ttu-id="598ae-112">Para a versão ANSI, este é o número de bytes; para a versão Unicode, este é o número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="598ae-112">For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="598ae-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="598ae-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="598ae-114">Um ponteiro para o buffer que recebe o nome do arquivo e o caminho.</span><span class="sxs-lookup"><span data-stu-id="598ae-114">A pointer to the buffer that receives the file name and path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="598ae-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="598ae-115">Return value</span></span>

<span data-ttu-id="598ae-116">Se a mensagem tiver sucesso, o valor de retorno será o tamanho, em caracteres, do nome do arquivo e da cadeia de caracteres do caminho, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="598ae-116">If the message succeeds, the return value is the size, in characters, of the file name and path string, including the terminating NULL character.</span></span> <span data-ttu-id="598ae-117">Esse é o número de bytes ou caracteres copiados para o buffer ou o tamanho de buffer necessário se o buffer for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="598ae-117">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="598ae-118">Se ocorrer um erro, o valor de retorno será menor que zero.</span><span class="sxs-lookup"><span data-stu-id="598ae-118">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="598ae-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="598ae-119">Remarks</span></span>

<span data-ttu-id="598ae-120">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="598ae-120">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="598ae-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="598ae-121">Requirements</span></span>



| <span data-ttu-id="598ae-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="598ae-122">Requirement</span></span> | <span data-ttu-id="598ae-123">Valor</span><span class="sxs-lookup"><span data-stu-id="598ae-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="598ae-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="598ae-124">Minimum supported client</span></span><br/> | <span data-ttu-id="598ae-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="598ae-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="598ae-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="598ae-126">Minimum supported server</span></span><br/> | <span data-ttu-id="598ae-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="598ae-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="598ae-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="598ae-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="598ae-129"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="598ae-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="598ae-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="598ae-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="598ae-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="598ae-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="598ae-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="598ae-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="598ae-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="598ae-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="598ae-134">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="598ae-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="598ae-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="598ae-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="598ae-136">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="598ae-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

