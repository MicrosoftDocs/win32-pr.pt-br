---
title: Mensagem de CDM_SETDEFEXT (Commdlg. h)
description: Define a extensão de nome de arquivo padrão para uma caixa de diálogo abrir ou salvar como no estilo do Explorer.
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- Caixas de diálogo de CDM_SETDEFEXT mensagem
topic_type:
- apiref
api_name:
- CDM_SETDEFEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bd5706e0bccf0b61c0737ef54d6e227e5593bc9
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590853"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="c2232-104">\_Mensagem CDM SETDEFEXT</span><span class="sxs-lookup"><span data-stu-id="c2232-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="c2232-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="c2232-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="c2232-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="c2232-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="c2232-107">Define a extensão de nome de arquivo padrão para uma caixa de diálogo **abrir** ou **salvar como** no estilo do Explorer.</span><span class="sxs-lookup"><span data-stu-id="c2232-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="c2232-108">A caixa de diálogo deve ter sido criada com o sinalizador **OFN \_ Explorer** ; caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="c2232-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="c2232-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2232-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2232-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2232-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2232-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="c2232-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c2232-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2232-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2232-113">Um ponteiro para a nova extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2232-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="c2232-114">Não deve incluir o ponto (.).</span><span class="sxs-lookup"><span data-stu-id="c2232-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2232-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2232-115">Return value</span></span>

<span data-ttu-id="c2232-116">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="c2232-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2232-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2232-117">Remarks</span></span>

<span data-ttu-id="c2232-118">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="c2232-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="c2232-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2232-119">Requirements</span></span>



| <span data-ttu-id="c2232-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2232-120">Requirement</span></span> | <span data-ttu-id="c2232-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c2232-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2232-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2232-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c2232-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2232-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c2232-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2232-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c2232-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2232-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c2232-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c2232-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2232-127"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2232-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2232-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2232-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c2232-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c2232-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c2232-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="c2232-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="c2232-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="c2232-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="c2232-132">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="c2232-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="c2232-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c2232-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c2232-134">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="c2232-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

