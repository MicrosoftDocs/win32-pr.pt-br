---
description: Manipula a mensagem do WM \_ CTLCOLOR para aplicativos que usam o ctl3d.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Função Ctl3dCtlColorEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752773"
---
# <a name="ctl3dctlcolorex-function"></a><span data-ttu-id="b879e-103">Função Ctl3dCtlColorEx</span><span class="sxs-lookup"><span data-stu-id="b879e-103">Ctl3dCtlColorEx function</span></span>

<span data-ttu-id="b879e-104">Manipula a mensagem do **WM \_ CTLCOLOR** para aplicativos que usam o ctl3d.</span><span class="sxs-lookup"><span data-stu-id="b879e-104">Handles the **WM\_CTLCOLOR** message for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="b879e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b879e-105">Syntax</span></span>


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="b879e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b879e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b879e-107">*wm*</span><span class="sxs-lookup"><span data-stu-id="b879e-107">*wm*</span></span> 
</dt> <dd>

<span data-ttu-id="b879e-108">A mensagem do **WM \_ CTLCOLOR** para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b879e-108">The **WM\_CTLCOLOR** message for the application.</span></span>

</dd> <dt>

<span data-ttu-id="b879e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b879e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b879e-110">Um identificador para o contexto de exibição (DC).</span><span class="sxs-lookup"><span data-stu-id="b879e-110">A handle to the display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="b879e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b879e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b879e-112">Um identificador para uma janela filho (controle).</span><span class="sxs-lookup"><span data-stu-id="b879e-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b879e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b879e-113">Return value</span></span>

<span data-ttu-id="b879e-114">Retorna um identificador para o pincel apropriado se a função tiver sucesso; caso contrário, ele retorna `(HBRUSH)(0)` indicando que ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="b879e-114">Returns a handle to the appropriate brush if the function succeeds; otherwise, it returns `(HBRUSH)(0)` indicating that an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="b879e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b879e-115">Remarks</span></span>

<span data-ttu-id="b879e-116">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b879e-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b879e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b879e-117">Requirements</span></span>



| <span data-ttu-id="b879e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b879e-118">Requirement</span></span> | <span data-ttu-id="b879e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b879e-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b879e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b879e-120">DLL</span></span><br/> | <dl> <span data-ttu-id="b879e-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b879e-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
