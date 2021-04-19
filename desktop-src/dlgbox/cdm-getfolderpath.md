---
title: Mensagem de CDM_GETFOLDERPATH (Commdlg. h)
description: Recupera o caminho da pasta ou do diretório aberto no momento para uma caixa de diálogo abrir no estilo do Explorer ou salvar como.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- Caixas de diálogo de CDM_GETFOLDERPATH mensagem
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
ms.openlocfilehash: fdd6a824892b1a3a31339e36e6a783bb00c08534
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590933"
---
# <a name="cdm_getfolderpath-message"></a><span data-ttu-id="ea45f-104">\_Mensagem GETFOLDERPATH CDM</span><span class="sxs-lookup"><span data-stu-id="ea45f-104">CDM\_GETFOLDERPATH message</span></span>

<span data-ttu-id="ea45f-105">\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="ea45f-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="ea45f-106">Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]</span><span class="sxs-lookup"><span data-stu-id="ea45f-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="ea45f-107">Recupera o caminho da pasta ou do diretório aberto no momento para uma caixa de diálogo **abrir** no estilo do Explorer ou **salvar como** .</span><span class="sxs-lookup"><span data-stu-id="ea45f-107">Retrieves the path of the currently open folder or directory for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="ea45f-108">A caixa de diálogo deve ter sido criada com o sinalizador **OFN \_ Explorer** ; caso contrário, a mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="ea45f-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="ea45f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea45f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea45f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea45f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea45f-111">O tamanho, em caracteres, do buffer de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="ea45f-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ea45f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea45f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea45f-113">Um ponteiro para o buffer que recebe o caminho.</span><span class="sxs-lookup"><span data-stu-id="ea45f-113">A pointer to the buffer that receives the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea45f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea45f-114">Return value</span></span>

<span data-ttu-id="ea45f-115">Se a mensagem tiver sucesso, o valor de retorno será o tamanho, em caracteres, da cadeia de caracteres do caminho, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="ea45f-115">If the message succeeds, the return value is the size, in characters, of the path string, including the terminating null character.</span></span> <span data-ttu-id="ea45f-116">Esse é o número de bytes ou caracteres copiados para o buffer ou o tamanho de buffer necessário se o buffer for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="ea45f-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="ea45f-117">Se ocorrer um erro, o valor de retorno será menor que zero.</span><span class="sxs-lookup"><span data-stu-id="ea45f-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea45f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea45f-118">Remarks</span></span>

<span data-ttu-id="ea45f-119">A macro correspondente é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="ea45f-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="ea45f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea45f-120">Requirements</span></span>



| <span data-ttu-id="ea45f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea45f-121">Requirement</span></span> | <span data-ttu-id="ea45f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ea45f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea45f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea45f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ea45f-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ea45f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ea45f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea45f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ea45f-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ea45f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ea45f-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ea45f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea45f-128"><dt>Commdlg. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea45f-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea45f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea45f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea45f-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ea45f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ea45f-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="ea45f-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="ea45f-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="ea45f-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="ea45f-133">**DA OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="ea45f-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="ea45f-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ea45f-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ea45f-135">Biblioteca de caixa de diálogo comum</span><span class="sxs-lookup"><span data-stu-id="ea45f-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

