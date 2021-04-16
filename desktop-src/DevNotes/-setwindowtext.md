---
description: Altera o texto da barra de título da janela especificada (se tiver uma).
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: Função _SetWindowText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 8832f8ee08877edae695a858874c3a2f87a2c286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752395"
---
# <a name="_setwindowtext-function"></a><span data-ttu-id="1e0f3-103">\_Função SetWindowText</span><span class="sxs-lookup"><span data-stu-id="1e0f3-103">\_SetWindowText function</span></span>

<span data-ttu-id="1e0f3-104">\[Essa função é um wrapper sobre a função **SetWindowText** .</span><span class="sxs-lookup"><span data-stu-id="1e0f3-104">\[This function is a wrapper over the **SetWindowText** function.</span></span> <span data-ttu-id="1e0f3-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="1e0f3-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="1e0f3-106">Os aplicativos devem chamar **SetWindowText** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="1e0f3-106">Applications should call **SetWindowText** directly.\]</span></span>

<span data-ttu-id="1e0f3-107">Altera o texto da barra de título da janela especificada (se tiver uma).</span><span class="sxs-lookup"><span data-stu-id="1e0f3-107">Changes the text of the specified window's title bar (if it has one).</span></span> <span data-ttu-id="1e0f3-108">Consulte [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span><span class="sxs-lookup"><span data-stu-id="1e0f3-108">See [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e0f3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e0f3-109">Syntax</span></span>


```C++
BOOL _SetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="1e0f3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e0f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e0f3-111">*...*</span><span class="sxs-lookup"><span data-stu-id="1e0f3-111">*...*</span></span> 
<span data-ttu-id="1e0f3-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1e0f3-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1e0f3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e0f3-113">Requirements</span></span>



| <span data-ttu-id="1e0f3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e0f3-114">Requirement</span></span> | <span data-ttu-id="1e0f3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1e0f3-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0f3-116">DLL</span><span class="sxs-lookup"><span data-stu-id="1e0f3-116">DLL</span></span><br/> | <dl> <span data-ttu-id="1e0f3-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e0f3-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e0f3-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e0f3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0f3-119">**SetWindowText**</span><span class="sxs-lookup"><span data-stu-id="1e0f3-119">**SetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
