---
description: Determina se o Terminal Server está no modo de instalação (somente no Windows Terminal Server 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: Função CtxGetIniMapping
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749737"
---
# <a name="ctxgetinimapping-function"></a><span data-ttu-id="e6c5b-103">Função CtxGetIniMapping</span><span class="sxs-lookup"><span data-stu-id="e6c5b-103">CtxGetIniMapping function</span></span>

<span data-ttu-id="e6c5b-104">\[Essa função não tem suporte e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="e6c5b-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="e6c5b-105">Ele pode mudar ou desaparecer completamente sem aviso prévio.</span><span class="sxs-lookup"><span data-stu-id="e6c5b-105">It may change or disappear completely without advance notice.</span></span> <span data-ttu-id="e6c5b-106">Em vez disso, use **VerifyVersionInfo**.\]</span><span class="sxs-lookup"><span data-stu-id="e6c5b-106">Instead, use **VerifyVersionInfo**.\]</span></span>

<span data-ttu-id="e6c5b-107">Determina se o Terminal Server está no modo de instalação (somente no Windows Terminal Server 4,0).</span><span class="sxs-lookup"><span data-stu-id="e6c5b-107">Determines whether the Terminal Server is in INSTALL mode (only on Windows Terminal Server 4.0).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c5b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6c5b-108">Syntax</span></span>


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a><span data-ttu-id="e6c5b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6c5b-109">Parameters</span></span>

<span data-ttu-id="e6c5b-110">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e6c5b-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6c5b-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e6c5b-111">Return value</span></span>

<span data-ttu-id="e6c5b-112">Essa função retornará **false** se o Terminal Server estiver no modo de instalação, **true** se estiver no modo de execução.</span><span class="sxs-lookup"><span data-stu-id="e6c5b-112">This function returns **FALSE** if the Terminal Server is in INSTALL mode, **TRUE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c5b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6c5b-113">Requirements</span></span>



| <span data-ttu-id="e6c5b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6c5b-114">Requirement</span></span> | <span data-ttu-id="e6c5b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e6c5b-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c5b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="e6c5b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="e6c5b-117"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6c5b-117"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6c5b-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6c5b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c5b-119">**VerifyVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="e6c5b-119">**VerifyVersionInfo**</span></span>](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
