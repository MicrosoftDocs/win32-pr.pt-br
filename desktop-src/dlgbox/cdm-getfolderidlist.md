---
title: Mensagem de CDM_GETFOLDERIDLIST (Commdlg. h)
description: Recupera o endereço da lista de identificadores de item correspondente à pasta em que uma caixa de diálogo abrir ou salvar no estilo do Explorer está aberta no momento.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- Caixas de diálogo de CDM_GETFOLDERIDLIST mensagem
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d16b53c90c3efc874b8aeabd1b97938a1b21ec
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590903"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="66eda-104">\_Mensagem CDM GETFOLDERIDLIST</span><span class="sxs-lookup"><span data-stu-id="66eda-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="66eda-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="66eda-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="66eda-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="66eda-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="66eda-107">Recupera o endereço da lista de identificadores de item correspondente à pasta em que uma caixa de diálogo **abrir** ou **salvar** no estilo do Explorer está aberta no momento.</span><span class="sxs-lookup"><span data-stu-id="66eda-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="66eda-108">A caixa de diálogo deve ter sido criada com o sinalizador **OFN \_ Explorer** ; caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="66eda-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="66eda-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66eda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66eda-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66eda-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66eda-111">O tamanho, em bytes, do buffer de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="66eda-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="66eda-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66eda-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66eda-113">Um ponteiro para o buffer que recebe a lista de identificadores de item.</span><span class="sxs-lookup"><span data-stu-id="66eda-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66eda-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66eda-114">Return value</span></span>

<span data-ttu-id="66eda-115">Se a mensagem tiver sucesso, o valor de retorno será o tamanho, em bytes, da lista de identificadores de item.</span><span class="sxs-lookup"><span data-stu-id="66eda-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="66eda-116">Esse é o número de bytes copiados para o buffer ou o tamanho de buffer necessário se o buffer for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="66eda-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="66eda-117">Se ocorrer um erro, o valor de retorno será menor que zero.</span><span class="sxs-lookup"><span data-stu-id="66eda-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="66eda-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="66eda-118">Remarks</span></span>

<span data-ttu-id="66eda-119">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="66eda-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="66eda-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66eda-120">Requirements</span></span>



| <span data-ttu-id="66eda-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="66eda-121">Requirement</span></span> | <span data-ttu-id="66eda-122">Valor</span><span class="sxs-lookup"><span data-stu-id="66eda-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66eda-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66eda-123">Minimum supported client</span></span><br/> | <span data-ttu-id="66eda-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66eda-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="66eda-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66eda-125">Minimum supported server</span></span><br/> | <span data-ttu-id="66eda-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66eda-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="66eda-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="66eda-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="66eda-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66eda-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66eda-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="66eda-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="66eda-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="66eda-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="66eda-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="66eda-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="66eda-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="66eda-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="66eda-133">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="66eda-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="66eda-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="66eda-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="66eda-135">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="66eda-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

