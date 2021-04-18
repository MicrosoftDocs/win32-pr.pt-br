---
description: A função IsWindowRedirectedForPrint determina se a janela especificada é redirecionada no momento para impressão.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: Função IsWindowRedirectedForPrint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764309"
---
# <a name="iswindowredirectedforprint-function"></a><span data-ttu-id="0e691-103">Função IsWindowRedirectedForPrint</span><span class="sxs-lookup"><span data-stu-id="0e691-103">IsWindowRedirectedForPrint function</span></span>

<span data-ttu-id="0e691-104">A função **IsWindowRedirectedForPrint** determina se a janela especificada é redirecionada no momento para impressão.</span><span class="sxs-lookup"><span data-stu-id="0e691-104">The **IsWindowRedirectedForPrint** function determines whether the specified window is currently redirected for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e691-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e691-105">Syntax</span></span>


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="0e691-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e691-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e691-107">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e691-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e691-108">O identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="0e691-108">The handle of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e691-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e691-109">Return value</span></span>

<span data-ttu-id="0e691-110">Se a janela for redirecionada no momento para impressão, a função retornará um valor diferente de zero; caso contrário, retornará zero.</span><span class="sxs-lookup"><span data-stu-id="0e691-110">If the window is currently redirected for printing, the function returns a nonzero value; otherwise, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e691-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e691-111">Remarks</span></span>

<span data-ttu-id="0e691-112">Uma janela é redirecionada para impressão quando processa uma chamada para a [**janela**](/windows/desktop/api/Winuser/nf-winuser-printwindow)do.</span><span class="sxs-lookup"><span data-stu-id="0e691-112">A window is redirected for printing when it processes a call to [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow).</span></span> <span data-ttu-id="0e691-113">Em uma chamada para o **diwindow**, uma janela renderiza seu conteúdo para um contexto de dispositivo fora da tela.</span><span class="sxs-lookup"><span data-stu-id="0e691-113">In a call to **PrintWindow**, a window renders its content to an off-screen device context.</span></span>

<span data-ttu-id="0e691-114">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0e691-114">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e691-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e691-115">Requirements</span></span>



| <span data-ttu-id="0e691-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e691-116">Requirement</span></span> | <span data-ttu-id="0e691-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0e691-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e691-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e691-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0e691-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e691-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e691-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e691-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0e691-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e691-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e691-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0e691-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e691-123"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e691-123"><dt>User32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e691-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e691-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e691-125">**Janela**</span><span class="sxs-lookup"><span data-stu-id="0e691-125">**PrintWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[<span data-ttu-id="0e691-126">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="0e691-126">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="0e691-127">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="0e691-127">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="0e691-128">**impressão do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0e691-128">**WM\_PRINT**</span></span>](/windows/desktop/gdi/wm-print)
</dt> <dt>

[<span data-ttu-id="0e691-129">**WM \_ FILEclient**</span><span class="sxs-lookup"><span data-stu-id="0e691-129">**WM\_PRINTCLIENT**</span></span>](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

