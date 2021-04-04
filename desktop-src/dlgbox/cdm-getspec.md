---
title: Mensagem de CDM_GETSPEC (Commdlg. h)
description: Recupera o nome do arquivo (não incluindo o caminho) do arquivo selecionado no momento em uma caixa de diálogo abrir no estilo do Explorer ou salvar como.
ms.assetid: 22a67c92-bd24-4cba-bef8-291d241e6ec8
keywords:
- Caixas de diálogo de CDM_GETSPEC mensagem
topic_type:
- apiref
api_name:
- CDM_GETSPEC
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2732bf2a8c581439a40538445853531b57cfc77a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085113"
---
# <a name="cdm_getspec-message"></a><span data-ttu-id="99c80-104">CDM \_ GETspec</span><span class="sxs-lookup"><span data-stu-id="99c80-104">CDM\_GETSPEC message</span></span>

<span data-ttu-id="99c80-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="99c80-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="99c80-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="99c80-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="99c80-107">Recupera o nome do arquivo (não incluindo o caminho) do arquivo selecionado no momento em uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** .</span><span class="sxs-lookup"><span data-stu-id="99c80-107">Retrieves the file name (not including the path) of the currently selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="99c80-108">A caixa de diálogo deve ter sido criada com o sinalizador **OFN \_ Explorer** ; caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="99c80-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="99c80-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99c80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99c80-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99c80-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99c80-111">O tamanho, em caracteres, do buffer de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="99c80-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="99c80-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99c80-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99c80-113">Um ponteiro para o buffer que recebe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="99c80-113">A pointer to the buffer that receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99c80-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99c80-114">Return value</span></span>

<span data-ttu-id="99c80-115">Se a mensagem tiver sucesso, o valor de retorno será o tamanho, em caracteres, da cadeia de caracteres de nome de arquivo, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="99c80-115">If the message succeeds, the return value is the size, in characters, of the file name string, including the terminating NULL character.</span></span> <span data-ttu-id="99c80-116">Esse é o número de bytes ou caracteres copiados para o buffer ou o tamanho de buffer necessário se o buffer for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="99c80-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="99c80-117">Se ocorrer um erro, o valor de retorno será menor que zero.</span><span class="sxs-lookup"><span data-stu-id="99c80-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="99c80-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="99c80-118">Remarks</span></span>

<span data-ttu-id="99c80-119">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="99c80-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="99c80-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99c80-120">Requirements</span></span>



| <span data-ttu-id="99c80-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="99c80-121">Requirement</span></span> | <span data-ttu-id="99c80-122">Valor</span><span class="sxs-lookup"><span data-stu-id="99c80-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c80-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99c80-123">Minimum supported client</span></span><br/> | <span data-ttu-id="99c80-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99c80-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="99c80-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99c80-125">Minimum supported server</span></span><br/> | <span data-ttu-id="99c80-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99c80-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99c80-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99c80-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="99c80-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99c80-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99c80-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="99c80-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="99c80-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="99c80-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="99c80-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="99c80-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="99c80-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="99c80-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="99c80-133">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="99c80-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="99c80-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="99c80-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="99c80-135">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="99c80-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

