---
description: Recupera o texto da barra de título da janela especificada.
ms.assetid: c14151f9-222f-40a2-837e-7f9a728efc82
title: Função _GetWindowText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 61c84c8a5f00ad97b8a76ef4139b20b74f1be085
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747464"
---
# <a name="_getwindowtext-function"></a><span data-ttu-id="f31ce-103">\_Função GetWindowText</span><span class="sxs-lookup"><span data-stu-id="f31ce-103">\_GetWindowText function</span></span>

<span data-ttu-id="f31ce-104">\[Essa função é um wrapper sobre a função **GetWindowText** .</span><span class="sxs-lookup"><span data-stu-id="f31ce-104">\[This function is a wrapper over the **GetWindowText** function.</span></span> <span data-ttu-id="f31ce-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="f31ce-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="f31ce-106">Os aplicativos devem chamar **GetWindowText** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="f31ce-106">Applications should call **GetWindowText** directly.\]</span></span>

<span data-ttu-id="f31ce-107">Recupera o texto da barra de título da janela especificada.</span><span class="sxs-lookup"><span data-stu-id="f31ce-107">Retrieves the text from the specified window's title bar.</span></span> <span data-ttu-id="f31ce-108">Consulte [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).</span><span class="sxs-lookup"><span data-stu-id="f31ce-108">See [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="f31ce-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f31ce-109">Syntax</span></span>


```C++
int _GetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="f31ce-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f31ce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f31ce-111">*...*</span><span class="sxs-lookup"><span data-stu-id="f31ce-111">*...*</span></span> 
<span data-ttu-id="f31ce-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f31ce-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f31ce-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f31ce-113">Requirements</span></span>



| <span data-ttu-id="f31ce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f31ce-114">Requirement</span></span> | <span data-ttu-id="f31ce-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f31ce-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f31ce-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f31ce-116">DLL</span></span><br/> | <dl> <span data-ttu-id="f31ce-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f31ce-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f31ce-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f31ce-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31ce-119">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="f31ce-119">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> </dl>

 

 
