---
title: CDM_GETFOLDERPATH mensagem (Commdlg.h)
description: Recupera o caminho da pasta ou diretório aberto no momento para uma caixa de diálogo Abrir ou Salvar como no estilo Explorer.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- CDM_GETFOLDERPATH caixa de diálogo de mensagem
topic_type:
- apiref
api_name:
- CDM_GETFOLDERPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d96b8d25714dc3f8bdcf016ac1fd69b2af2414f0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550001"
---
# <a name="cdm_getfolderpath-message"></a><span data-ttu-id="c7807-104">Mensagem \_ GETFOLDERPATH do CDM</span><span class="sxs-lookup"><span data-stu-id="c7807-104">CDM\_GETFOLDERPATH message</span></span>

<span data-ttu-id="c7807-105">\[Começando com o Windows Vista, as **caixas** de **diálogo** Abrir e Salvar como comuns foram superadas pela caixa de diálogo Item [Comum](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="c7807-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="c7807-106">Recomendamos que você use a API de Diálogo de Item Comum em vez dessas caixas de diálogo da Biblioteca de Caixas de Diálogo Comuns.\]</span><span class="sxs-lookup"><span data-stu-id="c7807-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="c7807-107">Recupera o caminho da pasta ou diretório aberto no  momento para uma caixa de diálogo Abrir ou Salvar **como** no estilo Explorer.</span><span class="sxs-lookup"><span data-stu-id="c7807-107">Retrieves the path of the currently open folder or directory for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="c7807-108">A caixa de diálogo deve ter sido criada com o **sinalizador OFN \_ EXPLORER;** caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="c7807-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="c7807-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7807-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7807-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7807-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7807-111">O tamanho, em caracteres, do buffer *lParam.*</span><span class="sxs-lookup"><span data-stu-id="c7807-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c7807-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7807-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7807-113">Um ponteiro para o buffer que recebe o caminho.</span><span class="sxs-lookup"><span data-stu-id="c7807-113">A pointer to the buffer that receives the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7807-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7807-114">Return value</span></span>

<span data-ttu-id="c7807-115">Se a mensagem for bem-sucedida, o valor de retorno será o tamanho, em caracteres, da cadeia de caracteres de caminho, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c7807-115">If the message succeeds, the return value is the size, in characters, of the path string, including the terminating null character.</span></span> <span data-ttu-id="c7807-116">Esse é o número de bytes ou caracteres copiados para o buffer ou o tamanho do buffer necessário se o buffer for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="c7807-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="c7807-117">Se ocorrer um erro, o valor de retorno será menor que zero.</span><span class="sxs-lookup"><span data-stu-id="c7807-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7807-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7807-118">Remarks</span></span>

<span data-ttu-id="c7807-119">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="c7807-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="c7807-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7807-120">Requirements</span></span>



| <span data-ttu-id="c7807-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7807-121">Requirement</span></span> | <span data-ttu-id="c7807-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c7807-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7807-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7807-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c7807-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7807-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c7807-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7807-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c7807-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7807-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7807-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c7807-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7807-128"><dt>Commdlg.h (inclua Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7807-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7807-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7807-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7807-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c7807-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c7807-131">**Getopenfilename**</span><span class="sxs-lookup"><span data-stu-id="c7807-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="c7807-132">**Getsavefilename**</span><span class="sxs-lookup"><span data-stu-id="c7807-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="c7807-133">**Openfilename**</span><span class="sxs-lookup"><span data-stu-id="c7807-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="c7807-134">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="c7807-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7807-135">Biblioteca de caixas de diálogo comuns</span><span class="sxs-lookup"><span data-stu-id="c7807-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

