---
title: CDM_SETDEFEXT mensagem (Commdlg.h)
description: Define a extensão de nome de arquivo padrão para uma caixa de diálogo Abrir ou Salvar como no estilo Explorer.
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- CDM_SETDEFEXT caixa de diálogo de mensagem
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
ms.openlocfilehash: 0b0b1169a2777d5a5f82925366c6723af741706d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550111"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="acbf8-104">Mensagem \_ SETDEFEXT do CDM</span><span class="sxs-lookup"><span data-stu-id="acbf8-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="acbf8-105">\[Começando com o Windows Vista, as **caixas** de **diálogo** Abrir e Salvar como comuns foram superadas pela caixa de diálogo Item [Comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="acbf8-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="acbf8-106">Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]</span><span class="sxs-lookup"><span data-stu-id="acbf8-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="acbf8-107">Define a extensão de nome de arquivo padrão para uma caixa de diálogo **Abrir** ou **Salvar como** no estilo Explorer.</span><span class="sxs-lookup"><span data-stu-id="acbf8-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="acbf8-108">A caixa de diálogo deve ter sido criada com o **sinalizador OFN \_ EXPLORER;** caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="acbf8-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="acbf8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acbf8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acbf8-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="acbf8-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acbf8-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="acbf8-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="acbf8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acbf8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acbf8-113">Um ponteiro para a nova extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="acbf8-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="acbf8-114">Não deve incluir o ponto (.).</span><span class="sxs-lookup"><span data-stu-id="acbf8-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acbf8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="acbf8-115">Return value</span></span>

<span data-ttu-id="acbf8-116">Essa mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="acbf8-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="acbf8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="acbf8-117">Remarks</span></span>

<span data-ttu-id="acbf8-118">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="acbf8-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="acbf8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acbf8-119">Requirements</span></span>



| <span data-ttu-id="acbf8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="acbf8-120">Requirement</span></span> | <span data-ttu-id="acbf8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="acbf8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acbf8-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acbf8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="acbf8-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="acbf8-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="acbf8-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acbf8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="acbf8-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="acbf8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="acbf8-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="acbf8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="acbf8-127"><dt>Commdlg.h (inclua Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="acbf8-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acbf8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="acbf8-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="acbf8-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="acbf8-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="acbf8-130">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="acbf8-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="acbf8-131">**Getsavefilename**</span><span class="sxs-lookup"><span data-stu-id="acbf8-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="acbf8-132">**Openfilename**</span><span class="sxs-lookup"><span data-stu-id="acbf8-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="acbf8-133">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="acbf8-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="acbf8-134">Biblioteca de caixas de diálogo comuns</span><span class="sxs-lookup"><span data-stu-id="acbf8-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

