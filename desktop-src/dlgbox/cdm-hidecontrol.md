---
title: Mensagem de CDM_HIDECONTROL (Commdlg. h)
description: Oculta o controle especificado em uma caixa de diálogo abrir no estilo do Explorer ou salvar como.
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- Caixas de diálogo de CDM_HIDECONTROL mensagem
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
ms.openlocfilehash: ff632b7d1e3c24c84f73498846db9e6bfa68fd74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756335"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="ed43b-104">\_Mensagem CDM HIDECONTROL</span><span class="sxs-lookup"><span data-stu-id="ed43b-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="ed43b-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ed43b-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="ed43b-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="ed43b-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="ed43b-107">Oculta o controle especificado em uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** .</span><span class="sxs-lookup"><span data-stu-id="ed43b-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="ed43b-108">A caixa de diálogo deve ter sido criada com o sinalizador **OFN \_ Explorer** ; caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="ed43b-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="ed43b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed43b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed43b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed43b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed43b-111">O identificador do controle a ser ocultado.</span><span class="sxs-lookup"><span data-stu-id="ed43b-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="ed43b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed43b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed43b-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="ed43b-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed43b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed43b-114">Return value</span></span>

<span data-ttu-id="ed43b-115">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ed43b-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed43b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed43b-116">Remarks</span></span>

<span data-ttu-id="ed43b-117">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="ed43b-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="ed43b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed43b-118">Requirements</span></span>



| <span data-ttu-id="ed43b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed43b-119">Requirement</span></span> | <span data-ttu-id="ed43b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ed43b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed43b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed43b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ed43b-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed43b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ed43b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed43b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ed43b-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed43b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ed43b-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ed43b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed43b-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed43b-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed43b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed43b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed43b-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ed43b-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ed43b-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="ed43b-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="ed43b-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="ed43b-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="ed43b-131">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="ed43b-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="ed43b-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ed43b-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ed43b-133">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="ed43b-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

