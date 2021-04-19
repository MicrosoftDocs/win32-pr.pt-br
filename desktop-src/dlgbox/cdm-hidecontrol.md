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
ms.openlocfilehash: 7c0f2f41017373d9064da8f1024066f131063d9d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590873"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="3ac82-104">\_Mensagem CDM HIDECONTROL</span><span class="sxs-lookup"><span data-stu-id="3ac82-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="3ac82-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="3ac82-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="3ac82-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="3ac82-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="3ac82-107">Oculta o controle especificado em uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** .</span><span class="sxs-lookup"><span data-stu-id="3ac82-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="3ac82-108">A caixa de diálogo deve ter sido criada com o sinalizador **OFN \_ Explorer** ; caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="3ac82-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="3ac82-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ac82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ac82-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ac82-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ac82-111">O identificador do controle a ser ocultado.</span><span class="sxs-lookup"><span data-stu-id="3ac82-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="3ac82-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ac82-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ac82-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="3ac82-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ac82-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ac82-114">Return value</span></span>

<span data-ttu-id="3ac82-115">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="3ac82-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ac82-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ac82-116">Remarks</span></span>

<span data-ttu-id="3ac82-117">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="3ac82-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="3ac82-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ac82-118">Requirements</span></span>



| <span data-ttu-id="3ac82-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac82-119">Requirement</span></span> | <span data-ttu-id="3ac82-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3ac82-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac82-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ac82-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3ac82-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ac82-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3ac82-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ac82-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3ac82-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ac82-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3ac82-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3ac82-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ac82-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ac82-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ac82-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ac82-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ac82-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="3ac82-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3ac82-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="3ac82-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="3ac82-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="3ac82-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="3ac82-131">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="3ac82-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="3ac82-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="3ac82-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3ac82-133">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="3ac82-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

