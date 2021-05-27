---
title: CDM_HIDECONTROL mensagem (Commdlg.h)
description: Oculta o controle especificado em uma caixa de diálogo Abrir ou Salvar como no estilo Explorer.
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- CDM_HIDECONTROL caixa de diálogo da mensagem
topic_type:
- apiref
api_name:
- CDM_HIDECONTROL
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f1a5a7a1830ceeb2c3671b0dfb538ad89e0a58
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548651"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="28d01-104">Mensagem \_ HIDECONTROL do CDM</span><span class="sxs-lookup"><span data-stu-id="28d01-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="28d01-105">\[Começando com o Windows Vista, as **caixas** de **diálogo** Abrir e Salvar como comuns foram superadas pela caixa de diálogo Item [Comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="28d01-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="28d01-106">Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]</span><span class="sxs-lookup"><span data-stu-id="28d01-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="28d01-107">Oculta o controle especificado em uma  caixa de diálogo Abrir ou Salvar **como** no estilo Explorer.</span><span class="sxs-lookup"><span data-stu-id="28d01-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="28d01-108">A caixa de diálogo deve ter sido criada com o **sinalizador OFN \_ EXPLORER;** caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="28d01-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="28d01-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28d01-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28d01-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28d01-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28d01-111">O identificador do controle a ser oculto.</span><span class="sxs-lookup"><span data-stu-id="28d01-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="28d01-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28d01-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28d01-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="28d01-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28d01-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28d01-114">Return value</span></span>

<span data-ttu-id="28d01-115">Essa mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="28d01-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28d01-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="28d01-116">Remarks</span></span>

<span data-ttu-id="28d01-117">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="28d01-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="28d01-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28d01-118">Requirements</span></span>



| <span data-ttu-id="28d01-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="28d01-119">Requirement</span></span> | <span data-ttu-id="28d01-120">Valor</span><span class="sxs-lookup"><span data-stu-id="28d01-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28d01-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28d01-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28d01-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28d01-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="28d01-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28d01-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28d01-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28d01-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="28d01-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="28d01-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="28d01-126"><dt>Commdlg.h (inclua Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="28d01-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28d01-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="28d01-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="28d01-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="28d01-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="28d01-129">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="28d01-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="28d01-130">**Getsavefilename**</span><span class="sxs-lookup"><span data-stu-id="28d01-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="28d01-131">**Openfilename**</span><span class="sxs-lookup"><span data-stu-id="28d01-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="28d01-132">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="28d01-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="28d01-133">Biblioteca de caixas de diálogo comuns</span><span class="sxs-lookup"><span data-stu-id="28d01-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

