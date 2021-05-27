---
title: CDM_GETFOLDERIDLIST mensagem (Commdlg.h)
description: Recupera o endereço da lista de identificadores de item correspondente à pasta que uma caixa de diálogo Abrir ou Salvar como no estilo Explorer tem aberta no momento.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST caixa de diálogo de mensagem
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
ms.openlocfilehash: bb3ffff4f80dc21ed685e589ed4780b43592c2d2
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549701"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="eb05f-104">Mensagem \_ GETFOLDERIDLIST do CDM</span><span class="sxs-lookup"><span data-stu-id="eb05f-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="eb05f-105">\[Começando com o Windows Vista, as **caixas** de **diálogo** Abrir e Salvar como comuns foram superadas pela caixa de diálogo Item [Comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="eb05f-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="eb05f-106">Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]</span><span class="sxs-lookup"><span data-stu-id="eb05f-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="eb05f-107">Recupera o endereço da lista de identificadores de item  correspondente à pasta que uma caixa de diálogo Abrir ou Salvar **como** no estilo Explorer tem aberta no momento.</span><span class="sxs-lookup"><span data-stu-id="eb05f-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="eb05f-108">A caixa de diálogo deve ter sido criada com o **sinalizador OFN \_ EXPLORER;** caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="eb05f-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="eb05f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb05f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb05f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb05f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb05f-111">O tamanho, em bytes, do buffer *lParam.*</span><span class="sxs-lookup"><span data-stu-id="eb05f-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="eb05f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb05f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb05f-113">Um ponteiro para o buffer que recebe a lista de identificadores de item.</span><span class="sxs-lookup"><span data-stu-id="eb05f-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb05f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb05f-114">Return value</span></span>

<span data-ttu-id="eb05f-115">Se a mensagem for bem-sucedida, o valor de retorno será o tamanho, em bytes, da lista de identificadores de item.</span><span class="sxs-lookup"><span data-stu-id="eb05f-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="eb05f-116">Esse é o número de bytes copiados para o buffer ou o tamanho do buffer necessário se o buffer for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="eb05f-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="eb05f-117">Se ocorrer um erro, o valor de retorno será menor que zero.</span><span class="sxs-lookup"><span data-stu-id="eb05f-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb05f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb05f-118">Remarks</span></span>

<span data-ttu-id="eb05f-119">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="eb05f-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="eb05f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb05f-120">Requirements</span></span>



| <span data-ttu-id="eb05f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb05f-121">Requirement</span></span> | <span data-ttu-id="eb05f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="eb05f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb05f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb05f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="eb05f-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eb05f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="eb05f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb05f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="eb05f-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eb05f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eb05f-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="eb05f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb05f-128"><dt>Commdlg.h (inclua Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb05f-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb05f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb05f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb05f-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="eb05f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eb05f-131">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="eb05f-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="eb05f-132">**Getsavefilename**</span><span class="sxs-lookup"><span data-stu-id="eb05f-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="eb05f-133">**Openfilename**</span><span class="sxs-lookup"><span data-stu-id="eb05f-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="eb05f-134">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="eb05f-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eb05f-135">Biblioteca de caixas de diálogo comuns</span><span class="sxs-lookup"><span data-stu-id="eb05f-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

