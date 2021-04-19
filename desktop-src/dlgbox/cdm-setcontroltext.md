---
title: Mensagem de CDM_SETCONTROLTEXT (Commdlg. h)
description: Define o texto para o controle especificado em uma caixa de diálogo abrir ou salvar como no estilo do Explorer.
ms.assetid: ff0e50b7-a14d-40d1-8576-f93a612f3aa3
keywords:
- Caixas de diálogo de CDM_SETCONTROLTEXT mensagem
topic_type:
- apiref
api_name:
- CDM_SETCONTROLTEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d75bb3d3ac486bbb43545df80c67383a7655b8
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590883"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="9ef70-104">\_Mensagem CDM SETCONTROLTEXT</span><span class="sxs-lookup"><span data-stu-id="9ef70-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="9ef70-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="9ef70-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="9ef70-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="9ef70-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="9ef70-107">Define o texto para o controle especificado em uma caixa de diálogo **abrir** ou **salvar como** no estilo do Explorer.</span><span class="sxs-lookup"><span data-stu-id="9ef70-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="9ef70-108">A caixa de diálogo deve ter sido criada com o sinalizador **OFN \_ Explorer** ; caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="9ef70-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="9ef70-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ef70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ef70-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ef70-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ef70-111">O identificador do controle para o qual o texto deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="9ef70-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="9ef70-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ef70-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ef70-113">O novo texto do controle.</span><span class="sxs-lookup"><span data-stu-id="9ef70-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ef70-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ef70-114">Return value</span></span>

<span data-ttu-id="9ef70-115">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9ef70-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ef70-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ef70-116">Remarks</span></span>

<span data-ttu-id="9ef70-117">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="9ef70-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="9ef70-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ef70-118">Requirements</span></span>



| <span data-ttu-id="9ef70-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ef70-119">Requirement</span></span> | <span data-ttu-id="9ef70-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9ef70-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef70-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ef70-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef70-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9ef70-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9ef70-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ef70-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef70-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9ef70-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ef70-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9ef70-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ef70-126"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ef70-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ef70-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ef70-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ef70-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="9ef70-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ef70-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="9ef70-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="9ef70-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="9ef70-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="9ef70-131">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="9ef70-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="9ef70-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="9ef70-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ef70-133">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="9ef70-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

